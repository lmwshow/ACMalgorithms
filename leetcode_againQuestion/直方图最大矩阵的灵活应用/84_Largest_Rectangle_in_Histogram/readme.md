题目链接:https://leetcode.com/problems/largest-rectangle-in-histogram/description/

题意:给定一个非负数组，里面每个元素表示长度为h[i]，宽为1的直方图，求其中组成的最大矩阵。

分析:直方图的最大矩阵算法，利用stack保存直方图的递增索引，一旦出现小于栈顶元素的高度，计算一次前面的矩阵面积，更新最大面积。
     栈顶元素出栈 curindex, 对于高度为h[curindex]计算以它为高(短板)的矩阵面积 , 由于stack中是一组递增的索引， 所以此时stack.peek() 和 curindex 直接的高度 都比 h[curindex] 高，不会成为短板.
     所有  ans = max(ans,h[curindex]*(stack.isEmpty()?i:(i-stack.peek()-1)))
     当stack为空时，说明当前h[curindex]为最矮短板， 最底层社会的人，长度就是全部。
