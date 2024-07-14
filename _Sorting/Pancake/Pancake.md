# Pseudocode

```
procedure pancakeSort(A: list of sortable items)
    n := length(A)
    for curr_size := n downto 1 do
        maxIndex := findMaxIndex(A, curr_size)
        if maxIndex != curr_size - 1 then
            flip(A, maxIndex)
            flip(A, curr_size - 1)
        end if
    end for
end procedure

procedure flip(A: list of sortable items, i: int)
    start := 0
    while start < i do
        swap(A[start], A[i])
        start := start + 1
        i := i - 1
    end while
end procedure
```