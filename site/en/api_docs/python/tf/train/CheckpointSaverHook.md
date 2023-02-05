page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.CheckpointSaverHook

## Class `CheckpointSaverHook`

Saves checkpoints every N steps or seconds.

Inherits From: [`SessionRunHook`](../../tf/train/SessionRunHook)

### Aliases:

* Class `tf.compat.v1.estimator.CheckpointSaverHook`
* Class `tf.compat.v1.train.CheckpointSaverHook`
* Class `tf.compat.v2.estimator.CheckpointSaverHook`
* Class `tf.estimator.CheckpointSaverHook`
* Class `tf.train.CheckpointSaverHook`



Defined in [`python/training/basic_session_run_hooks.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/basic_session_run_hooks.py).

<!-- Placeholder for "Used in" -->


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    checkpoint_dir,
    save_secs=None,
    save_steps=None,
    saver=None,
    checkpoint_basename='model.ckpt',
    scaffold=None,
    listeners=None
)
```

Initializes a `CheckpointSaverHook`.


#### Args:


* <b>`checkpoint_dir`</b>: `str`, base directory for the checkpoint files.
* <b>`save_secs`</b>: `int`, save every N secs.
* <b>`save_steps`</b>: `int`, save every N steps.
* <b>`saver`</b>: `Saver` object, used for saving.
* <b>`checkpoint_basename`</b>: `str`, base name for the checkpoint files.
* <b>`scaffold`</b>: `Scaffold`, use to get saver object.
* <b>`listeners`</b>: List of `CheckpointSaverListener` subclass instances. Used for
  callbacks that run immediately before or after this hook saves the
  checkpoint.


#### Raises:


* <b>`ValueError`</b>: One of `save_steps` or `save_secs` should be set.
* <b>`ValueError`</b>: At most one of `saver` or `scaffold` should be set.



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






