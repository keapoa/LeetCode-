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
