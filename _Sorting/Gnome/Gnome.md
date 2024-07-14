# Pseudocode

```
procedure gnomeSort(A: list of sortable items)
    index := 0
    while index < length(A) do
        if index == 0 or A[index] >= A[index - 1] then
            index := index + 1
        else
            swap(A[index], A[index - 1])
            index := index - 1
        end if
    end while
end procedure
```