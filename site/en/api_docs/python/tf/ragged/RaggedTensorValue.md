page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.ragged.RaggedTensorValue

## Class `RaggedTensorValue`

Represents the value of a `RaggedTensor`.



### Aliases:

* Class `tf.compat.v1.ragged.RaggedTensorValue`
* Class `tf.ragged.RaggedTensorValue`



Defined in [`python/ops/ragged/ragged_tensor_value.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/ragged/ragged_tensor_value.py).

<!-- Placeholder for "Used in" -->

Warning: `RaggedTensorValue` should only be used in graph mode; in
eager mode, the <a href="../../tf/RaggedTensor"><code>tf.RaggedTensor</code></a> class contains its value directly.

See <a href="../../tf/RaggedTensor"><code>tf.RaggedTensor</code></a> for a description of ragged tensors.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    values,
    row_splits
)
```

Creates a `RaggedTensorValue`.


#### Args:


* <b>`values`</b>: A numpy array of any type and shape; or a RaggedTensorValue.
* <b>`row_splits`</b>: A 1-D int32 or int64 numpy array.



## Properties

<h3 id="dtype"><code>dtype</code></h3>

The numpy dtype of values in this tensor.


<h3 id="flat_values"><code>flat_values</code></h3>

The innermost `values` array for this ragged tensor value.


<h3 id="nested_row_splits"><code>nested_row_splits</code></h3>

The row_splits for all ragged dimensions in this ragged tensor value.


<h3 id="ragged_rank"><code>ragged_rank</code></h3>

The number of ragged dimensions in this ragged tensor value.


<h3 id="row_splits"><code>row_splits</code></h3>

The split indices for the ragged tensor value.


<h3 id="shape"><code>shape</code></h3>

A tuple indicating the shape of this RaggedTensorValue.


<h3 id="values"><code>values</code></h3>

The concatenated values for all rows in this tensor.




## Methods

<h3 id="to_list"><code>to_list</code></h3>

``` python
to_list()
```

Returns this ragged tensor value as a nested Python list.




