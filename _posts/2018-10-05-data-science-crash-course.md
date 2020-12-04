---
layout: post
title:  "Data Science Crash Course: Interview Prep"
date:   2018-11-19
---

<br><br>

# Data Science Crash Course: Interview Prep

Internship application season is coming up! If you're studying for interviews, it can be hard to know where to start, so I've created a roundup of my favorite blog posts, course slides, Quora and StackExchange answers, and miscellaneous other resources that cover the basics of most machine learning and data science interviews.

Machine learning internship interviews often have three components: (1) an informational phone call, (2) a coding and/or machine learning phone screen, and (3) an in-person coding and/or machine learning interview, sometimes with a presentation. Depending on the company, some or all of these components may be required. The resources I listed below will be most useful for studying for the machine learning phone screen, in which you'll probably be asked to answer lots of basic questions about machine learning algorithms (e.g. "What is precision?" "Do you know what SVMs are? How do they work?").

These are the explanations I personally found most useful and intuitive. In particular, I look for resources that are both simple and complete: they lack clutter but they also explain every step without glossing or assuming knowledge on the part of the reader. 

This list isn't meant to be comprehensive, and it certainly shows my biases towards NLP and unsupervised methods. Pick and choose what's useful for you! And if you're just getting started with machine learning, I'd recommend taking a structured course, either through your university or through a free online resource like Coursera.

These explanations and visualizations are often very creative and thoughtful. Thank you to each of these authors for taking the time to craft and share these resources!


<br>

### Essentials
* Andrew Ng's machine learning [course](http://cs229.stanford.edu/syllabus.html) and [notes](http://www.holehouse.org/mlclass/) taken by Alex Holehouse
* [Wikipedia](https://en.wikipedia.org/wiki/Machine_learning)

<br>

### Statistics, Calculus, and Information Theory
* [Combinatorics Cheat Sheet](https://mste.illinois.edu/projects/aims/files/2007/lpitt/combinatorics-cheat-sheet.doc)
* [On Measures of Entropy and Information](http://threeplusone.com/gec/note) by Gavin E. Crooks
* [Harvard Statistics: Math Review for Stat 110](https://projects.iq.harvard.edu/files/stat110/files/math_review_handout.pdf) by Joe Blitzstein
* [ML Cheatsheet: Calculus](http://ml-cheatsheet.readthedocs.io/en/latest/calculus.html)
* [Stanford Probabilistic Graphical Models: Probability review](https://ermongroup.github.io/cs228-notes/preliminaries/probabilityreview/) by Volodymyr Kuleshov and Stefano Ermon
* [Probability Cheat Sheet](http://www.wzchen.com/probability-cheatsheet/) by Joe Blitzstein and William Chen
* [PennState Statistics: Confidence Intervals](https://onlinecourses.science.psu.edu/statprogram/node/135)

<br>

### Linear Algebra
* [Understanding Principal Component Analysis](https://medium.com/@aptrishu/understanding-principle-component-analysis-e32be0253ef0) by Rishav Kumar
* [A tutorial on Principal Components Analysis](http://www.cs.otago.ac.nz/cosc453/student_tutorials/principal_components.pdf) by Lindsay I. Smith
* [A Tutorial on Principal Component Analysis](https://arxiv.org/pdf/1404.1100.pdf) by Jonathon Shlens
* [Singular Value Decomposition Tutorial](http://site.iugaza.edu.ps/ahdrouss/files/2010/03/Singular_Value_Decomposition_Tutorial.pdf) by Kirk Baker

<br>

### KNN  
* [Brilliant: K-nearest Neighbors](https://brilliant.org/wiki/k-nearest-neighbors/) by Akshay Padmanabha and Christopher Williams  

<br>

### Perceptron
* [Orebro University: The Simple Perceptron](http://130.243.105.49/~lilien/ml/seminars/2007_02_01b-Janecek-Perceptron.pdf)
* [StackOverflow: Intuition for perceptron weight update rule](https://stackoverflow.com/questions/34477827/intuition-for-perceptron-weight-update-rule) by Ami Tavory  
* [StackExchange: Question regarding weight update rule in Perceptron](https://stats.stackexchange.com/questions/253240/question-regarding-weight-update-rule-in-perceptron) by Arman
* [Deep Learning: The Straight Dope: The Perceptron](http://gluon.mxnet.io/chapter02_supervised-learning/perceptron.html)

<br>

### Linear Regression  
* [Yale Statistics Course](http://www.stat.yale.edu/Courses/1997-98/101/linreg.htm) by Michelle Lacey  
* [ML Cheatsheet: Linear Regression](http://ml-cheatsheet.readthedocs.io/en/latest/linear_regression.html)
* [Toronto Course](http://www.cs.toronto.edu/~rgrosse/courses/csc321_2018/readings/L02%20Linear%20Regression.pdf) by Roger Grosse
* [Testing the Assumptions of Linear Regression](http://people.duke.edu/~rnau/testing.htm) by Robert Nau  
* [Ordinary Least Squares Linear Regression: Flaws, Problems, and Pitfalls](http://www.clockbackward.com/2009/06/18/ordinary-least-squares-linear-regression-flaws-problems-and-pitfalls/)

<br>

### Logistic Regression  
* [ML Cheatsheet: Logistic Regression](http://ml-cheatsheet.readthedocs.io/en/latest/logistic_regression.html)  
* [Is Logistic Regression a linear classifier?](https://homes.cs.washington.edu/~marcotcr/blog/linear-classifiers/) by Marco Tulio Ribeiro  
* [StackExchange: What's the difference between logistic regression and perceptron?](https://stats.stackexchange.com/questions/162257/whats-the-difference-between-logistic-regression-and-perceptron) by Antoni Parellada
* [Stanford Deep Learning Tutorial: Softmax Regression](http://ufldl.stanford.edu/tutorial/supervised/SoftmaxRegression/)
* [Deep Learning Tutorial - Softmax Regression](http://mccormickml.com/2014/06/13/deep-learning-tutorial-softmax-regression/) by Chris McCormick
* [Difference Between Softmax and Sigmoid Function](https://dataaspirant.com/2017/03/07/difference-between-softmax-function-and-sigmoid-function/) by Saimadhu Polamuri
* [Deep Learning - The Straight Dope: Binary classification with logistic regression](http://gluon.mxnet.io/chapter02_supervised-learning/logistic-regression-gluon.html)

<br>

### SVMs  
* [SVM Tutorial](http://web.mit.edu/zoya/www/SVM.pdf) by Zoya Gavrilov
* [An Idiot's guide to Support vector machines (SVMs)](http://web.mit.edu/6.034/wwwbob/svm.pdf) by Robert Berwick
* [Support Vector Machines, Succinctly](https://www.svm-tutorial.com/svm-tutorial/) by Alexadre Kowalczyk  
* [Quora: What is the kernel trick?](https://www.quora.com/What-is-the-kernel-trick) by Nikhil Garg
* [ResearchGate: SVM with large feature space?](https://www.researchgate.net/post/SVM_with_large_feature_space2) by Adrian Letchford, Katharina Morik, and Dmytro Prylipko

<br>

### LDA  
* [Introduction to Probabilistic Topic Models](https://www.semanticscholar.org/paper/Introduction-to-Probabilistic-Topic-Models-Blei/5f1038ad42ed8a4428e395c96d57f83d201ef3b3) by David Blei + [slides](https://pdfs.semanticscholar.org/01f3/290d6f3dee5978a53d9d2362f44daebc4008.pdf)
* [Probabilistic Topic Models](https://www.semanticscholar.org/paper/Probabilistic-Topic-Models-Erlbaum-Steyvers/418c7e1e2d9cd5695ddbe9898ed3852b565faefc) by Mark Steyvers and Tom Griffiths
* [Latent Dirichlet Allocation: Toward a Deeper Understanding](https://www.semanticscholar.org/paper/Latent-Dirichlet-Allocation%3A-Towards-a-Deeper-Unde-Reed/321478fa5adf3f6a4fe373f502b88d8cc21c853d) by Colorado Reed
* [Latent Dirichlet Allocation](http://www.utdallas.edu/~nrr150130/cs6375/2015fa/lects/Lecture_20_LDA.pdf) by Nicholas Ruozzi
* [Introduction to Latent Dirichlet Allocation](http://blog.echen.me/2011/08/22/introduction-to-latent-dirichlet-allocation/) by Edwin Chen  

<br>

### Naive Bayes  
* [Aylien: Naive Bayes for Dummies: A Simple Explanation](http://blog.aylien.com/naive-bayes-for-dummies-a-simple-explanation/) by Mike Waldron
* [Quora: What are the disadvantages of using a naive bayes for classification?](https://www.quora.com/What-are-the-disadvantages-of-using-a-naive-bayes-for-classification) by Simone Scardapane

<br>

### Deep Learning
* [fast.ai](http://www.fast.ai/) by Jeremy Howard and Rachel Thomas
* [Deep Learning](http://www.deeplearningbook.org/) by Ian Goodfellow, Yoshua Bengio, and Aaron Courville
* [Understanding LSTM Networks](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) by Christopher Olah
* [A Primer on Neural Network Models for Natural Language Processing](http://u.cs.biu.ac.il/~yogo/nnlp.pdf) by Yoav Goldberg

<br>

### Regularization
* [StackExchange: What is regularization in plain english?](https://stats.stackexchange.com/questions/4961/what-is-regularization-in-plain-english) by Toby Kelsey
* [Quora: What is regularization in machine learning?](https://www.quora.com/What-is-regularization-in-machine-learning) by Yassine Alouini
* [Quora: What's a good way to provide intuition as to why the lasso (L1 regularization) results in sparse weight vectors?](https://www.quora.com/Whats-a-good-way-to-provide-intuition-as-to-why-the-lasso-L1-regularization-results-in-sparse-weight-vectors) by Phillip Adkins (the second answer)
* [L1 Norm Regularization and Sparsity Explained for Dummies](https://medium.com/mlreview/l1-norm-regularization-and-sparsity-explained-for-dummies-5b0e4be3938a) by Shi Yan
* [Machine Learning Explained: Regularization](http://enhancedatascience.com/2017/07/04/machine-learning-explained-regularization/) by Antoine Guillot (?)
* [l0-Norm, l1-Norm, l2-Norm, ..., l-infinity Norm](https://rorasa.wordpress.com/2012/05/13/l0-norm-l1-norm-l2-norm-l-infinity-norm/) by Wattanit Hotrakool

<br>

### Evaluation and Model Comparison
* [Machine Learning Crash Course: Part 4 - The Bias-Variance Dilemma](https://ml.berkeley.edu/blog/2017/07/13/tutorial-4/) by Daniel Geng and Shannon Shih
* [Choosing a Machine Learning Classifier](http://blog.echen.me/2011/04/27/choosing-a-machine-learning-classifier/) by Edwin Chen
* [Machine Learning Done Wrong](http://ml.posthaven.com/machine-learning-done-wrong) by Cheng-Tao Chu
* [Machine Learning for Dummies Cheat Sheet](http://www.dummies.com/programming/big-data/data-science/machine-learning-dummies-cheat-sheet/) by John Paul Mueller and Luca Massaron
* [Classification Model Pros and Cons](https://github.com/ctufts/Cheat_Sheets/wiki/Classification-Model-Pros-and-Cons) by Chris Tufts
* [Handbook of Biological Statistics](http://www.biostathandbook.com/) by John H. McDonald

<br>

(I've tried to credit the authors wherever possible, but I couldn't identify a few of them. If you know who created these resources, please contact me!)

<br><br>

_November 19, 2018_

<br><br><br>
