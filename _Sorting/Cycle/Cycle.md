# Pseudocode

```
procedure cycleSort(A: list of sortable items)
    n := length(A)
    for cycle_start := 0 to n - 2 inclusive do
        item := A[cycle_start]
        pos := cycle_start
        for i := cycle_start + 1 to n - 1 inclusive do
            if A[i] < item then
                pos := pos + 1
        end for
        if pos == cycle_start then
            continue
        end if
        while item == A[pos] do
            pos := pos + 1
        end while
        if pos != cycle_start then
            swap(item, A[pos])
        end if
        while pos != cycle_start do
            pos := cycle_start
            for i := cycle_start + 1 to n - 1 inclusive do
                if A[i] < item then
                    pos := pos + 1
                end if
            end for
            while item == A[pos] do
                pos := pos + 1
            end while
            if item != A[pos] then
                swap(item, A[pos])
            end if
        end while
    end for
end procedure
```