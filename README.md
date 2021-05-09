# Regression_Line_Fitting
---
tags: Academic
---

# CVLab 2021 Winter Project 

###### Dead line: 2021/02/10

## Problem A: Line Fitting

Download two csv files `pA1.csv` and `pA2.csv` using:

```
wget -nc 140.114.76.206:8000/pA1.csv
wget -nc 140.114.76.206:8000/pA2.csv
```

You are asked to find the curve that fits the data using Stochastic Gradient Descent with a deep learning framework (PyTorch, Keras, etc). A1, A2 should be written in one Colab Notebook.

![](https://i.imgur.com/5Dff6V7.png)
Left is `pA1.csv` and right is `pA2.csv`.


Assume that the curve is $y = f(x;a, b) = ax + b$. You are asked to find the $a, b$ that makes the curve best fit the data `pA1.csv`. Requirements:

1. A PyTorch code that outputs $a$ and $b$. You get the points only if predicted $a, b$ and ground truth $\hat a, \hat b$ satisfies $|\hat a - a| \le 0.2$ and $|\hat b - b| \le 0.2$.
2. A 3D figure that visualizes the loss function (of whole dataset) against parameters space. The figure may differ with different setting.
    ![](https://i.imgur.com/rf7qszq.png =400x)

There's a sample code [here](https://colab.research.google.com/drive/1sd3PLMaFj7R5hTnJocUyBuRUfZju1C6x?usp=sharing). Feel free to modify it. Hyperparameters(loss function, optimizer, batch size, epoch, ...) are not restricted to the one used in sample code.

### A2

You are asked to fit the data `pA2.csv` using following model:

$$
y = f(x; \mathbf{w}) = w_0 x^2 + w_1 x + w_2
$$

where $\mathbf{w}$ are parameters.

Your code outputs $w_0, w_1, w_2$. Similar to problem A1, you get the points only if predicted $\mathbf{w}$ and ground truth $\mathbf{\hat w}$ satisfies $|w_0 - \hat w_0| < 0.2$, $|w_1 - \hat w_1| < 0.2$ and $|w_2 - \hat w_2| < 0.2$. Requirements:

1. Use `nn.Linear`(PyTorch) / `Dense`(Keras or Tensorflow) to accomplish the task.
2. A plot of loss against iteration or epoch.
    ![](https://i.imgur.com/M8SCTtT.png =400x)
    
    
## Report

Describe the methods you have tried in this project. The report should be written in Jupyter Notebooks using Markdown cells for each problem.
