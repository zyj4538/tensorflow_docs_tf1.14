page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.StepCounterHook

## Class `StepCounterHook`

Hook that counts steps per second.

Inherits From: [`SessionRunHook`](../../tf/train/SessionRunHook)

### Aliases:

* Class `tf.compat.v1.estimator.StepCounterHook`
* Class `tf.compat.v1.train.StepCounterHook`
* Class `tf.compat.v2.estimator.StepCounterHook`
* Class `tf.estimator.StepCounterHook`
* Class `tf.train.StepCounterHook`



Defined in [`python/training/basic_session_run_hooks.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/basic_session_run_hooks.py).

<!-- Placeholder for "Used in" -->


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    every_n_steps=100,
    every_n_secs=None,
    output_dir=None,
    summary_writer=None
)
```






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

Called at the end of session.

The `session` argument can be used in case the hook wants to run final ops,
such as saving a last checkpoint.

If `session.run()` raises exception other than OutOfRangeError or
StopIteration then `end()` is not called.
Note the difference between `end()` and `after_run()` behavior when
`session.run()` raises OutOfRangeError or StopIteration. In that case
`end()` is called but `after_run()` is not called.

#### Args:


* <b>`session`</b>: A TensorFlow Session that will be soon closed.



