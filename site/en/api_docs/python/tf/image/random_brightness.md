page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.image.random_brightness

Adjust the brightness of images by a random factor.

### Aliases:

* `tf.compat.v1.image.random_brightness`
* `tf.compat.v2.image.random_brightness`
* `tf.image.random_brightness`

``` python
tf.image.random_brightness(
    image,
    max_delta,
    seed=None
)
```



Defined in [`python/ops/image_ops_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/image_ops_impl.py).

<!-- Placeholder for "Used in" -->

Equivalent to `adjust_brightness()` using a `delta` randomly picked in the
interval `[-max_delta, max_delta)`.

#### Args:


* <b>`image`</b>: An image or images to adjust.
* <b>`max_delta`</b>: float, must be non-negative.
* <b>`seed`</b>: A Python integer. Used to create a random seed. See
  <a href="../../tf/random/set_random_seed"><code>tf.compat.v1.set_random_seed</code></a> for behavior.


#### Returns:

The brightness-adjusted image(s).



#### Raises:


* <b>`ValueError`</b>: if `max_delta` is negative.