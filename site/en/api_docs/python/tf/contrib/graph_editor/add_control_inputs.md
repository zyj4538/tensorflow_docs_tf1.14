page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.graph_editor.add_control_inputs

Add the control inputs cops to op.

``` python
tf.contrib.graph_editor.add_control_inputs(
    op,
    cops
)
```



Defined in [`contrib/graph_editor/reroute.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/graph_editor/reroute.py).

<!-- Placeholder for "Used in" -->

Warning: this function is directly manipulating the internals of the tf.Graph.

#### Args:


* <b>`op`</b>: a tf.Operation to which the control inputs are added.
* <b>`cops`</b>: an object convertible to a list of <a href="../../../tf/Operation"><code>tf.Operation</code></a>.

#### Raises:


* <b>`TypeError`</b>: if op is not a tf.Operation
* <b>`ValueError`</b>: if any cop in cops is already a control input of op.