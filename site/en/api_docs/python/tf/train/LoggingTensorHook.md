page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.LoggingTensorHook

## Class `LoggingTensorHook`

Prints the given tensors every N local steps, every N seconds, or at end.

Inherits From: [`SessionRunHook`](../../tf/train/SessionRunHook)

### Aliases:

* Class `tf.compat.v1.estimator.LoggingTensorHook`
* Class `tf.compat.v1.train.LoggingTensorHook`
* Class `tf.compat.v2.estimator.LoggingTensorHook`
* Class `tf.estimator.LoggingTensorHook`
* Class `tf.train.LoggingTensorHook`



Defined in [`python/training/basic_session_run_hooks.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/basic_session_run_hooks.py).

<!-- Placeholder for "Used in" -->

The tensors will be printed to the log, with `INFO` severity. If you are not
seeing the logs, you might want to add the following line after your imports:

```python
  tf.compat.v1.logging.set_verbosity(tf.compat.v1.logging.INFO)
```

Note that if `at_end` is True, `tensors` should not include any tensor
whose evaluation produces a side effect such as consuming additional inputs.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    tensors,
    every_n_iter=None,
    every_n_secs=None,
    at_end=False,
    formatter=None
)
```

Initializes a `LoggingTensorHook`.


#### Args:


* <b>`tensors`</b>: `dict` that maps string-valued tags to tensors/tensor names, or
  `iterable` of tensors/tensor names.
* <b>`every_n_iter`</b>: `int`, print the values of `tensors` once every N local
  steps taken on the current worker.
* <b>`every_n_secs`</b>: `int` or `float`, print the values of `tensors` once every N
  seconds. Exactly one of `every_n_iter` and `every_n_secs` should be
  provided.
* <b>`at_end`</b>: `bool` specifying whether to print the values of `tensors` at the
  end of the run.
* <b>`formatter`</b>: function, takes dict of `tag`->`Tensor` and returns a string.
  If `None` uses default printing all tensors.


#### Raises:


* <b>`ValueError`</b>: if `every_n_iter` is non-positive.



## Methods

<h3 id="after_create_session"><code>after_create_session</code></h3>

``` python
after_create_session(
    session,
    coord
)
```

Called when new TensorFlow session is created.

This is called to signal the hooks that a new session has been created. This
has two essential differences with the situation in which `begin` is called:

* When this is called, the graph is finalized and ops can no longer be added
    to the graph.
* This method will also be called as a result of recovering a wrapped
    session, not only at the beginning of the overall session.

#### Args:


* <b>`session`</b>: A TensorFlow Session that has been created.
* <b>`coord`</b>: A Coordinator object which keeps track of all threads.

<h3 id="after_run"><code>after_run</code></h3>

``` python
after_run(
    run_context,
    run_values
)
```




<h3 id="before_run"><code>before_run</code></h3>

``` python
before_run(run_context)
```




<h3 id="begin"><code>begin</code></h3>

``` python
begin()
```




<h3 id="end"><code>end</code></h3>

``` python
end(session)
```






