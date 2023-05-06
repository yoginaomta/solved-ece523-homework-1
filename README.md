Download Link: https://assignmentchef.com/product/solved-ece523-homework-1
<br>
Probability and Discriminant Classifiers

PART I: Maximum Posterior vs Probability of Chance Show/explain that when we are using the Bayes decision rule, where <em>c </em>is the number of classes. Derive an expression for <em>p</em>(err). Let <em>ω</em><sub>max </sub>be the state of nature for which <em>P</em>(<em>ω</em><sub>max</sub>|<strong>x</strong>) ≥ <em>P</em>(<em>ω<sub>i</sub></em>|<strong>x</strong>) for <em>i </em>=<em>,</em>1<em>…,c</em>. Show that <em>p</em>(err) ≤ (<em>c </em>− 1)<em>/c </em>when we use the Bayes rule to make a decision. Hint, use the results from the previous questions.

PART II: Bayes Decision Rule Classifier Let the elements of a vector <strong>x </strong>= [<em>x</em><sub>1</sub><em>,…,x<sub>d</sub></em>]<sup>T </sup>be binary valued. Let <em>P</em>(<em>ω<sub>j</sub></em>) be the prior probability of the class <em>ω<sub>j </sub></em>(<em>j </em>∈ [<em>c</em>]), and let

<em>p<sub>ij </sub></em>= <em>P</em>(<em>x<sub>i </sub></em>= 1|<em>ω<sub>j</sub></em>)

with all elements in <strong>x </strong>being independent. If, and and <em>p<sub>i</sub></em><sub>2 </sub>= 1 − <em>p</em>,

show that the minimum error decision rule is

Choose

Hint: Think back to ECE503 and types of random variables then start out with

Choose <em>ω</em><sub>1 </sub>if <em>P</em>(<em>ω</em><sub>1</sub>)<em>P</em>(<strong>x</strong>|<em>ω</em><sub>1</sub>) <em>&gt; P</em>(<em>ω</em><sub>2</sub>)<em>P</em>(<strong>x</strong>|<em>ω</em><sub>2</sub>)

PART III: The Ditzler Household Growing Up My parents have two kids now grown into adults. Obviously there is me, Greg. I was born on a Wednesday. What is the probability that I have a brother? You can assume that.

PART IV: Bayes classifier Let consider a Bayes classifier with <em>p</em>(<strong>x</strong>|<em>ω<sub>i</sub></em>) distributed as a multivariate Gaussian with mean <em>µ<sub>i </sub></em>and covariance Σ<em><sub>i </sub></em>= <em>σ</em><sup>2</sup><em>I </em>(note they all share the same covariance). We choose the class that has the largest

<em>g<sub>i</sub></em>(<strong>x</strong>) = log(<em>p</em>(<strong>x</strong>|<em>ω<sub>i</sub></em>)<em>P</em>(<em>ω<sub>i</sub></em>)) ∝ <strong>w</strong><em><sub>i</sub></em><sup>T</sup><strong>x </strong>+ <em>w</em><sub>0<em>i</em></sub>

Find <strong>w</strong><em><sub>i </sub></em>and <em>w</em><sub>0<em>i</em></sub>. Fact:

<ul>

 <li>Linear and Quadratic Classifiers – Code [20pts]

  <ul>

   <li>Write a general function to generate random samples from N(<em>µ,</em>Σ) in <em>d</em>-dimensions (i.e., <em>µ </em>∈ R<em><sup>d </sup></em>and Σ ∈ R<em><sup>d</sup></em><sup>×<em>d</em></sup>).</li>

   <li>Write a procedure of the discriminant of the following form</li>

  </ul></li>

</ul>

(1)

<ul>

 <li>Generate a 2D dataset with three classes and use the quadratic classifier above to learn the parameters and make predictions. As an example, you should generate training data shown below to estimate the the parameters of the classifier in (1) and you should test the classifier on another randomly generated dataset. It is also sufficient to show the dataset used to train your classifier and the decision boundary it produces.</li>

 <li>Write a procedure for computing the Mahalanobis distance between a point <strong>x </strong>and some mean vector <em>µ</em>, given a covariance matrix Σ.</li>

 <li>Implement the naïve Bayes classifier from scratch and then compare your results to that of Python’s built-in implementation. Use different means, covariance matrices, prior probabilities (indicated by relative data size for each class) to demonstrate that your implementations are correct.</li>

</ul>

<ul>

 <li>Misc Code  – Choose One</li>

</ul>

Problem I: Comparing Classifiers A text file, hw1-scores.txt, containing classifier errors measurements has been uploaded to D2L. Each of the columns represents a classifier and each row a data set that was evaluated. Are all of the classifiers performing equally? Is there one or more classifiers that is performing better than the others? Your response should be backed by statistics. Suggested reading:

<ul>

 <li>Janez Demšar, “Statistical Comparisons of Classifiers over Multiple Data Sets,” Journal of Machine Learning Research, vol. 7, 1–20.</li>

</ul>

Read the abstract to get an idea about the theme of comparisons. Sections 3.1.3 and 3.2.2 can be used to answer the question posed here.

Problem II: Sampling from a Distribution Let the set N ∈ [1<em>,…,n,…,N</em>] be a set of integers and <strong>p </strong>be a probability distribution <strong>p </strong>= [<em>p</em><sub>1</sub><em>,…,p<sub>n</sub>,…,p<sub>N</sub></em>] such that <em>p<sub>k </sub></em>is the probability of observing <em>k </em>∈ N. Note that since <strong>p </strong>is a distribution then 1<sup>T</sup><strong>p </strong>= 1 and 0 ≤ <em>p<sub>k </sub></em>≤ 1 ∀<em>n</em>. Write a function sample(<em>M,</em><strong>p</strong>) that returns <em>M </em>indices sampled from the distribution <strong>p</strong>. Provide evidence that your function is working as desired. Note that all sampling is assumed to be i.i.d. You must include a couple of paragraphs and documented code that discusses how you were able to accomplish this task.