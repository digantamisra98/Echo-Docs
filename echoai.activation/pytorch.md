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
f(x)=x\tanh(softplus(x))
$$

#### Shape: <a id="mish-shape"></a>

* Input:$$(\mathbf{N}, \ast)$$where$$\ast$$means, any number of additional dimensions
* Output:$$(\mathbf{N}, \ast)$$,same shape as input

#### Reference: <a id="mish-reference"></a>

[Mish: A Self Regularized Non-Monotonic Activation Function](https://www.bmvc2020-conference.com/assets/papers/0928.pdf)

## Swish



