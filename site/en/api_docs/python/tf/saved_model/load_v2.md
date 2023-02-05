page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.saved_model.load_v2

Load a SavedModel from `export_dir`.

### Aliases:

* `tf.compat.v1.saved_model.load_v2`
* `tf.compat.v2.saved_model.load`
* `tf.saved_model.load_v2`

``` python
tf.saved_model.load_v2(
    export_dir,
    tags=None
)
```



Defined in [`python/saved_model/load.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/saved_model/load.py).

<!-- Placeholder for "Used in" -->

Signatures associated with the SavedModel are available as functions:

```python
imported = tf.saved_model.load(path)
f = imported.signatures["serving_default"]
print(f(x=tf.constant([[1.]])))
```

Objects exported with <a href="../../tf/saved_model/save"><code>tf.saved_model.save</code></a> additionally have trackable
objects and functions assigned to attributes:

```python
exported = tf.train.Checkpoint(v=tf.Variable(3.))
exported.f = tf.function(
    lambda x: exported.v * x,
    input_signature=[tf.TensorSpec(shape=None, dtype=tf.float32)])
tf.saved_model.save(exported, path)
imported = tf.saved_model.load(path)
assert 3. == imported.v.numpy()
assert 6. == imported.f(x=tf.constant(2.)).numpy()
```

_Importing SavedModels from TensorFlow 1.x_

SavedModels from <a href="../../tf/estimator/Estimator"><code>tf.estimator.Estimator</code></a> or 1.x SavedModel APIs have a flat
graph instead of <a href="../../tf/function"><code>tf.function</code></a> objects. These SavedModels will have functions
corresponding to their signatures in the `.signatures` attribute, but also
have a `.prune` method which allows you to extract functions for new
subgraphs. This is equivalent to importing the SavedModel and naming feeds and
fetches in a Session from TensorFlow 1.x.

```python
imported = tf.saved_model.load(path_to_v1_saved_model)
pruned = imported.prune("x:0", "out:0")
pruned(tf.ones([]))
```

See <a href="../../tf/wrap_function"><code>tf.compat.v1.wrap_function</code></a> for details. These SavedModels also have a
`.variables` attribute containing imported variables, and a `.graph` attribute
representing the whole imported graph. For SavedModels exported from
<a href="../../tf/saved_model/save"><code>tf.saved_model.save</code></a>, variables are instead assigned to whichever attributes
they were assigned before export.

#### Args:


* <b>`export_dir`</b>: The SavedModel directory to load from.
* <b>`tags`</b>: A tag or sequence of tags identifying the MetaGraph to load. Optional
  if the SavedModel contains a single MetaGraph, as for those exported from
  <a href="../../tf/saved_model/load"><code>tf.saved_model.load</code></a>.


#### Returns:

A trackable object with a `signatures` attribute mapping from signature
keys to functions. If the SavedModel was exported by <a href="../../tf/saved_model/load"><code>tf.saved_model.load</code></a>,
it also points to trackable objects and functions which were attached
to the exported object.



#### Raises:


* <b>`ValueError`</b>: If `tags` don't match a MetaGraph in the SavedModel.