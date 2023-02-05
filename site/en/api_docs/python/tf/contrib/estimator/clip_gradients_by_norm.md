page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.estimator.clip_gradients_by_norm

Returns an optimizer which clips gradients before applying them.

``` python
tf.contrib.estimator.clip_gradients_by_norm(
    optimizer,
    clip_norm
)
```



Defined in [`contrib/estimator/python/estimator/extenders.py`](https://github.com/tensorflow/estimator/tree/master/tensorflow_estimator/contrib/estimator/python/estimator/extenders.py).

<!-- Placeholder for "Used in" -->


#### Example:



```python
optimizer = tf.train.ProximalAdagradOptimizer(
    learning_rate=0.1,
    l1_regularization_strength=0.001)
optimizer = tf.contrib.estimator.clip_gradients_by_norm(
    optimizer, clip_norm)
estimator = tf.estimator.DNNClassifier(
    feature_columns=[...],
    hidden_units=[1024, 512, 256],
    optimizer=optimizer)
```

#### Args:


* <b>`optimizer`</b>: An `tf.Optimizer` object to apply gradients.
* <b>`clip_norm`</b>: A 0-D (scalar) `Tensor` > 0. The clipping ratio.


#### Returns:

A `tf.Optimizer`.
