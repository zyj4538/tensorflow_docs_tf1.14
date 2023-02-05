page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.lookup.InitializableLookupTableBase

## Class `InitializableLookupTableBase`

Initializable lookup table interface.

Inherits From: [`LookupInterface`](../../../tf/contrib/lookup/LookupInterface)



Defined in [`python/ops/lookup_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/lookup_ops.py).

<!-- Placeholder for "Used in" -->

An initializable lookup tables persist across different steps.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    default_value,
    initializer
)
```

Construct a table object from a table reference.

If requires a table initializer object (subclass of `TableInitializerBase`).
It provides the table key and value types, as well as the op to initialize
the table. The caller is responsible to execute the initialization op.

#### Args:


* <b>`default_value`</b>: The value to use if a key is missing in the table.
* <b>`initializer`</b>: The table initializer to use.



## Properties

<h3 id="default_value"><code>default_value</code></h3>

The default value of the table.


<h3 id="key_dtype"><code>key_dtype</code></h3>

The table key dtype.


<h3 id="name"><code>name</code></h3>

The name of the table.


<h3 id="resource_handle"><code>resource_handle</code></h3>

Returns the resource handle associated with this Resource.


<h3 id="value_dtype"><code>value_dtype</code></h3>

The table value dtype.




## Methods

<h3 id="lookup"><code>lookup</code></h3>

``` python
lookup(
    keys,
    name=None
)
```

Looks up `keys` in a table, outputs the corresponding values.

The `default_value` is used for keys not present in the table.

#### Args:


* <b>`keys`</b>: Keys to look up. May be either a `SparseTensor` or dense `Tensor`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `SparseTensor` if keys are sparse, otherwise a dense `Tensor`.



#### Raises:


* <b>`TypeError`</b>: when `keys` or `default_value` doesn't match the table data
  types.

<h3 id="size"><code>size</code></h3>

``` python
size(name=None)
```

Compute the number of elements in this table.


#### Args:


* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A scalar tensor containing the number of elements in this table.




