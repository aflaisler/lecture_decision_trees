# Decision trees

Predict if John will play tennis
influence factors (=> training set)
Hard to guess
How do you do? How you predict?
=> try to understand


# How Can We Make Decisions ?
start counting
pure subset
need to go further to get pure subsets
replace example with Decisions
!! keep the count at each split

# Terminology
Nodes: Test for the value of a certain attribute
Branches: Correspond to the outcome of a test and Connect a node to the next node or leaf
Root: The node that performs the first split
Leaves: Terminal nodes that predict the outcome


# Regression Trees

Arrows

Split where the value min the mse of  its predictions


### Decision Tree Tradeoffs (Why Decision Trees)

Decision trees => very flexible and accurate while also being easily interpreted.
* Easily interpretable (With these algorithms it can be hard to interpret their results and understand ___why___ a certain instance was assigned a label. )
* Handles missing values and outliers
* Computationally _cheap_ to ___predict___
* Can handle irrelevant features
* Mixed data (nominal and continuous)

#### Why Not Decision Trees

* Computationally _expensive_ to ___train___
* Greedy algorithm (local optima) (salesman)
* Very easy to overfit

## Building decision-trees
How to predict with a decision tree it pretty clear: you just answer the questions and follow the path to the appropriate *leaf* node.
But how do we build a decision tree? How do we determine which feature we should split on? This is the crux of the decision tree algorithm.

# entropy
First, we need to discuss *entropy*. The entropy of a set is a measure of the amount of disorder. Intuitively
Low entropy?
High entropy? mix of labels => high entropy.


### Information Gain (explain why info gain versus average)
    - One that maximize the information about the prediction
In order to pick which feature to split on, we need a way of measuring how good the split is. This is what *information gain* is for. The *gini impurity* is another alternative, pretty similar.

We want to determine which attribute in a given set of training feature vectors is most useful for discriminating between the classes to be learned.

We will use it to decide the ordering of attributes in the nodes of a decision tree.
If our splits do a good job splitting on the boundary between classes, the splits have more predictive power

- One that maximize the information about the prediction

- Information gain tells us how important a given attribute of the feature vectors is.

## Information Gain = entropy(parent) – [average entropy(children)]
