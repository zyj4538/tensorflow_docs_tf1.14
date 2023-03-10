page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.nn.l2_loss

L2 Loss.

### Aliases:

* `tf.compat.v1.nn.l2_loss`
* `tf.compat.v2.nn.l2_loss`
* `tf.nn.l2_loss`

``` python
tf.nn.l2_loss(
    t,
    name=None
)
```



Defined in generated file: `python/ops/gen_nn_ops.py`.

<!-- Placeholder for "Used in" -->

Computes half the L2 norm of a tensor without the `sqrt`:

    output = sum(t ** 2) / 2

#### Args:


* <b>`t`</b>: A `Tensor`. Must be one of the following types: `half`, `bfloat16`, `float32`, `float64`.
  Typically 2-D, but may have any dimensions.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `t`.
