# 다익스트라 알고리즘

* O(ElogV)
* **출발지 고정, 음수 간선 없는 그래프에 해당한다.**
* 그래프 방향 유무는 상관 없다.
* 그래프의 한 정점에서 모든 정점까지의 최단거리를 각각 구할 때 사용한다.

## 방법론

0. A와 B 사이의 거리를 나타내는 **P[A][B]** 를 만들고 정보를 저장한다.
1. **미방문 집합**을 만든다.
	1. S = {}
	2. Q = {모든 A값 담기}
2. 출발점으로부터의 최단거리를 저장할 배열 **d[v]** 를 만든다.
	1. 출발 노드에는 0을, 출발점을 제외한 다른 노드들에는 INF를 채워 넣는다.
	2. 현재 노드를 나타내는 변수 A에 출발 노드의 번호를 저장한다.
3. A에서 갈 수 있는 노드 B에 대해, **d[A]+P[A][B]와 d[B]의 값을 비교**한다.
	1. d[A]+P[A][B] : 출발 노드에서 A를 거쳐서 B로 가는 최단거리
	2. d[B] : 출발노드에서 B로 바로가는 최단거리
4. **만약 d[A]+P[A][B]의 값이 더 작다면, d[B]의 값을 이 값으로 업데이트** 한다.
5. A의 모든 이웃 B에 대해 이 과정을 수행한다.
	1. 이후 정점 A를 Q에서 제거하고, S에 넣는다. 앞으로 A는 사용하지 않는다.
	2. Q에 있는 노드 중 출발점으로부터의 거리가 가장 짧은 노드를 골라서 그 노드를 A로 변경한다.
6. 더 이상 미방문 노드를 선택할 수 없을 때까지 3~5의 과정을 반복한다.


## 구현
```C++
int dijkstra(int start) {
    que.push({0, start});

    while (!que.empty()) {
        int cost = -que.top().first;
        int A = que.top().second;
        que.pop();

        if(D[A]<cost)
            continue;

        for (int i = 0; i < vec[A].size(); i++) {
            to = vec[A][i].first; 
            weight = vec[A][i].second;

            if (D[to] > D[A] + weight) {
                D[to] = D[A] + weight;
                que.push({-D[to], to});
            }
        }
    }

    return 0;
}

```
```python
def dijkstra(mat, start):
    dist = [INF] * (n+1)
    dist[start] = 0

    Q = []
    heapq.heappush(Q, [dist[start], start])

    while Q:
        curr_dist, curr_dest = heapq.heappop(Q)

        if curr_dist > dist[curr_dest]:
            continue

        for new_dest, new_dist in mat[curr_dest]:
            distance = curr_dist + new_dist
            
            if distance < dist[new_dest]:
                dist[new_dest] = distance

                heapq.heappush(Q, [dist[new_dest], new_dest])
            
    return dist
```