page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.signal.overlap_and_add

Reconstructs a signal from a framed representation.

### Aliases:

* `tf.compat.v1.signal.overlap_and_add`
* `tf.compat.v2.signal.overlap_and_add`
* `tf.contrib.signal.overlap_and_add`
* `tf.signal.overlap_and_add`

``` python
tf.signal.overlap_and_add(
    signal,
    frame_step,
    name=None
)
```



Defined in [`python/ops/signal/reconstruction_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/signal/reconstruction_ops.py).

<!-- Placeholder for "Used in" -->

Adds potentially overlapping frames of a signal with shape
`[..., frames, frame_length]`, offsetting subsequent frames by `frame_step`.
The resulting tensor has shape `[..., output_size]` where

    output_size = (frames - 1) * frame_step + frame_length

#### Args:


* <b>`signal`</b>: A [..., frames, frame_length] `Tensor`. All dimensions may be
  unknown, and rank must be at least 2.
* <b>`frame_step`</b>: An integer or scalar `Tensor` denoting overlap offsets. Must be
  less than or equal to `frame_length`.
* <b>`name`</b>: An optional name for the operation.


#### Returns:

A `Tensor` with shape `[..., output_size]` containing the overlap-added
frames of `signal`'s inner-most two dimensions.



#### Raises:


* <b>`ValueError`</b>: If `signal`'s rank is less than 2, or `frame_step` is not a
  scalar integer.