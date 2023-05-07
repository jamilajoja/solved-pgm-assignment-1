Download Link: https://assignmentchef.com/product/solved-pgm-assignment-1
<br>
<h1>1         Probabilities</h1>

In this excercise, you will prove some basic, but very important rules in probability theory.

<ol>

 <li>For any two events <em>E</em><sub>1 </sub>and <em>E</em><sub>2</sub>, prove</li>

</ol>

<em>p</em>(<em>E</em><sub>1 </sub>∪ <em>E</em><sub>2</sub>) = <em>p</em>(<em>E</em><sub>1</sub>) + <em>p</em>(<em>E</em><sub>2</sub>) − <em>p</em>(<em>E</em><sub>1 </sub>∩ <em>E</em><sub>2</sub>)                            (1)

what if <em>E</em><sub>1 </sub>and <em>E</em><sub>2 </sub>are two disjoint events?

<ol start="2">

 <li>(Bayes’ law) Given the Kolmogorov definition for conditional probabilities</li>

</ol>

(2)

derive Bayes’ law:

(3)

<ol start="3">

 <li>(Law of total probability) Let <em>E</em><sub>1</sub>, …, <em>E<sub>n </sub></em>be mutually disjoint events in the probability space Ω such that Ω =. Then for any event <em>B </em>in the same space Ω show that</li>

</ol>

)                       (4)

<ol start="4">

 <li>(Linearity of expectation) For any finite collection of discrete random variables <em>X</em><sub>1</sub><em>,…,X<sub>n </sub></em>with finite expectations, show that</li>

</ol>

<em>n                      n</em>

E[<sup>X</sup><em>X<sub>i</sub></em>] = <sup>X</sup>E[<em>X<sub>i</sub></em>]                                                (5)

<em>i</em>=1                   <em>i</em>=1

<ol start="5">

 <li>Let <em>X</em>, <em>Y </em>, <em>Z </em>be three disjoint subsets of random variables. We say <em>X </em>and <em>Y </em>are conditionally independent given <em>Z </em>if and only if</li>

</ol>

<em>p<sub>X,Y </sub></em>|<em><sub>Z</sub></em>(<em>x,y </em>| <em>z</em>) = <em>p<sub>X</sub></em>|<em><sub>Z</sub></em>(<em>x </em>| <em>z</em>)<em>p<sub>Y </sub></em>|<em><sub>Z</sub></em>(<em>y </em>| <em>z</em>)                                (6)

Show that <em>X </em>and <em>Y </em>are conditionally independent given <em>Z </em>if and only if the joint distribution for the three subsets of random variables factors in the following form:

<em>p<sub>X,Y,Z</sub></em>(<em>x,y,z</em>) = <em>h</em>(<em>x,z</em>)<em>g</em>(<em>y,z</em>)                                        (7)

(Be careful to prove both directions!)

<h1>2         Complexity analysis</h1>

Consider the three random variables <em>X,Y,Z </em>all of which are binary.

<ul>

 <li>How many states do you need in general to fully specify the joint distribution <em>p</em>(<em>x,y,z</em>)?</li>

 <li>How many states are needed if the distribution does factorize in <em>p</em>(<em>x,y,z</em>) = <em>p</em>(<em>x </em>| <em>y</em>)<em>p</em>(<em>y </em>| <em>z</em>)<em>p</em>(<em>z</em>)?</li>

 <li>How many states do you need, if the variables are not binary but can take values in {1<em>,</em>2<em>,…,N</em>}; consider both previous cases.</li>

 <li>How many states do you need to specify a distribution over all 8bit grayscale images of size 1000 × 1000 pixels? There are random variables <em>x</em><sub>1</sub><em>,x</em><sub>2</sub><em>,…,x</em><sub>1<em>M </em></sub>with <em>x<sub>i </sub></em>∈ {0<em>,…,</em>255} for <em>i </em>= 1<em>,…M</em>.</li>

 <li>Do you have an idea of how to represent the distribution more compactly?</li>

</ul>

Provide the number of states needed by your method.

<h1>3         Chest Clinic Network</h1>

The chest clinic network above concerns the diagnosis of lung disease (tuberculosis,lung cancer, or both, or neiter). In this model a visit to asia is assumed to increase the probability of lung cancer. We have the following binary variables.

<em>x</em>positive X-ray <em>d</em>Dyspnea (shortness of breath) <em>e</em>Either Tuberculosis or Lung Cancer <em>t</em>Tuberculosis <em>l</em>Lung cancer <em>b</em>Bronchitis <em>a</em>Visited Asia <em>s</em>Smoker

<ol>

 <li>Write down the factorization of the distribution implied by the graph.</li>

 <li>Are the following independence statements implied by the graph? (And how do you conclude this?)

  <ul>

   <li>tuberculosis⊥⊥smoking|shortness of breath</li>

   <li>tuberculosis⊥⊥smoking|bronchitis</li>

   <li>lung cancer⊥⊥bronchitis|smoking</li>

   <li>visit to Asia⊥⊥smoking|lung cancer</li>

   <li>visit to Asia⊥⊥smoking|lung cancer,shortness of breath</li>

  </ul></li>

 <li>Calculate by hand the values for <em>p</em>(<em>d</em>). The Conditional Probability Table (CPT) is:</li>

</ol>

<table width="403">

 <tbody>

  <tr>

   <td width="142"><em>p</em>(<em>a </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.01,</td>

   <td width="142"><em>p</em>(<em>s </em>= 1)</td>

   <td width="26">=</td>

   <td width="24">0.5</td>

  </tr>

  <tr>

   <td width="142"><em>p</em>(<em>t </em>= 1 | <em>a </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.05,</td>

   <td width="142"><em>p</em>(<em>t </em>= 1 | <em>a </em>= 0)</td>

   <td width="26">=</td>

   <td width="24">0.01</td>

  </tr>

  <tr>

   <td width="142"><em>p</em>(<em>l </em>= 1 | <em>s </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.1,</td>

   <td width="142"><em>p</em>(<em>l </em>= 1 | <em>s </em>= 0)</td>

   <td width="26">=</td>

   <td width="24">0.01</td>

  </tr>

  <tr>

   <td width="142"><em>p</em>(<em>b </em>= 1 | <em>s </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.6,</td>

   <td width="142"><em>p</em>(<em>b </em>= 1 | <em>s </em>= 0)</td>

   <td width="26">=</td>

   <td width="24">0.3</td>

  </tr>

  <tr>

   <td width="142"><em>p</em>(<em>x </em>= 1 | <em>e </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.98,</td>

   <td width="142"><em>p</em>(<em>x </em>= 1 | <em>e </em>= 0)</td>

   <td width="26">=</td>

   <td width="24">0.05</td>

  </tr>

  <tr>

   <td width="142"><em>p</em>(<em>d </em>= 1 | <em>e </em>= 1<em>,b </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.9,</td>

   <td width="142"><em>p</em>(<em>d </em>= 1 | <em>e </em>= 1<em>,b </em>= 0)</td>

   <td width="26">=</td>

   <td width="24">0.7</td>

  </tr>

  <tr>

   <td width="142"><em>p</em>(<em>d </em>= 1 | <em>e </em>= 0<em>,b </em>= 1)</td>

   <td width="26">=</td>

   <td width="43">0.8,</td>

   <td width="142"><em>p</em>(<em>d </em>= 1 | <em>e </em>= 0<em>,b </em>= 0)</td>

   <td width="26">=</td>

   <td width="24">0.1</td>

  </tr>

 </tbody>

</table>

and

= 0<em>,</em>

<em>.</em>