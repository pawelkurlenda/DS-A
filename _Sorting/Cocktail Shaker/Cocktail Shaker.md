# Pseudocode

```
procedure cocktailShakerSort(A: list of sortable items)
    n := length(A)
    swapped := true
    start := 0
    end := n - 1
    while swapped do
        swapped := false
        for i := start to end - 1 inclusive do
            if A[i] > A[i + 1] then
                swap(A[i], A[i + 1])
                swapped := true
            end if
        end for
        if not swapped then
            break
        end if
        swapped := false
        end := end - 1
        for i := end - 1 downto start inclusive do
            if A[i] > A[i + 1] then
                swap(A[i], A[i + 1])
                swapped := true
            end if
        end for
        start := start + 1
    end while
end procedure
```