page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>
<script src="/_static/js/managed/mathjax/MathJax.js?config=TeX-AMS-MML_SVG"></script>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.rsqrt

Computes reciprocal of square root of x element-wise.

### Aliases:

* `tf.compat.v1.math.rsqrt`
* `tf.compat.v1.rsqrt`
* `tf.compat.v2.math.rsqrt`
* `tf.math.rsqrt`
* `tf.rsqrt`

``` python
tf.math.rsqrt(
    x,
    name=None
)
```



Defined in generated file: `python/ops/gen_math_ops.py`.

<!-- Placeholder for "Used in" -->

I.e., \\(y = 1 / \sqrt{x}\\).

#### Args:


* <b>`x`</b>: A `Tensor`. Must be one of the following types: `bfloat16`, `half`, `float32`, `float64`, `complex64`, `complex128`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `x`.
