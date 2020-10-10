# 吃豆人实验

## version
`0.1.5`

## Lab 2.5
> 在角落迷宫的四个角上面有四个豆。这个搜索问题要求找到一条访问所有四个角落的最短的路径。  

实验报告给出的指令 `python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem` 要求我们使用 bfs 搜索，prob 类型为 CornersProblem。 我们需要补充 `searchAgent` 文件下 `CornersProblem` 类的方法。  
<br>
与问题2类似，我们使用 bfs，区别在于问题2的 state 仅包含坐标信息，而问题5的应该再包含元组 (bool, bool, bool ,bool), 表示是否吃到四个角的豆子。  
**state结构:**
state: ((x, y), (haveEatenFood1, haveEatenFood2, haveEatenFood3, haveEatenFood4))  
终止状态为 ((_, _), (true, true, ture, ture))  (_代表任意值)

