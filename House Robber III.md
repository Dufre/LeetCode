# Question

The thief has found himself a new place for his thievery again. There is only one entrance to this area, called the "root." Besides the root, each house has one and only one parent house. After a tour, the smart thief realized that "all houses in this place forms a binary tree". It will automatically contact the police if two directly-linked houses were broken into on the same night.

Determine the maximum amount of money the thief can rob tonight without alerting the police.

**Example 1:**
```
Input: [3,2,3,null,3,null,1]

     3
    / \
   2   3
    \   \ 
     3   1

Output: 7 
Explanation: Maximum amount of money the thief can rob = 3 + 3 + 1 = 7.
```
**Example 2:**
```
Input: [3,4,5,1,3,null,1]

     3
    / \
   4   5
  / \   \ 
 1   3   1

Output: 9
Explanation: Maximum amount of money the thief can rob = 4 + 5 = 9.
```

# Algorithm
Before this problem, maybe you should solve [House Robber](https://leetcode.com/problems/house-robber/) and [House Robber II](https://leetcode.com/problems/house-robber-ii/) first.

This is DP Problem, we can find recursive relation.

- cur node: `cur`
- left child node of cur: `left`
- right child node of cur: `right`
- left child node of left: `leftleft` 
- right child node of left: `leftright`
- left child node of right: `rightleft`
- right child node of right: `rightright`
- res[0]: end of root
- res[1]: end of left node or right node

So, the max value of cur node has two choice:
- cur->value + left[1] + right[1]
- max(left[0], right[0])

And actually, you can use res[2] to record this two choice.

# Code

**C++**
```c
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    //res[0]: end of root; res[1]: end of left node or right node
    vector<int> res = {0, 0};
    int rob(TreeNode* root) {
        helper(root);
        return max(res[0], res[1]);
    }
    
    vector<int> helper(TreeNode* root){
        if (root == NULL){
            res[0] = 0;
            res[1] = 0;
            return res;
        }
        
        vector<int> left = helper(root->left);
        vector<int> right = helper(root->right);
        
        res[0] = root->val + left[1] + right[1];
        res[1] = max(left[0], left[1]) + max(right[0], right[1]);
        
        return res;
    }
};
```
**Java**
```
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    //res[0]: end of root; res[1]: end of left node or right node
    //private int[] res = new int[2];
    public int rob(TreeNode root) {
        int[] res = helper(root);
        return Math.max(res[0], res[1]);
    }
    
    private int[] helper(TreeNode root){
        if (root == null){
            return new int[2];
        }
        
        int[] left = helper(root.left);
        int[] right = helper(root.right);
        int[] res = new int[2];
        
        res[0] = root.val + left[1] + right[1];
        res[1] = Math.max(left[0], left[1]) + Math.max(right[0], right[1]);
        
        return res;
    }
}
```
