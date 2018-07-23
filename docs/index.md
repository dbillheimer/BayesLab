--- 
title: "BayesLab - Exploring Bayesian Hierarchical Modeling and Predictive Inference"
author: "Dean Billheimer"
date: "2018-07-23"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib]
biblio-style: apalike
link-citations: yes
github-repo: dbillheimer/BayesLab
url: 'http\://github.com/dbillheimer/BayesLab/'
description: "Explores the use of Bayesian hierarchical modeling and predictive inference."
---

# Preface {-}


Bayesian inference in hierarchical models offers
advantages in estimation and inference by "borrowing strength" across similar
groups.  While I understand the principles of hierarchical modeling, I suspect
I'm missing some of the nuances of how this works. On a different topic (but
related!), I think a predictive approach to inference may lead to improved
interpretation of experimental/analysis results.  That is, the "reproducibility crisis" in
science, may instead be viewed as an interpretation crisis, at least in part. This ebook 
explores theoretical and practical advantages of Bayesian hierarchical modeling
and predictive inference.

Specifically, there are multiple issues I want to explore:

1. Efficiency gains in factorial experiments.
By way of example, suppose I have a two-factor experiment (A and B) each
with two levels.  The full factorial structure consists of ab, aB, Ab, and
AB.  Further, suppose A is the primary factor of interest, and B is more
exploratory (think predictive biomarker).  A standard sample size calculation
($\delta = 1$, $\alpha = 0.05$, power 0.8) evaluating A only requires $n=17$ EUs per group,
for each of two groups (a and A).  Conversely, the full factorial suggests
$n=12$ for each of the four groups to test the main A effect (via linear
contrast).  What's up with that?

	It "feels" like the first analysis (two group) puts all posterior
	probability on the "no B effect" hypothesis, while the second assumes the
	general hypothesis of four disparate groups. Neither of these is
	satisfactory. Each assumes something (or appears to) about the effect of B.

2. What do we do with sample size?  Maybe information gain or other metrics are
   better criteria than power?  For phase III trials with FDA review, fixed
   significance level $\alpha = 0.05$, and high power ($> 80$\%) may be
   appropriate (maybe?). What about for laboratory studies with mice? or translational 
   studies with prospectively sampled tissue specimens? or a phase I/II study
   with a single dose? or a single arm trial against a historical control?
   Reasonable loss/utility structures for developmental experiments seem to be
   not that well developed (or at least I don't know them).


3. How does explicit hierarchical modeling improve upon sequential (conditional) modeling
   based on sufficient statistics?

4. Superficially, any advantages from hierarchical modeling would seem to accrue
   from Stein's result regarding MSE (EMSE?) for estimation of multiple
   parameters.  Is this the only phenomenon at work here?

5. What constitutes a reproducible result? Surely it must include something
   about the (expected) result of a future experiment. Perhaps this idea should inform our
   utility structure?

