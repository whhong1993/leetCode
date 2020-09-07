## Question:

[https://leetcode-cn.com/problems/consecutive-numbers-sum/][https://leetcode-cn.com/problems/consecutive-numbers-sum/]

给定一个正整数 N，试求有多少组连续正整数满足所有数字之和为 N?

示例 1:

输入: 5
输出: 2
解释: 5 = 5 = 2 + 3，共有两组连续整数([5],[2,3])求和后为 5。
示例 2:

输入: 9
输出: 3
解释: 9 = 9 = 4 + 5 = 2 + 3 + 4
示例 3:

输入: 15
输出: 4
解释: 15 = 15 = 8 + 7 = 4 + 5 + 6 = 1 + 2 + 3 + 4 + 5
说明: 1 <= N <= 10 ^ 9

## Solution:

```php
class Solution {
    /**
     * @param Integer $N
     * @return Integer
     */
    function consecutiveNumbersSum($N) {
        $res = 0;
        $loop = ($N + 1) / 2; //也可换成根号下 2N + 1 
        for ($i = 1; $i <= $loop; $i++) {
            $k = ((2 * $N / $i) - $i + 1) / 2;
            if ($k <= 0) break;
            if (($k - ($k / 1)) === 0) {
                $res ++;
            }
            
        }
        return $res;
    }
}
```

[https://leetcode-cn.com/problems/consecutive-numbers-sum/]: https://leetcode-cn.com/problems/consecutive-numbers-sum/