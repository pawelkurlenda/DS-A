# Pseudocode

```
procedure bucketSort(A: list of sortable items)
    n := length(A)
    max := findMax(A)
    buckets := new list of length n
    for i := 0 to n - 1 inclusive do
        buckets[i] := new empty list
    end for
    for i := 0 to n - 1 inclusive do
        index := n * A[i] / (max + 1)
        append A[i] to buckets[index]
    end for
    for i := 0 to n - 1 inclusive do
        insertionSort(buckets[i])
    end for
    index := 0
    for i := 0 to n - 1 inclusive do
        for j := 0 to length(buckets[i]) - 1 inclusive do
            A[index] := buckets[i][j]
            index := index + 1
        end for
    end for
end procedure
```