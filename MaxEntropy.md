DISCLAIMER:
The entire thing may appear disconnected as of now. This is just notes jotted down!
ToDo: Add a reason with 'WHY ARE WE DOING WHAT WE ARE DOING' for each of these steps!

[Required]
Probability Distribution: Mathematical Description of 'Random' phenomenon in terms of probabiltiy.


Principle of Max Entropy:
The Probability Distribtion which best represents the current knowledge is the one with max Entropy

Max Entropy
to be used when:Independent Features

How:
Identify context, 



Empirical Probability:
Ration of number of outcomes in which a specific event occurs to the total number of trials in EXPERIMENTAL SPACE; 
Say Event A occurs in 5 times when i toss a dice with 6 faces 10 times.
The empirical probablility is 5/10
(NOTE THE EXPERIMENTAL SPACE and NOT THEORITICAL SPACE)


Empirical P(x,y)= Number of times (x,y) has occured in total Training data / (Total number of samples in Training data)


Indicator Function: 

Will return true if class of document is Ci , given that the it contains word Wk; else false.

This will basically indicate whether class is something specific given that the document contained a certain word!

This above indicator funciton is called Feature


Expected Value:
is the long run average value of repititions of the experiment it represents!

For example, the expected value in rolling a six-sided die is 3.5 because, roughly speaking, the average of all the numbers that come up in an extremely large number of rolls is very nearly always quite close to three and a half. 


How to calculate?
Each value that the variable can assume multiplied by its probability of occuring, and the output is summed to get the expected value



Representation:
We express each feature as the expected value of the feature i.e. the value of the feature and the probability of the given value being assigned to that feature.

Say, Expected value of feature(~p(x,y)) = For all values of that p(x,y can take) :(value of p(x,y) * probability of that value occuring)
probability = ~p(x,y)// if each training sample (x,y) occurs only once, ~p(x,y) would be 1/N where N is the total number of training samples
value = f(x,y)[This will be 1/0  depending on whether the class of document given the word is present]

Model: 
Model is the Summation equation we got..
Expected value of feature(~p(x,y)) = For all values of that p(x,y can take) :(value of p(x,y) * probability of that value occuring)

When we have a statistic that matters, we want our model to accord to it...its only obvious!
how to do that?
we constrain the expected value that the model assigns to the expected value of feature.
i.e. Expected value (Feature) = Expected value of Model that is constrained
		~p(x) is the empirical distribution in of x in dataset, all data set.
 Constrained model = (~p(x) p(y|x)))	/* the first part is the probability */ * Value of f(x,y)/*the second is the value */

 DOUBT: How is the probability ~p(x) p (y|x)?
 Solution: Its is not ~p(x)* p(y|x)....it is p(y|x) ~p(x) i.e.
 probabililty that class of document is y given that a word 'x' is in it * experimental probability that 'x' is present in data set

 This gives us the Expected value for y to be the class of a document when a word x is present in it


Probability vs Information:
Probablity: count NUMBER OF OCCURENCES in N TRIALS
Information: count AVERAGE OCCURENCES of PATTERNS in N for large N



