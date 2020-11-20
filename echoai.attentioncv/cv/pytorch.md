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

![Triplet Attention](../../.gitbook/assets/triplet.png)

#### Parameters: <a id="triplet-parameters"></a>

* **no\_spatial** - switches on the spatial attention branch in Triplet Attention. Default: `False`
* **kernel\_size** - window size of the convolution filters in Triplet Attention. Default: 7

#### Shape: <a id="triplet-shape"></a>

* Input:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$4 dimensional feature map tensor.
* Output:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$,same shape as input

#### Reference: <a id="triplet-reference"></a>

[Rotate to Attend: Convolutional Triplet Attention Module](https://arxiv.org/abs/2010.03045)

## Squeeze Excite Attention

```python
echoAI.Attention.cv.t_attn.SE(gate_channels, reduction_ratio = 16)
```

![Squeeze Excite Attention](../../.gitbook/assets/electronics-08-00385-g001.png)

#### Parameters: <a id="se-parameters"></a>

* **gate\_channels** - number of channels in the input tensor. Datatype: `Integer`
* **reduction\_ratio** - squeeze bottleneck factor of the MLP in Squeeze Excite Attention. Default: 16

#### Shape: <a id="se-shape"></a>

* Input:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$4 dimensional feature map tensor.
* Output:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$,same shape as input

#### Reference: <a id="se-reference"></a>

[Squeeze-and-Excitation Networks](https://arxiv.org/abs/1709.01507)

## Convolutional Block Attention Module 

```python
echoAI.Attention.cv.t_attn.SE(gate_channels, reduction_ratio = 16)
```

 **Supports both Convolutional Block Attention Module \(CBAM\) and Bottleneck Attention Module \(CBAM\)**

![](../../.gitbook/assets/x1.png)

![Convolutional Block Attention Module and Bottleneck Attention Module](../../.gitbook/assets/5-figure2-1.png)

#### Parameters: <a id="se-parameters"></a>

* **gate\_channels** - number of channels in the input tensor. Datatype: `Integer`
* **reduction\_ratio** - squeeze bottleneck factor of the MLP in Squeeze Excite Attention. Default: 16

#### Shape: <a id="se-shape"></a>

* Input:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$4 dimensional feature map tensor.
* Output:$$(\mathbf{N}, \mathbf{C}, \mathbf{H}, \mathbf{W})$$,same shape as input

#### Reference: <a id="se-reference"></a>

[Squeeze-and-Excitation Networks](https://arxiv.org/abs/1709.01507)



