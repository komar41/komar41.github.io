---
layout: page
title: Min-Support Apriori
description: Python implementation of minimum support apriori algorithm
img: "assets/img/projects/ms_apriori/thumbnail.png"
importance: 13
category: Other
---

<h4><u>Access this project</u></h4>
<b>GitHub repo:</b> <a href='https://github.com/komar41/MSApriori'>https://github.com/komar41/MSApriori</a> <br>
<b>Tools used:</b> Python.
<p align='justify'>
The Apriori algorithm is a fundamental data mining technique for finding frequent itemsets in transaction databases. It works by identifying individual items that meet a minimum support threshold, then extends to larger itemsets, pruning those that don't meet the threshold.
</p>
<p align='justify'>
<b>Key concepts:</b>
<ul>
    <li>Itemset: Collection of items</li>
    <li>Support: Frequency of an itemset</li>
    <li>Frequent itemset: Itemset with support above a threshold</li>
</ul>
</p>
<p align='justify'>
<b>Example:</b><br>
Transaction database:
<ul>
    <li>T1: {A, B, C}</li>
    <li>T2: {B, C, D}</li>
    <li>T3: {A, C, D}</li>
    <li>T4: {B, C, D}</li>
</ul>
<b>Minimum support:</b> 50% (2 transactions)

<b>Process:</b><br>

<ul>
    <li>Find frequent 1-itemsets: {A}, {B}, {C}, {D}</li>
    <li>Generate 2-itemsets: {A,B}, {A,C}, {A,D}, {B,C}, {B,D}, {C,D}</li>
    <li>Prune infrequent: {A,B}</li>
    <li>Continue until no more frequent itemsets found</li>
</ul>
<b>Result:</b> Frequent itemsets {A}, {B}, {C}, {D}, {B,C}, {B,D}, {C,D}

</p>
<p align='justify'>
The MSApriori algorithm is an extension of the classic Apriori algorithm for association rule mining. It addresses a limitation of the original Apriori algorithm by allowing different minimum support thresholds for different items. This is particularly useful when dealing with datasets that contain both frequent and rare items of interest.
</p>
<p align='justify'>
<b>Key features of MSApriori:</b><br>
<ul>
    <li>Multiple Minimum Support (MIS): Each item can have its own minimum support threshold.</li>
    <li>Support Difference Constraint (SDC): Ensures that the support values of items in a frequent itemset are not too different from each other.</li>
</ul>
</p>
<p align='justify'>
<b>Example:</b><br>
Let's consider a small transaction database:
<ul>
    <li>Transaction 1: {A, B, C, D}</li>
    <li>Transaction 2: {B, C, E}</li>
    <li>Transaction 3: {A, B, C, E}</li>
    <li>Transaction 4: {B, D, E}</li>
</ul>
Suppose we have the following MIS values:

<ul>
    <li>MIS(A) = 40%</li>
    <li>MIS(B) = 20%</li>
    <li>MIS(C) = 30%</li>
    <li>MIS(D) = 20%</li>
    <li>MIS(E) = 20%</li>
    <li>SDC = 10%</li>
</ul>
The algorithm would proceed as follows:<br>
Count the support of each item:<br>
A: 50%, B: 100%, C: 75%, D: 50%, E: 75%

Generate frequent 1-itemsets based on their MIS values:<br>
{B}, {C}, {D}, {E} (A is excluded as its support is below its MIS)

Generate candidate 2-itemsets and check their support:<br>
{B, C}, {B, D}, {B, E}, {C, D}, {C, E}, {D, E}

Prune itemsets that don't meet the SDC constraint or individual MIS values.<br>
Continue generating and pruning larger itemsets until no more frequent itemsets can be found.

The final output would be the frequent itemsets that satisfy both the MIS and SDC constraints.

</p>
<p align='center'>
  <img src="https://github.com/user-attachments/assets/a6ce000a-6e8a-4e0a-b70c-bf61ca64243f" alt="MSApriori Algorithm" width="60%">
</p>
<p align='center'>
  <small>Image source: <a href="https://www.datacamp.com/tutorial/market-basket-analysis-r">Datacamp</a></small>
</p>
<h4><u>Input</u></h4>
<p align='justify'>
The program takes two input files in plain text format:
</p>
<h5>1. Data File</h5>
<p align='justify'>
Contains transactions, with each line representing a transaction and items represented by integer numbers.<br>
<b>Example:</b>
<pre><code>10, 50, 30, 40
1, 2, 4, 6, 8, 9, 10
3, 4, 5
7, 9, 20</code></pre>
</p>
<h5>2. Parameter File</h5>
<p align='justify'>
Contains MIS (Minimum Item Support) values for items and SDC (Support Difference Constraint).<br>
<b>Example:</b>
<pre><code>MIS(1) = 0.02
MIS(2) = 0.04
...
MIS(rest) = 0.01
SDC = 0.003</code></pre>
<p>Note: 'rest' refers to all other items not given specific MIS values.</p>
</p>
<h4><u>Output</u></h4>
<p align='justify'>
The output file follows a specific format:
<pre><code>(Length-1 <number of length 1 frequent itermsets>
<length-1 itemset 1>
<length-1 itemset 3>
...
)
(Length-2 <number of length 2 frequent itermsets>
<length-2 itemset 1>
<length-2 itemset 3>
...
)</code></pre>
<b>Example output:</b>
<pre><code>(Length-1 3
(1)
(2)
(11)
)
(Length-2 2
(1 2)
(2 3)
)</code></pre>
</p>
<h4><u>Implementation Details</u></h4>
<p align='justify'>
<ul>
    <li>The algorithm reads the data and parameter files to initialize the transaction database and MIS values.</li>
    <li>It then performs the MSApriori algorithm to find frequent itemsets.</li>
    <li>The output is generated according to the specified format, listing frequent itemsets of each length.</li>
</ul>
</p>
<h4><u>Usage</u></h4>
<p align='justify'>
<ol>
    <li>Prepare the data file and parameter file as per the specified format.</li>
    <li>Run the MSApriori algorithm through the jupyter notebook: <code>MSApriori Final Version.ipynb</code></li>
    <li>The output will be generated in a file named <code>output.txt</code>.</li>
</ol>
</p>
<h4><u>Important Notes</u></h4>
<p align='justify'>
<ul>
    <li>The implementation strictly follows the input and output format specifications.</li>
    <li>No additional symbols or punctuation marks are used in the output beyond what is specified.</li>
    <li>The indentation in the output is not significant, but the round brackets must be placed correctly.</li>
</ul>
</p>
<h4><u>References</u></h4>
<p align='justify'>
<ul>
    <li>R. Agrawal and R. Srikant. "Fast algorithms for mining association rules." In Proc. 1994 Int. Conf. Very Large Data Bases (VLDB'94), pages 487-499, Santiago, Chile, Sept. 1994.</li>
    <li>B. Liu, W. Hsu, and Y. Ma. "Mining association rules with multiple minimum supports." In Proceedings of the fifth ACM SIGKDD international conference on Knowledge discovery and data mining, pages 337-341. ACM, 1999.</li>
</ul>
</p>
<h4><u>Team</u></h4>
<p align='justify'>
<ul>
    <li>Kazi Shahrukh Omar</li>
    <li>Soham Pradhan</li>
</ul>
</p>
