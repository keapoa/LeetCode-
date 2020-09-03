# LeetCode-
总结一些经典Leetcode题目写法---对应代码在同名文件中。比如1.1对应1.1  
一, 背包问题(均可拓展成0/1背包,完全背包，多重背包)。  
    总结各种套路：    
    1，组合问题：一个列表，一个目标值，求可能组合总数。(完全背包问题：数字可重复使用)(组合问题均可用DFS做)，动态背包作为优化方案。  
        考虑顺序指：2,1,1跟1,2,1是不同的. 这里面初始化都要初始化为1   
        考虑顺序：1.4  不考虑顺序：1.3  推导公式：dp[i]+=dp[i][i-num].解法细节不同：考虑顺序：先遍历target,后遍历nums.不考虑顺序：先遍历nums后遍历target. 具体写法参考代码  
        两者皆可用DFS，只是会有很多重复子问题。考虑顺序很简单，直接剪枝即可。不考虑顺序剪枝会麻烦些.但更符合完全背包问题。从背包角度更容易思考和优化.  
        组合变型题：1.5，可转化为0/1背包问题        
    2，最值问题，最大个数，最小个数。    
        递推公式：dp[i] = min(dp[i],dp[i-num]) or dp[i] = max(dp[i],dp[i-num]),比如最大：1.1，最小1.2。这两种题均可拓展为三种背包问题。      
    背包问题优化的时候二维数组转一维度数组要注意是否覆盖上一行，然后思考是否需逆序遍历。  
    1.1 https://leetcode-cn.com/problems/ones-and-zeroes/  一和零   
    1.2 https://leetcode-cn.com/problems/coin-change/   零钱兑换  
    1.3 https://leetcode-cn.com/problems/coin-change-2/ 零钱兑换2  
    1.4 https://leetcode-cn.com/problems/combination-sum-iv/ 组合总和IV  
    1.5 https://leetcode-cn.com/problems/partition-equal-subset-sum/ 分割等和子集
