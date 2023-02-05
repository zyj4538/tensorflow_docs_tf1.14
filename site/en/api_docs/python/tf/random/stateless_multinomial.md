page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.random.stateless_multinomial

Draws deterministic pseudorandom samples from a multinomial distribution. (deprecated)

### Aliases:

* `tf.compat.v1.random.stateless_multinomial`
* `tf.contrib.stateless.stateless_multinomial`
* `tf.random.stateless_multinomial`

``` python
tf.random.stateless_multinomial(
    logits,
    num_samples,
    seed,
    output_dtype=tf.dtypes.int64,
    name=None
)
```



Defined in [`python/ops/stateless_random_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/stateless_random_ops.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Use <a href="../../tf/random/stateless_categorical"><code>tf.random.stateless_categorical</code></a> instead.

This is a stateless version of <a href="../../tf/random/categorical"><code>tf.random.categorical</code></a>: if run twice with the
same seeds, it will produce the same pseudorandom numbers.  The output is
consistent across multiple runs on the same hardware (and between CPU
and GPU), but may change between versions of TensorFlow or on non-CPU/GPU
hardware.

#### Example:



```python
# samples has shape [1, 5], where each value is either 0 or 1 with equal
# probability.
samples = tf.random.stateless_categorical(
    tf.math.log([[10., 10.]]), 5, seed=[7, 17])
```

#### Args:


* <b>`logits`</b>: 2-D Tensor with shape `[batch_size, num_classes]`.  Each slice
  `[i, :]` represents the unnormalized log-probabilities for all classes.
* <b>`num_samples`</b>: 0-D.  Number of independent samples to draw for each row slice.
* <b>`seed`</b>: A shape [2] integer Tensor of seeds to the random number generator.
* <b>`output_dtype`</b>: integer type to use for the output. Defaults to int64.
* <b>`name`</b>: Optional name for the operation.


#### Returns:

The drawn samples of shape `[batch_size, num_samples]`.
