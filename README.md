Download Link: https://assignmentchef.com/product/solved-bit-project2-least-squares-regression-and-nearest-neighbor-classifiers
<br>



<strong>task 2.1: least squares regression for missing value prediction </strong>Download the file whData.dat, remove the outliers (as in the previous project) and collect the remaining height and weight data in two vectors

<em>x </em>= [<em>x</em><sub>1 </sub><em>x</em><sub>2 </sub><em>… x<sub>n</sub></em>]<em><sup>T                        </sup></em>and <em>y</em><em>,</em>

respectively.

Use the method of least squares to fit polynomial models

<em>d</em>

<em>y</em>(<em>x</em>) = <sup>X</sup><em>w<sub>j</sub>x<sup>j</sup></em>

<em>j</em>=0

to the data. In particular, fit models for <em>d </em>∈ {1<em>,</em>5<em>,</em>10} and plot your results. Use each of your resulting models to predict weight values for the outliers (i.e. the data points in whData.dat where the weight value is −1).

<strong> note:</strong>

There are numerous ways of how this can be done. However, depending on how you implement your solution, you may run into numerical problems (you should recognize them when they occur). In this case, it is not acceptable to give up and simply claim that the method did not work. Rather, you should either double your efforts and try to come up with an implementation that works or provide an in-depth analysis as to why and where your code failed and point out possible solutions.

<strong>task 2.2: conditional expectation for missing value prediction </strong>Fit a bi-variate Gaussian to the height and weight data in <em>x </em>and <em>y </em>to model the joint density <em>p</em>(<em>x,y</em>) of heights and weights.

Given your fitted bi-variate Gaussian, use the idea of conditional expectation to predict the weight values for the outliers. That is, let <em>x<sub>o </sub></em>denote the available height data of an outlier and compute

Do this either analytically as discussed in the lecture or numerically and report your results.

<strong>task 2.3: Bayesian regression for missing value prediction </strong>Use the method of Bayesian regression to fit a fifth degree polynomial

to the height and weight data in <em>x </em>and <em>y</em>. Assume a Gaussian prior

for the parameter vector <em>w </em>where <em>µ</em><sub>0 </sub>= <strong>0 </strong>and. Plot you resulting model and compare it to the corresponding model (<em>d </em>= 5) from task 2.1 <strong>task 2.4: Boolean functions and the Boolean Fourier transform </strong>In the <a href="https://www.researchgate.net/project/lectures-on-pattern-recognition">supplementary material for lecture 07</a><a href="https://www.researchgate.net/project/lectures-on-pattern-recognition">,</a> we already briefly discussed elemental cellular automata.

A one-dimensional (or elemental) <em>cellular automaton </em>consists of

<ul>

 <li>an infinite sequence of cells {<em>x<sub>i</sub></em>}<em><sub>i</sub></em><sub>∈</sub>N in two possible states; typically these states are assumed to be 0 or 1, here, however, we consider</li>

 <li>a update rule for how to update a cell based on its and its two neighbors’ current states</li>

</ul>

At time <em>t </em>= 0, the <em>x<sub>i </sub></em>are (randomly) initialized, and, at any (discrete) time step <em>t</em>, all cells are updated simultaneously. Here is an illustrative example where we use +1 =  and −1 =

<em>t </em><em>…… </em><em>t </em>+ 1 <em>……</em>

This update process continues forever and it is common practice to plot subsequent (finite sized) state sequences below each other to visualize the evolution of an automaton under a certain rule. Here are some examples of possible evolutions starting from the same initial configuration

rule 32                                                    rule 108

rule 126                                                   rule 110

From now on, we remove notational clutter. That is, instead of

we simply write <em>y </em>= <em>f</em>(<em>x</em>) where <em>x </em>∈ {+1<em>,</em>−1}<sup>3 </sup>and <em>y </em>∈ {+1<em>,</em>−1}.

The naming convention for the rules of elemental cellular automata is due to Wolfram (1984) and illustrated in the following tables.

<table width="518">

 <tbody>

  <tr>

   <td width="259">


    <table width="245">

     <tbody>

      <tr>

       <td width="44"> </td>

       <td colspan="2" width="81"><em>X</em></td>

       <td width="45"><em>y</em></td>

       <td width="74">(<em>y </em>+ <strong>1</strong>)<em>/</em>2</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">+1</td>

       <td width="45">+1</td>

       <td width="45">−1</td>

       <td width="74">0</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">+1</td>

       <td width="45">−1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">−1</td>

       <td width="45">+1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">−1</td>

       <td width="45">−1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">+1</td>

       <td width="45">+1</td>

       <td width="45">−1</td>

       <td width="74">0</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">+1</td>

       <td width="45">−1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">−1</td>

       <td width="45">+1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">−1</td>

       <td width="45">−1</td>

       <td width="45">−1</td>

       <td width="74">0</td>

      </tr>

     </tbody>

    </table></td>

   <td width="259">


    <table width="245">

     <tbody>

      <tr>

       <td width="44"> </td>

       <td colspan="2" width="81"><em>X</em></td>

       <td width="45"><em>y</em></td>

       <td width="74">(<em>y </em>+ <strong>1</strong>)<em>/</em>2</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">+1</td>

       <td width="45">+1</td>

       <td width="45">−1</td>

       <td width="74">0</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">+1</td>

       <td width="45">−1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">−1</td>

       <td width="45">+1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">+1</td>

       <td width="36">−1</td>

       <td width="45">−1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">+1</td>

       <td width="45">+1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">+1</td>

       <td width="45">−1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">−1</td>

       <td width="45">+1</td>

       <td width="45">+1</td>

       <td width="74">1</td>

      </tr>

      <tr>

       <td width="44">−1</td>

       <td width="36">−1</td>

       <td width="45">−1</td>

       <td width="45">−1</td>

       <td width="74">0</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

rule 110                                                                            rule 126

For <em>x </em>∈ {+1<em>,</em>−1}<sup>3</sup>, there are 2<sup>3 </sup>= 8 possible input patterns for each rule. For each input pattern, there are 2 possible outputs or target values. Hence, the total number of possible rules is 2<sup>2</sup><sup>3 </sup>= 256.

Using the language of pattern recognition, we may collect the possible input patterns in an 8 × 3 design matrix <em>X </em>and the target values of each rule in an 8 dimensional target vector <em>y</em>. Converting a rule’s target vector from bipolar to binary yields a byte representation of a number between 0 and 255 and provides the rule’s name.

<strong>Here is your first sub-task:              </strong>For rules 110 and 126, determine

<em>w</em><sup>∗ </sup>= argmin <sub> </sub><em>Xw </em><em>w</em>

and then compute <em>y</em>ˆ = <em>Xw</em><sup>∗</sup>

Now, compare <em>y </em>and <em>y</em>ˆ. What do you observe?

<strong> note:</strong>

Don’t be alarmed! What we did here hardly makes sense and was mainly intended to prepare ourselves for what comes next.

Each possible rule <em>y </em>= <em>f</em>(<em>x</em>) governing the behavior of a cellular automaton is an instance of a <em>Boolean function</em>

<em>f </em>: {−1<em>,</em>+1}<em><sup>m </sup></em>→ {−1<em>,</em>+1}                                                                          (1)

where in our case <em>m </em>= 3. In what follows, we let I denote the index set of the elements <em>x<sub>i </sub></em>of <em>x</em>, that is

<em>.</em>

The power set 2<sup>I </sup>of I is the set of all subsets of I. In other words,

and we note that |2<sup>I</sup>| = 2<em><sup>m</sup></em>.

Every Boolean function <em>f </em>of the form in (1) can be uniquely expressed as a multilinear polynomial

<em>f</em>(<em>x</em>) = <sup>X </sup><em>w</em><sub>S </sub><sup>Y</sup><em>x<sub>i                                                                                                                                                                            </sub></em>(2)

S∈2<sup>I                </sup><em>i</em>∈S

which is known as the <em>Boolean Fourier series expansion </em>of <em>f</em>. In contrast to the complex exponentials which form the basis functions for conventional Fourier analysis, here the basis functions are the parity functions

<em>ϕ</em><sub>S</sub>(<em>x</em>) = <sup>Y</sup><em>x<sub>i</sub></em>

<em>i</em>∈S

where by definition

<em>ϕ</em><sub>∅</sub>(<em>x</em>) = <sup>Y</sup><em>x<sub>i </sub></em>= 1<em>.</em>

<em>i</em>∈∅

Given these definitions, we can rewrite (2) as follows

<em>f</em>(<em>x</em>) = <sup>X </sup><em>w</em><sub>S </sub><em>ϕ</em><sub>S </sub>= <em>w</em><em><sup>T</sup>ϕ</em>

S∈2<sup>I</sup>

and recognize that any Boolean function is an inner product between two vectors <em>w </em>∈ R<sup>2</sup><em><sup>m </sup></em>and <em>ϕ </em>∈ {+1<em>,</em>−1}<sup>2</sup><em><sup>m</sup></em>.

<strong>Here is your second sub-task:           </strong>Implement a function <em>ϕ </em>: {+1<em>,</em>−1}<em><sup>m </sup></em>→ {+1<em>,</em>−1}<sup>2</sup><em><sup>m</sup></em>

such that <em>ϕ </em>= <em>ϕ</em>(<em>x</em>). To be specific, for <em>x </em>= [<em>x</em><sub>1</sub><em>,x</em><sub>2</sub><em>,x</em><sub>3</sub>]<em><sup>T </sup></em>∈ {+1<em>,</em>−1}<sup>3</sup>, your function should produce

     1     

 <em>x</em><sub>1 </sub>

 <em>x</em><sub>2 </sub>



 <em>x</em><sub>3 </sub> <em>ϕ </em>= <sub> </sub><em>x</em>1 <em>x</em>2  

             

 <em>x</em>1 <em>x</em>3 

             

 <em>x</em>2 <em>x</em>3  <em>x</em>1 <em>x</em>2 <em>x</em>3

However, implement it such that is works for arbitrary <em>m </em>∈ N and not just for <em>m </em>= 3. This will come in handy in the next project.

<strong>Here is your third sub-task: </strong>For rules 110 and 126, turn the design matrix <em>X </em>into a “feature” design matrix <strong>Φ</strong>, then determine <em>w</em><sup>∗ </sup>= argmin <em>w</em>

and finally compute

<em>y</em>ˆ = <strong>Φ</strong><em>w</em><sup>∗</sup>

Now, compare <em>y </em>and <em>y</em>ˆ. What do you observe?

<strong>task 2.4: nearest neighbor classifier</strong>

Implement a function that realizes an <em>n</em>-nearest neighbor classifier, i.e. a function that decides the class label of a test data point from the majority of the labels among the <em>n </em>nearest training data.

Download the files data2-train.dat and data2-test.dat of labeled 2D data and determine the recognition accuracy (percentage of correctly classified data points) of your classifier for <em>n </em>∈ {1<em>,</em>3<em>,</em>5}.

Determine the overall run time for computing the 1-nearest neighbor of every data in data2-test.dat.

<strong>task 2.5: computing a kD-tree</strong>

Implement a function that computes <em>and plots </em>up to four different kinds of <em>k</em>D-trees of the data in data2-train.dat where <em>k </em>= 2.

Determine overall run time for computing the 1-nearest neighbor of every data in data2-test.dat by means of your <em>k</em>D-tree.

<strong> note:</strong>

Since scipy provides functions for <em>k</em>D-tree computation, you may use those for your run time evaluations. However, just using these functions is of course too easy. Therefore, implement your own function for building and plotting a tree (you may ignore the problem of searching the tree). Your function for building the tree should allow for choosing how to determine the dimension for splitting and for choosing how to determine the split point. In particular, you should enable the following two methods for selecting the splitting dimension:

<ol>

 <li>alternate between the <em>x </em>and the <em>y </em>dimension</li>

 <li>split the data along the dimension of higher variance</li>

</ol>

With respect to computing the split point, you should enable the following to ideas:

<ol>

 <li>split at the midpoint of the data</li>

 <li>split at the median of the data</li>

</ol>

Given the data in data2-train.dat create all four possible <em>k</em>D-trees and plot them. what do you observe?