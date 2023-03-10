page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.losses.get_total_loss

Returns a tensor whose value represents the total loss.

### Aliases:

* `tf.compat.v1.losses.get_total_loss`
* `tf.losses.get_total_loss`

``` python
tf.losses.get_total_loss(
    add_regularization_losses=True,
    name='total_loss'
)
```



Defined in [`python/ops/losses/util.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/losses/util.py).

<!-- Placeholder for "Used in" -->

In particular, this adds any losses you have added with `tf.add_loss()` to
any regularization losses that have been added by regularization parameters
on layers constructors e.g. <a href="../../tf/layers"><code>tf.layers</code></a>. Be very sure to use this if you
are constructing a loss_op manually. Otherwise regularization arguments
on <a href="../../tf/layers"><code>tf.layers</code></a> methods will not function.

#### Args:


* <b>`add_regularization_losses`</b>: A boolean indicating whether or not to use the
  regularization losses in the sum.
* <b>`name`</b>: The name of the returned tensor.


#### Returns:

A `Tensor` whose value represents the total loss.



#### Raises:


* <b>`ValueError`</b>: if `losses` is not iterable.