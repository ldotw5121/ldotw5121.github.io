---
layout: single
title: 벨만-포드 알고리즘
categories: [Assignment]
use_math: true
---

# **개요**

---

음수 가중치를 갖는 그래프에서 최단 경로를 찾는 것을 목적으로 하는 알고리즘이다.

음수 가중치가 순환하고 있는 경우에, 순환을 하면 할 수록 거리값이 무한대로 발산하기 때문에 이 때에는 최단 경로에 도달할 수 없다는 의미로 false값을 반환하고 함수를 종료시킬 수 있다.



# **의사코드**

![](https://i.imgur.com/Co6NVQ8.png)

1. **line 1**

   ​	그래프를 초기화 한다.

   ​	처음 시작할 노드를 제외한 모든 노드의 d[v]값을 무한대로 할당하고, 
   ​	시작노드의 d[v]값만 0으로 할당해준다.

2. **line 2 - 4**

   ​	노드의 수만큼 반복문을 돌며 모든 엣지에 대해 순환을 하게된다.

3. **line 5 - 8**

   ​	음수 가중치를 갖는 순환경로의 존재를 확인한다.

   ​	존재하면 최단경로가없다는 의미로 **false값**을 반환하고 존재하지 않는다면 알고리즘의 수행이 완료 되었다	는 의미로 **true값**을 반환한다.





# **시간복잡도**

---

그래프의 초기화 작업에 걸리는 $O(V)$

순환의 반복에 대해 걸리는 $O(E)$.

순환은 V-1번에 대해 총 $O(E)$번의 순환을 수행하므로

$ O(VE) $.

그래프의 엣지 수가 대체로 노드 수의 제곱에 근사하기에,

$ O(V^3) $









---



**출처**

[Shortest Path Algorithms](https://www.hackerearth.com/practice/algorithms/graphs/shortest-path-algorithms/tutorial/)

[위키피디아/벨먼-포드 알고리즘]([https://ko.wikipedia.org/wiki/%EB%B2%A8%EB%A8%BC-%ED%8F%AC%EB%93%9C_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98](https://ko.wikipedia.org/wiki/벨먼-포드_알고리즘))

[슈도코드](https://i.imgur.com/Co6NVQ8.png)