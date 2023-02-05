page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.convolutional_delta_orthogonal

## Class `convolutional_delta_orthogonal`

Initializer that generates a delta orthogonal kernel for ConvNets.

Inherits From: [`Initializer`](../../../tf/keras/initializers/Initializer)



Defined in [`python/ops/init_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/init_ops.py).

<!-- Placeholder for "Used in" -->

The shape of the tensor must have length 3, 4 or 5. The number of input
filters must not exceed the number of output filters. The center pixels of the
tensor form an orthogonal matrix. Other pixels are set to be zero. See
algorithm 2 in (Xiao et al., 2018).


#### Args:


* <b>`gain`</b>: Multiplicative factor to apply to the orthogonal matrix. Default is 1.
  The 2-norm of an input is multiplied by a factor of `gain` after applying
  this convolution.
* <b>`seed`</b>: A Python integer. Used to create random seeds. See
  <a href="../../../tf/random/set_random_seed"><code>tf.compat.v1.set_random_seed</code></a> for behavior.
* <b>`dtype`</b>: Default data type, used if no `dtype` argument is provided when
  calling the initializer. Only floating point types are supported.

#### References:

[Xiao et al., 2018](http://proceedings.mlr.press/v80/xiao18a.html)
([pdf](http://proceedings.mlr.press/v80/xiao18a/xiao18a.pdf))


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    gain=1.0,
    seed=None,
    dtype=tf.dtypes.float32
)
```






## Methods

<h3 id="__call__"><code>__call__</code></h3>

``` python
__call__(
    shape,
    dtype=None,
    partition_info=None
)
```




<h3 id="from_config"><code>from_config</code></h3>

``` python
from_config(
    cls,
    config
)
```

Instantiates an initializer from a configuration dictionary.


#### Example:



```python
initializer = RandomUniform(-1, 1)
config = initializer.get_config()
initializer = RandomUniform.from_config(config)
```

#### Args:


* <b>`config`</b>: A Python dictionary. It will typically be the output of
  `get_config`.


#### Returns:

An Initializer instance.


<h3 id="get_config"><code>get_config</code></h3>

``` python
get_config()
```






