page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.nest.assert_shallow_structure

Asserts that `shallow_tree` is a shallow structure of `input_tree`.

``` python
tf.contrib.framework.nest.assert_shallow_structure(
    shallow_tree,
    input_tree,
    check_types=True,
    expand_composites=False,
    check_subtrees_length=True
)
```



Defined in [`python/util/nest.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/util/nest.py).

<!-- Placeholder for "Used in" -->

That is, this function tests if the `input_tree` structure can be created from
the `shallow_tree` structure by replacing its leaf nodes with deeper
tree structures.

#### Examples:



The following code will raise an exception:

```python
  shallow_tree = {"a": "A", "b": "B"}
  input_tree = {"a": 1, "c": 2}
  assert_shallow_structure(shallow_tree, input_tree)
```

The following code will raise an exception:

```python
  shallow_tree = ["a", "b"]
  input_tree = ["c", ["d", "e"], "f"]
  assert_shallow_structure(shallow_tree, input_tree)
```

The following code will not raise an exception:

```python
  shallow_tree = ["a", "b"]
  input_tree = ["c", ["d", "e"], "f"]
  assert_shallow_structure(shallow_tree, input_tree,
    check_subtrees_length=False)
```

#### Args:


* <b>`shallow_tree`</b>: an arbitrarily nested structure.
* <b>`input_tree`</b>: an arbitrarily nested structure.
* <b>`check_types`</b>: if `True` (default) the sequence types of `shallow_tree` and
  `input_tree` have to be the same. Note that even with check_types==True,
  this function will consider two different namedtuple classes with the same
  name and _fields attribute to be the same class.
* <b>`expand_composites`</b>: If true, then composite tensors such as tf.SparseTensor
   and tf.RaggedTensor are expanded into their component tensors.
* <b>`check_subtrees_length`</b>: if `True` (default) the subtrees `shallow_tree` and
  `input_tree` have to be the same length. If `False` sequences are treated
  as key-value like mappings allowing them to be considered as valid
  subtrees. Note that this may drop parts of the `input_tree`.

#### Raises:


* <b>`TypeError`</b>: If `shallow_tree` is a sequence but `input_tree` is not.
* <b>`TypeError`</b>: If the sequence types of `shallow_tree` are different from
  `input_tree`. Only raised if `check_types` is `True`.
* <b>`ValueError`</b>: If the sequence lengths of `shallow_tree` are different from
  `input_tree`.