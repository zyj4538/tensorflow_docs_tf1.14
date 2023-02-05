page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.nn.relu_layer

Computes Relu(x * weight + biases).

### Aliases:

* `tf.compat.v1.nn.relu_layer`
* `tf.nn.relu_layer`

``` python
tf.nn.relu_layer(
    x,
    weights,
    biases,
    name=None
)
```



Defined in [`python/ops/nn_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/nn_impl.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`x`</b>: a 2D tensor.  Dimensions typically: batch, in_units
* <b>`weights`</b>: a 2D tensor.  Dimensions typically: in_units, out_units
* <b>`biases`</b>: a 1D tensor.  Dimensions: out_units
* <b>`name`</b>: A name for the operation (optional).  If not specified
  "nn_relu_layer" is used.


#### Returns:

A 2-D Tensor computing relu(matmul(x, weights) + biases).
Dimensions typically: batch, out_units.
