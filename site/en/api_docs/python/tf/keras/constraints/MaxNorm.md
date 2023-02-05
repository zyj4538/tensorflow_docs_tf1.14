page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.constraints.MaxNorm

## Class `MaxNorm`

MaxNorm weight constraint.

Inherits From: [`Constraint`](../../../tf/keras/constraints/Constraint)

### Aliases:

* Class `tf.compat.v1.keras.constraints.MaxNorm`
* Class `tf.compat.v1.keras.constraints.max_norm`
* Class `tf.compat.v2.keras.constraints.MaxNorm`
* Class `tf.compat.v2.keras.constraints.max_norm`
* Class `tf.keras.constraints.MaxNorm`
* Class `tf.keras.constraints.max_norm`



Defined in [`python/keras/constraints.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/constraints.py).

<!-- Placeholder for "Used in" -->

Constrains the weights incident to each hidden unit
to have a norm less than or equal to a desired value.

#### Arguments:


* <b>`m`</b>: the maximum norm for the incoming weights.
* <b>`axis`</b>: integer, axis along which to calculate weight norms.
    For instance, in a `Dense` layer the weight matrix
    has shape `(input_dim, output_dim)`,
    set `axis` to `0` to constrain each weight vector
    of length `(input_dim,)`.
    In a `Conv2D` layer with `data_format="channels_last"`,
    the weight tensor has shape
    `(rows, cols, input_depth, output_depth)`,
    set `axis` to `[0, 1, 2]`
    to constrain the weights of each filter tensor of size
    `(rows, cols, input_depth)`.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    max_value=2,
    axis=0
)
```






## Methods

<h3 id="__call__"><code>__call__</code></h3>

``` python
__call__(w)
```




<h3 id="get_config"><code>get_config</code></h3>

``` python
get_config()
```






