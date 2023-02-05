page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.lookup.IdTableWithHashBuckets

## Class `IdTableWithHashBuckets`

String to Id table wrapper that assigns out-of-vocabulary keys to buckets.

Inherits From: [`LookupInterface`](../../../tf/contrib/lookup/LookupInterface)



Defined in [`python/ops/lookup_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/lookup_ops.py).

<!-- Placeholder for "Used in" -->

For example, if an instance of `IdTableWithHashBuckets` is initialized with a
string-to-id table that maps:

* `emerson -> 0`
* `lake -> 1`
* `palmer -> 2`

The `IdTableWithHashBuckets` object will performs the following mapping:

* `emerson -> 0`
* `lake -> 1`
* `palmer -> 2`
* `<other term> -> bucket_id`, where bucket_id will be between `3` and
`3 + num_oov_buckets - 1`, calculated by:
`hash(<term>) % num_oov_buckets + vocab_size`

If input_tensor is `["emerson", "lake", "palmer", "king", "crimson"]`,
the lookup result is `[0, 1, 2, 4, 7]`.

If `table` is None, only out-of-vocabulary buckets are used.

#### Example usage:



```python
num_oov_buckets = 3
input_tensor = tf.constant(["emerson", "lake", "palmer", "king", "crimnson"])
table = tf.IdTableWithHashBuckets(
    tf.StaticHashTable(tf.TextFileIdTableInitializer(filename),
                       default_value),
    num_oov_buckets)
out = table.lookup(input_tensor).
table.init.run()
print(out.eval())
```

The hash function used for generating out-of-vocabulary buckets ID is handled
by `hasher_spec`.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    table,
    num_oov_buckets,
    hasher_spec=tf.contrib.lookup.FastHashSpec,
    name=None,
    key_dtype=None
)
```

Construct a `IdTableWithHashBuckets` object.


#### Args:


* <b>`table`</b>: Table that maps <a href="../../../tf#string"><code>tf.string</code></a> or <a href="../../../tf#int64"><code>tf.int64</code></a> keys to <a href="../../../tf#int64"><code>tf.int64</code></a> ids.
* <b>`num_oov_buckets`</b>: Number of buckets to use for out-of-vocabulary keys.
* <b>`hasher_spec`</b>: A `HasherSpec` to specify the hash function to use for
  assignation of out-of-vocabulary buckets  (optional).
* <b>`name`</b>: A name for the operation (optional).
* <b>`key_dtype`</b>: Data type of keys passed to `lookup`. Defaults to
  `table.key_dtype` if `table` is specified, otherwise <a href="../../../tf#string"><code>tf.string</code></a>. Must
  be string or integer, and must be castable to `table.key_dtype`.


#### Raises:


* <b>`ValueError`</b>: when `table` in None and `num_oov_buckets` is not positive.
* <b>`TypeError`</b>: when `hasher_spec` is invalid.



## Properties

<h3 id="init"><code>init</code></h3>

DEPRECATED FUNCTION

Warning: THIS FUNCTION IS DEPRECATED. It will be removed after 2018-12-15.
Instructions for updating:
Use `initializer` instead.

<h3 id="initializer"><code>initializer</code></h3>




<h3 id="key_dtype"><code>key_dtype</code></h3>

The table key dtype.


<h3 id="name"><code>name</code></h3>




<h3 id="resource_handle"><code>resource_handle</code></h3>




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

Looks up `keys` in the table, outputs the corresponding values.

It assigns out-of-vocabulary keys to buckets based in their hashes.

#### Args:


* <b>`keys`</b>: Keys to look up. May be either a `SparseTensor` or dense `Tensor`.
* <b>`name`</b>: Optional name for the op.


#### Returns:

A `SparseTensor` if keys are sparse, otherwise a dense `Tensor`.



#### Raises:


* <b>`TypeError`</b>: when `keys` doesn't match the table key data type.

<h3 id="size"><code>size</code></h3>

``` python
size(name=None)
```

Compute the number of elements in this table.




