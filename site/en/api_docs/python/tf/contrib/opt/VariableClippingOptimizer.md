page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.opt.VariableClippingOptimizer

## Class `VariableClippingOptimizer`

Wrapper optimizer that clips the norm of specified variables after update.

Inherits From: [`Optimizer`](../../../tf/train/Optimizer)



Defined in [`contrib/opt/python/training/variable_clipping_optimizer.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/opt/python/training/variable_clipping_optimizer.py).

<!-- Placeholder for "Used in" -->

This optimizer delegates all aspects of gradient calculation and application
to an underlying optimizer.  After applying gradients, this optimizer then
clips the variable to have a maximum L2 norm along specified dimensions.
NB: this is quite different from clipping the norm of the gradients.

Multiple instances of `VariableClippingOptimizer` may be chained to specify
different max norms for different subsets of variables.

This is more efficient at serving-time than using normalization during
embedding lookup, at the expense of more expensive training and fewer
guarantees about the norms.


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    opt,
    vars_to_clip_dims,
    max_norm,
    use_locking=False,
    colocate_clip_ops_with_vars=False,
    name='VariableClipping'
)
```

Construct a new clip-norm optimizer.


#### Args:


* <b>`opt`</b>: The actual optimizer that will be used to compute and apply the
  gradients. Must be one of the Optimizer classes.
* <b>`vars_to_clip_dims`</b>: A dict with keys as Variables and values as lists
  of dimensions along which to compute the L2-norm.  See
  <a href="../../../tf/clip_by_norm"><code>tf.clip_by_norm</code></a> for more details.
* <b>`max_norm`</b>: The L2-norm to clip to, for all variables specified.
* <b>`use_locking`</b>: If `True` use locks for clip update operations.
* <b>`colocate_clip_ops_with_vars`</b>: If `True`, try colocating the clip norm
  ops with the corresponding variable.
* <b>`name`</b>: Optional name prefix for the operations created when applying
  gradients.  Defaults to "VariableClipping".



## Methods

<h3 id="apply_gradients"><code>apply_gradients</code></h3>

``` python
apply_gradients(
    grads_and_vars,
    global_step=None,
    name=None
)
```




<h3 id="compute_gradients"><code>compute_gradients</code></h3>

``` python
compute_gradients(
    *args,
    **kwargs
)
```




<h3 id="get_name"><code>get_name</code></h3>

``` python
get_name()
```




<h3 id="get_slot"><code>get_slot</code></h3>

``` python
get_slot(
    *args,
    **kwargs
)
```




<h3 id="get_slot_names"><code>get_slot_names</code></h3>

``` python
get_slot_names(
    *args,
    **kwargs
)
```




<h3 id="minimize"><code>minimize</code></h3>

``` python
minimize(
    loss,
    global_step=None,
    var_list=None,
    gate_gradients=GATE_OP,
    aggregation_method=None,
    colocate_gradients_with_ops=False,
    name=None,
    grad_loss=None
)
```

Add operations to minimize `loss` by updating `var_list`.

This method simply combines calls `compute_gradients()` and
`apply_gradients()`. If you want to process the gradient before applying
them call `compute_gradients()` and `apply_gradients()` explicitly instead
of using this function.

#### Args:


* <b>`loss`</b>: A `Tensor` containing the value to minimize.
* <b>`global_step`</b>: Optional `Variable` to increment by one after the
  variables have been updated.
* <b>`var_list`</b>: Optional list or tuple of `Variable` objects to update to
  minimize `loss`.  Defaults to the list of variables collected in
  the graph under the key `GraphKeys.TRAINABLE_VARIABLES`.
* <b>`gate_gradients`</b>: How to gate the computation of gradients.  Can be
  `GATE_NONE`, `GATE_OP`, or  `GATE_GRAPH`.
* <b>`aggregation_method`</b>: Specifies the method used to combine gradient terms.
  Valid values are defined in the class `AggregationMethod`.
* <b>`colocate_gradients_with_ops`</b>: If True, try colocating gradients with
  the corresponding op.
* <b>`name`</b>: Optional name for the returned operation.
* <b>`grad_loss`</b>: Optional. A `Tensor` holding the gradient computed for `loss`.


#### Returns:

An Operation that updates the variables in `var_list`.  If `global_step`
was not `None`, that operation also increments `global_step`.



#### Raises:


* <b>`ValueError`</b>: If some of the variables are not `Variable` objects.



#### Eager Compatibility
When eager execution is enabled, `loss` should be a Python function that
takes no arguments and computes the value to be minimized. Minimization (and
gradient computation) is done with respect to the elements of `var_list` if
not None, else with respect to any trainable variables created during the
execution of the `loss` function. `gate_gradients`, `aggregation_method`,
`colocate_gradients_with_ops` and `grad_loss` are ignored when eager
execution is enabled.



<h3 id="variables"><code>variables</code></h3>

``` python
variables()
```

A list of variables which encode the current state of `Optimizer`.

Includes slot variables and additional global variables created by the
optimizer in the current default graph.

#### Returns:

A list of variables.




## Class Members

* `GATE_GRAPH = 2` <a id="GATE_GRAPH"></a>
* `GATE_NONE = 0` <a id="GATE_NONE"></a>
* `GATE_OP = 1` <a id="GATE_OP"></a>
