page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.image.angles_to_projective_transforms

Returns projective transform(s) for the given angle(s).

``` python
tf.contrib.image.angles_to_projective_transforms(
    angles,
    image_height,
    image_width,
    name=None
)
```



Defined in [`contrib/image/python/ops/image_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/image/python/ops/image_ops.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`angles`</b>: A scalar angle to rotate all images by, or (for batches of images)
    a vector with an angle to rotate each image in the batch. The rank must
    be statically known (the shape is not `TensorShape(None)`.
* <b>`image_height`</b>: Height of the image(s) to be transformed.
* <b>`image_width`</b>: Width of the image(s) to be transformed.


#### Returns:

A tensor of shape (num_images, 8). Projective transforms which can be given
  to <a href="../../../tf/contrib/image/transform"><code>tf.contrib.image.transform</code></a>.
