page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.eager.Network

## Class `Network`

Represents the composition of a set of Layers.

Inherits From: [`Layer`](../../../tf/layers/Layer)



Defined in [`contrib/eager/python/network.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/eager/python/network.py).

<!-- Placeholder for "Used in" -->

*Deprecated*. Please inherit from <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a>, and see its documentation
for details. <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a> should be a drop-in replacement for
`tfe.Network` in most cases, but note that `track_layer` is no longer
necessary or supported. Instead, `Layer` instances are tracked on attribute
assignment (see the section of <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a>'s documentation on
subclassing). Since the output of `track_layer` is often assigned to an
attribute anyway, most code can be ported by simply removing the `track_layer`
calls.

<a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a> works with all TensorFlow `Layer` instances, including those
from <a href="../../../tf/layers"><code>tf.layers</code></a>, but switching to the <a href="../../../tf/keras/layers"><code>tf.keras.layers</code></a> versions along with
the migration to <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a> is recommended, since it will preserve
variable names.  Feel free to import it with an alias to avoid excess typing
:).

`Network` implements the `Layer` interface and adds convenience methods for
managing sub-`Layer`s, such as listing variables.

`Layer`s (including other `Network`s) should be added via `track_layer`. They
can then be used when overriding the `Network.call` method:

```python
class TwoLayerNetwork(tfe.Network):

  def __init__(self, name):
    super(TwoLayerNetwork, self).__init__(name=name)
    self.layer_one = self.track_layer(tf.compat.v1.layers.Dense(16,
    input_shape=(8,)))
    self.layer_two = self.track_layer(tf.compat.v1.layers.Dense(1,
    input_shape=(16,)))

  def call(self, inputs):
    return self.layer_two(self.layer_one(inputs))
```

After constructing an object and calling the `Network`, a list of variables
created by tracked `Layer`s is available via `Network.variables`:

```python
net = TwoLayerNetwork(name="net")
output = net(tf.ones([1, 8]))
print([v.name for v in net.variables])
```

This example prints variable names, one kernel and one bias per
<a href="../../../tf/layers/Dense"><code>tf.compat.v1.layers.Dense</code></a> layer:

```
['net/dense/kernel:0',
 'net/dense/bias:0',
 'net/dense_1/kernel:0',
 'net/dense_1/bias:0']
```

These variables can be passed to a `Saver` (<a href="../../../tf/train/Saver"><code>tf.compat.v1.train.Saver</code></a>, or
<a href="../../../tf/contrib/eager/Saver"><code>tf.contrib.eager.Saver</code></a> when executing eagerly) to save or restore the
`Network`, typically alongside a global step and
<a href="../../../tf/train/Optimizer"><code>tf.compat.v1.train.Optimizer</code></a>
variables when checkpointing during training.

Note that the semantics of calling a `Network` with graph execution (i.e. not
executing eagerly) may change slightly in the future. Currently stateful ops
are pruned from the graph unless they or something that depends on them is
executed in a session, but this behavior is not consistent with eager
execution (where stateful ops are executed eagerly). `Layer`s from <a href="../../../tf/layers"><code>tf.layers</code></a>
do not depend on this pruning and so will not be affected, but `Network`s
which rely on stateful ops being added to the graph but not executed (e.g. via
custom `Layer`s which manage stateful ops) may break with this change.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(name=None)
```

Configure the `Network`. (deprecated)

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Please inherit from <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a>, and see its documentation for details. <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a> should be a drop-in replacement for `tfe.Network` in most cases, but note that `track_layer` is no longer necessary or supported. Instead, `Layer` instances are tracked on attribute assignment (see the section of <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a>'s documentation on subclassing). Since the output of `track_layer` is often assigned to an attribute anyway, most code can be ported by simply removing the `track_layer` calls.

<a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a> works with all TensorFlow `Layer` instances, including those from <a href="../../../tf/layers"><code>tf.layers</code></a>, but switching to the <a href="../../../tf/keras/layers"><code>tf.keras.layers</code></a> versions along with the migration to <a href="../../../tf/keras/Model"><code>tf.keras.Model</code></a> is recommended, since it will preserve variable names. Feel free to import it with an alias to avoid excess typing :).

#### Args:


* <b>`name`</b>: The name to use for this `Network`. If specified, it must be unique
  in the context where this `Network` is first (1) added to another
  `Network` (in which case it must not share a name with other `Layers`
  added to that `Network`), or (2) built/called (in which case no other
  'top-level' `Network`s may share this name). If unspecified or None, the
  `Network` will be named using its class name, with a number appended if
  necessary for uniqueness (e.g. MyNetwork -> 'my_network_1').


#### Raises:


* <b>`ValueError`</b>: If `name` is not valid. Note that some naming errors will
  instead be raised when the `Network` is called.



## Properties

<h3 id="graph"><code>graph</code></h3>

DEPRECATED FUNCTION

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Stop using this property because tf.layers layers no longer track their graph.

<h3 id="layers"><code>layers</code></h3>




<h3 id="scope_name"><code>scope_name</code></h3>






## Methods

<h3 id="get_layer"><code>get_layer</code></h3>

``` python
get_layer(
    name=None,
    index=None
)
```

Get a contained <a href="../../../tf/layers/Layer"><code>tf.compat.v1.layers.Layer</code></a> either by name or index.


#### Args:


* <b>`name`</b>: String matching one of the names of a contained `Layer`. Note that
  the names of `Layer`s added to `Network`s may not be unique when doing
  layer sharing (i.e. adding a `Layer` to this `Network` which was already
  added to another `Network`). The lowest index `Layer` with a matching
  name will be returned.
* <b>`index`</b>: Integer in [0, number of layers). Layers are assigned an index by
  the order they are added.


#### Returns:

A <a href="../../../tf/layers/Layer"><code>tf.compat.v1.layers.Layer</code></a> object.



#### Raises:


* <b>`ValueError`</b>: If neither or both of 'index' or 'name' is specified, or the
  lookup failed.

<h3 id="track_layer"><code>track_layer</code></h3>

``` python
track_layer(layer)
```

Track a Layer in this Network.

`Network` requires that all `Layer`s used in `call()` be tracked so that the
`Network` can export a complete list of variables.

#### Args:


* <b>`layer`</b>: A <a href="../../../tf/layers/Layer"><code>tf.compat.v1.layers.Layer</code></a> object.


#### Returns:

The passed in `layer`.



#### Raises:


* <b>`RuntimeError`</b>: If __init__ has not been called.
* <b>`TypeError`</b>: If `layer` is the wrong type.
* <b>`ValueError`</b>: If a `Layer` with the same name has already been added.



