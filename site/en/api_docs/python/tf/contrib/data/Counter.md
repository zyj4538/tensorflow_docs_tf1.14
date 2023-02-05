page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.data.Counter

Creates a `Dataset` that counts from `start` in steps of size `step`. (deprecated)

``` python
tf.contrib.data.Counter(
    start=0,
    step=1,
    dtype=tf.dtypes.int64
)
```



Defined in [`contrib/data/python/ops/counter.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/data/python/ops/counter.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Use <a href="../../../tf/data/experimental/Counter"><code>tf.data.experimental.Counter(...)</code></a>.

#### For example:



```python
Dataset.count() == [0, 1, 2, ...)
Dataset.count(2) == [2, 3, ...)
Dataset.count(2, 5) == [2, 7, 12, ...)
Dataset.count(0, -1) == [0, -1, -2, ...)
Dataset.count(10, -1) == [10, 9, ...)
```

#### Args:


* <b>`start`</b>: (Optional.) The starting value for the counter. Defaults to 0.
* <b>`step`</b>: (Optional.) The step size for the counter. Defaults to 1.
* <b>`dtype`</b>: (Optional.) The data type for counter elements. Defaults to
  <a href="../../../tf#int64"><code>tf.int64</code></a>.


#### Returns:

A `Dataset` of scalar `dtype` elements.
