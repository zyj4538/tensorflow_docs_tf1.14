page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.graph_editor.get_ops_ios

Return all the <a href="../../../tf/Operation"><code>tf.Operation</code></a> which are connected to an op in ops.

``` python
tf.contrib.graph_editor.get_ops_ios(
    ops,
    control_inputs=False,
    control_outputs=None,
    control_ios=None
)
```



Defined in [`contrib/graph_editor/select.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/graph_editor/select.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`ops`</b>: an object convertible to a list of <a href="../../../tf/Operation"><code>tf.Operation</code></a>.
* <b>`control_inputs`</b>: A boolean indicating whether control inputs are enabled.
* <b>`control_outputs`</b>: An instance of `util.ControlOutputs` or `None`. If not
  `None`, control outputs are enabled.
* <b>`control_ios`</b>:  An instance of `util.ControlOutputs` or `None`. If not `None`,
  both control inputs and control outputs are enabled. This is equivalent to
  set `control_inputs` to `True` and `control_outputs` to the
  `util.ControlOutputs` instance.

#### Returns:

All the <a href="../../../tf/Operation"><code>tf.Operation</code></a> surrounding the given ops.


#### Raises:


* <b>`TypeError`</b>: if `ops` cannot be converted to a list of <a href="../../../tf/Operation"><code>tf.Operation</code></a>.