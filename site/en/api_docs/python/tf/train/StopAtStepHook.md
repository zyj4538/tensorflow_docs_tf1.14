page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.StopAtStepHook

## Class `StopAtStepHook`

Hook that requests stop at a specified step.

Inherits From: [`SessionRunHook`](../../tf/train/SessionRunHook)

### Aliases:

* Class `tf.compat.v1.estimator.StopAtStepHook`
* Class `tf.compat.v1.train.StopAtStepHook`
* Class `tf.compat.v2.estimator.StopAtStepHook`
* Class `tf.estimator.StopAtStepHook`
* Class `tf.train.StopAtStepHook`



Defined in [`python/training/basic_session_run_hooks.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/basic_session_run_hooks.py).

<!-- Placeholder for "Used in" -->


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    num_steps=None,
    last_step=None
)
```

Initializes a `StopAtStepHook`.

This hook requests stop after either a number of steps have been
executed or a last step has been reached. Only one of the two options can be
specified.

if `num_steps` is specified, it indicates the number of steps to execute
after `begin()` is called. If instead `last_step` is specified, it
indicates the last step we want to execute, as passed to the `after_run()`
call.

#### Args:


* <b>`num_steps`</b>: Number of steps to execute.
* <b>`last_step`</b>: Step after which to stop.


#### Raises:


* <b>`ValueError`</b>: If one of the arguments is invalid.



## Methods

<h3 id="after_create_session"><code>after_create_session</code></h3>

``` python
after_create_session(
    session,
    coord
)
```




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



