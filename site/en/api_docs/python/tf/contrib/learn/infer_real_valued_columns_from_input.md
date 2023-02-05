page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.learn.infer_real_valued_columns_from_input

Creates `FeatureColumn` objects for inputs defined by input `x`. (deprecated)

``` python
tf.contrib.learn.infer_real_valued_columns_from_input(x)
```



Defined in [`contrib/learn/python/learn/estimators/estimator.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/learn/python/learn/estimators/estimator.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Please specify feature columns explicitly.

This interprets all inputs as dense, fixed-length float values.

#### Args:


* <b>`x`</b>: Real-valued matrix of shape [n_samples, n_features...]. Can be
   iterator that returns arrays of features.


#### Returns:

List of `FeatureColumn` objects.
