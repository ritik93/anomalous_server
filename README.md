## Problem Statement
  
The dataset contains two features - 
   * throughput (mb/s) and 
   * latency (ms) of response of each server.

While our servers were operating, we collected $m=307$ examples of how they were behaving, and thus have an unlabeled dataset $\{x^{(1)}, \ldots, x^{(m)}\}$. 
* We suspect that the vast majority of these examples are “normal” (non-anomalous) examples of the servers operating normally, but there might also be some examples of servers acting anomalously within this dataset.  
  
  
## Solution
We will use a Gaussian model to detect anomalous examples in our dataset. 
* We will first start on a 2D dataset that will allow us to visualize what the algorithm is doing.
* On that dataset we will fit a Gaussian distribution and then find values that have very low probability and hence can be considered anomalies. 
* After that, we will apply the anomaly detection algorithm to a larger dataset with many dimensions.
