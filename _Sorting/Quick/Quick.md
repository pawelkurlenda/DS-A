# Pseudocode

```
procedure quickSort(A: list of sortable items, low: int, high: int)
    if low < high then
        pivotIndex := partition(A, low, high)
        quickSort(A, low, pivotIndex - 1)
        quickSort(A, pivotIndex + 1, high)
    end if
end procedure

procedure partition(A: list of sortable items, low: int, high: int) returns int
    pivot := A[high]
    i := low - 1
    for j := low to high - 1 inclusive do
        if A[j] <= pivot then
            i := i + 1
            swap(A[i], A[j])
        end if
    end for
    swap(A[i + 1], A[high])
    return i + 1
end procedure
```