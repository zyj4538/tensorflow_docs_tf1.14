page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.learn.run_n

Run `output_dict` tensors `n` times, with the same `feed_dict` each run. (deprecated)

``` python
tf.contrib.learn.run_n(
    output_dict,
    feed_dict=None,
    restore_checkpoint_path=None,
    n=1
)
```



Defined in [`contrib/learn/python/learn/graph_actions.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/learn/python/learn/graph_actions.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed after 2017-02-15.
Instructions for updating:
graph_actions.py will be deleted. Use tf.train.* utilities instead. You can use learn/estimators/estimator.py as an example.

#### Args:


* <b>`output_dict`</b>: A `dict` mapping string names to tensors to run. Must all be
  from the same graph.
* <b>`feed_dict`</b>: `dict` of input values to feed each run.
* <b>`restore_checkpoint_path`</b>: A string containing the path to a checkpoint to
  restore.
* <b>`n`</b>: Number of times to repeat.


#### Returns:

A list of `n` `dict` objects, each containing values read from `output_dict`
tensors.
