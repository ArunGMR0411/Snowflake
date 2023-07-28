TRADITIONAL ARCHITECTURE
========================

## 1. Shared-Disk:
------------------

>Here we have single data storage Node - All the Nodes which executes/computes the queries access this shared Disk Node.  

**Advantages:**
>Easy to Manage  
Single source of all data

**Disadvantages:**
>Single point of Failure, if the Data node fails, no process can execute until it is fixed.  
Bandwidth and network latency, as everytime the data has to flow to and from the data node.  
Limited scalability.  

## 2. Shared-Nothing:
---------------
>Here, each Node has its own Data Storage and its own computation node  
This is what is being used in Spark and Hadoop - For example, Spark does not usually shuffle its data with other nodes instead tries to store the data necessary for the current computation within the node where the execution is happening.  
Just incase, Data needs to be shared, it happens through network.

**Advantages:**
> Co-locating compute and storage avoids network latency issues when data is not shared between nodes.  
Improved Scaling over shared disk.  

**Disadvantages:**
> Tendency to over provision which leads to increase in cost and hard to maintain the systems.  
