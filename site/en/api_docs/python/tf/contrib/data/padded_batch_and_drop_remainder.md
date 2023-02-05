page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.data.padded_batch_and_drop_remainder

A batching and padding transformation that omits the final small batch. (deprecated)

``` python
tf.contrib.data.padded_batch_and_drop_remainder(
    batch_size,
    padded_shapes,
    padding_values=None
)
```



Defined in [`contrib/data/python/ops/batching.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/data/python/ops/batching.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Use <a href="../../../tf/data/Dataset#padded_batch"><code>tf.data.Dataset.padded_batch(..., drop_remainder=True)</code></a>.

Like <a href="../../../tf/data/Dataset#padded_batch"><code>tf.data.Dataset.padded_batch</code></a>, this transformation combines
consecutive elements of this dataset into batches. However, if the batch
size does not evenly divide the input dataset size, this transformation will
drop the final smaller element.

See <a href="../../../tf/contrib/data/batch_and_drop_remainder"><code>tf.contrib.data.batch_and_drop_remainder</code></a> for more details.

#### Args:


* <b>`batch_size`</b>: A <a href="../../../tf#int64"><code>tf.int64</code></a> scalar <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>, representing the number of
  consecutive elements of this dataset to combine in a single batch.
* <b>`padded_shapes`</b>: A nested structure of <a href="../../../tf/TensorShape"><code>tf.TensorShape</code></a> or <a href="../../../tf#int64"><code>tf.int64</code></a> vector
  tensor-like objects. See <a href="../../../tf/data/Dataset#padded_batch"><code>tf.data.Dataset.padded_batch</code></a> for details.
* <b>`padding_values`</b>: (Optional.) A nested structure of scalar-shaped <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>.
  See <a href="../../../tf/data/Dataset#padded_batch"><code>tf.data.Dataset.padded_batch</code></a> for details.


#### Returns:

A `Dataset` transformation function, which can be passed to
<a href="../../../tf/data/Dataset#apply"><code>tf.data.Dataset.apply</code></a>
