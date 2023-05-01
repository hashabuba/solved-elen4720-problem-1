Download Link: https://assignmentchef.com/product/solved-elen4720-problem-1
<br>
<h1>Problem 1</h1>

Imagine you have a sequence of <em>N </em>observations (<em>x</em><sub>1</sub><em>,…,x<sub>N</sub></em>), where each <em>x<sub>i </sub></em>∈ {0<em>,</em>1<em>,</em>2<em>,…,</em>∞}. You model this sequence as i.i.d. from a Poisson distribution with unknown parameter <em>λ </em>∈ R+, where

<ul>

 <li>What is the joint likelihood of the data (<em>x</em><sub>1</sub><em>,…,x<sub>N</sub></em>)?</li>

 <li>Derive the maximum likelihood estimate <em>λ</em><sub>ML </sub>for <em>λ</em>.</li>

</ul>

To help learn <em>λ</em>, you use a prior distribution. You select the distribution <em>p</em>(<em>λ</em>) = gamma(<em>a,b</em>).

<ul>

 <li>Derive the maximum a posteriori (MAP) estimate <em>λ</em><sub>MAP </sub>for <em>λ</em>?</li>

 <li>Use Bayes rule to derive the posterior distribution of <em>λ </em>and identify the name of this distribution.</li>

 <li>What is the mean and variance of <em>λ </em>under this posterior? Discuss how it relates to <em>λ</em><sub>ML </sub>and <em>λ</em><sub>MAP</sub>.</li>

</ul>

<h1>Problem 2</h1>

You have data (<em>x<sub>i</sub>,y<sub>i</sub></em>) for <em>i </em>= 1<em>,…,n</em>, where <em>x </em>∈ R<em><sup>d </sup></em>and <em>y </em>∈ R. You model this as <em>y<sub>i </sub><sup>iid</sup></em>∼ <em>N</em>(<em>x<sup>T</sup><sub>i </sub>w,σ</em><sup>2</sup>). You use the data you have to approximate <em>w </em>with <em>w</em><sub>RR </sub>= (<em>λI </em>+ <em>X<sup>T</sup>X</em>)<sup>−<a href="#_ftn1" name="_ftnref1">[1]</a></sup><em>X<sup>T</sup>y</em>, where <em>X </em>and <em>y </em>are defined as in the lectures. Derive the results for E[<em>w</em><sub>RR</sub>] and V[<em>w</em><sub>RR</sub>] given in the slides.

<h1>Problem 3</h1>

In this problem you will analyze data using the linear regression techniques we have discussed. The goal of the problem is to predict the miles per gallon a car will get using six quantities (features) about that car. The zip file containing the data can be found on Courseworks.<sup>1 </sup>The data is broken into training and testing sets. Each row in both “<em>X</em>” files contain six features for a single car (plus a 1 in the 7th dimension) and the same row in the corresponding “<em>y</em>” file contains the miles per gallon for that car.

Remember to submit all original source code with your homework. Put everything you are asked to show below in the PDF file.

<em><u>Part 1</u>. </em>Using the training data only, write code to solve the ridge regression problem

<em>.</em>

<ul>

 <li>For <em>λ </em>= 0<em>,</em>1<em>,</em>2<em>,</em>3<em>,…,</em>5000, solve for <em>w</em><sub>RR</sub>. (Notice that when <em>λ </em>= 0, <em>w</em><sub>RR </sub>= <em>w</em><sub>LS</sub>.) In one figure, plot the 7 values in <em>w</em><sub>RR </sub>as a function of <em>df</em>(<em>λ</em>). You will need to call a built in SVD function to do this as discussed in the slides. Be sure to label your 7 curves by their dimension in <em>x</em>.<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a></li>

 <li>Two dimensions clearly stand out over the others. Which ones are they and what information canwe get from this?</li>

 <li>For <em>λ </em>= 0<em>,…,</em>50, predict all 42 test cases. Plot the root mean squared error (RMSE)<a href="#_ftn3" name="_ftnref3"><sup>[3]</sup></a> on the test set as a function of <em>λ</em>—<em>not </em>as a function of <em>df</em>(<em>λ</em>). What does this figure tell you when choosing <em>λ </em>for this problem (and when choosing between ridge regression and least squares)?</li>

</ul>

<em><u>Part 2</u>. </em>Modify your code to learn a <em>p</em>th-order polynomial regression model for <em>p </em>= 1<em>,</em>2<em>,</em>3. (You’ve already done <em>p </em>= 1 above.) For this implementation use the method discussed in the slides. Also, be sure to standardize each additional dimension of your data.

<ul>

 <li>In one figure, plot the test RMSE as a function of <em>λ </em>= 0<em>,…,</em>100 for <em>p </em>= 1<em>,</em>2<em>,</em>3. Based on this plot, which value of <em>p </em>should you choose and why? How does your assessment of the ideal value of <em>λ </em>change for this problem?</li>

</ul>

<a href="#_ftnref1" name="_ftn1">[1]</a> See https://archive.ics.uci.edu/ml/datasets/Auto+MPG for more details on this dataset. Since I have done some preprocessing, you <em>must </em>use the data provided with this homework.

<a href="#_ftnref2" name="_ftn2">[2]</a> The dimensions correspond to: 1. cylinders, 2. displacement, 3. horsepower, 4. weight, 5. acceleration, 6. year made

<a href="#_ftnref3" name="_ftn3">[3]</a> RMSE<em>.</em>