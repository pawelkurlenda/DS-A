# Pseudocode

```
procedure shellSort(A: list of sortable items)
    n := length(A)
    gap := n / 2
    while gap > 0 do
        for i := gap to n - 1 inclusive do
            temp := A[i]
            j := i
            while j >= gap and A[j - gap] > temp do
                A[j] := A[j - gap]
                j := j - gap
            end while
            A[j] := temp
        end for
        gap := gap / 2
    end while
end procedure
```