# Python 

# Navigation

1.  [Earthquakes](#quakes)

    * [Data Exploration](#data-exploration)
    * [ACF](#acf)
    * [Relationship between x(t) and x(t-1)](#relationship-between-xt-and-xt-1)
    * [ACF of Residuals](#acf-of-residuals)

2.  [Cardiovascular Mortality Rate](#cmort)

    * [Data Exploration](#data-exploration-1)
    * [First Differences](#first-differences)
    * [ACF](#acf-1)
    * [Relationship between x(t) and x(t-1)](#relationship-between-xt-and-xt-1-1)
    * [ACF of Residuals](#acf-of-residuals-1)

# 


```python
import pandas as pd
import numpy as np

file_url = 'https://online.stat.psu.edu/stat510/sites/stat510/files/L01/quakes.dat'

x = pd.read_csv(file_url, delim_whitespace=True, header=None)
x = x.to_numpy().flatten()
x = x[~np.isnan(x)]
```
