---
description: >-
  This page contains details of all activation functions for PyTorch backend
  supported in Echo.
---

# PyTorch

## Mish

```python
echoAI.Activation.t_ops.Mish()
```

Applies the element-wise function:

$$
\textbf{Mish}(x)=x\tanh(\text{softplus}(x))
$$

#### Shape: <a id="mish-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means, any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$,same shape as input

#### Reference: <a id="mish-reference"></a>

[Mish: A Self Regularized Non-Monotonic Activation Function](https://www.bmvc2020-conference.com/assets/papers/0928.pdf)

## Swish

```python
echoAI.Activation.t_ops.Swish(eswish = False, swish = True, beta = 1.735, flatten = False)
```

Allows the following element-wise functions:

$$
\textbf{Swish}(x)=x\text{sigmoid}(\beta_{1} x)
$$

$$
\textbf{ESwish}(x)=\beta x\text{sigmoid}(x)
$$

$$
\textbf{SILU}(x)=x\text{sigmoid}(x)
$$

$$
\textbf{Flatten T-Swish}(x)= \begin{cases}
    x\text{sigmoid}(x) & \text{if } x\geq 0\\
    0              & \text{otherwise}
\end{cases}
$$

#### Parameters: <a id="swish-parameters"></a>

* **eswish** - Uses E-Swish activation function. Default: `False`.
* **swish** - Uses Swish activation function. Default: `False`.
* **flatten** - Uses Flatten T-Swish activation function. Default: `False`.
* **beta** - $$\beta$$parameter used for E-Swish formulation. Default: 1.375

{% hint style="info" %}
Note: When **eswish**, **swish** and **flatten** are `False`, it initializes the _SILU_ activation function by default.
{% endhint %}

#### Shape: <a id="swish-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means, any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$,same shape as input

#### References: <a id="swish-reference"></a>

[Searching for Activation Functions](https://arxiv.org/abs/1710.05941)

[E-swish: Adjusting Activations to Different Network Depths](https://arxiv.org/abs/1801.07145)

[Flatten-T Swish: a thresholded ReLU-Swish-like activation function for deep learning](https://arxiv.org/abs/1812.06247)

[Sigmoid-Weighted Linear Units for Neural Network Function Approximation in Reinforcement Learning](https://arxiv.org/abs/1702.03118)

## Aria2

```python
echoAI.Activation.t_ops.Aria2(beta = 0.5, alpha = 1.0)
```

Applies the element-wise function:

$$
\textbf{Aria2}(x)= {(1+e^{-\beta \ast x})}^{-\alpha}
$$

#### Parameters: <a id="aria-parameters"></a>

* **beta** -$$\beta$$is the exponential growth rate. Default: 0.5
* **alpha** -$$\alpha$$is a hyper-parameter which has a two-fold effect; it reduces the curvature in 3rd quadrant as well as increases the curvature in first quadrant while lowering the value of activation. Default: 1.0

#### Shape: <a id="aria-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means, any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$,same shape as input

#### Reference: <a id="aria-reference"></a>

[ARiA: Utilizing Richard's Curve for Controlling the Non-monotonicity of the Activation Function in Deep Neural Nets](https://arxiv.org/abs/1805.08878)

####   <a id="aria-reference"></a>

