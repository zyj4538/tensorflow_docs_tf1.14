page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.control_dependencies

Wrapper for <a href="../tf/Graph#control_dependencies"><code>Graph.control_dependencies()</code></a> using the default graph.

### Aliases:

* `tf.compat.v1.control_dependencies`
* `tf.compat.v2.control_dependencies`
* `tf.control_dependencies`

``` python
tf.control_dependencies(control_inputs)
```



Defined in [`python/framework/ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/framework/ops.py).

<!-- Placeholder for "Used in" -->

See <a href="../tf/Graph#control_dependencies"><code>tf.Graph.control_dependencies</code></a>
for more details.

When eager execution is enabled, any callable object in the `control_inputs`
list will be called.

#### Args:


* <b>`control_inputs`</b>: A list of `Operation` or `Tensor` objects which must be
  executed or computed before running the operations defined in the context.
  Can also be `None` to clear the control dependencies. If eager execution
  is enabled, any callable object in the `control_inputs` list will be
  called.


#### Returns:

A context manager that specifies control dependencies for all
operations constructed within the context.
