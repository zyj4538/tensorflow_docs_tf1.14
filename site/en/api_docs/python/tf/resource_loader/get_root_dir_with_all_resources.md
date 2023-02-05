page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.resource_loader.get_root_dir_with_all_resources

Get a root directory containing all the data attributes in the build rule.

### Aliases:

* `tf.compat.v1.resource_loader.get_root_dir_with_all_resources`
* `tf.resource_loader.get_root_dir_with_all_resources`

``` python
tf.resource_loader.get_root_dir_with_all_resources()
```



Defined in [`python/platform/resource_loader.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/platform/resource_loader.py).

<!-- Placeholder for "Used in" -->


#### Returns:

The path to the specified file present in the data attribute of py_test
or py_binary. Falls back to returning the same as get_data_files_path if it
fails to detect a bazel runfiles directory.
