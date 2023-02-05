page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.tuple

Group tensors together.

### Aliases:

* `tf.compat.v1.tuple`
* `tf.tuple`

``` python
tf.tuple(
    tensors,
    name=None,
    control_inputs=None
)
```



Defined in [`python/ops/control_flow_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/control_flow_ops.py).

<!-- Placeholder for "Used in" -->

This creates a tuple of tensors with the same values as the `tensors`
argument, except that the value of each tensor is only returned after the
values of all tensors have been computed.

`control_inputs` contains additional ops that have to finish before this op
finishes, but whose outputs are not returned.

This can be used as a "join" mechanism for parallel computations: all the
argument tensors can be computed in parallel, but the values of any tensor
returned by `tuple` are only available after all the parallel computations
are done.

See also <a href="../tf/group"><code>tf.group</code></a> and
<a href="../tf/control_dependencies"><code>tf.control_dependencies</code></a>.

#### Args:


* <b>`tensors`</b>: A list of `Tensor`s or `IndexedSlices`, some entries can be `None`.
* <b>`name`</b>: (optional) A name to use as a `name_scope` for the operation.
* <b>`control_inputs`</b>: List of additional ops to finish before returning.


#### Returns:

Same as `tensors`.



#### Raises:


* <b>`ValueError`</b>: If `tensors` does not contain any `Tensor` or `IndexedSlices`.
* <b>`TypeError`</b>: If `control_inputs` is not a list of `Operation` or `Tensor`
  objects.