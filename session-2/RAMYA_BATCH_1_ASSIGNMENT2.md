Ramya Ragupathy|Batch 1

## Assignment 2A:

[Github link](https://github.com/ramyaragupathy/mlblr-eip/blob/master/session-2/CS231n-python-numpy-tutorial.ipynb)

## Assignment 2B:

**Step 0**: Read input and output

```python
import numpy as np
X = np.array([[1,0,1,0],[1,0,1,1],[0,1,0,1]])
y = ([[1],[1],[0]])
```

**Step 1**: Initialize weights and biases with random values 

```python
wh = np.random.randn(4,3)
bh = np.random.rand(1,3)
```

**Step 2**: Calculate hidden layer input

```python
hidden_layer_input = np.dot(X,wh) + bh
```

**Step 3**: Perform non-linear transformation on hidden linear input

```python
def sigmoid(X):
    return (1 / (1 + np.exp(- X)))
hiddenlayer_activations = sigmoid(hidden_layer_input)
```

**Step 4**: Perform linear and non-linear transformation of hidden layer activation at output layer


```python
output_layer_input = np.dot(hiddenlayer_activations, wout )
output = sigmoid(output_layer_input)
```


**Step 5**: Calculate gradient of Error(E) at output layer

```python
E = y-output
```


**Step 6**: Compute slope at output and hidden layer


```python
def dsigmoid(y):
    return y * (1.0 - y) 
Slope_output_layer= dsigmoid(output)
Slope_hidden_layer = dsigmoid(hiddenlayer_activations)
```

**Step 7**: Compute delta at output layer


```python
lr = 1
d_output = E * Slope_output_layer * lr
```

**Step 8**: Calculate Error at hidden layer

```python
Error_at_hidden_layer = np.dot(d_output, np.transpose(wout))
```


**Step 9**: Compute delta at hidden layer

```python
d_hiddenlayer = Error_at_hidden_layer * Slope_hidden_layer
```


**Step 10**: Update weight at both output and hidden layer

```python
wout = wout + np.dot(np.transpose(hiddenlayer_activations), d_output) * lr
wh = wh + np.dot(np.transpose(X),d_hiddenlayer) * lr
```

**Step 11**: Update biases at both output and hidden layer

```python
bh = bh + np.sum(d_hiddenlayer, axis=0) * lr
bout = bout + np.sum(d_output, axis=0) * lr
```
