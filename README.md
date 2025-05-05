# Network-Analysis-and-Community-Detection-in-Corporate-Email-Networks-

Dataset Information:
The network was generated using email data from a large European research institution. We have anonymized information about all incoming and outgoing email between members of the research institution. The e-mails only represent communication between institution members (the core), and the dataset does not contain incoming messages from or outgoing messages to the rest of the world. A directed edge (u, v, t) means that person u sent an e-mail to person v at time t. A separate edge is created for each recipient of the e-mail. We also have four sub-networks corresponding to the communication between members of four different departments at the institution. Node IDs in the sub-networks do not correspond to the same node ID in the entire network.
The static version of this network is the same as the largest weakly connected component of the email-Eu-core network (although the node IDs are not the same).
Dataset statistics (email-Eu-core-temporal)
Nodes	986
Temporal Edges	332334
Edges in static graph	24929
Time span	803 days

Dataset statistics (email-Eu-core-temporal-Dept1)
Nodes	309
Temporal Edges	61046
Edges in static graph	3031
Time span	803 days

Dataset statistics (email-Eu-core-temporal-Dept2)
Nodes	162
Temporal Edges	46772
Edges in static graph	1772
Time span	803 days

Dataset statistics (email-Eu-core-temporal-Dept3)
Nodes	89
Temporal Edges	12216
Edges in static graph	1506
Time span	802 days
Dataset statistics (email-Eu-core-temporal-Dept4)
Nodes	142
Temporal Edges	48141
Edges in static graph	1375
Time span	803 days

Objectives:
To study network measures and community detection within a research institute’s email network.
•	Determine Network Properties of the datasets 
o	Finding number of Degrees, In-Degree, and Out-Degree
o	Average Clustering Coefficient
o	Average Degree
o	Numbers of Strongly Connected Components (SCC)
o	Numbers of Weakly Connected Components (WCC)
o	Numbers of Attracting Components
o	Degree Centrality

•	Determine Communities in Email Network
o	K-Clique Percolation Method
o	Girvan Newman Method
o	Louvain Method 

Network Properties:
•	Number of degrees, in-degrees, and out-degrees

 <img width="355" alt="image" src="https://github.com/user-attachments/assets/b3a8386d-15d3-449b-9fc8-1e5514bcd9e6" />



•	Degree Centrality

<img width="355" alt="image" src="https://github.com/user-attachments/assets/ab3567c4-ee40-43c7-a556-835d0ab853e3" />


 

•	Properties

<img width="355" alt="image" src="https://github.com/user-attachments/assets/59c19f90-5d33-4377-9e46-c4fb736ddeb8" />




Visualization of the dataset:
Dataset statistics (email-Eu-core-temporal)

<img width="335" alt="image" src="https://github.com/user-attachments/assets/0c4c4b9a-ad58-4e20-9f4c-3910ed496180" />


 
email-Eu-core-temporal-Dept1 

<img width="335" alt="image" src="https://github.com/user-attachments/assets/26874e58-977a-4519-9365-8dfec72f2482" />

 
email-Eu-core-temporal-Dept2

<img width="335" alt="image" src="https://github.com/user-attachments/assets/aec384cd-134e-49e1-98f3-b8120e51d3c6" />



email-Eu-core-temporal-Dept3

<img width="335" alt="image" src="https://github.com/user-attachments/assets/7254ba08-e7c0-42ba-ae9e-2809f5ed1b05" />

 


email-Eu-core-temporal-Dept4

<img width="335" alt="image" src="https://github.com/user-attachments/assets/bc9d74e4-4398-4acb-8aa5-389277321646" />




Community Detection:
Community Detection is defined as two nodes who are more closely connected to each other due to their greater number of interactions are likely to be part of the same community.
It helps to understand unique set of correlation within a community that distinguished them from other community.
•	K-Clique Percolation Method
This is a method to find overlapping communities. It is based on the concept that internal edges of community is likely to form cliques and intercommunity edges are unlikely to form cliques.
Algorithm:
1.	Locate maximal Cliques 
2.	Convert from Cliques to K-Cliques communities

<img width="319" alt="image" src="https://github.com/user-attachments/assets/e5081fa6-4a4b-472a-860b-b01603bb15c2" />

 
 
•	Girvan Newman Method
Girvan Newman is an hierarchical method used for detecting communities in complex systems.
Algorithm:
1.	For every edge, calculate the edge betweenness centrality
2.	Remove the edge with the highest betweenness centrality
3.	Calculate the betweenness centrality for every remaining edge
4.	Repeat Step 2 and 4, until there are no edges left

<img width="335" alt="image" src="https://github.com/user-attachments/assets/28fc91c3-97d2-49b4-8da0-1727cf84a36f" />

  
 
Using Girvan Newman Method, we find 3 communities.

•	Louvain Method
The method is a greedy optimization method that attempts to optimize the "modularity" of a partition of the network. It is suitable for large networks.
Algorithm:
1.	Firstly, look for "small" communities by optimizing modularity locally.
2.	Secondly, it aggregates nodes belonging to the same community and builds a new network whose nodes are the communities. 
3.	Repeat Step 2 and 3, until a maximum of modularity is attained and a hierarchy of communities is produced.


<img width="399" alt="image" src="https://github.com/user-attachments/assets/093acca1-4c53-4132-b3f9-4b84bb439761" />

 
