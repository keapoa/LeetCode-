# LeetCode-
总结一些经典Leetcode题目写法---对应代码在同名文件中。比如1.1对应1.1，后面对应的都是数字_+对应类别问题  
动态规划系列  
    一, 背包问题(均可拓展成0/1背包,完全背包,多重背包)。  
        总结各种套路：    
        1，组合问题：一个列表，一个目标值，求可能组合总数。(完全背包问题：数字可重复使用)(组合问题均可用DFS做)，动态方案作为优化方案。  
            考虑顺序指：2,1,1跟1,2,1是不同的. 这里面初始化都要初始化为1   
            考虑顺序：1.4  不考虑顺序：1.3  推导公式：dp[i]+=dp[i][i-num].解法细节不同：考虑顺序：先遍历target,后遍历nums.不考虑顺序：先遍历nums后遍历target. 具体写法参考代码  
            两者皆可用DFS，只是会有很多重复子问题。考虑顺序很简单，直接DFS剪枝即可。不考虑顺序剪枝会麻烦些.但更符合完全背包问题。从背包角度更容易思考和优化.  
            组合变型题：1.5，可转化为0/1背包问题        
        2，最值问题，最大个数，最小个数。    
            递推公式：dp[i] = min(dp[i],dp[i-num]) or dp[i] = max(dp[i],dp[i-num]),比如最大：1.1，最小1.2。这两种题均可拓展为三种背包问题。      
        背包问题优化的时候二维数组转一维度数组要注意是否覆盖上一行，然后思考是否需逆序遍历。  
        1.1 https://leetcode-cn.com/problems/ones-and-zeroes/  一和零   
        1.2 https://leetcode-cn.com/problems/coin-change/   零钱兑换  
        1.3 https://leetcode-cn.com/problems/coin-change-2/ 零钱兑换2  
        1.4 https://leetcode-cn.com/problems/combination-sum-iv/ 组合总和IV  
        1.5 https://leetcode-cn.com/problems/partition-equal-subset-sum/ 分割等和子集  
    二, 子序列子串问题  
        #回文通常利用二维数组：回文的判断需要左右两个边界，这里子串要注意相邻相同的情况。其它一维即可。  
        https://leetcode-cn.com/problems/longest-palindromic-subsequence/  最长回文子序列    
        https://leetcode-cn.com/problems/longest-palindrome/ 最长回文串--这个意思是给的字符串能组合成的最长回文串  
        https://leetcode-cn.com/problems/longest-palindromic-substring/ 最长回文子串  
        https://leetcode-cn.com/problems/longest-increasing-subsequence/  最长上升子序列    
        https://leetcode-cn.com/problems/longest-common-subsequence/  最长公共子序列  
        https://leetcode-cn.com/problems/longest-continuous-increasing-subsequence/  最长连续递增序列  这个直接滑动窗口就行。  
    三, 丑数问题       
        #解法：常规解法：判断丑数->生成。最小堆，动态规划。  
        https://leetcode-cn.com/problems/chou-shu-lcof/submissions/  
        https://leetcode-cn.com/problems/ugly-number/   
    四, 二三四数之和    
        #套路题解：排序，双指针求二数之和，注意去重，三数一个循环套用二数之和函数，注意去重，一次类推。  
        https://leetcode-cn.com/problems/4sum/submissions/  
        https://leetcode-cn.com/problems/3sum/  
        https://leetcode-cn.com/problems/two-sum/   
    五, k相关题目  
        https://leetcode-cn.com/problems/smallest-k-lcci/submissions/  最小k个数,三种解法。  
        https://leetcode-cn.com/problems/kth-largest-element-in-a-stream/  数据流中的第k大元素  
        https://leetcode-cn.com/problems/merge-k-sorted-lists/submissions/  合并k个升序链表  
    六, DFS组合型题目    
        https://leetcode-cn.com/problems/subsets/  子集  
        https://leetcode-cn.com/problems/subsets-ii/    
        https://leetcode-cn.com/problems/permutations/  排列  
        https://leetcode-cn.com/problems/permutations-ii/    
        https://leetcode-cn.com/problems/zi-fu-chuan-de-pai-lie-lcof/  字符串排列  
        https://leetcode-cn.com/problems/generate-parentheses/  括号生成  
    七, DFS路径型题目  
        https://leetcode-cn.com/problems/path-sum/  路径总和    
        https://leetcode-cn.com/problems/path-sum-ii/  路径总和Ⅱ    
        https://leetcode-cn.com/problems/path-sum-iii/  路径总和Ⅲ    
        https://leetcode-cn.com/problems/minimum-path-sum/  最小路径和    
    八, BFS类型题目    
        https://leetcode-cn.com/problems/binary-tree-level-order-traversal/  二叉树的层次遍历    
        https://leetcode-cn.com/problems/binary-tree-level-order-traversal-ii/  二叉树的层次遍历Ⅱ    
        https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/  二叉树的锯齿形层次遍历    
        https://leetcode-cn.com/problems/average-of-levels-in-binary-tree/  二叉树的层平均值    
        https://leetcode-cn.com/problems/minimum-depth-of-binary-tree/  二叉树的最小深度  这个比较容易出错    
        https://leetcode-cn.com/problems/average-of-levels-in-binary-tree/  二叉树的层  
        https://leetcode-cn.com/problems/populating-next-right-pointers-in-each-node/  填充每个节点的下一个节点  
    九, 翻转链表题目    
        https://leetcode-cn.com/problems/reverse-linked-list/  反转链表    
        https://leetcode-cn.com/problems/reverse-linked-list-ii/  反转链表Ⅱ    
        https://leetcode-cn.com/problems/reverse-nodes-in-k-group/  k个一组反转链表    
    十, 链表快慢指针    
       https://leetcode-cn.com/problems/linked-list-cycle/  环形链表    
       https://leetcode-cn.com/problems/linked-list-cycle-ii/  环形链表Ⅱ    
       https://leetcode-cn.com/problems/happy-number/  快乐数  非链表    
       https://leetcode-cn.com/problems/middle-of-the-linked-list/  链表的中间节点  
    十一, 双指针    
       https://leetcode-cn.com/problems/two-sum/  两数之和    
       https://leetcode-cn.com/problems/squares-of-a-sorted-array/  有序数组的平方  
       https://leetcode-cn.com/problems/subarray-product-less-than-k/  乘积小于k的子数组  
    十二, 删除重复节点问题  
       https://leetcode-cn.com/problems/shu-zu-zhong-zhong-fu-de-shu-zi-lcof/  删除数组中的重复数字  
       https://leetcode-cn.com/problems/remove-duplicates-from-sorted-array/  删除排序数组中的重复项  
       https://leetcode-cn.com/problems/remove-duplicates-from-sorted-array-ii/  删除排序数组中的重复项Ⅱ  
       https://leetcode-cn.com/problems/remove-duplicates-from-sorted-list/  删除排序链表中的重复项  
       https://leetcode-cn.com/problems/remove-duplicates-from-sorted-list-ii/  删除排序链表中的重复项Ⅱ  
    十三, 滑动窗口题目  
       https://leetcode-cn.com/problems/subarray-sum-equals-k/  
       https://leetcode-cn.com/problems/longest-substring-with-at-least-k-repeating-characters/  至少有K个重复字符的最长子串  
       https://leetcode-cn.com/problems/longest-substring-without-repeating-characters/  无重复字符的最长子串  
    十四, 子数组子串子序列等
    十五, 单调双向队列题目，单调栈    
        https://leetcode-cn.com/problems/hua-dong-chuang-kou-de-zui-da-zhi-lcof/  滑动窗口最大值    
    十六, 二叉树遍历  
        #一般有DFS和迭代法，DFS较简单，迭代法(用栈模拟递归过程)常用一个栈一个当前变量，对于后序遍历左右中通常转为中右左进行遍历，结果取反即可。  
        #对于前序后序迭代：中在前面，直接一个栈即可，注意先入后出。比如前序->中前后，需要先入后在入前，会先弹出前。中序遍历：前中后  
        #N叉树更简单-理解root.children包含所有节点可迭代即可  
        https://leetcode-cn.com/problems/binary-tree-inorder-traversal/  二叉树的中序遍历  
        https://leetcode-cn.com/problems/binary-tree-preorder-traversal/  二叉树的前序遍历  
        https://leetcode-cn.com/problems/binary-tree-postorder-traversal/  二叉树的后序遍历  
        https://leetcode-cn.com/problems/binary-tree-level-order-traversal/  二叉树的层序遍历  
        https://leetcode-cn.com/problems/binary-tree-level-order-traversal-ii/  二叉树的层序遍历Ⅱ  
        https://leetcode-cn.com/problems/n-ary-tree-preorder-traversal/  N叉树的前序遍历  
        https://leetcode-cn.com/problems/n-ary-tree-postorder-traversal/  N叉树的后序遍历  
        https://leetcode-cn.com/problems/n-ary-tree-level-order-traversal/ N叉树的层序遍历  
    十七, 二叉树深度理解递归  
        #1:明确函数定义是什么。2:明确子树做什么。3:明确终止条件是什么。4:如何将子问题转化为大问题。  
        #二叉树题目均可这样思考。这里挑个别题目    
        #这种题目：可以前序(有点自顶向下的意思)走也可以后序(有点自底向上的意思)走。
        #前序：中-前-后,先判断中间，递归两边。后序：前-后-中，先递归前后，后判断中。
        https://leetcode-cn.com/problems/flatten-binary-tree-to-linked-list/  二叉树转化为单链表->就是单向子树均指向右边。    
        https://leetcode-cn.com/problems/invert-binary-tree/  翻转二叉树    
        https://leetcode-cn.com/problems/ping-heng-er-cha-shu-lcof/  平衡二叉树  
        
        
