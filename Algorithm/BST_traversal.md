Inorder with Iterator version
```
    def postorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        stack = []
        ret_list = []
        while root is not None:
          stack.append(root)
          root = root.left
        
        while len(stack) > 0:
          node = stack[-1].right
          
          if node is not None:
            stack.append(node)
            next_push_node = node.left
            while next_push_node is not None:
              stack.append(next_push_node)
              next_push_node = next_push_node.left
          else:
            node = stack.pop()
            while len(stack) > 0 and stack[-1].right == node:
              node = stack.pop()
          
          ret_list.append(node.val)
          
        return ret_list

```
Inorder with Iterator version:
```
    def preorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        ret_list = []
        stack = []
        while root is not None:
          stack.append(root)
          ret_list.append(root.val)
          root = root.left
        
        while len(stack) > 0:
          node = stack[-1].right
          if node is not None:
            stack.append(node)
            ret_list.append(node.val)
            node = node.left
            while node is not None:
              stack.append(node)
              ret_list.append(node.val)
              node = node.left
          else:
            node = stack.pop()
            while len(stack) > 0 and stack[-1].right == node:
              node = stack.pop()
          
        return ret_list
```

Postorder with Iterator version:

```
    def postorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        stack = []
        ret_list = []
        while root is not None:
          stack.append(root)
          root = root.left
        
        while len(stack) > 0:
          node = stack[-1].right
          
          if node is not None:
            stack.append(node)
            next_push_node = node.left
            while next_push_node is not None:
              stack.append(next_push_node)
              next_push_node = next_push_node.left
          else:
            node = stack.pop()
            ret_list.append(node.val)
            while len(stack) > 0 and stack[-1].right == node:
              node = stack.pop()
              ret_list.append(node.val)
            
        return ret_list

```
