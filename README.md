# leetcode_Regular_Expression_Matching
+ input 값을 주고 regular expression을 주면 regular expression으로 우리의 input값을 찾을 수 있는지 구하는 문제
+ 給一個input值和一個regular expression判斷出是否可以透過regular expression找出我們給的input值

-----
+ Example1
```
Input: s = "aa", p = "a"
Output: false
Explanation: "a" does not match the entire string "aa".
```
----
+ Example2
```
Input: s = "aa", p = "a*"
Output: true
Explanation: '*' means zero or more of the preceding element, 'a'. Therefore, by repeating 'a' once, it becomes "aa".
```
----
+ Example3
```
Input: s = "ab", p = ".*"
Output: true
Explanation: ".*" means "zero or more (*) of any character (.)".
```
----
```python
import re
class Solution:
    def isMatch(self, s: str, p: str) -> bool:
        res = re.findall(p,s) # findall을 이용하여 문제에서 주어진 regular expression으로 답을 찾을 수 있는지 판단 후 res에 저장하기
        ans = True if len(res) != 0 and res[0] == s else False # 저장된 답의 길이가 0이 아니고 저장된 답이 처음에 주어진input값과 같을떄 return True else False
        return(ans)
```
---
```
결론 : 
요번에도 역시 re를 이용하여 쉽게 regualr expression 을 사용해 문제를 풀 수 있었다
```
---
```
結論:
透過簡單的函示庫 re來解答這次的問題
```
---
### Result
Runtime: 71 ms, faster than 61.61% of Python3 online submissions for Regular Expression Matching.\
Memory Usage: 14 MB, less than 61.00% of Python3 online submissions for Regular Expression Matching.
