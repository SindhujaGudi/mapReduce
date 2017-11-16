# mapReduce

 How many neighbors you have? 
 
In this project, you are asked to work on the MapReduce framework. 
MapReduce is one of important techniques to solve Big Data problems.  
Mainly, it has two main phases; namely Map phase and Reduce phase. In each one of these, you have sub-phases. 
Briefly, on a cluster of nodes/cores, during the Map phase, the cluster nodes running the map program should emit key-value pairs based on the split chunks of the input file. 
These key-value pairs will be consumed by the cluster nodes running the reduce program. 
The reduce component usually summarizes the data received by the map phase to produce the final output after the combining the output coming from several nodes.  
Objectives: 
1- Understanding the conceptual bases of the Map-Reduce frame work 
2- Solving a problem by applying the Map-Reduce framework 
3- Having the hands-on experience of developing and running Map-Reduce programs 
4- Gaining the skills for not only developing the code, but also:  
  a. creating excitable jar files,  
  b. moving data back and forth between the local system and the Hadoop file system,  
  c. configuring a Map-Reduce job,  
  d. submitting the job for execution, and  
  e. Obtaining the results.  
You will be given a network file. The file has the network you will work with. 
When you download the file from the link given below, you need to open it. 
You can extract the compressed file using WinRAR for instance. 
To open the network file, notepad or notepad++ will not be a good choice because the file is huge for a simple text editor. 
However, you can open it using a free editor such as PilotLite. The file needs a very simple cleaning. 
You need to remove the first 4 lines in order to keep the network only. 

Task One: 
In this project you will be solving the problem of counting the neighboring nodes of a node in a network. 
If two nodes have a link/an edge, they are considered neighbors. 
You can think of the network as Friendship network (nodes are friends and links represent friendship relations), Co-Authorship network (nodes are authors and links represent common work) …etc.    

Bonus Task: 
In this part, you are only asked to report the top 30 nodes with the largest number of neighbors in the network. 
If several nodes have the same number of neighbors, then you can break these ties randomly. 
If you decided to submit the bonus part, you have to submit separate files that are called Bonus.java AND Bonus.jar 
For the bonus part, the code has to produce accurate/correct results. No partial credit will be given. 
For more information please see below: 
1. General Information: Data Description  
  a. The network has 
    i. Nodes: 3072441  
    ii. Edges: 117185083 
  b. The uncompressed file size: 1.64 GB 
  c. The data in the file has the following format: 
  d.   
  1 11
  1 12
  1 13
  2 5
  2 6
  2 15
  2 60
  2 62
  e. The numbers represent node ids 
  f. Each line shows a link/edge in the network 
  g. In a line, every two nodes are delimited by the tab character (\t) 
  h. For instance, in the snapshot given in point d., the neighbors of node 1 are: 11, 12, and 13. The neighbors count is 3 (this is the number you need to report for each node) 
  i. For example, the output of the previous snapshot network given in d. would look like: 
  1 3 
  2 5 
  5 1 
  6 1 
  11 1 
  12 1 
  13 1 
  15 1 
  60 1 
  62 1  

Hints: 
As a starting point, you can think of only using a small part of the network during your development. 
a. For example you may use only the first 100 links/edges or even less. This will make testing your code easier.  
b. This is called working with toy dataset. This way, producing results will be faster and solving problems will be quicker. 
I recommend you think thoroughly of what your map and reduce parts will do before implementation begins.     

NOTE:
You should be developing this project under the Cloudera virtual machine. 
You should not need to install any special packages or libraries except the default compilers and libraries.
You need to develop the code using Java language only. 
In a zipped file, you are required to include two files: 
a. The MR.java code file 
b. The MR.jar executable file; it will be used to run your code 
c. Only one zipped file should be submitted per group.  
d. Your code file has to start with a block of comment.  1. This comment block has: Students names, ids, and sections 

For the bonus part: 
a. The Bonus.java code file 
b. The Bonus.jar executable file; it will be used to run your code 
c. Only one zipped file should be submitted per group.  
d. Your code file has to start with a block of comment.  1. This comment block has: Students names, ids, and sections 

The network file can be found in: a. http://snap.stanford.edu/data/bigdata/communities/com-orkut.ungraph.txt.gz 
Example that you may use on How to run the code: (Similarly for the bonus part with needed modifications) 
a. $ hadoop jar MR.jar MR  /user/cloudera/input_mr  /user/cloudera/output_mr 
b. The input_mr will have the input network data to work on 
c. The output will be stored in the output_mr folder 
