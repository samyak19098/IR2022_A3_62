# IR2022_A3_62

##Question - 1

We were asked to pick a real-world network dataset with nodes > 100, so for this purpose, we have chosen wiki-vote to be our dataset. The network has information about Wikipedia voting (related to the promotion of user to adminship) and the data is collected from the period of the start of Wikipedia to Januray 2008. The nodes in the network represent the Wikipedia users, and a directed edge in the graph from ith node to jth node represents that user i voted for user j.

###Methodology

Firstly, it was observed that the nodeIDs were not continuous in a particular range of integers thus we assigned a unique node number to each node and maintained a map from nodeID to nodeNumber and vice versa too. the nodeNumber is an integer in the range [0, N] where N = Number of nodes in the graph.
Following this, we form an ‘adjacency matrix’ and ‘edge list’ representing the network. The ‘adjacency matrix’ A is an NxN matrix where Aij=1 if there is an edge from the node with nodeNumber ‘i’ to the node with nodeNumber ‘j’ in the directed network otherwise, Aij = 0. Edge list is a list of tuples where each tuple (i,j) represents that there is an edge from the node with nodeNumber ‘i’ to the node with nodeNumber ‘j’ in the directed network. 
