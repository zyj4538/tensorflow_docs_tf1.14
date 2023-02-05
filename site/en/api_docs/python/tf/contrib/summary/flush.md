page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.summary.flush

``` python
tf.contrib.summary.flush(
    writer=None,
    name=None
)
```



Defined in [`tensorflow/python/ops/summary_ops_v2.py`](https://github.com/tensorflow/tensorflow/blob/r1.13/tensorflow/python/ops/summary_ops_v2.py).

Forces summary writer to send any buffered data to storage.

This operation blocks until that finishes.

#### Args:

* <b>`writer`</b>: The `tf.summary.SummaryWriter` resource to flush.
    The thread default will be used if this parameter is None.
    Otherwise a <a href="../../../tf/no_op"><code>tf.no_op</code></a> is returned.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

The created <a href="../../../tf/Operation"><code>tf.Operation</code></a>.