page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.input_pipeline.obtain_next

Basic wrapper for the ObtainNextOp.

``` python
tf.contrib.input_pipeline.obtain_next(
    string_list_tensor,
    counter
)
```



Defined in [`contrib/input_pipeline/python/ops/input_pipeline_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/input_pipeline/python/ops/input_pipeline_ops.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`string_list_tensor`</b>: A tensor that is a list of strings
* <b>`counter`</b>: an int64 ref tensor to keep track of which element is returned.


#### Returns:

An op that produces the element at counter + 1 in the list, round
robin style.
