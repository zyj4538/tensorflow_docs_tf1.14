page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.image.compose_transforms

Composes the transforms tensors.

``` python
tf.contrib.image.compose_transforms(*transforms)
```



Defined in [`contrib/image/python/ops/image_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/image/python/ops/image_ops.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`*transforms`</b>: List of image projective transforms to be composed. Each
    transform is length 8 (single transform) or shape (N, 8) (batched
    transforms). The shapes of all inputs must be equal, and at least one
    input must be given.


#### Returns:

A composed transform tensor. When passed to <a href="../../../tf/contrib/image/transform"><code>tf.contrib.image.transform</code></a>,
    equivalent to applying each of the given transforms to the image in
    order.
