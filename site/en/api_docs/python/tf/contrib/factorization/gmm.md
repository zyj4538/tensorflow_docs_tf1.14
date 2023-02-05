page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.factorization.gmm

Creates the graph for Gaussian mixture model (GMM) clustering.

``` python
tf.contrib.factorization.gmm(
    inp,
    initial_clusters,
    num_clusters,
    random_seed,
    covariance_type=FULL_COVARIANCE,
    params='wmc'
)
```



Defined in [`contrib/factorization/python/ops/gmm_ops.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/factorization/python/ops/gmm_ops.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`inp`</b>: An input tensor or list of input tensors
* <b>`initial_clusters`</b>: Specifies the clusters used during
  initialization. Can be a tensor or numpy array, or a function
  that generates the clusters. Can also be "random" to specify
  that clusters should be chosen randomly from input data. Note: type
  is diverse to be consistent with skflow.
* <b>`num_clusters`</b>: number of clusters.
* <b>`random_seed`</b>: Python integer. Seed for PRNG used to initialize centers.
* <b>`covariance_type`</b>: one of "diag", "full".
* <b>`params`</b>: Controls which parameters are updated in the training
  process. Can contain any combination of "w" for weights, "m" for
  means, and "c" for covars.


#### Returns:


* <b>`Note`</b>: tuple of lists returned to be consistent with skflow
A tuple consisting of:
* <b>`assignments`</b>: A vector (or list of vectors). Each element in the vector
  corresponds to an input row in 'inp' and specifies the cluster id
  corresponding to the input.
* <b>`training_op`</b>: an op that runs an iteration of training.
* <b>`init_op`</b>: an op that runs the initialization.