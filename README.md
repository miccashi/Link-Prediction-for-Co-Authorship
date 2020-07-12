# Link-Prediction-for-Co-Authorship

1. Introduction The network graph model has been generalized in many domains, such as social, biological, academic networks, to express relationships between entities (Wang, Satuluri & Parthasarathy, 2007). Link prediction is one of the interests in mining information from these complex networks, which can be used to predict future relationships between entities, find missing links, and identify spurious links in the network. 


2. Dataset
The network consists of 4085 nodes in total which means the maximum number of edges can achieve 𝑛(𝑛 − 1)/2 = 8,341,570, in which there only exist 26935 truly existing edges. Considering that there is the same number of true and fake edges in the test dataset, using all fake edges to train the model is not practical and would make classes unbalanced. Apart from this, there is no knowledge about how to choose the test dataset, we randomly choose the same number of negative samples with positive samples but intentionally add more fake edges with the shortest distance of 2 than randomly selected in order to improve the generalizability of the model.


Performance：

Algorithms                              AUC of logistic Regression            AUC of Neural Network    

Baseline(Random) Model                          50%                                 50% 


Mainstream Topological Features
(CN, Jaccard, SI, HPI, HDI, LHNI,
AA, Katz, COS, and LP) + 
Semantic Features                               93.24%                              97.56% 


Mainstream Topological Features +
Semantic Features + 
Community-Based Link Reliability                95.35%                              98.99% 
