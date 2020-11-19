---
description: >-
  This page contains details of all activation functions for MegEngine backend
  supported in Echo.
---

# MegEngine

## Mish

```python
echoAI.Activation.m_ops.Mish()
```

Applies the element-wise function:

$$
\textbf{Mish}(x)=x\tanh(\text{softplus}(x))
$$

#### Shape: <a id="mish-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="mish-reference"></a>

[Mish: A Self Regularized Non-Monotonic Activation Function](https://www.bmvc2020-conference.com/assets/papers/0928.pdf)

## Swish

```python
echoAI.Activation.m_ops.Swish(eswish = False, swish = True, beta = 1.735, flatten = False)
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

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### References: <a id="swish-reference"></a>

[Searching for Activation Functions](https://arxiv.org/abs/1710.05941)

[E-swish: Adjusting Activations to Different Network Depths](https://arxiv.org/abs/1801.07145)

[Flatten-T Swish: a thresholded ReLU-Swish-like activation function for deep learning](https://arxiv.org/abs/1812.06247)

[Sigmoid-Weighted Linear Units for Neural Network Function Approximation in Reinforcement Learning](https://arxiv.org/abs/1702.03118)

## Aria2

```python
echoAI.Activation.m_ops.Aria2(beta = 0.5, alpha = 1.0)
```

Applies the element-wise function:

$$
\textbf{Aria2}(x)= {(1+e^{-\beta \ast x})}^{-\alpha}
$$

#### Parameters: <a id="aria-parameters"></a>

* **beta** -$$\beta$$is the exponential growth rate. Default: 0.5
* **alpha** -$$\alpha$$is a hyper-parameter which has a two-fold effect; it reduces the curvature in 3rd quadrant as well as increases the curvature in first quadrant while lowering the value of activation. Default: 1.0

#### Shape: <a id="aria-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="aria-reference"></a>

[ARiA: Utilizing Richard's Curve for Controlling the Non-monotonicity of the Activation Function in Deep Neural Nets](https://arxiv.org/abs/1805.08878)

## ELiSH

```python
echoAI.Activation.m_ops.Elish(hard = False)
```

Allows the following element-wise functions:

$$
\textbf{ELiSH}(x)= \begin{cases}
    x\text{sigmoid}(x) & \text{if } x \geq 0\\
    (e^{x}-1)\text{sigmoid}(x) & \text{otherwise}
\end{cases}
$$

$$
\textbf{Hard ELiSH}(x)= \begin{cases}
    x\max(0, \min(1,(x+1)/2)) & \text{if } x \geq 0\\
    (e^{x}-1)\max(0, \min(1,(x+1)/2)) & \text{otherwise}
\end{cases}
$$

#### Parameter: <a id="elish-parameters"></a>

* **hard** - ****Uses Hard ELiSH activation function. Default: `False`

#### Shape: <a id="elish-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="elish-references"></a>

[The Quest for the Golden Activation Function](https://arxiv.org/abs/1808.00783)

## ISRU

```python
echoAI.Activation.m_ops.ISRU(alpha = 1.0, isrlu = False)
```

Allows the following element-wise functions:

$$
\textbf{ISRU}(x)= \frac{x}{\sqrt{1+\alpha x^{2}}}
$$

$$
\textbf{ISRLU}(x)= \begin{cases}
    x & \text{if } x \geq 0\\
    \frac{x}{\sqrt{1+\alpha x^{2}}} & \text{otherwise}
\end{cases}
$$

#### Parameters: <a id="isru-parameters"></a>

* **alpha** - ****hyperparameter$$\alpha$$controls the value to which an ISRLU saturates for negative inputs. Default: 1.0
* **isrlu** - Uses ISRLU activation function. Default: `False`

#### Shape: <a id="isru-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="isru-references"></a>

[Improving Deep Learning by Inverse Square Root Linear Units \(ISRLUs\)](https://arxiv.org/abs/1710.09967)

## NLReLU

```python
echoAI.Activation.m_ops.NLReLU(beta = 1.0)
```

Applies the element-wise function:

$$
\textbf{NLReLU}(x)= \ln(\beta\max(0,x)+1.0)
$$

#### Parameters: <a id="nlrelu-shape"></a>

* **beta** - $$\beta$$parameter used for NLReLU formulation. Default: 1.0

#### Shape: <a id="nlrelu-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="nlrelu-reference"></a>

[Natural-Logarithm-Rectified Activation Function in Convolutional Neural Networks](https://arxiv.org/abs/1908.03682)

## Soft Clipping

```python
echoAI.Activation.m_ops.SoftClipping(alpha = 0.5)
```

Applies the element-wise function:

$$
\textbf{Soft Clipping}(x)= \frac{1}{\alpha}\log{\big(\frac{1+e^{\alpha x}}{1+e^{\alpha (x-1)}}\big)}
$$

#### Parameters: <a id="softclipping-parameters"></a>

* **alpha** -$$\alpha$$hyper-parameter, which determines how close to linear the central region is and how sharply the linear region turns to the asymptotic values. Default: 0.5

#### Shape: <a id="softclipping-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="softclipping-reference"></a>

[Neural Network-Based Approach to Phase Space Integration](https://arxiv.org/abs/1810.11509)

## Soft Exponential

```python
echoAI.Activation.m_ops.SoftExponential(alpha = None)
```

Applies the element-wise function:

$$
\textbf{Soft Exponential}(x)= \begin{cases}
    \frac{-\log{(1+\alpha(x + \alpha))}}{\alpha} & \text{if } \alpha < 0\\
     x & \text{if } \alpha = 0\\
    \frac{e^{\alpha x}-1}{\alpha} & \text{if } \alpha > 0
\end{cases}
$$

#### Parameters: <a id="softexponential-parameters"></a>

* **alpha** -$$\alpha$$trainable hyper-parameter which is initialized to zero by default. Default: `None`

#### Shape: <a id="softexponential-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="softexponential-reference"></a>

[A continuum among logarithmic, linear, and exponential functions, and its potential to improve generalization in neural networks](https://arxiv.org/abs/1602.01321)

## SQNL

```python
echoAI.Activation.m_ops.SQNL()
```

Applies the element-wise function:

$$
\textbf{SQNL}(x)= \begin{cases}
    1 & \text{if } x > 2\\
     x - \frac{x^2}{4} & \text{if } 0 \leq x \leq 2\\
     x + \frac{x^2}{4} & \text{if } -2 \leq x < 0\\
    -1 & \text{if } x < -2
\end{cases}
$$

#### Shape: <a id="sqnl-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="sqnl-reference"></a>

[SQNL: A New Computationally Efficient Activation Function](https://ieeexplore.ieee.org/document/8489043)

## SReLU

```python
echoAI.Activation.m_ops.SReLU(in_features, parameters = None)
```

Applies the element-wise function:

$$
\textbf{SReLU}(x_{i})= \begin{cases}
    t_i^r + a_i^r(x_i - t_i^r) & \text{if } x_i \geq t_i^r\\
     x_i & \text{if } t_i^r > x_i > t_i^l\\
     t_i^l + a_i^l(x_i - t_i^l) & x_i \leq  t_i^l 
\end{cases}
$$

#### Parameters: <a id="srelu-parameters"></a>

* **in\_features** - Shape of the input. Datatype: `Tuple`
* **parameters** - \( $$t^r,t^l,a^r,a^l$$ \) parameters for manual initialization, Default: `None`. If `None` is passed, parameters are initialized randomly.

#### Shape: <a id="srelu-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$, same shape as input

#### Reference: <a id="srelu-reference"></a>

[Deep Learning with S-shaped Rectified Linear Activation Units](https://arxiv.org/abs/1512.07030)

## FReLU

```python
echoAI.Activation.m_ops.FReLU(in_channels)
```

Applies the element-wise function:

$$
\textbf{FReLU}(x)= \max(x,\mathbb{T}(x))
$$

#### Parameter: <a id="frelu-parameter"></a>

* **in\_channels** - Number of channels in the input tensor. Datatype: `Integer`

#### Shape: <a id="frelu-shape"></a>

* Input:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$where$$\mathbf{C}$$indicates the number of channels.
* Output:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$, same shape as input

#### Reference: <a id="frelu-reference"></a>

[Funnel Activation for Visual Recognition](https://arxiv.org/abs/2007.11824)

