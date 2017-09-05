--- 
title: "BayesLab - Exploring Bayesian Hierarchical Modeling"
author: "Dean Billheimer"
date: "2017-09-05"
site: bookdown::bookdown_site
documentclass: book
bibliography: [book.bib]
biblio-style: apalike
link-citations: yes
github-repo: dbillheimer/BayesLab
url: 'http\://github.com/dbillheimer/BayesLab/'
description: "Explores the use of Bayesian hierarchical inference in linear models."
---

# Preface {-}

To Dean:

Bayesian inference in models with linear structure (e.g. linear models) offers
advantages in estimation and inference by "borrowing strength" across similar
groups.  I don't really understand exactly how this works. This ebook is
explores theoretical and practical advantages of this approach.

Specifically, there are multiple issues I want to understand:

1. Efficiency gains in factorial experiments.
By way of example, suppose I have a two-factor experiment (A and B) each
with two levels.  The full factorial structure consists of ab, aB, Ab, and
AB.  Further, suppose A is the primary factor of interest, and B is more
exploratory (think predictive biomarker).  A standard sample size calculation
($\alpha = 0.05$, power 0.8) evaluating A only requires $n=17$ EUs per group,
for each of two groups (a and A).  Conversely, the full factorial suggests
$n=12$ for each of the four groups to test the main A effect (via linear
contrast).  What's up with that?

	It "feels" like the first analysis (two group) puts all posterior
	probability on the "no B effect" hypothesis, while the second assumes the
	general hypothesis of four disparate groups. Neither of these is satisfactory.

2. What do we do with sample size?  Maybe information gain or other metrics are
   better criteria that power?  For phase III trials with FDA review, fixed
   significance level $\alpha = 0.05$, and high power ($> 80$\%) may be (maybe?)
   appropriate. What about for laboratory studies with mice? or translational
   studies with prospectively sampled tissue specimens? or a phase I/II study
   with a single dose? or a single arm trial against a historical control?

	- close by, when is response adaptive randomization worthwhile?


3. How does explicit hierarchical modeling improve upon sequential modeling
   based on sufficient statistics?

4. Superficially, any advantages from hierarchical modeling would seem to accrue
   from Stein's result regarding MSE (EMSE?) for estimation of multiple
   parameters.  Is this the only phenomenon at work here?


I think the information encoded in prior distributions on parameters is subtle.
