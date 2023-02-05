page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.VariableAggregation

## Class `VariableAggregation`

Indicates how a distributed variable will be aggregated.



### Aliases:

* Class `tf.VariableAggregation`
* Class `tf.compat.v1.VariableAggregation`



Defined in [`python/ops/variables.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/variables.py).

<!-- Placeholder for "Used in" -->

<a href="../tf/distribute/Strategy"><code>tf.distribute.Strategy</code></a> distributes a model by making multiple copies
(called "replicas") acting data-parallel on different elements of the input
batch. When performing some variable-update operation, say
`var.assign_add(x)`, in a model, we need to resolve how to combine the
different values for `x` computed in the different replicas.

* `NONE`: This is the default, giving an error if you use a
  variable-update operation with multiple replicas.
* `SUM`: Add the updates across replicas.
* `MEAN`: Take the arithmetic mean ("average") of the updates across replicas.
* `ONLY_FIRST_REPLICA`: This is for when every replica is performing the same
  update, but we only want to perform the update once. Used, e.g., for the
  global step counter.
* `ONLY_FIRST_TOWER`: Deprecated alias for `ONLY_FIRST_REPLICA`.

## Class Members

* `MEAN` <a id="MEAN"></a>
* `NONE` <a id="NONE"></a>
* `ONLY_FIRST_REPLICA` <a id="ONLY_FIRST_REPLICA"></a>
* `SUM` <a id="SUM"></a>
