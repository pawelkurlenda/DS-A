# Pseudocode

```
procedure countingSort(A: list of sortable items)
    max := findMax(A)
    count := new list of length max + 1 initialized to 0
    for i := 0 to length(A) - 1 inclusive do
        count[A[i]] := count[A[i]] + 1
    end for
    index := 0
    for i := 0 to max inclusive do
        while count[i] > 0 do
            A[index] := i
            index := index + 1
            count[i] := count[i] - 1
        end while
    end for
end procedure
```