page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.backend.spatial_3d_padding

Pads 5D tensor with zeros along the depth, height, width dimensions.

### Aliases:

* `tf.compat.v1.keras.backend.spatial_3d_padding`
* `tf.compat.v2.keras.backend.spatial_3d_padding`
* `tf.keras.backend.spatial_3d_padding`

``` python
tf.keras.backend.spatial_3d_padding(
    x,
    padding=((1, 1), (1, 1), (1, 1)),
    data_format=None
)
```



Defined in [`python/keras/backend.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/backend.py).

<!-- Placeholder for "Used in" -->

Pads these dimensions with respectively
"padding[0]", "padding[1]" and "padding[2]" zeros left and right.

For 'channels_last' data_format,
the 2nd, 3rd and 4th dimension will be padded.
For 'channels_first' data_format,
the 3rd, 4th and 5th dimension will be padded.

#### Arguments:


* <b>`x`</b>: Tensor or variable.
* <b>`padding`</b>: Tuple of 3 tuples, padding pattern.
* <b>`data_format`</b>: One of `channels_last` or `channels_first`.


#### Returns:

A padded 5D tensor.



#### Raises:


* <b>`ValueError`</b>: if `data_format` is neither
    `channels_last` or `channels_first`.