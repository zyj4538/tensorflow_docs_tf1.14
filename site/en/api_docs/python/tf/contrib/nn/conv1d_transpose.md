page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.nn.conv1d_transpose

``` python
tf.contrib.nn.conv1d_transpose(
    value,
    filter,
    output_shape,
    stride,
    padding='SAME',
    data_format='NWC',
    name=None
)
```



Defined in [`tensorflow/python/ops/nn_ops.py`](https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/python/ops/nn_ops.py).

The transpose of `conv1d`.

This operation is sometimes called "deconvolution" after [Deconvolutional
Networks](https://www.matthewzeiler.com/mattzeiler/deconvolutionalnetworks.pdf), but is
actually the transpose (gradient) of `conv1d` rather than an actual
deconvolution.

#### Args:

* <b>`value`</b>: A 3-D `Tensor` of type `float` and shape
    `[batch, in_width, in_channels]` for `NWC` data format or
    `[batch, in_channels, in_width]` for `NCW` data format.
* <b>`filter`</b>: A 3-D `Tensor` with the same type as `value` and shape
    `[filter_width, output_channels, in_channels]`.  `filter`'s
    `in_channels` dimension must match that of `value`.
* <b>`output_shape`</b>: A 1-D `Tensor` representing the output shape of the
    deconvolution op.
* <b>`stride`</b>: An `integer`.  The number of entries by which
    the filter is moved right at each step.
* <b>`padding`</b>: A string, either `'VALID'` or `'SAME'`. The padding algorithm.
    See the "returns" section of <a href="../../../tf/nn/convolution"><code>tf.nn.convolution</code></a> for details.
* <b>`data_format`</b>: A string. 'NHWC' and 'NCHW' are supported.
* <b>`name`</b>: Optional name for the returned tensor.


#### Returns:

A `Tensor` with the same type as `value`.


#### Raises:

* <b>`ValueError`</b>: If input/output depth does not match `filter`'s shape, or if
    padding is other than `'VALID'` or `'SAME'`.