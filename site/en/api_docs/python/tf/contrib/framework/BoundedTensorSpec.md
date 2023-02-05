page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.BoundedTensorSpec

## Class `BoundedTensorSpec`

A `TensorSpec` that specifies minimum and maximum values.

Inherits From: [`TensorSpec`](../../../tf/TensorSpec)



Defined in [`python/framework/tensor_spec.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/framework/tensor_spec.py).

<!-- Placeholder for "Used in" -->


#### Example usage:


```python
spec = tensor_spec.BoundedTensorSpec((1, 2, 3), tf.float32, 0, (5, 5, 5))
tf_minimum = tf.convert_to_tensor(spec.minimum, dtype=spec.dtype)
tf_maximum = tf.convert_to_tensor(spec.maximum, dtype=spec.dtype)
```

Bounds are meant to be inclusive. This is especially important for
integer types. The following spec will be satisfied by tensors
with values in the set {0, 1, 2}:

```python
spec = tensor_spec.BoundedTensorSpec((3, 5), tf.int32, 0, 2)
```

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    shape,
    dtype,
    minimum,
    maximum,
    name=None
)
```

Initializes a new `BoundedTensorSpec`.


#### Args:


* <b>`shape`</b>: Value convertible to <a href="../../../tf/TensorShape"><code>tf.TensorShape</code></a>. The shape of the tensor.
* <b>`dtype`</b>: Value convertible to <a href="../../../tf/dtypes/DType"><code>tf.DType</code></a>. The type of the tensor values.
* <b>`minimum`</b>: Number or sequence specifying the minimum element bounds
  (inclusive). Must be broadcastable to `shape`.
* <b>`maximum`</b>: Number or sequence specifying the maximum element bounds
  (inclusive). Must be broadcastable to `shape`.
* <b>`name`</b>: Optional string containing a semantic name for the corresponding
  array. Defaults to `None`.


#### Raises:


* <b>`ValueError`</b>: If `minimum` or `maximum` are not provided or not
  broadcastable to `shape`.
* <b>`TypeError`</b>: If the shape is not an iterable or if the `dtype` is an invalid
  numpy dtype.



## Properties

<h3 id="dtype"><code>dtype</code></h3>

Returns the `dtype` of elements in the tensor.


<h3 id="maximum"><code>maximum</code></h3>

Returns a NumPy array specifying the maximum bounds (inclusive).


<h3 id="minimum"><code>minimum</code></h3>

Returns a NumPy array specifying the minimum bounds (inclusive).


<h3 id="name"><code>name</code></h3>

Returns the (optionally provided) name of the described tensor.


<h3 id="shape"><code>shape</code></h3>

Returns the `TensorShape` that represents the shape of the tensor.




## Methods

<h3 id="__eq__"><code>__eq__</code></h3>

``` python
__eq__(other)
```




<h3 id="__ne__"><code>__ne__</code></h3>

``` python
__ne__(other)
```




<h3 id="from_spec"><code>from_spec</code></h3>

``` python
@classmethod
from_spec(
    cls,
    spec
)
```




<h3 id="from_tensor"><code>from_tensor</code></h3>

``` python
from_tensor(
    cls,
    tensor,
    name=None
)
```




<h3 id="is_compatible_with"><code>is_compatible_with</code></h3>

``` python
is_compatible_with(spec_or_tensor)
```

Returns True if spec_or_tensor is compatible with this TensorSpec.

Two tensors are considered compatible if they have the same dtype
and their shapes are compatible (see <a href="../../../tf/TensorShape#is_compatible_with"><code>tf.TensorShape.is_compatible_with</code></a>).

#### Args:


* <b>`spec_or_tensor`</b>: A tf.TensorSpec or a tf.Tensor


#### Returns:

True if spec_or_tensor is compatible with self.




