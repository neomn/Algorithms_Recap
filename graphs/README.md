# Graphs
### different types of graphs
![graph-types](assets/types-of-graphs.png)

## Dijkstra
Dijkstra's algorithm is used to find the shortest path between two nodes in a graph. Some key properties and uses of Dijkstra's algorithm include:

* It is used to find the shortest path from a starting node to all other nodes in a weighted graph. The weights on edges can represent distances, costs, etc.
* Works on graphs with nonnegative edge weights. Does not work for graphs with negative edge weights.
* Uses a greedy approach to iteratively calculate shortest paths and update distances.
* At each iteration, it finds the unvisited node with the smallest known distance from the start node, calculates its distance from its neighbors, and updates the neighbor distances if shorter paths are found.
* Maintains a priority queue (often implemented with a min heap) to efficiently find the node with lowest distance at each step.
* Runs in O(E log V) time, where E is the number of edges and V is the number of vertices/nodes.
* Key applications include route planning, network routing, and any problem that requires finding shortest paths on a graph.
  
  ![dijkstra-2](assets/dijkstra-2.gif)
  
```Python
import heapq

graph = {
  'A': {'B': 4, 'D': 2},
  'B': {'A': 4,'C': 3, 'D': 1, 'E': 5},
  'C': {'B': 3, 'E': 6},
  'D': {'A': 2, 'B': 1, 'E': 8},
  'E': {'D': 8, 'B': 5, 'C': 6}
}

def dijkstra(graph, start, goal):
  distances = {node: float('inf') for node in graph}
  distances[start] = 0
  
  queue = [(0, start)]
  while queue:
    current_distance, current_node = heapq.heappop(queue)
    if current_distance > distances[current_node]:
      continue
    for neighbor, weight in graph[current_node].items():
      new_distance = current_distance + weight
      if new_distance < distances[neighbor]:
        distances[neighbor] = new_distance
        heapq.heappush(queue, (new_distance, neighbor))        
  return distances[goal]

print(dijkstra(graph, 'A', 'E'))
```
