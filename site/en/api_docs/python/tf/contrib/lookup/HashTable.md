page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.lookup.HashTable

## Class `HashTable`

A generic hash table implementation.





Defined in [`contrib/lookup/lookup_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/lookup/lookup_ops.py).

<!-- Placeholder for "Used in" -->


#### Example usage:



```python
table = tf.HashTable(
    tf.KeyValueTensorInitializer(keys, values), -1)
out = table.lookup(input_tensor)
table.init.run()
print(out.eval())
```

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    initializer,
    default_value,
    shared_name=None,
    name=None
)
```

Creates a non-initialized `HashTable` object.

Creates a table, the type of its keys and values are specified by the
initializer.
Before using the table you will have to initialize it. After initialization
the table will be immutable.

#### Args:


* <b>`initializer`</b>: The table initializer to use. See `HashTable` kernel for
  supported key and value types.
* <b>`default_value`</b>: The value to use if a key is missing in the table.
* <b>`shared_name`</b>: If non-empty, this table will be shared under the given name
  across multiple sessions.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `HashTable` object.




## Properties

<h3 id="default_value"><code>default_value</code></h3>

The default value of the table.


<h3 id="init"><code>init</code></h3>




<h3 id="initializer"><code>initializer</code></h3>




<h3 id="key_dtype"><code>key_dtype</code></h3>

The table key dtype.


<h3 id="name"><code>name</code></h3>




<h3 id="resource_handle"><code>resource_handle</code></h3>

Returns the resource handle associated with this Resource.


<h3 id="value_dtype"><code>value_dtype</code></h3>

The table value dtype.




## Methods

<h3 id="export"><code>export</code></h3>

``` python
export(name=None)
```

Returns tensors of all keys and values in the table.


#### Args:


* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A pair of tensors with the first tensor containing all keys and the
  second tensors containing all values in the table.


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




