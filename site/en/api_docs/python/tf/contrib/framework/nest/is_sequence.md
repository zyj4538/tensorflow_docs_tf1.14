page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.nest.is_sequence

Returns true if its input is a collections.Sequence (except strings).

``` python
tf.contrib.framework.nest.is_sequence(o)
```



Defined in [`python/pywrap_tensorflow_internal.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/pywrap_tensorflow_internal.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`seq`</b>: an input sequence.


#### Returns:

True if the sequence is a not a string and is a collections.Sequence or a
dict.
