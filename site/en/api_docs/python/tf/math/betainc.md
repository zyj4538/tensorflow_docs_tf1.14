page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>
<script src="/_static/js/managed/mathjax/MathJax.js?config=TeX-AMS-MML_SVG"></script>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.betainc

Compute the regularized incomplete beta integral \\(I_x(a, b)\\).

### Aliases:

* `tf.betainc`
* `tf.compat.v1.betainc`
* `tf.compat.v1.math.betainc`
* `tf.compat.v2.math.betainc`
* `tf.math.betainc`

``` python
tf.math.betainc(
    a,
    b,
    x,
    name=None
)
```



Defined in generated file: `python/ops/gen_math_ops.py`.

<!-- Placeholder for "Used in" -->

The regularized incomplete beta integral is defined as:


\\(I_x(a, b) = \frac{B(x; a, b)}{B(a, b)}\\)

where


\\(B(x; a, b) = \int_0^x t^{a-1} (1 - t)^{b-1} dt\\)


is the incomplete beta function and \\(B(a, b)\\) is the *complete*
beta function.

#### Args:


* <b>`a`</b>: A `Tensor`. Must be one of the following types: `float32`, `float64`.
* <b>`b`</b>: A `Tensor`. Must have the same type as `a`.
* <b>`x`</b>: A `Tensor`. Must have the same type as `a`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `a`.
