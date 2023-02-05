page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.saved_model.main_op.main_op

Returns a main op to init variables and tables. (deprecated)

### Aliases:

* `tf.compat.v1.saved_model.main_op.main_op`
* `tf.saved_model.main_op.main_op`

``` python
tf.saved_model.main_op.main_op()
```



Defined in [`python/saved_model/main_op_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/saved_model/main_op_impl.py).

<!-- Placeholder for "Used in" -->

Warning: THIS FUNCTION IS DEPRECATED. It will be removed in a future version.
Instructions for updating:
This function will only be available through the v1 compatibility library as tf.compat.v1.saved_model.main_op.main_op.

Returns the main op including the group of ops that initializes all
variables, initializes local variables and initialize all tables.

#### Returns:

The set of ops to be run as part of the main op upon the load operation.
