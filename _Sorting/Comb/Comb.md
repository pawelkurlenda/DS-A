# Pseudocode

```
procedure combSort(A: list of sortable items)
    n := length(A)
    gap := n
    shrink := 1.3
    sorted := false
    while gap > 1 or not sorted do
        gap := int(gap / shrink)
        if gap < 1 then
            gap := 1
        end if
        sorted := true
        for i := 0 to n - gap - 1 inclusive do
            if A[i] > A[i + gap] then
                swap(A[i], A[i + gap])
                sorted := false
            end if
        end for
    end while
end procedure
```