page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.image.per_image_standardization

Linearly scales `image` to have zero mean and unit variance.

### Aliases:

* `tf.compat.v1.image.per_image_standardization`
* `tf.compat.v2.image.per_image_standardization`
* `tf.image.per_image_standardization`

``` python
tf.image.per_image_standardization(image)
```



Defined in [`python/ops/image_ops_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/image_ops_impl.py).

<!-- Placeholder for "Used in" -->

This op computes `(x - mean) / adjusted_stddev`, where `mean` is the average
of all values in image, and
`adjusted_stddev = max(stddev, 1.0/sqrt(image.NumElements()))`.

`stddev` is the standard deviation of all values in `image`. It is capped
away from zero to protect against division by 0 when handling uniform images.

#### Args:


* <b>`image`</b>: An n-D Tensor where the last 3 dimensions are `[height, width,
  channels]`.


#### Returns:

The standardized image with same shape as `image`.



#### Raises:


* <b>`ValueError`</b>: if the shape of 'image' is incompatible with this function.