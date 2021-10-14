---
layout: post
title: bfs/dfs - kakao blind recruitment(2)
categories: programmers
---

### 접근법

> 어쩌구 저ㄱ쩌구....블라블라


##### 어쩌구 저ㄱ쩌구....블라블라

### 문제풀이

	

```python
from collections import deque


def solution(n, computers):
    answer = 0
    visited = [0] * n
    nodes = []
    while 0 in visited:
        print(visited)
        x = visited.index(0)
        print(x)
        nodes.append(x)
        visited[x] = 1
        while nodes:
            node = nodes.pop(0)
            visited[node] = 1
            for i in range(n):
                if visited[i] == 0 and computers[node][i] == 1:
                    nodes.append(i)
                    visited[i] = 1
        answer += 1
    return answer
```
