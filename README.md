We will be trying to predict new problem to coder based on its previous records. We will be using user-user collaborative filtering. We are also given with the problem data for the profiling of problems.
There will be step by step guide to how the analysis and prediction is being done.

Data Analysis Part
===

By making the countplot of the ranks, we get to know that there are small number of people who are at the advanced level, and we have very less number of experts.
![rank_countplot](https://user-images.githubusercontent.com/20907692/45989603-ee7cf380-c06b-11e8-841d-0b971935ebd4.png)88

From this countplot, we get an idea of the counts of the people who had attempted any of the problems. There are very less people 
who had made more number of attempts, which is a little non-obvious, because i expected that more number of people would had made more number of attempts, since all are not experts.
![attempts_countplot](https://user-images.githubusercontent.com/20907692/45989741-6d722c00-c06c-11e8-9c04-fae2a78c82dc.png)

Prediction Part
===

First approach:
=====
A problem solved by most of the coders has been taken, and an algorithm for the prediction of attempts which a new coder will make is applied. This will check the algorithm prediction. 

After applying the above approach we are getting an accuracy of 52.14%. But after applying bootstrapping, we can increase the accuracy by 10% i.e, it goes upto 62%.

But there is problem with this approach, it can only give good prediction for the problem solved by many coders, but it works drastically bad when it comes to predict for the problem which is solved by 10-20 Coders.

Second approach
===
Taking the negative point from the previous approach, i thought of a solution called Clustering.

Clusters of similar type of problems will be made, and when we get an input from the user, i will check which cluster the input problem_id belongs to, and after that take all the questions of that particular cluster and try to predict the attempts from that particular cluster of problems.

3 different K values for the K-Means algorithm is been taken according to the elbow method for checking the accuracy of the clustering.

Future Work
===
* Apply the GMM algorithm for Clustering and check its prediction accordingly.
* make the whole program according to the inputs which is expected to get from the user.
* Develop the final Recommendation Engine for the Coders.

