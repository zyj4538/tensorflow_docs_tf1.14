page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.SessionRunArgs

## Class `SessionRunArgs`

Represents arguments to be added to a <a href="../../tf/InteractiveSession#run"><code>Session.run()</code></a> call.



### Aliases:

* Class `tf.compat.v1.estimator.SessionRunArgs`
* Class `tf.compat.v1.train.SessionRunArgs`
* Class `tf.compat.v2.estimator.SessionRunArgs`
* Class `tf.estimator.SessionRunArgs`
* Class `tf.train.SessionRunArgs`



Defined in [`python/training/session_run_hook.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/session_run_hook.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`fetches`</b>: Exactly like the 'fetches' argument to Session.Run().
  Can be a single tensor or op, a list of 'fetches' or a dictionary
  of fetches.  For example:
    fetches = global_step_tensor
    fetches = [train_op, summary_op, global_step_tensor]
    fetches = {'step': global_step_tensor, 'summ': summary_op}
  Note that this can recurse as expected:
    fetches = {'step': global_step_tensor,
               'ops': [train_op, check_nan_op]}
* <b>`feed_dict`</b>: Exactly like the `feed_dict` argument to `Session.Run()`
* <b>`options`</b>: Exactly like the `options` argument to <a href="../../tf/InteractiveSession#run"><code>Session.run()</code></a>, i.e., a
  config_pb2.RunOptions proto.

## Properties

<h3 id="fetches"><code>fetches</code></h3>




<h3 id="feed_dict"><code>feed_dict</code></h3>




<h3 id="options"><code>options</code></h3>






