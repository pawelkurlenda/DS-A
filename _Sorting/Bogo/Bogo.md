# Pseudocode

```
procedure bogoSort(A: list of sortable items)
    while not isSorted(A) do
        shuffle(A)
    end while
end procedure

procedure isSorted(A: list of sortable items) returns boolean
    for i := 1 to length(A) - 1 inclusive do
        if A[i - 1] > A[i] then
            return false
        end if
    end for
    return true
end procedure

procedure shuffle(A: list of sortable items)
    for i := 0 to length(A) - 1 inclusive do
        j := random number from 0 to i inclusive
        swap(A[i], A[j])
    end for
end procedure
```