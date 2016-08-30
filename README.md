# ML
h(ø) is the prediction from our hypothesis
y is the actual value

h(ø) depends on ø1, ø2,....øn all the parameters that the hypothesis should depend on.
x is the input feature of the training set.



we want to our prediction and actual value in training set to be same. i.e. the difference between the prediction and actual correct value to be minimum(ideally 0)
so we want h(ø) ~ y i.e. h(ø) - y ~ 0
i.e. min of [h(ø)-y]----------------equation 1
square equation 1 on to simplify maths.
min [h(ø) -y]^2

Basically the equation means:
h(ø) for x(i)--------->the equation represents prediction of y for the ith input in training set for some constant value of ø's.
Note that ø's are the constants that we will populate for the entire training set.
To explain:
we need optimal value of ø for the entire training set, i.e. we will optimize ø for each value input in training set so that prediction matches actual output.

initialize ø;
foreach x in training set,
	update ø such that the value is optimal for all the inputs encountered so far.

Now at this state, we will have the optimal value of ø such that the entire set will be mapped to the closest prediction	 

Assignment1:
Predict the house costm (say); i dont remember the prob. just focus on how!!
Objective: Get the values of ø0 and ø1.
Input: Training set with X, and Y
Approach: Get predictions for each training set and update value of ø0 and ø1.
How to get predicitons? and what is prediciton?
Remember prediction is the h(ø) for x for a single training set.
So, we need to compute ø0 + ø1 x(i)) for each value in training set
we transform X to 1,X to compute the above equation(Remember how matrix multiplication works) and try to get [1,x](1x2 matrix) [ø0,ø1](2x1 matrix)

Compute Cost:




Feature Scaling:
WHY?
The feature takes different range of values; area in square metres(2000-16000) to number of bedrooms(1-5).
So, the gradient descent would take looong time to get the optimal values(why it would take long time? thats out of scope for now, tip: the contour would be vertically elongated and not in circles, so by gradient descent, would go to-fro,and would take long time to find local minima!)

WHAT?
So, we scale each feature to be under the range of -1 ---- 1.
now, the contours would look like circles. and gradient descent can be achieved faster!


Logistic Regression(Classifcation Problem):
We need a hypothesis which has values from 0----1.
so we have a sigmoid funciton that will restrict it to 0-1
Sigmoid Function: g(z)= 1/(1+(e^(-z)) ---- Dont get scared: this will just map any value of z supplied in the range of 0-1

We have a new Cost function: for the reason that we will not have a convex plot, so not sure if we can get to global minimal.
So the new one will get us one.
New Cost function: 
Cost(hø(x),y) = {-log (hø(x)) for y=1} and { -log( 1 - hø(x) ) for y=0 }


DECISION BOUNDARY:
This is nothing but the condition where equation that you get for a certain set of ø..
basically, something crossing it(for linear), would be predicting true, and inside would be predicting false(or vice-versa for that matter!)


Now minimize Cost function: (1/m) * for i=1-->m (Cost(hø(x),y))

Minimzed Cost function Simplified: [ - '(y)' log(hø(x)) - { '(1-y)' log (1-hø(x)) } ]

How to minimize: Same as before:

Advanced optimization..
Why?
Dont know
What?
We need a costFunction that would return (Cost,Gradient) at each iteration.


Overfitting:
Increasing number of features will result in incorrect prediction.

	Fix for Overfit:
	Reduce number of features
		Manually select which features to keep
		Model Selection Algorithm
	Regularization:
		Reduce the maginitude of øj (Works well when we have lots of features , all contrbuting a bit to y)



What am I looking for?
--> Something to map multiple features to one answer, such that when i ask for any one of the features, it should be able to identify the one in subset and get the answer..

I am hoping getting into detail of one of the algo's will help me drill that down..

Naive Bayes Algorithm:
It has multiple variations
Multinominal: when the multiple occurrences of the words matter a lot in the classification problem--Where does this belong..Topic classification
Binarized Multinomial Naive Bayes is used when the frequencies of the words don’t play a key role in our classification.--Movie Review

Naive Bayes isn;t what we really need. It has the basic assumption that we are mapping it to class!
