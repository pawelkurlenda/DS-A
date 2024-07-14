# Pseudocode

```
procedure stoogeSort(A: list of sortable items, l: int, h: int)
    if l >= h then
        return
    end if
    if A[l] > A[h] then
        swap(A[l], A[h])
    end if
    if h - l + 1 > 2 then
        t := (h - l + 1) / 3
        stoogeSort(A, l, h - t)
        stoogeSort(A, l + t, h)
        stoogeSort(A, l, h - t)
    end if
end procedure
```