# Pseudocode

```
procedure selectionSort(A: list of sortable items)
    n := length(A)
    for i := 0 to n - 2 inclusive do
        minIndex := i
        for j := i + 1 to n - 1 inclusive do
            if A[j] < A[minIndex] then
                minIndex := j
            end if
        end for
        swap(A[i], A[minIndex])
    end for
end procedure
```