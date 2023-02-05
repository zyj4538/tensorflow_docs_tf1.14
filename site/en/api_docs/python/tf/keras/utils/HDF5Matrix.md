page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.utils.HDF5Matrix

## Class `HDF5Matrix`

Representation of HDF5 dataset to be used instead of a Numpy array.



### Aliases:

* Class `tf.compat.v1.keras.utils.HDF5Matrix`
* Class `tf.compat.v2.keras.utils.HDF5Matrix`
* Class `tf.keras.utils.HDF5Matrix`



Defined in [`python/keras/utils/io_utils.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/keras/utils/io_utils.py).

<!-- Placeholder for "Used in" -->


#### Example:



```python
    x_data = HDF5Matrix('input/file.hdf5', 'data')
    model.predict(x_data)
```

Providing `start` and `end` allows use of a slice of the dataset.

Optionally, a normalizer function (or lambda) can be given. This will
be called on every slice of data retrieved.

#### Arguments:


* <b>`datapath`</b>: string, path to a HDF5 file
* <b>`dataset`</b>: string, name of the HDF5 dataset in the file specified
    in datapath
* <b>`start`</b>: int, start of desired slice of the specified dataset
* <b>`end`</b>: int, end of desired slice of the specified dataset
* <b>`normalizer`</b>: function to be called on data when retrieved


#### Returns:

An array-like HDF5 dataset.


<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    datapath,
    dataset,
    start=0,
    end=None,
    normalizer=None
)
```






## Properties

<h3 id="dtype"><code>dtype</code></h3>

Gets the datatype of the dataset.


#### Returns:

A numpy dtype string.


<h3 id="ndim"><code>ndim</code></h3>

Gets the number of dimensions (rank) of the dataset.


#### Returns:

An integer denoting the number of dimensions (rank) of the dataset.


<h3 id="shape"><code>shape</code></h3>

Gets a numpy-style shape tuple giving the dataset dimensions.


#### Returns:

A numpy-style shape tuple.


<h3 id="size"><code>size</code></h3>

Gets the total dataset size (number of elements).


#### Returns:

An integer denoting the number of elements in the dataset.




## Methods

<h3 id="__getitem__"><code>__getitem__</code></h3>

``` python
__getitem__(key)
```




<h3 id="__len__"><code>__len__</code></h3>

``` python
__len__()
```






## Class Members

* `refs` <a id="refs"></a>
