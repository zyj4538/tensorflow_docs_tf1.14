page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.queue_runner.start_queue_runners

Starts all queue runners collected in the graph. (deprecated)

### Aliases:

* `tf.compat.v1.train.queue_runner.start_queue_runners`
* `tf.compat.v1.train.start_queue_runners`
* `tf.train.queue_runner.start_queue_runners`
* `tf.train.start_queue_runners`

``` python
tf.train.queue_runner.start_queue_runners(
    sess=None,
    coord=None,
    daemon=True,
    start=True,
    collection=tf.GraphKeys.QUEUE_RUNNERS
)
```



Defined in [`python/training/queue_runner_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/queue_runner_impl.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
To construct input pipelines, use the <a href="../../../tf/data"><code>tf.data</code></a> module.

This is a companion method to `add_queue_runner()`.  It just starts
threads for all queue runners collected in the graph.  It returns
the list of all threads.

#### Args:


* <b>`sess`</b>: `Session` used to run the queue ops.  Defaults to the
  default session.
* <b>`coord`</b>: Optional `Coordinator` for coordinating the started threads.
* <b>`daemon`</b>: Whether the threads should be marked as `daemons`, meaning
  they don't block program exit.
* <b>`start`</b>: Set to `False` to only create the threads, not start them.
* <b>`collection`</b>: A `GraphKey` specifying the graph collection to
  get the queue runners from.  Defaults to <a href="../../../tf/GraphKeys#QUEUE_RUNNERS"><code>GraphKeys.QUEUE_RUNNERS</code></a>.


#### Raises:


* <b>`ValueError`</b>: if `sess` is None and there isn't any default session.
* <b>`TypeError`</b>: if `sess` is not a <a href="../../../tf/Session"><code>tf.compat.v1.Session</code></a> object.


#### Returns:

A list of threads.



#### Raises:


* <b>`RuntimeError`</b>: If called with eager execution enabled.
* <b>`ValueError`</b>: If called without a default <a href="../../../tf/Session"><code>tf.compat.v1.Session</code></a> registered.



#### Eager Compatibility
Not compatible with eager execution. To ingest data under eager execution,
use the <a href="../../../tf/data"><code>tf.data</code></a> API instead.

