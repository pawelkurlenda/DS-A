# Pseudocode

```
procedure treeSort(A: list of sortable items)
    root := null
    for i := 0 to length(A) - 1 inclusive do
        root := insert(root, A[i])
    end for
    index := 0
    inorderTraversal(root, A, index)
end procedure

procedure insert(node: TreeNode, value: int) returns TreeNode
    if node == null then
        return new TreeNode(value)
    end if
    if value < node.value then
        node.left := insert(node.left, value)
    else
        node.right := insert(node.right, value)
    end if
    return node
end procedure

procedure inorderTraversal(node: TreeNode, A: list of sortable items, index: int)
    if node != null then
        inorderTraversal(node.left, A, index)
        A[index] := node.value
        index := index + 1
        inorderTraversal(node.right, A, index)
    end if
end procedure
```