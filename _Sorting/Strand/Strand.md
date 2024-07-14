# Pseudocode

```
procedure strandSort(A: list of sortable items) returns list
    if length(A) == 0 then
        return A
    end if
    result := new empty list
    while not A.isEmpty() do
        sublist := new list containing the first element of A
        A.removeFirst()
        i := 0
        while i < length(A) do
            if A[i] >= sublist[-1] then
                sublist.append(A[i])
                A.removeAt(i)
            else
                i := i + 1
            end if
        end while
        result := merge(result, sublist)
    end while
    return result
end procedure

procedure merge(left: list, right: list) returns list
    result := new empty list
    while not left.isEmpty() and not right.isEmpty() do
        if left[0] <= right[0] then
            result.append(left.removeFirst())
        else
            result.append(right.removeFirst())
        end if
    end while
    while not left.isEmpty() do
        result.append(left.removeFirst())
    end while
    while not right.isEmpty() do
        result.append(right.removeFirst())
    end while
    return result
end procedure
```