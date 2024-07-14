# Pseudocode

```
procedure pigeonholeSort(A: list of sortable items)
    min := findMin(A)
    max := findMax(A)
    size := max - min + 1
    holes := new list of length size
    for i := 0 to length(A) - 1 inclusive do
        holes[A[i] - min].append(A[i])
    end for
    index := 0
    for i := 0 to size - 1 inclusive do
        while not holes[i].isEmpty() do
            A[index] := holes[i].pop()
            index := index + 1
        end while
    end for
end procedure
```