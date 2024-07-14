# Pseudocode

```
procedure mergeSort(A: list of sortable items)
    if length(A) > 1 then
        mid := length(A) / 2
        left := A[0 : mid]
        right := A[mid : length(A)]
        mergeSort(left)
        mergeSort(right)
        merge(A, left, right)
    end if
end procedure

procedure merge(A: list of sortable items, left: list, right: list)
    i := 0, j := 0, k := 0
    while i < length(left) and j < length(right) do
        if left[i] < right[j] then
            A[k] := left[i]
            i := i + 1
        else
            A[k] := right[j]
            j := j + 1
        end if
        k := k + 1
    end while
    while i < length(left) do
        A[k] := left[i]
        i := i + 1
        k := k + 1
    end while
    while j < length(right) do
        A[k] := right[j]
        j := j + 1
        k := k + 1
    end while
end procedure
```