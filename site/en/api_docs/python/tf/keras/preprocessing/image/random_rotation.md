page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.preprocessing.image.random_rotation

Performs a random rotation of a Numpy image tensor.

### Aliases:

* `tf.compat.v1.keras.preprocessing.image.random_rotation`
* `tf.compat.v2.keras.preprocessing.image.random_rotation`
* `tf.keras.preprocessing.image.random_rotation`

``` python
tf.keras.preprocessing.image.random_rotation(
    x,
    rg,
    row_axis=1,
    col_axis=2,
    channel_axis=0,
    fill_mode='nearest',
    cval=0.0,
    interpolation_order=1
)
```

<!-- Placeholder for "Used in" -->

# Arguments
    x: Input tensor. Must be 3D.
    rg: Rotation range, in degrees.
    row_axis: Index of axis for rows in the input tensor.
    col_axis: Index of axis for columns in the input tensor.
    channel_axis: Index of axis for channels in the input tensor.
    fill_mode: Points outside the boundaries of the input
        are filled according to the given mode
        (one of `{'constant', 'nearest', 'reflect', 'wrap'}`).
    cval: Value used for points outside the boundaries
        of the input if `mode='constant'`.
    interpolation_order: int, order of spline interpolation.
        see `ndimage.interpolation.affine_transform`

# Returns
    Rotated Numpy image tensor.