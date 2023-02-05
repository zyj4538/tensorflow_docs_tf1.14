page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.layers.recompute_grad

Decorator that recomputes the function on the backwards pass.

``` python
tf.contrib.layers.recompute_grad(
    *args,
    **kwargs
)
```



Defined in [`contrib/layers/python/layers/rev_block_lib.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/layers/python/layers/rev_block_lib.py).

<!-- Placeholder for "Used in" -->

To use this function, you must use `ResourceVariable`s (i.e.
`variable_scope(name, use_resource=True), which are the default in Eager mode
and when running on TPU.

Warning: Because the function will be called again on the backwards pass, the
user should be careful to not use ops in their function that mutate state or
have randomness (for example, batch normalization or dropout). If the function
does have such operations, it is recommended that the function take the
`is_recomputing` keyword argument which will be `False` on the forward pass
and `True` on the backwards pass so that it can disable state changes when
`is_recomputing=True` (for example, not updating the moving averages in batch
normalization).

#### Args:


* <b>`fn`</b>: a function that takes Tensors (all as positional arguments) and returns
  a tuple of Tensors. Note that `fn` should not close over any other
  Tensors or Variables.
* <b>`use_data_dep`</b>: `bool`, if `True` will use a dummy data dependency to force
  the recompute to happen. If `False` will use a control dependency. By
  default will be `True` if in an XLA context and `False` otherwise. XLA
  ignores control dependencies and so this data dependency is necessary.
* <b>`tupleize_grads`</b>: `bool`, if `True` will use control dependencies to ensure
  that all gradients are produced before any are consumed by downstream ops.
  If `use_data_dep` is also `True`, will use a data dependency instead of
  a control dependency.


#### Returns:

A wrapped fn that is identical to fn when called, but its activations will
be discarded and recomputed on the backwards pass (i.e. on a call to
tf.gradients).



#### Raises:


* <b>`ValueError`</b>: if `fn` closes over any Tensors or Variables.