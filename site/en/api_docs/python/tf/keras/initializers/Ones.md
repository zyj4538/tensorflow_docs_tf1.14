page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.initializers.Ones

## Class `Ones`

Inherits From: [`Initializer`](../../../tf/keras/initializers/Initializer)

### Aliases:

* Class `tf.initializers.ones`
* Class `tf.keras.initializers.Ones`
* Class `tf.keras.initializers.ones`
* Class `tf.ones_initializer`



Defined in [`tensorflow/python/ops/init_ops.py`](https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/python/ops/init_ops.py).

Initializer that generates tensors initialized to 1.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(dtype=tf.dtypes.float32)
```

Initialize self.  See help(type(self)) for accurate signature.



## Methods

<h3 id="__call__"><code>__call__</code></h3>

``` python
__call__(
    shape,
    dtype=None,
    partition_info=None
)
```

Returns a tensor object initialized as specified by the initializer.

#### Args:

* <b>`shape`</b>: Shape of the tensor.
* <b>`dtype`</b>: Optional dtype of the tensor. If not provided use the initializer
    dtype.
* <b>`partition_info`</b>: Optional information about the possible partitioning of a
    tensor.

<h3 id="from_config"><code>from_config</code></h3>

``` python
from_config(
    cls,
    config
)
```

Instantiates an initializer from a configuration dictionary.

Example:

```python
initializer = RandomUniform(-1, 1)
config = initializer.get_config()
initializer = RandomUniform.from_config(config)
```

#### Args:

* <b>`config`</b>: A Python dictionary.
    It will typically be the output of `get_config`.


#### Returns:

An Initializer instance.

<h3 id="get_config"><code>get_config</code></h3>

``` python
get_config()
```

Returns the configuration of the initializer as a JSON-serializable dict.

#### Returns:

A JSON-serializable Python dict.



