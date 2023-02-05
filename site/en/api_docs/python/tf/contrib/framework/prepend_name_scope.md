page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.prepend_name_scope

Prepends name scope to a name.

``` python
tf.contrib.framework.prepend_name_scope(
    name,
    import_scope
)
```



Defined in [`python/framework/ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/framework/ops.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`name`</b>: A `string` name.
* <b>`import_scope`</b>: Optional `string`. Name scope to add.


#### Returns:

Name with name scope added, or the original name if import_scope
is None.
