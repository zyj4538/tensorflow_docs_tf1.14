page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.learn.NotFittedError

## Class `NotFittedError`

Exception class to raise if estimator is used before fitting.





Defined in [`contrib/learn/python/learn/estimators/_sklearn.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/learn/python/learn/estimators/_sklearn.py).

<!-- Placeholder for "Used in" -->

USE OF THIS EXCEPTION IS DEPRECATED.

This class inherits from both ValueError and AttributeError to help with
exception handling and backward compatibility.

#### Examples:


>>> from sklearn.svm import LinearSVC
>>> from sklearn.exceptions import NotFittedError
>>> try:
...     LinearSVC().predict([[1, 2], [2, 3], [3, 4]])
... except NotFittedError as e:
...     print(repr(e))
...                        # doctest: +NORMALIZE_WHITESPACE +ELLIPSIS
NotFittedError('This LinearSVC instance is not fitted yet',)

Copied from
https://github.com/scikit-learn/scikit-learn/master/sklearn/exceptions.py

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    *args,
    **kwargs
)
```






