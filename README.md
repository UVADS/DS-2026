# Computational Probability, Fall 2026

## Overview

This course is all about variation, uncertainty, and randomness.  Students will learn the vocabulary of uncertainty and the mathematical and computational tools to understand and describe it.

## Instructors

Section 1: [Thomas Stewart](https://tgstewart.xyz)  
1919 Ivy Rm 348  
thomas.stewart@virginia.edu  
Github: thomasgstewart

Section 2 and 3: [Gianluca Guadagni]()  
1919 Ivy Rm 431  
gg5d@virginia.edu  
Github: gg5d

## Teaching assistants

Stephen Olsen  
Graduate student in Data Science  
wft5tv@virginia.edu  


Anu Jajodia  
Graduate student in Data Science  
nhg6tv@virginia.edu  
 

Maxwell Cooper  
Graduate student in Data Science  
juk5gq@virginia.edu  

## Instruction & Office hours

**Format of the class:** In-class time will be a combination of lectures, group assignments, live coding, and student presentations.  **Please note:** Circumstances may require the face-to-face portion of the class to be online.

**Time & Location:** Tues & Thurs, Data Science building

| Section | Time | Room |
|:---|:---:|:---:|
|1 | 12:30 - 1:45pm| 205 |
|2 | 12:30 - 1:45pm| 206 |
|3 | 2:00 - 3:15pm | 206 |

**Office Hours:**

| Time | Location | Alternate location* |
|:---:|:---:|:---:|
| Mon 2 - 4pm | Hub | 4th floor puzzle space |
| Tue 3:30 - 5:30pm | Rm 431 | |
| Wed 12:00 - 2:00pm | Hub | 4th floor puzzle space |
| Wed 3:00 - 5:00pm | Hub | 4th floor puzzle space |

*If the Hub is being used for an event, office hours will be on the 4th floor landing of the SDS building.

## Textbooks 

The following textbooks are freely available online via the UVA library.

[Understanding Uncertainty](https://ebookcentral.proquest.com/lib/uva/reader.action?docID=1574353)
by Dennis V. Lindley  

[Understanding Probability, 3rd edition](https://ebookcentral.proquest.com/lib/uva/reader.action?docID=944763)  
by Henk Tijms  

[Introduction to Probability: Models and Applications](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119549345)  
by N. Balakrishnan, Markos V. Koutras, Konstadinos G. Politis  

The following textbooks may also be helpful.

Probability and Statistics for Data Science  
by Norman Matloff  

Introduction to Probability Models  
by Sheldon M. Ross 

## Course notes

[Course notes (link)](https://tgstewart.cloud/compprob)

## Computing

Computing tasks will be shown in Python and R.

## Big ideas & Learning Outcomes

The following are the four ideas that I hope will persist with students after the minutia of the Poisson distribution has faded from memory.  Expand each section to see the associated learning outcomes and topics.

<details>
<summary>Probability is a framework for organizing beliefs; it is not a statement of what your beliefs should be.</summary>

| Learning outcomes | Topics |
|:------|:---|
| compare and contrast different definitions of probability, illustrating differences with simple examples | <ul><li>long-run proportion<li>personal beliefs<li>combination of beliefs and data |
| express the rules of probability verbally, mathematically, and computationally| <ul><li>AND, OR, complement, total probability<li>simulation error (relative and absolute) |
| illustrate the rules of probability with examples| |
| using long-run proportion definition of probability, derive the univariate rules of probability| |
| organize/express bivariate random variables in cross tables| |
| define joint, conditional, and marginal probabilities| |
| identify joint, conditional, and marginal probabilities in cross tables| |
| identify when a research question calls for a joint, conditional, or marginal probability| |
| describe the connection between conditional probabilities and prediction| |
| derive Bayes rule from cross tables| |
| apply Bayes rules to answer research questions| |
| determine if joint outcomes are independent| |
| calculate a measure of association between joint outcomes| |
| apply cross table framework to the special case of binary outcomes| <ul><li>Sensitivity<li>Specificity<li>Positive predictive value<li>Negative predictive value<li>Prevalence<li>Incidence |
| define/describe confounding variables | <ul><li>Simpson's paradox<li>DAGs<li>causal pathway |
| list approaches for avoiding confounding | <ul><li>stratification<li>randomization |
</details>

<details>
<summary>Probability models are a powerful framework for describing and simplifying real world phenomena as a means of answering research questions.</summary>

| Learning outcomes | Topics |
|:------|:---|
| list various data types| |
| match each data type with probability models that may describe it| <ul><li>Bernoulli<li>binomial<li>negative binomial<li>Poisson<li>Gaussian<li>gamma<li>mixture  |
| discuss the degree to which models describe the underlying data | |
| tease apart model fit and model utility| |
| express probability models both mathematically, computationally, and graphically| <ul><li>PMF/PDF<li>CMF/CDF<li>quantile function<li>histogram/eCDF |
| employ probability models (computationally and analytically) to answer research questions| |
| explain and implement different approaches for fitting probability models from data| <ul><li> Tuning <li>Method of Moments<li>Maximum likelihood<li>Bayesian posterior<li>kernel density estimation|
|visualize the uncertainty inherent in fitting probability models from data| <ul><li>sampling distribution<li>posterior distribution<li>bootstrap distribution |
| explore how to communicate uncertainty when constructing models and answering research questions| <ul><li>confidence intervals<li>support intervals<li>credible intervals<li>bootstrap intervals|
| propagate uncertainty in simulations | |
| explore the trade-offs of model complexity and generalizability| |
</details>

<details>
<summary>Probability is a framework for coherently updating beliefs based on new information and data.</summary>

| Learning outcomes | Topics |
|:------|:---|
| select prior distributions which reflect personal belief | <ul><li>informative vs weakly informative priors|
| implement bayesian updating | |
| manipulate the posterior distribution to answer research questions | |

</details>

<details>
<summary>Probability models can be expressed and applied mathematically and computationally.</summary>

| Learning outcomes | Topics |
|:------|:---|
| use probability models to build simulations of complex real world processes to answer research questions | |

</details>

## Classroom environment

The instructor may occasionally designate portions of class time as "No Laptop No Phone" periods. During these times, please put away laptops and cell phones in your bags. You're encouraged to take notes using paper and pencil instead. If you need to use your devices, you're welcome to step out of the classroom briefly. The instructor will provide gentle reminders about this policy, and continued non-compliance may result in point deductions from your final exam grade.

## Grading

Courses carrying a Data Science subject area use the following grading system: A, A-; B+, B, B-; C+, C, C-; D+, D, D-; F.  The symbol W is used when a student officially drops a course before its completion or if the student withdraws from an academic program of the University.

Grading Scale: 

 - 93-100 A
 - 90-92 A- 
 - 87-89 B+
 - 83-86 B 
 - 80-82 B- 
 - 77-79 C+ 
 - 73-76 C 
 - 70-72 C- 
 - <70 F

Grades will be a weighted average of the final exam score (30%), the midterm exams (each 20%), the deliverables (5% each) and homeworks (20%).

Homeworks sets are assigned regularly, and will appear in the course calendar.  On the due date, class will end with a single question pulled from (and potentially modified) the HW set.  You will have 15 minutes to write a solution.  It is closed book and closed note.  One homework grade will be dropped when calculating the final grade.

Rather than accepting late/missed homework, students may schedule a 10 minute oral exam with the TAs.  The TAs will ask you to explain a homework problem (potentially modified).  Students may schedule up to two oral exams during the semester.

Deliverables are larger assignments than homework.  To complete the deliverables, you will use probability models to build simulations of complex real world processes to answer questions. 

Midterm exams are graded on a 100 point scale.  For midterm 1, if your grade on midterm 2 or the final is higher, the higher score will replace the score for midterm 1.  Likewise, for midterm 2, if your grade on the final exam is higher, the higher score will replace the score for midterm 2.  For example, suppose your exams scores for the midterms and final were 72, 88, 85.  For the purposes of the final grade, your exam scores would be 88, 88, 85.

## Final exam schedule

The final exam for all sections is **Saturday, December 12, 2025** from **2:00PM-5:00PM** in rooms DS 205, 206, 246.

## 2026 Calendar

Homeworks, deliverables, reading assignments, and exams will be posted on the course calendar below.  Homeworks are due before the start of class.

| Date | Topic | Due |
|:-----|:------|:----|
| Tu Aug 25 | Syllabus & 31¢ Coin | |
| Th Aug 27 | Definitions of Probability | |
| Tu Sep 01 | Data types and summaries<br>Random variables (RV) |  |
| Th Sep 03 | Rules of prob of 1 cat/ordinal variable | HW 1  |
| Tu Sep 08 | Rules of prob of 2 cat/ordinal variables<br>+ Cell prob<br>+ Conditional prob (row and col)<br>+ Marginal prob<br>+ Independence<br>+ Correlation<br>+ Bayes rule |  |
| Th Sep 10 | Cont. |  |
| Tu Sep 15 | Cont. |  |
| Th Sep 17 | Prediction diagnostics<br>+ Sensitivity<br>+ Specificity<br>+ PPV<br>+ NPV | |
| Tu Sep 22 | Random variables from an urn<br>+ Sampling (with / without replacement)<br>+ Order (hands / sequences) | |
| Th Sep 24 | More univariate, discrete random variables<br>+ Binomial<br>+ Negative binomial (Geometric)<br>+ World Series<br>+ Poisson | |
| Tu Sep 29 | Exam prep | |
| Th Oct 01 | EXAM 1 |  |
| Tu Oct 06 | FALL BREAK (no class) | |
| Th Oct 08 | Compute refresh<br>+ Python<br>+ Markdown<br>+ Literate programing<br>+ Reproducible reports<br>+ .venv<br>+ working dir| |
| Tu Oct 13 | Simulation<br>+ Birthday problem<br>+ Monty Hall<br>+ Poker | |
| Th Oct 15 | Variation & num replicates<br>Law of large numbers| |
| Tu Oct 20 | 1 continuous RV<br>+ density/PDF<br>+ CDF<br> Calc review<br>+ Area under curve | Deliverable 1 |
| Th Oct 22 | Cont.<br>+ normal<br>+ gamma<br>+ beta<br>+ mixture |  |
| Tu Oct 27 | 2 continuous RV |  |
| Th Oct 29 | Cont.<br>Exam prep |  |
| Tu Nov 03 | ELECTION DAY (No class)| |
| Th Nov 05 | EXAM II| |
| Tu Nov 10 | Observational data<br>+ Confounding<br>+ Simpson's paradox<br>~~+ DAGs~~<br>+ Randomization/stratification | |
| Th Nov 12 | Calc review<br>+ Min/max with $f^{\prime}$<br>Estimation<br>+ MLE<br>+ Bayes<br>+ KDE| |
| Tu Nov 17 | Communicating uncertainty<br>+ Confidence intervals<br>--+empirical<br>--+asymptotic<br>+ Support intervals<br>+ Credible intervals| |
| Th Nov 19 | Simulation of operating characteristics| |
| Tu Nov 24 | THANKSGIVING (No class)| |
| Th Nov 26 | THANKSGIVING (No class)| |
| Tu Dec 01 | (Time allowing) Markov Chains | |
| Th Dec 03 | Cont. | Deliverable 2 |
| Tu Dec 08 | Exam Prep| |
| Sa Dec 12 | FINAL EXAM (2pm)| |


## A few Policies that will Govern the Class

There are many additional policies that this course inherits from the School of Data Science course policies, please see [here](https://myuva-my.sharepoint.com/:w:/r/personal/vzm6dw_virginia_edu/Documents/courses/computational-probability-fall-2024/DS-2026-BSDS%20Syllabus%20Policies%20Fall%202025.docx?d=wf898dd6ef8574e8ea29ee2fb3c8fce0f&csf=1&web=1&e=rGq6bD).

