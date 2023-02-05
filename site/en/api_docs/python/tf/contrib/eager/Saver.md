page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.eager.Saver

## Class `Saver`

A tf.compat.v1.train.Saver adapter for use when eager execution is enabled.





Defined in [`contrib/eager/python/saver.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/eager/python/saver.py).

<!-- Placeholder for "Used in" -->

`Saver`'s name-based checkpointing strategy is fragile. Please switch to
<a href="../../../tf/train/Checkpoint"><code>tf.train.Checkpoint</code></a> or <a href="../../../tf/keras/Model#save_weights"><code>tf.keras.Model.save_weights</code></a>, which perform a more
robust object-based saving. These APIs will load checkpoints written by
`Saver`.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(var_list)
```

A  tf.compat.v1.train.Saver adapter for use when eager execution is enabled.

  The API, and on-disk format, mimic tf.compat.v1.train.Saver except that no
  Session is needed.

#### Args:


* <b>`var_list`</b>: The list of variables that will be saved and restored. Either a
  list of <a href="../../../tf/Variable"><code>tf.Variable</code></a> objects, or a dictionary mapping names to
  <a href="../../../tf/Variable"><code>tf.Variable</code></a> objects.


#### Raises:


* <b>`RuntimeError`</b>: if invoked when eager execution has not been enabled.



## Methods

<h3 id="restore"><code>restore</code></h3>

``` python
restore(file_prefix)
```

Restores previously saved variables.


#### Args:


* <b>`file_prefix`</b>: Path prefix where parameters were previously saved.
  Typically obtained from a previous `save()` call, or from
  <a href="../../../tf/train/latest_checkpoint"><code>tf.train.latest_checkpoint</code></a>.

<h3 id="save"><code>save</code></h3>

``` python
save(
    file_prefix,
    global_step=None
)
```

Saves variables.


#### Args:


* <b>`file_prefix`</b>: Path prefix of files created for the checkpoint.
* <b>`global_step`</b>: If provided the global step number is appended to file_prefix
  to create the checkpoint filename. The optional argument can be a
  Tensor, a Variable, or an integer.


#### Returns:

A string: prefix of filenames created for the checkpoint. This may be
 an extension of file_prefix that is suitable to pass as an argument
 to a subsequent call to `restore()`.




