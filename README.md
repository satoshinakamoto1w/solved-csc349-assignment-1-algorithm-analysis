Download Link: https://assignmentchef.com/product/solved-csc349-assignment-1-algorithm-analysis
<br>
Analysis of algorithms concerns two broad concepts: <em>correctness </em>and <em>complexity</em>. Given that an algorithm produces the correct output for any input, we are interested in the resources it requires in different situations. In this assignment, you’ll measure and predict the running times of three algorithms that solve the same problem in different ways. <strong>Deliverables:</strong>

<strong>GitHub Classroom: </strong><a href="https://classroom.github.com/a/Bc17ge2K">https://classroom.github.com/a/Bc17ge2K</a>

<strong>Required Files:                   </strong>compile.sh, run.sh

<strong>Optional Files: </strong>*.py, *.java, *.clj, *.kt, *.js, *.sh <strong>Part 1: Ground Rules</strong>

Throughout this class, you may implement your assignments in one of the following languages:

<ul>

 <li>Python 3.7.4 <em><sub>· </sub></em>Clojure 1.10.1<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a><sup>                                                              </sup><em><sub>· </sub></em>Node.js 12.10.0</li>

 <li>Java 12.0.2 <em><sub>· </sub></em>Kotlin 1.3.50<sup>2                                                                    </sup><em><sub>· </sub></em>GNU Bash 5.0.2<sup>3</sup></li>

</ul>

However, Python is recommended as it is the only language I can help you with.

To make automated grading possible, you will also need to submit two short shell scripts: one to compile your submission, one to run it. Further details, along with sample submissions in all supported languages, can be found here: <a href="https://github.com/csc349fall19/asgn-samples">https://github.com/csc349fall19/asgn-samples </a>Furthermore:

<ul>

 <li>Submit only source code files as they are. Any directories or compressed files will be ignored.</li>

 <li>For record-keeping purposes, you must hand in original source files, not pre-compiled files.</li>

 <li>You may not use <em>any </em>third party libraries<sup>4</sup>, even if they are installed on Cal Poly’s Unix servers.</li>

</ul>

<h1>Part 2: GitHub Classroom</h1>

In this class, you’ll submit your programs through GitHub, an online host for tool known simply as “git”. Git tracks changes you make to files so that you can easily undo or combine changes while working on a project. You should already be familiar with the basic features of git from previous classes, such as CSC 202 and CSC 203. If not, the following resources might be helpful:

<ul>

 <li><a href="https://help.github.com/en/articles/set-up-git">https://help.github.com/en/articles/set-up-git</a></li>

 <li><a href="https://help.github.com/en/articles/cloning-a-repository">https://help.github.com/en/articles/cloning-a-repository</a></li>

 <li><a href="https://help.github.com/en/articles/managing-files-using-the-command-line">https://help.github.com/en/articles/managing-files-using-the-command-line</a></li>

 <li><a href="https://help.github.com/en/articles/pushing-to-a-remote">https://help.github.com/en/articles/pushing-to-a-remote</a></li>

</ul>

GitHub Classroom allows your instructors to accept electronic submissions through GitHub.

<ol>

 <li>Enter your Cal Poly and GitHub usernames in this form: <a href="https://forms.gle/fkYfJRpyLNCtRWAs9">https://forms.gle/fkYfJRpyLNCtRWAs9</a><a href="https://forms.gle/fkYfJRpyLNCtRWAs9">. </a>This allows us to determine who should get credit for your electronically submitted assignments.</li>

 <li>Accept this GitHub Classroom assignment: <a href="https://classroom.github.com/a/Bc17ge2K">https://classroom.github.com/a/Bc17ge2K</a><a href="https://classroom.github.com/a/Bc17ge2K">.</a> This will create a new repository for you on GitHub which you will use to submit this assignment, as well as provide some sample inputs and their expected outputs.</li>

</ol>

<sup>1</sup>You may assume that the Clojure JARs are in the classpath and that the clj and clojure commands are available.

<sup>2</sup>You may assume that the Kotlin lib is in the classpath and that the Kotlin bin is in the path, for JVM-backed Kotlin.

<sup>3</sup>Not that I’d recommend it — this is very much <em>not </em>what Bash was designed for.

<sup>4</sup>And your submission won’t have Internet access when it’s run, so you cannot use apt/pip/lein/npm to install them.

<strong>Assignment 1 — Algorithm Analysis</strong>

Fall 2019                                                                                                                                                     <strong>Due: Friday, September 27<sup>th</sup></strong>

<h1>Part 3: Sorting Algorithms</h1>

Recall that there exist several algorithms commonly used to solve the sorting problem, including:

<ul>

 <li>SelectionSort repeatedly <em>selects </em>the smallest element from among the as-yet-unsorted elements.</li>

 <li>InsertionSort repeatedly <em>inserts </em>the next unsorted element into a sorted subsequence.</li>

 <li>MergeSort recursively sorts the two halves of a sequence, then <em>merges </em>the sorted halves back together. In your programming language of choice per Part 1, implement these three algorithms for sequences of integers. Your program must accept as a command line argument the name of a file containing such a sequence, printing to stdout the results of applying the three algorithms. For example:</li>

</ul>

&gt;$ ./compile.sh

&gt;$ ./run.sh in1.txt

Selection Sort: -16, -15, -14, -7, -6, -5, -4, 0, 1, 2, 5, 7, 8, 13, 14, 15

Insertion Sort: -16, -15, -14, -7, -6, -5, -4, 0, 1, 2, 5, 7, 8, 13, 14, 15

Merge Sort                                        : -16, -15, -14, -7, -6, -5, -4, 0, 1, 2, 5, 7, 8, 13, 14, 15

Your program will be tested using diff, so its printed output must match <em>exactly</em>.

<h1>Part 4: Analysis</h1>

Record the running times of each algorithm for sequences of randomly generated integers between <sub>5<em>,</em>000 </sub>and 10<em><sub>,</sub></em><sub>000 </sub>elements in length, in increments of <sub>10</sub>. That is to say:

<ol>

 <li>Randomly generate a sequence of <sub>5<em>,</em>000 </sub>integers. Run the three sorts and record their running times. 2. Randomly generate a sequence of <sub>5<em>,</em>010 </sub>integers. Run the three sorts and record their running times.</li>

 <li>Randomly generate a sequence of <sub>5<em>,</em>020 </sub> Run the three sorts and record their running times.</li>

 <li>…</li>

</ol>

You may certainly write a program to automate this process, however, note that this is separate from and should not be a part of the program specified in Part 3.

Plot these timing results, with the length of the sequence on the horizontal axis and the running time on the vertical axis — you should have a scatter plot with <sub>500 </sub>points for each algorithm.

Finally, using these empirical running times, extrapolate: How long should each algorithm take to sort <sub>25<em>,</em>000 </sub>elements? How many elements should each be able to sort in <sub>10 </sub>minutes? Consider fitting a curve to your plots in order to answer these questions.


