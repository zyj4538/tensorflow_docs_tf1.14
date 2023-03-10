page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.gan.losses.wargs.mutual_information_penalty

Returns a penalty on the mutual information in an InfoGAN model.

``` python
tf.contrib.gan.losses.wargs.mutual_information_penalty(
    structured_generator_inputs,
    predicted_distributions,
    weights=1.0,
    scope=None,
    loss_collection=tf.GraphKeys.LOSSES,
    reduction=losses.Reduction.SUM_BY_NONZERO_WEIGHTS,
    add_summaries=False
)
```



Defined in [`contrib/gan/python/losses/python/losses_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/python/losses/python/losses_impl.py).

<!-- Placeholder for "Used in" -->

This loss comes from an InfoGAN paper https://arxiv.org/abs/1606.03657.

#### Args:


* <b>`structured_generator_inputs`</b>: A list of Tensors representing the random noise
  that must  have high mutual information with the generator output. List
  length should match `predicted_distributions`.
* <b>`predicted_distributions`</b>: A list of `tfp.distributions.Distribution`s.
  Predicted by the recognizer, and used to evaluate the likelihood of the
  structured noise. List length should match `structured_generator_inputs`.
* <b>`weights`</b>: Optional `Tensor` whose rank is either 0, or the same dimensions as
  `structured_generator_inputs`.
* <b>`scope`</b>: The scope for the operations performed in computing the loss.
* <b>`loss_collection`</b>: collection to which this loss will be added.
* <b>`reduction`</b>: A <a href="../../../../../tf/losses/Reduction"><code>tf.compat.v1.losses.Reduction</code></a> to apply to loss.
* <b>`add_summaries`</b>: Whether or not to add summaries for the loss.


#### Returns:

A scalar Tensor representing the mutual information loss.
