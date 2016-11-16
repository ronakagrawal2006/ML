Getting Started with Audio Processing:
Objective:
Need to find dataset for splitting audio; audio in the sense that need a dataset with multiple voices
The output would be a Split in those voices.

Q1: How would we represent that audio file?
Q2: How would you extract features?
Q3:

Useful Links:
git clone https://github.com/riddhishb/ipython-notebooks


Approach:
Try to get the rationale behind Split of voice over multiple microphones.
Identify how is it using the other input for split of voices.
Then try and come up with an approach that allows split over a single input.

Understanding how the multiple input split works below:

m microphones.
Assuming that each microphone has a single speaker, bascially m speakers for m microphones, and each microphone has a
dominant voice(all are distinct)


The signal received by the microphone labelled i over the entire time of recording will be denoted by  Xi .
A particular sample of this recorded signal, recorded at the time index j will then be denoted by  Xij .

Xij  corresponds to the sound sample recorded by the ith mike at the time (indexed by) j.

If we stack up these row vectors, we will get an m x N matrix whose ith row corresponds to the samples recorded by a \
particular microphone. A 'vertical slice' of this matrix, i.e a column corresponds to all the samples recorded at a given instant of time, indexed by the indices of the corresponding microphone.



This means that each  Xi  is some linear combination of the vectors  S1  through  Sm.
Putting it all together, we conclude that  X=AS; for some m x m matrix A, called the mixing matrix.
Our objective is to then find an "un-mixing" matrix W that satisfies  S=WX.
If we know this W, as we already have X, we can calculate S by a direct multiplication.

Our objective is to find the matrix W. As we have assumed that the number of microphones is equal to the number of independent conversations, it turns out that the matrix A is invertible and hence W is just the inverse of A.
Hence, it suffices to find A. We will employ Singular Value Decomposition(SVD) on the matrix A.


A=UDV∗  for orthogonal matrices U, V* and diagonal matrix D. by SVD( factorizing A to get orthogonal vectors--did not get completely but we are splitting the values to generate A.



Current Status:
The above approach uses multiple microphones, and needs a source as well to make a split. Hence, is not usable.
We have found a different link where we can split 


Question:
Do we really need source for implementing source?
No. We dont. The source was supplied just for transformation, and nothing else.

http://stackoverflow.com/questions/20414667/cocktail-party-algorithm-svd-implementation-in-one-line-of-code








