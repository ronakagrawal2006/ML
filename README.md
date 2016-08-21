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

now at this state, we will have the optimal value of ø such that the entire set will be mapped to the closest prediction	 



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




 Logistic Regression:
 
