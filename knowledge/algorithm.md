# Data Structure
## binary tree
binary tree has recursive structure so lots of problem can be tackled by recursive algorithm. 
There are three kinds of travesal for tree structure:
* Pre-order
* In-order
* Post-order

## Problems
* [Balanced Binary Tree](https://leetcode.com/problems/balanced-binary-tree/)
Given a binary tree, determine if it is height-balanced.
For this problem, a height-balanced binary tree is defined as a binary tree in which the depth of the two subtrees of every node never differ by more than 1.

<code>public class Solution {
    public boolean isBalanced(TreeNode root) {
        return Depth(root) >= 0;
    } 
    public int Depth(TreeNode root) {
        if(root == null)
            return 0;
        else {
            int left = Depth(root.left);
            int right = Depth(root.right);
            if(left >= 0 && right >= 0 && Math.abs(left - right) < 2)
                return Math.max(left, right) + 1;
            else
                return -1;
        }
    }
}</code>
