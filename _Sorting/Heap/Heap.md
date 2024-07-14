# Pseudocode

```
procedure heapSort(A: list of sortable items)
    n := length(A)
    for i := n / 2 - 1 downto 0 do
        heapify(A, n, i)
    end for
    for i := n - 1 downto 0 do
        swap(A[0], A[i])
        heapify(A, i, 0)
    end for
end procedure

procedure heapify(A: list of sortable items, n: int, i: int)
    largest := i
    left := 2 * i + 1
    right := 2 * i + 2
    if left < n and A[left] > A[largest] then
        largest := left
    end if
    if right < n and A[right] > A[largest] then
        largest := right
    end if
    if largest != i then
        swap(A[i], A[largest])
        heapify(A, n, largest)
    end if
end procedure
```