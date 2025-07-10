---
layout: page
title: Halliday Physics Problem Solving
permalink: /projects/physics-halliday/
---

# Halliday Physics Problem Solving

## 📋 Project Description
This project includes programming solutions for selected problems from Halliday and Resnick's "Fundamentals of Physics" textbook.

## 🎯 Objectives
- Teaching physics through programming
- Implementing theoretical concepts in code
- Creating interactive educational resources

## 🛠️ Technologies Used
- **Python**: Main programming language
- **NumPy**: Numerical computations
- **Matplotlib**: Graph plotting
- **SciPy**: Complex equation solving

## 📊 Sample Code
```python
import numpy as np
import matplotlib.pyplot as plt

# Example: Projectile motion
def projectile_motion(v0, angle, g=9.81):
t_flight = 2 * v0 * np.sin(angle) / g
t = np.linspace(0, t_flight, 100)
x = v0 * np.cos(angle) * t
y = v0 * np.sin(angle) * t - 0.5 * g * t**2
return x, y

## 🔗 Useful Links
- [GitHub Repository](https://github.com/SMustafa12/Solve-Physics-I-of-Halliday)
- [NumPy Documentation](https://numpy.org/doc/)
- [Halliday Physics Textbook](https://www.wiley.com/en-us/Fundamentals+of+Physics)

## 📈 Results and Achievements
- Solved over 20 problems using numerical methods
- Created reusable library components
- Generated educational visualizations and graphs

[Back to Projects](../projects/)


**File: `projects/mathematical-methods.md`**
```markdown
---
layout: page
title: Mathematical Methods with Python
permalink: /projects/mathematical-methods/
---

# Mathematical Methods with Python

## 📋 Project Description
This project focuses on solving Question 27 from "Mathematical Methods using Python: Applications in Physics and Engineering" textbook, involving experimental data analysis of Maxwell-Boltzmann velocity distribution.

## 🎯 Objectives
- Analyze experimental molecular velocity data
- Implement Maxwell-Boltzmann distribution fitting
- Compare theoretical models with experimental results

## 🛠️ Technologies Used
- **Python**: Core programming language
- **SciPy**: Curve fitting and optimization
- **NumPy**: Mathematical operations
- **Matplotlib**: Data visualization

## 📊 Implementation Details
### Maxwell-Boltzmann Function
The project implements the Maxwell-Boltzmann distribution:
$$f(v) = a v^2 \exp(-b v^2)$$

### Key Features
- Curve fitting using `scipy.optimize.curve_fit`
- Statistical parameter estimation
- Visualization of fitted vs. experimental data
- Error analysis and goodness of fit metrics

## 🔬 Sample Code
```python
import numpy as np
from scipy.optimize import curve_fit
import matplotlib.pyplot as plt

def maxwell_boltzmann(v, a, b):
"""Maxwell-Boltzmann distribution function"""
return a * v**2 * np.exp(-b * v**2)

# Fitting experimental data
popt, pcov = curve_fit(maxwell_boltzmann, velocity_data, frequency_data)

## 📈 Results
- Successful fitting of Maxwell-Boltzmann distribution
- Accurate parameter estimation (a, b)
- High correlation coefficient between model and data
- Comprehensive statistical analysis

## 🔗 Links
- [GitHub Repository](https://github.com/SMustafa12/Q27_Mathematical-Metods-using-python-Application-in-Physics-and-Engineering)
- [SciPy Documentation](https://docs.scipy.org/)

[Back to Projects](../projects/)


**File: `projects/physics-problem-solving.md`**
```markdown
---
layout: page
title: Advanced Physics Problem Solving
permalink: /projects/physics-problem-solving/
---

# Advanced Physics Problem Solving

## 📋 Project Description
This project demonstrates multiple computational approaches to solving complex physics problems, specifically focusing on Question 7.40 from Halliday-Resnick Fundamentals of Physics.

## 🎯 Objectives
- Compare different numerical integration methods
- Implement analytical approximations
- Validate computational accuracy through multiple approaches

## 🛠️ Technologies Used
- **Python**: Main programming language
- **NumPy**: Numerical computations
- **SciPy**: Advanced mathematical functions
- **Matplotlib**: Result visualization

## 📊 Implementation Methods

### 1. Taylor Series Approximation
First-order analytical solution using Taylor expansion for quick approximation.

### 2. Numerical Integration
Python-based integration using built-in numerical methods for high precision.

### 3. Data Segmentation Analysis
Discrete analysis using 5000 data points for detailed computational study.

## 🔬 Sample Code
```python
import numpy as np
from scipy import integrate
import matplotlib.pyplot as plt

def integrand(x):
"""Define the integrand function"""
return np.exp(-x**2) * np.sin(x)

# Method 1: Taylor approximation
def taylor_approx(x, terms=5):
result = 0
for n in range(terms):
result += (-1)**n * x**(2*n+1) / np.math.factorial(2*n+1)
return result

# Method 2: Numerical integration
result_numerical, error = integrate.quad(integrand, 0, np.pi)

# Method 3: Discrete analysis
x_discrete = np.linspace(0, np.pi, 5000)
y_discrete = integrand(x_discrete)
result_discrete = np.trapz(y_discrete, x_discrete)

## 📈 Results and Comparison
- **Taylor Approximation**: Fast computation, moderate accuracy
- **Numerical Integration**: High precision, optimal for exact solutions
- **Discrete Analysis**: Detailed insight into function behavior
- **Validation**: All methods show consistent results within acceptable error margins

## 🔗 Links
- [GitHub Repository](https://github.com/SMustafa12/-Solution-Question-7.40-of-Fundamentals-of-Physics-Halliday-Resnick)
- [NumPy Integration Guide](https://numpy.org/doc/stable/reference/routines.math.html)

[Back to Projects](../projects/)


**File: `projects/data-analysis.md`**
```markdown
---
layout: page
title: Statistical Data Analysis
permalink: /projects/data-analysis/
---

# Statistical Data Analysis

## 📋 Project Description
Comprehensive statistical analysis framework for large datasets, featuring detailed analysis of 500 numerical data points using various statistical methods and transformations.

## 🎯 Objectives
- Implement complete statistical analysis pipeline
- Compare different statistical measures
- Analyze effects of linear transformations on data
- Create robust statistical visualization tools

## 🛠️ Technologies Used
- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Mathematical operations
- **Matplotlib**: Data visualization
- **SciPy**: Statistical functions

## 📊 Analysis Components

### Part 1: Original Data Analysis
- **Frequency Distribution**: Class interval analysis
- **Descriptive Statistics**: Mean and standard deviation for grouped data
- **Visualization**: Frequency histograms and cumulative frequency curves
- **Quartile Analysis**: Q1, Q2, Q3 determination and interquartile range
- **Robust Statistics**: 10% Trimmed mean and Winsorized mean calculations
- **Distribution Fitting**: Gaussian distribution parameter estimation

### Part 2: Linear Transformation Analysis
- **Transformation**: Applied linear transformation $y = 5 - 3x$
- **Comparative Analysis**: Statistical measures before and after transformation
- **Relationship Study**: Impact of linear transformation on data characteristics

## 🔬 Sample Code
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from scipy import stats

class StatisticalAnalyzer:
def __init__(self, data):
self.data = np.array(data)
self.n = len(data)
    
def descriptive_stats(self):
"""Calculate basic descriptive statistics"""
return {
'mean': np.mean(self.data),
'std': np.std(self.data),
'median': np.median(self.data),
'mode': stats.mode(self.data)[0][0]
}
    
def quartiles(self):
"""Calculate quartiles and IQR"""
q1 = np.percentile(self.data, 25)
q2 = np.percentile(self.data, 50)
q3 = np.percentile(self.data, 75)
iqr = q3 - q1
return q1, q2, q3, iqr
    
def robust_means(self, trim_percent=0.1):
"""Calculate trimmed and winsorized means"""
trimmed_mean = stats.trim_mean(self.data, trim_percent)
winsorized_data = stats.mstats.winsorize(self.data, limits=trim_percent/2)
winsorized_mean = np.mean(winsorized_data)
return trimmed_mean, winsorized_mean
    
def linear_transform(self, a=5, b=-3):
"""Apply linear transformation y = a + b*x"""
return a + b * self.data

## 📈 Key Findings
- **Data Distribution**: Comprehensive frequency analysis with clear visualization
- **Central Tendency**: Multiple measures providing robust statistical insight
- **Variability**: Standard deviation and IQR analysis
- **Transformation Effects**: Linear transformation preserves relative relationships
- **Robust Statistics**: Trimmed and Winsorized means reduce outlier influence

## 🔗 Links
- [GitHub Repository](https://github.com/SMustafa12/500-Data-analysis)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [SciPy Stats Guide](https://docs.scipy.org/doc/scipy/reference/stats.html)

[Back to Projects](../projects/)


These English versions maintain the same professional structure while providing comprehensive details about each project's methodology, implementation, and results.
