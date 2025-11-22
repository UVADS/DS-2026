# HW: Confounding and Intermediate Variables

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

# Submission instructions
1. Create a Quarto or Jupyter Notebook report with your answers.
2. Render your report to HTML then print to PDF.
2. Submit your PDF report to GradeScope via [Canvas (link)](https://canvas.its.virginia.edu/courses/153564/assignments/793415).  You must identify each question in GradeScope to recieve credit.