page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.remove_checkpoint

Removes a checkpoint given by `checkpoint_prefix`. (deprecated)

### Aliases:

* `tf.compat.v1.train.remove_checkpoint`
* `tf.train.remove_checkpoint`

``` python
tf.train.remove_checkpoint(
    checkpoint_prefix,
    checkpoint_format_version=tf.train.SaverDef.V2,
    meta_graph_suffix='meta'
)
```



Defined in [`python/training/checkpoint_management.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/checkpoint_management.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
Use standard file APIs to delete files with this prefix.

#### Args:


* <b>`checkpoint_prefix`</b>: The prefix of a V1 or V2 checkpoint. Typically the result
  of <a href="../../tf/train/Saver#save"><code>Saver.save()</code></a> or that of <a href="../../tf/train/latest_checkpoint"><code>tf.train.latest_checkpoint()</code></a>, regardless of
  sharded/non-sharded or V1/V2.
* <b>`checkpoint_format_version`</b>: <a href="../../tf/train/SaverDef#CheckpointFormatVersion"><code>SaverDef.CheckpointFormatVersion</code></a>, defaults to
  <a href="../../tf/train/SaverDef#V2"><code>SaverDef.V2</code></a>.
* <b>`meta_graph_suffix`</b>: Suffix for `MetaGraphDef` file. Defaults to 'meta'.