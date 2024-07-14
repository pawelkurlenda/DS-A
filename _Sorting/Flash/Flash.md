# Pseudocode

```
procedure flashSort(A: list of sortable items)
    n := length(A)
    m := int(0.45 * n)
    L := new list of length m initialized to 0
    minVal := findMin(A)
    maxIndex := findMaxIndex(A)
    maxVal := A[maxIndex]
    if minVal == maxVal then
        return
    end if
    c1 := (m - 1) / (maxVal - minVal)
    for i := 0 to n - 1 inclusive do
        k := int(c1 * (A[i] - minVal))
        L[k] := L[k] + 1
    end for
    for k := 1 to m - 1 inclusive do
        L[k] := L[k] + L[k - 1]
    end for
    swap(A[maxIndex], A[0])
    move := 0
    j := 0
    k := m - 1
    while move < n - 1 do
        while j > L[k] - 1 do
            j := j + 1
            k := int(c1 * (A[j] - minVal))
        end while
        flash := A[j]
        while j != L[k] do
            k := int(c1 * (flash - minVal))
            hold := A[L[k] - 1]
            A[L[k] - 1] := flash
            flash := hold
            L[k] := L[k] - 1
            move := move + 1
        end while
    end while
    insertionSort(A)
end procedure
```