page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.graph_editor.make_view

Create a SubGraphView from selected operations and passthrough tensors.

### Aliases:

* `tf.contrib.graph_editor.make_view`
* `tf.contrib.graph_editor.sgv`

``` python
tf.contrib.graph_editor.make_view(
    *args,
    **kwargs
)
```



Defined in [`contrib/graph_editor/subgraph.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/graph_editor/subgraph.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`*args`</b>: list of 1) regular expressions (compiled or not) or 2) (array of)
  <a href="../../../tf/Operation"><code>tf.Operation</code></a> 3) (array of) <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>. Those objects will be converted
  into a list of operations and a list of candidate for passthrough tensors.
* <b>`**kwargs`</b>: keyword graph is used 1) to check that the ops and ts are from
  the correct graph 2) for regular expression query

#### Returns:

A subgraph view.


#### Raises:


* <b>`TypeError`</b>: if the optional keyword argument graph is not a <a href="../../../tf/Graph"><code>tf.Graph</code></a>
  or if an argument in args is not an (array of) <a href="../../../tf/Tensor"><code>tf.Tensor</code></a>
  or an (array of) <a href="../../../tf/Operation"><code>tf.Operation</code></a> or a string or a regular expression.
* <b>`ValueError`</b>: if one of the keyword arguments is unexpected.