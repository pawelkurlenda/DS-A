# Pseudocode

```
procedure timSort(A: list of sortable items)
    minRun := 32
    n := length(A)
    for i := 0 to n - 1 step minRun do
        insertionSort(A, i, min(i + minRun - 1, n - 1))
    end for
    size := minRun
    while size < n do
        for start := 0 to n - 1 inclusive step 2 * size do
            mid := start + size - 1
            end := min(start + 2 * size - 1, n - 1)
            if mid < end then
                merge(A, start, mid, end)
            end if
        end for
        size := 2 * size
    end while
end procedure
```