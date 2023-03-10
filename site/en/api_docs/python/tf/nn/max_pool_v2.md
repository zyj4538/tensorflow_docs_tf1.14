page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.nn.max_pool_v2

Performs the max pooling on the input.

### Aliases:

* `tf.compat.v1.nn.max_pool_v2`
* `tf.compat.v2.nn.max_pool`
* `tf.nn.max_pool_v2`

``` python
tf.nn.max_pool_v2(
    input,
    ksize,
    strides,
    padding,
    data_format=None,
    name=None
)
```



Defined in [`python/ops/nn_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/nn_ops.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`input`</b>:  Tensor of rank N+2, of shape `[batch_size] + input_spatial_shape +
  [num_channels]` if `data_format` does not start with "NC" (default), or
  `[batch_size, num_channels] + input_spatial_shape` if data_format starts
  with "NC". Pooling happens over the spatial dimensions only.
* <b>`ksize`</b>: An int or list of `ints` that has length `1`, `N` or `N+2`. The size
  of the window for each dimension of the input tensor.
* <b>`strides`</b>: An int or list of `ints` that has length `1`, `N` or `N+2`. The
  stride of the sliding window for each dimension of the input tensor.
* <b>`padding`</b>: A string, either `'VALID'` or `'SAME'`. The padding algorithm. See
  the "returns" section of <a href="../../tf/nn/convolution"><code>tf.nn.convolution</code></a> for details.
* <b>`data_format`</b>: A string. Specifies the channel dimension. For N=1 it can be
  either "NWC" (default) or "NCW", for N=2 it can be either "NHWC" (default)
  or "NCHW" and for N=3 either "NDHWC" (default) or "NCDHW".
* <b>`name`</b>: Optional name for the operation.


#### Returns:

A `Tensor` of format specified by `data_format`.
The max pooled output tensor.
