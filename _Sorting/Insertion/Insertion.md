# Pseudocode

```
procedure insertionSort(A: list of sortable items)
    for i := 1 to length(A) - 1 inclusive do
        key := A[i]
        j := i - 1
        while j >= 0 and A[j] > key do
            A[j + 1] := A[j]
            j := j - 1
        end while
        A[j + 1] := key
    end for
end procedure
```