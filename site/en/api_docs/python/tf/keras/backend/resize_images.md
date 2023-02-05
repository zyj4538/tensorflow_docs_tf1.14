page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.backend.resize_images

Resizes the images contained in a 4D tensor.

### Aliases:

* `tf.compat.v1.keras.backend.resize_images`
* `tf.compat.v2.keras.backend.resize_images`
* `tf.keras.backend.resize_images`

``` python
tf.keras.backend.resize_images(
    x,
    height_factor,
    width_factor,
    data_format,
    interpolation='nearest'
)
```



Defined in [`python/keras/backend.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/backend.py).

<!-- Placeholder for "Used in" -->


#### Arguments:


* <b>`x`</b>: Tensor or variable to resize.
* <b>`height_factor`</b>: Positive integer.
* <b>`width_factor`</b>: Positive integer.
* <b>`data_format`</b>: One of `"channels_first"`, `"channels_last"`.
* <b>`interpolation`</b>: A string, one of `nearest` or `bilinear`.


#### Returns:

A tensor.



#### Raises:


* <b>`ValueError`</b>: in case of incorrect value for
  `data_format` or `interpolation`.