page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.global_variables

Returns global variables.

### Aliases:

* `tf.compat.v1.global_variables`
* `tf.global_variables`

``` python
tf.global_variables(scope=None)
```



Defined in [`python/ops/variables.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/ops/variables.py).

<!-- Placeholder for "Used in" -->

Global variables are variables that are shared across machines in a
distributed environment. The `Variable()` constructor or `get_variable()`
automatically adds new variables to the graph collection
<a href="../tf/GraphKeys#GLOBAL_VARIABLES"><code>GraphKeys.GLOBAL_VARIABLES</code></a>.
This convenience function returns the contents of that collection.

An alternative to global variables are local variables. See
<a href="../tf/local_variables"><code>tf.compat.v1.local_variables</code></a>

#### Args:


* <b>`scope`</b>: (Optional.) A string. If supplied, the resulting list is filtered
  to include only items whose `name` attribute matches `scope` using
  `re.match`. Items without a `name` attribute are never returned if a
  scope is supplied. The choice of `re.match` means that a `scope` without
  special tokens filters by prefix.


#### Returns:

A list of `Variable` objects.
