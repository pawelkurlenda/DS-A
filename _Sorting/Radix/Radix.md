# Pseudocode

```
procedure radixSort(A: list of sortable items)
    maxNumber := findMax(A)
    exp := 1
    while maxNumber / exp > 0 do
        countingSortByDigit(A, exp)
        exp := exp * 10
    end while
end procedure

procedure countingSortByDigit(A: list of sortable items, exp: int)
    n := length(A)
    output := new list of length n
    count := new list of length 10 initialized to 0
    for i := 0 to n - 1 inclusive do
        index := (A[i] / exp) % 10
        count[index] := count[index] + 1
    end for
    for i := 1 to 9 inclusive do
        count[i] := count[i] + count[i - 1]
    end for
    for i := n - 1 downto 0 do
        index := (A[i] / exp) % 10
        output[count[index] - 1] := A[i]
        count[index] := count[index] - 1
    end for
    for i := 0 to n - 1 inclusive do
        A[i] := output[i]
    end for
end procedure
```