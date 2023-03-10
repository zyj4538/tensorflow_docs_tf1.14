page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.layers.InputSpec

## Class `InputSpec`



### Aliases:

* Class `tf.keras.layers.InputSpec`
* Class `tf.layers.InputSpec`



Defined in [`tensorflow/python/keras/engine/input_spec.py`](https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/python/keras/engine/input_spec.py).

Specifies the ndim, dtype and shape of every input to a layer.

Every layer should expose (if appropriate) an `input_spec` attribute:
a list of instances of InputSpec (one per input tensor).

A None entry in a shape is compatible with any dimension,
a None shape is compatible with any shape.

#### Arguments:

* <b>`dtype`</b>: Expected DataType of the input.
* <b>`shape`</b>: Shape tuple, expected shape of the input
        (may include None for unchecked axes).
* <b>`ndim`</b>: Integer, expected rank of the input.
* <b>`max_ndim`</b>: Integer, maximum rank of the input.
* <b>`min_ndim`</b>: Integer, minimum rank of the input.
* <b>`axes`</b>: Dictionary mapping integer axes to
        a specific dimension value.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    dtype=None,
    shape=None,
    ndim=None,
    max_ndim=None,
    min_ndim=None,
    axes=None
)
```

Initialize self.  See help(type(self)) for accurate signature.



