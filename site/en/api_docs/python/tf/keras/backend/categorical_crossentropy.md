page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.backend.categorical_crossentropy

Categorical crossentropy between an output tensor and a target tensor.

### Aliases:

* `tf.compat.v1.keras.backend.categorical_crossentropy`
* `tf.compat.v2.keras.backend.categorical_crossentropy`
* `tf.keras.backend.categorical_crossentropy`

``` python
tf.keras.backend.categorical_crossentropy(
    target,
    output,
    from_logits=False,
    axis=-1
)
```



Defined in [`python/keras/backend.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/backend.py).

<!-- Placeholder for "Used in" -->


#### Arguments:


* <b>`target`</b>: A tensor of the same shape as `output`.
* <b>`output`</b>: A tensor resulting from a softmax
    (unless `from_logits` is True, in which
    case `output` is expected to be the logits).
* <b>`from_logits`</b>: Boolean, whether `output` is the
    result of a softmax, or is a tensor of logits.
* <b>`axis`</b>: Int specifying the channels axis. `axis=-1` corresponds to data
    format `channels_last', and `axis=1` corresponds to data format
    `channels_first`.


#### Returns:

Output tensor.



#### Raises:


* <b>`ValueError`</b>: if `axis` is neither -1 nor one of the axes of `output`.