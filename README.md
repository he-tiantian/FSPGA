Discovering Fuzzy Structural Patterns for Graph Analytics (FSPGA)

This repository contains the materials related to the manuscript "Discovering Fuzzy Structural Patterns for Graph Analytics," including the drafted version of the paper, and the executable of the algorithm.

If you want to read the full text of the paper, please check http://ieeexplore.ieee.org/document/8253904/. 

You are welcome to cite our paper via: T. He, and K. C. C. Chan, "Discovering Fuzzy Structural Patterns for Graph Analytics," IEEE Transactions on Fuzzy Systems, doi:10.1109/TFUZZ.2018.2791951, 2018.


How to use FSPGA 

To use FSPGA (FSPGA.exe) to detect clusters in an attributed graph, please firstly prepare four files, which are named as "Config.txt," "edgelist," "vertex2aid," and "statistics" and put them into the directory where FSPGA.exe is. The detailed information for these files is the following:

edgelist: This file contains the connections in the attributed graph. There are two columns in this file which are the ids of source and target nodes. It should be noted that the starting node id must be 0.

vertex2aid: This file contains attributes that each vertex in the graph is associated with. There are two columns. The first column contains the vertex ids and the second column contains the ids of attributes that are labeled with each vertex. It should be noted that the starting ids for both node and attribute must be 0.

Config.txt: This file contains the parameters used by FSPGA. There are 5 reals in this file. They are the settings related to the number of clusters, the bias between edge structure and attribute similarity in the optimization process, beta (degree of overlapping), the maximum number of optimizing iterations, and the minimum change of C between two iterations. Here is an example: 4 0.5 0.1 300 1e-9 This means the initial settings of FSPGA are the following: 4 clusters, 0.5 bias, 0.1 beta, 300 iterations of optimization, and 1e-9 minimum change. These parameters can be modified accordingly, or one may follow recommendations in the paper of FSPGA.

statistics: This file contains the information of the attributed graph. Here is an example: 500 9000 50 It means this attributed graph contained 500 vertices, 9000 edges, and 50 attributes, respectively. To help users get familiar with the files used by FSPGA, we provide the corresponding files of a set of attributed graph data which are in the directory ".\example". One may check them for the details.

After completing all the preparations, one is able to run FSPGA to perform the task of clustering in attributed graph data by running a .bat file in which contains the following codes: "FSPGA.exe pause." The results of clustering in the attributed graph will be written into a file after FSPGA completes the optimization process. If FSPGA cannot be executed, please check readme.txt for the requirements of running environment, which is in the zip file.

Notice: This software is permitted to use only for research and non-commercial activities. If you have any question, please feel free to contact us via tiantian.he@outlook.com.

At last, thanks very much for using FSPGA.
