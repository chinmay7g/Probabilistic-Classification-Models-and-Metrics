# Probabilistic-Classification-Models-and-Metrics
  PRECISION ,RECALL, F_1

Classification problems have metrics of the type whether the classification made was true or false.
Hence they use a confusion matrix of TN,FN,FP,TP. The performance of a classifier is measured by means of 

Accuracy = (No. of correct observations) / (No. of total observations)

Precision = TP / (TP + FP)

Recall = TP / ( TP + FN)

F_1 score = Gives a tradeoff between precision and recall.

Consider a classification example between a cat and a dog. In reality it is a cat. Our model will try to make classifications
whether it's a cat or dog. Plotting the three metrics for such cases we realise from the given image: 

![Prec,Recall,F1](https://user-images.githubusercontent.com/55191934/75093495-3af19900-55a8-11ea-9aa1-4804a8b693da.PNG)

Since, classifiers gives us a probable value, i.e, it gives us a 70% probability of it being a cat. Rather than saying 70 out of 100 
images passed are cats. Hence the concept of probabilistic models.

We understand from this graph that, for a given particular threshold, which states 50% of data are cats, we make a statement which
can besubjected to precision of the model. As we increase the threshold value, we make more certain and confident statements
that it indeed is a cat, which is the true case. As the threshold value lowers, the model becomes too liberal in classifying.

In more simpler words, for an actual observation of cat, greater the threshold value, the more 'picky' the model becomes and more 
precise in it's classification. Lesser the threshold value, the more 'liberal' model becomes and gives away the classification of cat
to many.
F_1 score gives a balanced tradeoff between precision and recall.

Since this metric is largely dependent on the threshold parameter, a metric which is independent of it must be sought, and hence, 
the area under the curve is chosen as a metric for better performance.

Consider the following diagram:

![AUC](https://user-images.githubusercontent.com/55191934/75093703-1f878d80-55aa-11ea-8932-cb414097b848.png)

Here the area under red curve depicts a greater area under curve, which translates that for a small change in recall, the precision
isn't much affected, whereas in the green one, for a change in threshold, the precision drops too far below. Hence a smarter choice
would be the model with the red metric.

![Prec v Recall](https://user-images.githubusercontent.com/55191934/75093729-6c6b6400-55aa-11ea-8968-d7e309c973e5.PNG)

A metric used for optimising the classifiers is called Log-loss function, or oftenly called as a cross-entropy.
It is used to comment on a models performance rather than it's accuracy.
Model is rewarded if the probability of correct prediction is higher, and conversely will penalize for it being too overconfident
for a wrong prediction.

Lower the log loss, better the model performs.
Greater the log loss, the model doesn't perform well. 

Below is a graph depicting log loss function:

![Logloss](https://user-images.githubusercontent.com/55191934/75093990-d84ecc00-55ac-11ea-997b-1f82f64fa699.PNG)

