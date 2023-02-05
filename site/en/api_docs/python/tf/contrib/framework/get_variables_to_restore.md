page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.get_variables_to_restore

Gets the list of the variables to restore.

``` python
tf.contrib.framework.get_variables_to_restore(
    include=None,
    exclude=None
)
```



Defined in [`contrib/framework/python/ops/variables.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/framework/python/ops/variables.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`include`</b>: an optional list/tuple of scope strings for filtering which
  variables from the VARIABLES collection to include. None would include all
  the variables.
* <b>`exclude`</b>: an optional list/tuple of scope strings for filtering which
  variables from the VARIABLES collection to exclude. None it would not
  exclude any.


#### Returns:

a list of variables to restore.



#### Raises:


* <b>`TypeError`</b>: include or exclude is provided but is not a list or a tuple.