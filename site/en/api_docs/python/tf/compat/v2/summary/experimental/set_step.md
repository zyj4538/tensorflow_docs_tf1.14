page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.compat.v2.summary.experimental.set_step

Sets the default summary step for the current thread.

``` python
tf.compat.v2.summary.experimental.set_step(step)
```



Defined in [`python/ops/summary_ops_v2.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/summary_ops_v2.py).

<!-- Placeholder for "Used in" -->

For convenience, this function sets a default value for the `step` parameter
used in summary-writing functions elsewhere in the API so that it need not
be explicitly passed in every such invocation. The value can be a constant
or a variable, and can be retrieved via `tf.summary.experimental.get_step()`.

Note: when using this with @tf.functions, the step value will be captured at
the time the function is traced, so changes to the step outside the function
will not be reflected inside the function unless using a <a href="../../../../../tf/Variable"><code>tf.Variable</code></a> step.

#### Args:


* <b>`step`</b>: An `int64`-castable default step value, or None to unset.