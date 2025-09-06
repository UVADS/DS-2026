# Create a report using Quarto

Previously, you wrote a simple report using a Jupyter notebook.  In this assignment, you will create a report using Quarto.  The starting point for the quarto report is below.  You'll see that the report already includes a script that generates a static figure and an interactive figure reporting the probability of a shared birthday for all class sizes.

Please complete the quarto report by:

1. Adding text to the `interactive plot` section, explaining a few ways in which the reader can interact with the plot (Before begin the assignment, you may want to render the report to HTML so that you can try out some of the interactive features.)
1. Tweaking the code so that the table reports percentages rather than probabilities
1. Adding code that will solve a slightly different version of the birthday problem: What is the probability that at least 3 individuals share a birthday in a class of 60?
1. Adding text which explains how your solution for this version of the birthday problem is different from the solution you provided in the previous homework.
1. Adding labels to all the code chunks  (See quarto documenation.)
1. Turn on code folding for the entire report (See quarto documenation.)
1. Adding your favorite equation.  If you don't have one, use $e^{i\pi}-1 = 0$.  (See [link](https://quarto.org/docs/visual-editor/technical.html#equations))
1. Insert a picture of your shoes taken in the UVADS classroom (See markdown documentation.)


## Submission instructions

1. Render your report as an HTML file.
2. Within your browser, print to PDF.
3. Submit the report to [Gradescope via Canvas (link)](https://canvas.its.virginia.edu/courses/153564/assignments/763128).

## Starting point

~~~

---
title: "Birthday problem, all class sizes"
format: html
---

```{python}
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
import plotly.express as px
from IPython.display import Markdown
from tabulate import tabulate
```

```{python}
R = 10000
out = [None] * R
for i in range(R):
    A = np.random.choice(range(1,366),366)
    B = pd.Series(A)
    C = B.duplicated("first")
    D = np.asarray(C).nonzero()
    out[i] = D[0][0] + 1

```

## Static plot

```{python}
sns.ecdfplot(out)
plt.xlabel("Class size")
plt.ylabel("Probability")
plt.title("Proability of shared birthday")
plt.margins(y=5)
plt.ylim(-0.05,1.05)
plt.axhline(y=0, color='lightgrey', linestyle='--', linewidth=1)
plt.axhline(y=1, color='lightgrey', linestyle='--', linewidth=1, alpha = 0.7)
plt.show()
```

## Interactive plot

```{python}
df = pd.DataFrame({'Class size': out})
fig = px.ecdf(df, x = "Class size")
fig.show()
```

## A table

```{python}
thresholds = list(range(10, 80, 10))

df = pd.DataFrame({
    'Class size': thresholds,
    'Shared birthday probability': [np.mean(np.array(out) < t) for t in thresholds]
})

Markdown(tabulate(df, showindex = False, headers = df.columns))
```

# At least 3 people share a birthday

For a class of size 60, what is the probability that at least 3 people share a birthday?

# My favorite math equation

# My shoes

~~~