page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.data.experimental.get_single_element

Returns the single element in `dataset` as a nested structure of tensors.

### Aliases:

* `tf.compat.v1.data.experimental.get_single_element`
* `tf.compat.v2.data.experimental.get_single_element`
* `tf.data.experimental.get_single_element`

``` python
tf.data.experimental.get_single_element(dataset)
```



Defined in [`python/data/experimental/ops/get_single_element.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/data/experimental/ops/get_single_element.py).

<!-- Placeholder for "Used in" -->

This function enables you to use a <a href="../../../tf/data/Dataset"><code>tf.data.Dataset</code></a> in a stateless
"tensor-in tensor-out" expression, without creating a
<a href="../../../tf/data/Iterator"><code>tf.compat.v1.data.Iterator</code></a>.
This can be useful when your preprocessing transformations are expressed
as a `Dataset`, and you want to use the transformation at serving time.
For example:

```python
input_batch = tf.compat.v1.placeholder(tf.string, shape=[BATCH_SIZE])

def preprocessing_fn(input_str):
  # ...
  return image, label

dataset = (tf.data.Dataset.from_tensor_slices(input_batch)
           .map(preprocessing_fn, num_parallel_calls=BATCH_SIZE)
           .batch(BATCH_SIZE))

image_batch, label_batch = tf.data.experimental.get_single_element(dataset)
```

#### Args:


* <b>`dataset`</b>: A <a href="../../../tf/data/Dataset"><code>tf.data.Dataset</code></a> object containing a single element.


#### Returns:

A nested structure of <a href="../../../tf/Tensor"><code>tf.Tensor</code></a> objects, corresponding to the single
element of `dataset`.



#### Raises:


* <b>`TypeError`</b>: if `dataset` is not a <a href="../../../tf/data/Dataset"><code>tf.data.Dataset</code></a> object.
InvalidArgumentError (at runtime): if `dataset` does not contain exactly
  one element.