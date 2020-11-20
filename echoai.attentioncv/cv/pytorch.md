---
description: >-
  This page contains the list of all attention models and non-local layers for
  computer vision enabled with PyTorch backend available in Echo.
---

# PyTorch

## Triplet Attention

```python
echoAI.Attention.cv.t_attn.TripletAttention(no_spatial = False, kernel_size = 7)
```

####   <a id="triplet-shape"></a>

![Triplet Attention](../../.gitbook/assets/triplet.png)

#### Parameters: <a id="triplet-shape"></a>

* **no\_spatial** - switches on the spatial attention branch in Triplet Attention. Default: `False`
* **kernel\_size** - window size of the convolution filters in Triplet Attention. Default: 7

#### Shape: <a id="triplet-shape"></a>

* Input:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$4 dimensional feature map tensor.
* Output:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$,same shape as input

#### Reference: <a id="triplet-reference"></a>

[Rotate to Attend: Convolutional Triplet Attention Module](https://arxiv.org/abs/2010.03045)



