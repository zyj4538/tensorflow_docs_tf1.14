page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.graph_util.convert_variables_to_constants

Replaces all the variables in a graph with constants of the same values. (deprecated)

### Aliases:

* `tf.compat.v1.graph_util.convert_variables_to_constants`
* `tf.graph_util.convert_variables_to_constants`

``` python
tf.graph_util.convert_variables_to_constants(
    sess,
    input_graph_def,
    output_node_names,
    variable_names_whitelist=None,
    variable_names_blacklist=None
)
```



Defined in [`python/framework/graph_util_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/framework/graph_util_impl.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Use <a href="../../tf/graph_util/convert_variables_to_constants"><code>tf.compat.v1.graph_util.convert_variables_to_constants</code></a>

If you have a trained graph containing Variable ops, it can be convenient to
convert them all to Const ops holding the same values. This makes it possible
to describe the network fully with a single GraphDef file, and allows the
removal of a lot of ops related to loading and saving the variables.

#### Args:


* <b>`sess`</b>: Active TensorFlow session containing the variables.
* <b>`input_graph_def`</b>: GraphDef object holding the network.
* <b>`output_node_names`</b>: List of name strings for the result nodes of the graph.
* <b>`variable_names_whitelist`</b>: The set of variable names to convert (by default,
                          all variables are converted).
* <b>`variable_names_blacklist`</b>: The set of variable names to omit converting
                          to constants.


#### Returns:

GraphDef containing a simplified version of the original.
