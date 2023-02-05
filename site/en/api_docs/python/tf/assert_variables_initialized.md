page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.assert_variables_initialized

Returns an Op to check if variables are initialized.

### Aliases:

* `tf.assert_variables_initialized`
* `tf.compat.v1.assert_variables_initialized`

``` python
tf.assert_variables_initialized(var_list=None)
```



Defined in [`python/ops/variables.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/variables.py).

<!-- Placeholder for "Used in" -->

NOTE: This function is obsolete and will be removed in 6 months.  Please
change your implementation to use `report_uninitialized_variables()`.

When run, the returned Op will raise the exception `FailedPreconditionError`
if any of the variables has not yet been initialized.

Note: This function is implemented by trying to fetch the values of the
variables. If one of the variables is not initialized a message may be
logged by the C++ runtime. This is expected.

#### Args:


* <b>`var_list`</b>: List of `Variable` objects to check. Defaults to the
  value of `global_variables().`


#### Returns:

An Op, or None if there are no variables.



**NOTE** The output of this function should be used.  If it is not, a warning will be logged.  To mark the output as used, call its .mark_used() method.