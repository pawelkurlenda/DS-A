# Pseudocode

```
procedure bitonicSort(A: list of sortable items, up: boolean)
    bitonicSortUtil(A, 0, length(A), up)
end procedure

procedure bitonicSortUtil(A: list of sortable items, low: int, cnt: int, up: boolean)
    if cnt > 1 then
        k := cnt / 2
        bitonicSortUtil(A, low, k, true)
        bitonicSortUtil(A, low + k, cnt - k, false)
        bitonicMerge(A, low, cnt, up)
    end if
end procedure

procedure bitonicMerge(A: list of sortable items, low: int, cnt: int, up: boolean)
    if cnt > 1 then
        k := cnt / 2
        for i := low to low + k - 1 inclusive do
            if (A[i] > A[i + k]) == up then
                swap(A[i], A[i + k])
            end if
        end for
        bitonicMerge(A, low, k, up)
        bitonicMerge(A, low + k, cnt - k, up)
    end if
end procedure
```