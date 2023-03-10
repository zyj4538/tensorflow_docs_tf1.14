page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.wrappers.scikit_learn.KerasRegressor

## Class `KerasRegressor`

Implementation of the scikit-learn regressor API for Keras.



### Aliases:

* Class `tf.compat.v1.keras.wrappers.scikit_learn.KerasRegressor`
* Class `tf.compat.v2.keras.wrappers.scikit_learn.KerasRegressor`
* Class `tf.keras.wrappers.scikit_learn.KerasRegressor`



Defined in [`python/keras/wrappers/scikit_learn.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/wrappers/scikit_learn.py).

<!-- Placeholder for "Used in" -->
  

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    build_fn=None,
    **sk_params
)
```






## Methods

<h3 id="check_params"><code>check_params</code></h3>

``` python
check_params(params)
```

Checks for user typos in `params`.


#### Arguments:


* <b>`params`</b>: dictionary; the parameters to be checked


#### Raises:


* <b>`ValueError`</b>: if any member of `params` is not a valid argument.

<h3 id="filter_sk_params"><code>filter_sk_params</code></h3>

``` python
filter_sk_params(
    fn,
    override=None
)
```

Filters `sk_params` and returns those in `fn`'s arguments.


#### Arguments:


* <b>`fn`</b>: arbitrary function
* <b>`override`</b>: dictionary, values to override `sk_params`


#### Returns:


* <b>`res`</b>: dictionary containing variables
    in both `sk_params` and `fn`'s arguments.

<h3 id="fit"><code>fit</code></h3>

``` python
fit(
    x,
    y,
    **kwargs
)
```

Constructs a new model with `build_fn` & fit the model to `(x, y)`.


#### Arguments:


* <b>`x`</b>: array-like, shape `(n_samples, n_features)`
    Training samples where `n_samples` is the number of samples
    and `n_features` is the number of features.
* <b>`y`</b>: array-like, shape `(n_samples,)` or `(n_samples, n_outputs)`
    True labels for `x`.
* <b>`**kwargs`</b>: dictionary arguments
    Legal arguments are the arguments of <a href="../../../../tf/keras/Model#fit"><code>Sequential.fit</code></a>


#### Returns:


* <b>`history`</b>: object
    details about the training history at each epoch.

<h3 id="get_params"><code>get_params</code></h3>

``` python
get_params(**params)
```

Gets parameters for this estimator.


#### Arguments:


* <b>`**params`</b>: ignored (exists for API compatibility).


#### Returns:

Dictionary of parameter names mapped to their values.


<h3 id="predict"><code>predict</code></h3>

``` python
predict(
    x,
    **kwargs
)
```

Returns predictions for the given test data.


#### Arguments:


* <b>`x`</b>: array-like, shape `(n_samples, n_features)`
    Test samples where `n_samples` is the number of samples
    and `n_features` is the number of features.
* <b>`**kwargs`</b>: dictionary arguments
    Legal arguments are the arguments of <a href="../../../../tf/keras/Model#predict"><code>Sequential.predict</code></a>.


#### Returns:


* <b>`preds`</b>: array-like, shape `(n_samples,)`
    Predictions.

<h3 id="score"><code>score</code></h3>

``` python
score(
    x,
    y,
    **kwargs
)
```

Returns the mean loss on the given test data and labels.


#### Arguments:


* <b>`x`</b>: array-like, shape `(n_samples, n_features)`
    Test samples where `n_samples` is the number of samples
    and `n_features` is the number of features.
* <b>`y`</b>: array-like, shape `(n_samples,)`
    True labels for `x`.
* <b>`**kwargs`</b>: dictionary arguments
    Legal arguments are the arguments of <a href="../../../../tf/keras/Model#evaluate"><code>Sequential.evaluate</code></a>.


#### Returns:


* <b>`score`</b>: float
    Mean accuracy of predictions on `x` wrt. `y`.

<h3 id="set_params"><code>set_params</code></h3>

``` python
set_params(**params)
```

Sets the parameters of this estimator.


#### Arguments:


* <b>`**params`</b>: Dictionary of parameter names mapped to their values.


#### Returns:

self




