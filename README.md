# Project Title

Fairness-aware fake news mitigation using counter information propagation
## Description

In this repository, all contribution presented in the paper Fairness-aware fake news mitigation using counter information propagation are collected.



### Dependencies

* To make use of the presented code, version 3.7 or above for python were used.
* The necessary packages are imported at the beginning of each code file.


### Installing

* The code in the repository shall encourage future work in the area of fairness. Thus, it is for public use and can directly be used after being downloaded.

### Content

*The proposed fairness aware method for the IBM problem, namely WRRS, found in WRRS.ipynb under the function FWRRS_method.
  This can be utilized to generate a positive seed S_P to block the propagation of some information a seed S_N will be spreading using COICM (Campaign Oblivious Independent cascade model) in
  the inputted network, while maximizing the fairness of the intervention of S_P against the information of S_N across the communities 
  present in such network.
  The input consists then of:
    - A network G(V, E), this shall be defined using networkx in python.
    - A set S_N of node in G, this will spread the information which shall be blocked.
    - A budget k, representing the number of nodes which will be selected to construct S_P
    - A partioning into communities of network G, partition
    - A probability, min_inf, used to define the minimum probability of infection for a path to be explored in the constructed WRRS 
    - A threshold value, threshold, used to consider the set of WRRs sufficient.
                             
* Extensions for existing methods, to achieve higher fairness.
  First is Parity seeding, which was adapted for the IBM problem, as it was originally designed for the IM problem. The input similar to FWWRS consists of G, S_N, k and partition. This can be found in Parity_seeding_IBM.ipynb by calling parity_seeding_IBM
  Second is Fair_CMIA-O defined in Fair_CMIA-O.ipynb in the function CMIA_O_fair_new. The only additional input compared to parity seeding is a threshold used to determine if a path in the generated MIIAs should be explored.
*The HICH-BA model, defined in HICH-BA.ipynb called in the function hichba. Used to generate social networks with specified characteristics such as community sizes, clustering coefficient, etc. 
  This model uses the following parameters: 
    (i) n, i.e., the desired number of nodes,
    (ii) p_N, i.e., the probability of adding a node to the graph, with probability 1 − pN an edge is added,
    (iii) r, list where each entry r_i corresponds to the probability of a new node belonging to community i,
    (iv) h, i.e., the homophily factor and represents the probability of a node establishing an intra-community connection,
    (v)p_T, the probability to form a close triad connection,
    (vi) p_PA, the probability with which a new edge will be established using the preferential attachment (PA)


## Authors

Critina Gutierrez Bierbooms
cgubierbooms@gmail.com

Akrati Saxena 
a.saxena@liacs.leidenuniv.nl

