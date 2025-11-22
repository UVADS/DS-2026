**NOTE: This is a double homework.  It is worth 2 homework assignments.**

# Part 1: Confounding and Intermediate Variables

## Question 1

Read chapter 8 of Understanding Uncertainty.

## Question 2

In chapter 8, you read about two examples: a medical trial and an agricultural trial.  The medical trial was an example of confounding variables.  The agricultural example was an example of intermediate variables.  Explain what confounding variables and intermediate variables are.

## Question 3

As data scientists, we are often interested in how predictors (X) relate to outcomes (Y).  Our understanding of the relationship between X and Y may be impacted by a third variable Z.  Identify 2 examples (X, Y, Z) where Z is a confounding variable.  Identify 2 examples (X, Y, Z) where Z in an intermediate variable.  Select examples that are relevant to your interests.  In each example, note which variable is the predictor (X), which is the the outcome (Y), and which is Z.

## Question 4 (Call back to Exam 2 Prep)

The following function generates data from a cohort of individuals who were diagnosed with disease X.  In the dataset genderated by `vax_data` the variables are: vaccination status, disease severity, and disease duration.

```
import numpy as np
import pandas as pd

def vax_data(R, seed=None):
    if seed is not None:
        np.random.seed(seed)
    vs = np.random.binomial(1, 0.5, R)
    ds = np.random.binomial(1, 0.25 * (vs == 1) + 0.75 * (vs == 0))
    rt = np.random.binomial(1, 0.7 * (ds == 1) + 0.5 * (ds == 0))

    df = pd.DataFrame({
        "vaccination_status": np.where(vs == 1, "vaccinated", "unvaccinated"),
        "disease_severity": np.where(ds == 1, "mild", "severe"),
        "recovery_time": np.where(rt == 1, "short", "long")
    })

    return df
```

Using seed = `20251028`, generate 1000 draws from the function.  Calculate a summary of the effect of vaccination by calculating the difference is conditional probabilities:

$$
\Delta = P(\text{Short recovery}|\text{vaccinated}) - P(\text{Short recovery}|\text{unvaccinated})
$$

## Question 5 (Call back to Exam 2 Prep)

Calculate the treatment effect as before, but this time calculate it separately for the mild and severe populations.

## Question 6

Is disease severity a confounding variable or an intermediate variable? Explain your answer.

## Question 7

Determine if the vaccine is effective.  Justify your answer. 

## Question 8 

Suppose you want to know if going to office hours improves performance on an exam.

Identify 2 variables that might be confounding and 2 variables that might be intermediate.  (Total of 4 variables.)  Explain why each example is confonding or intermediate.  

# Part 2: Continuous random variables

The material on continuous random variables in the course notes will be helpful for this section.

## Question 9

Baseball Batting Average: A baseball analyst models a rookie player's true batting average using a Beta(81, 219) distribution (based on 300 at-bats with 81 hits).

(a) What is the probability that the player's true batting average is between 0.250 and 0.300?
(b) Calculate the 90th percentile of the player's batting average distribution.

## Question 10

Project Completion: A project manager models the proportion of a software project completed by next Friday using a Beta(5, 2) distribution.

(a) What is the expected proportion completed?
(b) What is the probability that less than 60% will be completed?

## Question 11

Manufacturing Quality: A factory produces bolts with diameters following a Normal(10.0, 0.05²) mm distribution. Bolts must be between 9.9 and 10.1 mm to meet specifications.

(a) What percentage of bolts fail to meet specifications?
(b) If the factory produces 10,000 bolts per day, how many are expected to be rejected?
(c) What is the probability density at the target diameter of 10.0 mm?

## Question 12

Standardized Test Scores: SAT Math scores follow approximately Normal(520, 115²) distribution.

(a) A scholarship requires a score in the top 10%. What is the minimum score needed?
(b) What is the probability a student scores between 500 and 650?
(c) If 5 students take the test independently, what is the probability all score above 600?

## Question 13

Annual Rainfall: Annual rainfall (in inches) in a desert region follows a Gamma(shape=2, scale=3) distribution.

(a) What is the probability of receiving more than 9 inches of rain in a year?
(b) What is the probability of receiving between 3 and 6 inches?
(c) Calculate the median annual rainfall.

## Question 14

Insurance Claims: The size of insurance claims (in thousands of dollars) follows a Gamma(shape=2.5, scale=4) distribution.

(a) What percentage of claims exceed $15,000?
(b) What is the probability density at a claim of $10,000?
(c) Find the claim amount such that 90% of claims are below this value.

## Question 15

Customer Arrivals: Customers arrive at a coffee shop with time between arrivals following an Exponential(λ=4) distribution (time in minutes).

(a) What is the probability the next customer arrives within 30 seconds (0.5 minutes)?
(b) What is the probability that more than 2 minutes pass between consecutive customers?
(c) Find the 90th percentile of time between arrivals.

## Question 16

Radioactive Decay: The time until the next decay event of a radioactive sample follows an Exponential(λ=0.05) distribution (time in seconds).

(a) What is the probability of waiting more than 30 seconds for the next decay?
(b) What is the expected waiting time?
(c) What is the probability density at t=20 seconds?
(d) Generate a plot of the density, with the region corresponding to the probability that the next event occurs in less than 5 seconds or more that 25 seconds.

## Question 17

Manufacturing Tolerance: A machine cuts wooden boards to a length that is equally likely to fall anywhere between 98.5 cm and 101.5 cm.

(a) What is the probability that a randomly selected board has length between 99.4 cm and 100.2 cm?
(b) What is the 90th percentile of board lenghts?

## Question 18

Emergency Room Wait Times: At a small clinic, the wait time for non-urgent patients is modeled as Uniform(10, 40) minutes.

(a) What is the wait time threshold such that 90% of patients wait less than that time?

## Question 19

Randomized Appointment Scheduling: A dentist randomly assigns check-up appointment start times uniformly over a 4-hour window from 8:00 AM to 12:00 PM.

(a) Create a plot of the PDF of appointment start time.
(b) Shade the portion of the PDF that corresponds to the probability of an appointment starting before 10:30 AM?
(c) What is the probability of an appointment between 9:30 and 10:45?

## Question 20

Consider a random variable $X$ with the following density function, with $c$ unknown:

$$
f(x) = c\sqrt(1-x^2)\qquad -1 \leq x \leq 1
$$

Find the value of $c$ that makes the $F$ a valid density function.

## Question 21

Consider a random variable $X$ with the following density function, with $c$ unknown:

$$
f(x) = c\sqrt(1-x^2)\qquad 0 \leq x \leq 1
$$

Find the value of $c$ that makes the $F$ a valid density function.

## Question 22

Consider a random variable $X$ with the following density function:

$$
f(x) = \frac{1}{2} sin(x) \qquad 0 \leq x \leq \pi
$$

The following python function generates draws from the distribution of X.

```
import numpy as np

def b_rvs(n):
    return np.arccos(-2*np.random.uniform(size=n) + 1)
```

This code will generate a histogram of 10,000 draws from the distribution.

```
x = b_rvs(10000)
import matplotlib.pyplot as plt
plt.hist(x, bins=100, density=True)
```

(a) Show that histogram matches the density by overlaying the a plot of the density function onto the histogram.

(b) Use the random draws to calculate $E[X]$.

(c) Use calculus to calculate $E[X]$.  

```
# HINT:
from sympy import *
x = symbols('x')
integrate(x*sin(x)/2,x)
```

(d) Compare your solutions from (b) and (c).  What was the simulation error?

(e) Use the random draws to calculate $V[X] = E[X^2] - E[X]^2$.

(f) Use calculus to calculate $V[X]$  (HINT: see hint from part (c))

(g) Use the random draws to calculate the mean absolute difference.

(h) Compare your calculation in (g) to the analytic solution provided by the following commands.  What was the simulation error?

```
from sympy import *
x = symbols('x')
integrate(abs(x-pi/2)*sin(x)/2,(x,0,pi))
```

(i) Use the random draws to calculate the IQR.

(j) Calculate the IQR analytically (using calculus/algebra.)

(k) Compare your solutions from (i) and (j).  What was the simulation error?

# Submission instructions
1. Create a PDF report with your answers.
2. Submit your report to GradeScope via [Canvas (link TBD)]().  You must identify each question in GradeScope to recieve credit.