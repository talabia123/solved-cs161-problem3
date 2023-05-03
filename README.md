Download Link: https://assignmentchef.com/product/solved-cs161-problem3
<br>
Exercises should be completed <strong>on your own.</strong>

<ol>

 <li><strong> </strong>Siggi and Ollie are playing the following game of chance. Siggi will roll a fair six-sided die. If Siggi rolls a 1, 2, 3, or 4, then Ollie will flip a fair coin. If the coin comes up heads, Siggi pays Ollie a dollar. Otherwise, Ollie pays Siggi a dollar. On the other hand, if Siggi rolls a 5 or a 6, then Ollie pays Siggi a dollar immediately.

  <ul>

   <li>How much money does Siggi make in expectation? How much money does Ollie make in expectation?</li>

   <li>What is the probability that Ollie makes money? What is the probability that Siggi makes money? (c) What is the probability that both Ollie and Siggi make money?</li>

  </ul></li>

</ol>

(d) Suppose you know that Siggi made money. Conditional on that event, what is the probability that Siggi rolled a 1?

<ol start="2">

 <li><strong> </strong>In this exercise, we’ll explore different types of randomized algorithms. We say that a randomized algorithm is a <strong>Las Vegas Algorithm </strong>if it is always correct, but the running time is a random variable. We say that a randomized algorithm is a <strong>Monte Carlo Algorithm </strong>if there is some probability that it is incorrect. For example, QuickSort (with a random pivot) is a Las Vegas algorithm, since it always produces a sorted array (but if we get very unlucky QuickSort may be slow).</li>

</ol>

Consider the following task. The population of <em>n </em>tricky and trustworthy toads from HW1 is back. As before, you are guaranteed that there are strictly more than <em>n/</em>2 trustworthy toads in the population. Your goal is to find a single trustworthy toad. However, this time you’ve arrived on the island with a toad expert. The expert can determine whether a given toad is tricky or trustworthy, but she takes time Θ(<em>n</em>) to do it.

The algorithms given in Figure 1 all attempt to identify a single trustworthy toad. Fill in the chart below. You may use asymptotic notation for the running times; for the probability of returning a truthful toad, give the tightest bound that you can.

<table width="577">

 <tbody>

  <tr>

   <td width="97">Algorithm</td>

   <td width="129">Monte Carlo or Las Vegas?</td>

   <td width="92">Expected running time</td>

   <td width="92">Worst-case running time</td>

   <td width="167">Probability of returning a truthful toad</td>

  </tr>

  <tr>

   <td width="97"><strong>Algorithm 1</strong></td>

   <td width="129"> </td>

   <td width="92"> </td>

   <td width="92"> </td>

   <td width="167"> </td>

  </tr>

  <tr>

   <td width="97"><strong>Algorithm 2</strong></td>

   <td width="129"> </td>

   <td width="92"> </td>

   <td width="92"> </td>

   <td width="167"> </td>

  </tr>

  <tr>

   <td width="97"><strong>Algorithm 3</strong></td>

   <td width="129"> </td>

   <td width="92"> </td>

   <td width="92"> </td>

   <td width="167"> </td>

  </tr>

 </tbody>

</table>

If it helps in writing up your solution, the L<sup>A</sup>TEXcode for the table (which you can copy and paste and fill in) has been reproduced at the end of this problem set. <strong>[We are expecting: Your answers, and for each algorithm, a short informal justification of your answers.]</strong>

Put the toads in a random order ;

/* Assume it takes time <em>O</em>(<em>n</em>) to put the <em>n </em>toads in a random order                                                              */

Figure 1: Three algorithms for finding a truthful toad

<ol start="3">

 <li><strong> </strong>This exercise references the IPython notebook HW3.ipynb, available on the course website.</li>

</ol>

In our implementation of radixSort in class, we used bucketSort to sort each digit. Why did we use bucketSort and not some other sorting algorithm? There are several reasons, and we’ll explore one of them in this exercise.

<ul>

 <li><strong> </strong>One reason we chose bucketSort was that it makes radixSort work correctly! In ipynb, we’ve implemented four different sorting algorithms—bucketSort, quickSort, and two versions of mergeSort—as well as radixSort. Modify the code for radixSort to use each one of these four algorithms as an inner sorting algorithm. Which ones work?

  <ul>

   <li>Does using bucketSort work correctly?</li>

   <li>Does using quickSort work correctly?</li>

   <li>Does using mergeSort (with merge1) work correctly?</li>

   <li>Does using mergeSort (with merge2) work correctly?</li>

  </ul></li>

</ul>

<strong>[We are expecting: Yes or no for each part.]</strong>

<ul>

 <li>Explain what you saw above. What was special about the algorithms which worked? Why does this matter? (You may wish to play around with ipynb to “debug” the incorrect cases.)<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a></li>

</ul>

Make sure that the algorithms that you observed to work do have the property, and that those that you observed not to work don’t have the property.

<strong>[We are expecting: A clear definition of the special property and a short but convincing explanation of why it matters. You do not need to justify why each of the algorithms do or do not have the property but you should understand why they do or do not.]</strong>

<h1>Problems</h1>

You may talk with your fellow CS161-ers about the problems. However:

<ul>

 <li>Try the problems on your own <em>before </em></li>

 <li>Write up your answers yourself, in your own words. You should never share your typed-up solutions with your collaborators.</li>

 <li>If you collaborated, list the names of the students you collaborated with at the beginning of each problem.</li>

</ul>

<ol>

 <li><strong> </strong>Suppose that <em>n </em>flamingos are standing in a line.</li>

</ol>

Each flamingo has a political leaning: left, right, or center. You’d like to sort the flamingos so that all the left-leaning ones are on the left, the right-leaning ones are on the right, and the centrist flamingos are in the middle. You can only do two sorts of operations on the flamingos:

<table width="461">

 <tbody>

  <tr>

   <td width="79">Operation</td>

   <td width="382">Result</td>

  </tr>

  <tr>

   <td width="79">poll(j)</td>

   <td width="382">Ask the flamingo in position <em>j </em>about its political leanings</td>

  </tr>

  <tr>

   <td width="79">swap(i,j)</td>

   <td width="382">Swap the flamingo in position <em>j </em>with the flamingo in position <em>i</em></td>

  </tr>

 </tbody>

</table>

However, in order to do either operation, you need to pay the flamingos to co-operate: each operation costs one brine shrimp.<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> Also, you didn’t bring a piece of paper or a pencil, so you can’t write anything down and have to rely on your memory. Like many humans, you can remember up to seven<a href="#_ftn3" name="_ftnref3"><sup>[3]</sup></a> integers between 0 and <em>n </em>− 1 at a time.

Design an algorithm to sort the flamingos which costs <em>O</em>(<em>n</em>) brine shrimp, and uses no extra memory other than storing at most seven<a href="#_ftn4" name="_ftnref4"><sup>[4]</sup></a> integers between 0 and <em>n </em>− 1.

<strong>[We are expecting: Pseudocode with a short explanation of the idea of your algorithm; an informal justification that it works, uses only </strong><em>O</em>(<em>n</em>) <strong>brine shrimp and not too much memory.]</strong>

<ol start="2">

 <li><strong> </strong>Suppose that <em>n </em>flamingos are standing in a line, ordered from shortest to tallest.</li>

</ol>

You have a measuring stick of a certain height, and you would like to identify flamingo which is the same height as the stick, or else report that there is no such flamingo. The only operation you are allowed to do is compareToStick(f), where <em>f </em>is a flamingo, which returns taller if <em>f </em>is taller than the stick, shorter if <em>f </em>is shorter than the stick, and the same if <em>f </em>is the same height as the stick. As in Problem 1, you forgot to bring a piece of paper, so you can only store up to seven integers in {0<em>,…,n </em>− 1} at a time. And, as in Problem 1, you have to pay a Flamingo a brine shrimp in order to compare it to the stick.

<ul>

 <li>Give an algorithm which either finds a flamingo the same height as the stick, or else returns “No such flamingo,” in the model above which uses <em>O</em>(log(<em>n</em>)) brine shrimp.</li>

</ul>

<strong>[We are expecting: Pseudocode and an English description. You do not need to justify the correctness or brine shrimp usage. ]</strong>

<ul>

 <li><strong> </strong>Prove that any algorithm in this model of computation must use Ω(log(<em>n</em>)) brine shrimp. <strong>[We are expecting: A short but convincing argument.]</strong></li>

</ul>

<ol start="3">

 <li><strong> </strong>A wise flamingo has knowledge of an array <em>A </em>of length <em>n</em>, so that <em>A</em>[<em>i</em>] ∈{1<em>,…,k</em>} for all <em>i</em>. (Note that the elements of <em>A </em>are not necessarily distinct). You don’t have direct access to the list, but you can ask the wise flamingo <em>any </em>yes/no questions about it. For example, you could ask “If I remove <em>A</em>[5] and swap <em>A</em>[7] with <em>A</em>[8], would the array be sorted?” or “do molecular and morphological studies support a relationship between grebes and flamingos?”</li>

</ol>

This time you did bring a paper and pencil, and your job is to write down all of the elements of <em>A </em>in sorted order.<a href="#_ftn5" name="_ftnref5"><sup>[5]</sup></a> As usual, the wise flamingo charges one brine shimp per question.

<ul>

 <li><strong> </strong>Give a procedure to output a sorted version of <em>A </em>which uses <em>O</em>(<em>k </em>log(<em>n</em>)) brine shrimp. You may assume that you know <em>n </em>and <em>k</em>, although this is not necessary.</li>

</ul>

<strong>[We are expecting: Pseudocode, with an English explanation of what it is doing, why it is correct, and why it only uses </strong><em>O</em>(<em>k </em>log(<em>n</em>)) <strong>brine shrimp. ]</strong>

<ul>

 <li><strong> </strong>Prove that any procedure to solve this problem must use Ω(<em>k </em>log(<em>n/k</em>)) brine shrimp.</li>

</ul>

<strong>[We are expecting: A short but convincing argument.]</strong>

Here is L<sup>A</sup>TEX code for the table in Exercise 3:

begin{tabular}{|c|p{3cm}|p{2cm}|p{2cm}|p{4cm}|}

hline

Algorithm &amp; Monte~Carlo or Las~Vegas? &amp; Expected running time &amp;

Worst-case running time &amp; Probability of returning a truthful toad \

hline

textbf{Algorithm 1} &amp; &amp; &amp; &amp; \

hline

textbf{Algorithm 2} &amp; &amp; &amp; &amp; \

hline

textbf{Algorithm 3} &amp; &amp; &amp; &amp; \

hline

end{tabular}

<a href="#_ftnref1" name="_ftn1">[1]</a> <strong>Note: </strong>Yes, we talked about this a bit in class—that’s why it’s an exercise and not a problem!

<a href="#_ftnref2" name="_ftn2">[2]</a> According to Wikipedia, flamingos eat brine shrimp. Yum!

<a href="#_ftnref3" name="_ftn3">[3]</a> <a href="https://en.wikipedia.org/wiki/The_Magical_Number_Seven,_Plus_or_Minus_Two">https://en.wikipedia.org/wiki/The_Magical_Number_Seven,_Plus_or_Minus_Two</a>

<a href="#_ftnref4" name="_ftn4">[4]</a> You don’t need to use all seven storage spots, but you can if you want to. Can you do it with only two?

<a href="#_ftnref5" name="_ftn5">[5]</a> Note that you don’t have any ability to change the array <em>A </em>itself, you can only ask the wise flamingo about it.