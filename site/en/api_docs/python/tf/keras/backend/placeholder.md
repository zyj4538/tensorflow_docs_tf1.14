page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.backend.placeholder

Instantiates a placeholder tensor and returns it.

### Aliases:

* `tf.compat.v1.keras.backend.placeholder`
* `tf.compat.v2.keras.backend.placeholder`
* `tf.keras.backend.placeholder`

``` python
tf.keras.backend.placeholder(
    shape=None,
    ndim=None,
    dtype=None,
    sparse=False,
    name=None
)
```



Defined in [`python/keras/backend.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/backend.py).

<!-- Placeholder for "Used in" -->


#### Arguments:


* <b>`shape`</b>: Shape of the placeholder
    (integer tuple, may include `None` entries).
* <b>`ndim`</b>: Number of axes of the tensor.
    At least one of {`shape`, `ndim`} must be specified.
    If both are specified, `shape` is used.
* <b>`dtype`</b>: Placeholder type.
* <b>`sparse`</b>: Boolean, whether the placeholder should have a sparse type.
* <b>`name`</b>: Optional name string for the placeholder.


#### Raises:


* <b>`ValueError`</b>: If called with eager execution.


#### Returns:

Tensor instance (with Keras metadata included).



#### Examples:


```python
    >>> from keras import backend as K
    >>> input_ph = K.placeholder(shape=(2, 4, 5))
    >>> input_ph
    <tf.Tensor 'Placeholder_4:0' shape=(2, 4, 5) dtype=float32>
```