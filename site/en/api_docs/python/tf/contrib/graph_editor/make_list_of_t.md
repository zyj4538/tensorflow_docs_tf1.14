page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.graph_editor.make_list_of_t

Convert ts to a list of <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>.

``` python
tf.contrib.graph_editor.make_list_of_t(
    ts,
    check_graph=True,
    allow_graph=True,
    ignore_ops=False
)
```



Defined in [`contrib/graph_editor/util.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/graph_editor/util.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`ts`</b>: can be an iterable of <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>, a <a href="../../../tf/Graph"><code>tf.Graph</code></a> or a single tensor.
* <b>`check_graph`</b>: if `True` check if all the tensors belong to the same graph.
* <b>`allow_graph`</b>: if `False` a <a href="../../../tf/Graph"><code>tf.Graph</code></a> cannot be converted.
* <b>`ignore_ops`</b>: if `True`, silently ignore <a href="../../../tf/Operation"><code>tf.Operation</code></a>.

#### Returns:

A newly created list of <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>.


#### Raises:


* <b>`TypeError`</b>: if `ts` cannot be converted to a list of <a href="../../../tf/Tensor"><code>tf.Tensor</code></a> or,
 if `check_graph` is `True`, if all the ops do not belong to the same graph.