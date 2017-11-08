# Producing Bland-Altman plots in Python
Requires [matplotlib](https://github.com/matplotlib/matplotlib) (2.1.0) and [numpy](https://www.scipy.org/scipylib/download.html) (1.12.1).

## Introduction

From the [Wikipedia article](https://en.wikipedia.org/wiki/Bland%E2%80%93Altman_plot):
_A Bland–Altman plot ... is a method of data plotting used in analyzing the agreement between two different assays._

[Bland and Altman et al.](https://www-users.york.ac.uk/~mb55/meas/ba.pdf) has been cited over 20,000 times.

## Usage

- Place `bland_altman.py` in your working directory.
- To load the function into your Python script or Jupyter notebook, run
  ```python
  from .bland_altman import bland_altman_plot
  ```

## Example
```python
from .bland_altman import bland_altman_plot
import numpy as np

# Seed the random number generator.
# This ensures that the results below are reproducible.
np.random.seed(9999)
m1 = np.random.random(20)
m2 = np.random.random(20)

my_bland_altman_plot = bland_altman_plot(m1, m2)
```

This should produce the following image.

![A Bland-Altman plot](https://github.com/josesho/bland_altman/raw/master/bland-altman-plot.png)
