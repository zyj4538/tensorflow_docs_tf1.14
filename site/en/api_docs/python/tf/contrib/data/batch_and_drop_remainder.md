page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.data.batch_and_drop_remainder

A batching transformation that omits the final small batch (if present). (deprecated)

``` python
tf.contrib.data.batch_and_drop_remainder(batch_size)
```



Defined in [`contrib/data/python/ops/batching.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/data/python/ops/batching.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Use <a href="../../../tf/data/Dataset#batch"><code>tf.data.Dataset.batch(..., drop_remainder=True)</code></a>.

Like <a href="../../../tf/data/Dataset#batch"><code>tf.data.Dataset.batch</code></a>, this transformation combines
consecutive elements of this dataset into batches. However, if the batch
size does not evenly divide the input dataset size, this transformation will
drop the final smaller element.

The following example illustrates the difference between this
transformation and `Dataset.batch()`:

```python
dataset = tf.data.Dataset.range(200)
batched =
dataset.apply(tf.contrib.data.batch_and_drop_remainder(128))
print(batched.output_shapes)  # ==> "(128,)" (the batch dimension is known)
```

By contrast, `dataset.batch(128)` would yield a two-element dataset with
shapes `(128,)` and `(72,)`, so the batch dimension would not be statically
known.

#### Args:


* <b>`batch_size`</b>: A <a href="../../../tf#int64"><code>tf.int64</code></a> scalar <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>, representing the number of
  consecutive elements of this dataset to combine in a single batch.


#### Returns:

A `Dataset` transformation function, which can be passed to
<a href="../../../tf/data/Dataset#apply"><code>tf.data.Dataset.apply</code></a>
