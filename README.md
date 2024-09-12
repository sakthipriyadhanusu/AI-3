# Ex.No: 1 Implementation of Breadth First Search

REGISTER NUMBER : 212222040139
# AIM:
To write a python program to implement Breadth first Search.

# Algorithm:
Start the program
Create the graph by using adjacency list representation
Define a function bfs and take the set “visited” is empty and “queue” is empty
Search start with initial node and add the node to visited and queue.
For each neighbor node, check node is not in visited then add node to visited and queue list.
Creating loop to print the visited node.
Call the bfs function by passing arguments visited, graph and starting node.
Stop the program.

# Program:
```
import math
def minimax (curDepth, nodeIndex, maxTurn, scores,targetDepth):
    # base case : targetDepth reached
    if (curDepth == targetDepth):
        return scores[nodeIndex]
    if (maxTurn):
        return max(minimax(curDepth + 1, nodeIndex * 2,False, scores, targetDepth),
                   minimax(curDepth + 1, nodeIndex * 2 + 1,
                    False, scores, targetDepth))
     
    else:
        return min(minimax(curDepth + 1, nodeIndex * 2, True, scores, targetDepth),
                   minimax(curDepth + 1, nodeIndex * 2 + 1,
                     True, scores, targetDepth))
     
# Driver code
scores = [3, 5, 2, 9, 12, 5, 23, 20]
treeDepth = math.log(len(scores), 2) # calculate depth of node  log 8 (base 2) = 3)
print("The optimal value is : ", end = "")
print(minimax(0, 0, True, scores,treeDepth))
```
# Output:
![image](https://github.com/user-attachments/assets/358fef5b-f306-4fb5-8f63-204ac7aeeae2)

# Result:
Thus the breadth first search order was found sucessfully.
