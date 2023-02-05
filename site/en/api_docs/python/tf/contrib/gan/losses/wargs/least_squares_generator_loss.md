page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.gan.losses.wargs.least_squares_generator_loss

Least squares generator loss.

``` python
tf.contrib.gan.losses.wargs.least_squares_generator_loss(
    discriminator_gen_outputs,
    real_label=1,
    weights=1.0,
    scope=None,
    loss_collection=tf.GraphKeys.LOSSES,
    reduction=losses.Reduction.SUM_BY_NONZERO_WEIGHTS,
    add_summaries=False
)
```



Defined in [`contrib/gan/python/losses/python/losses_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/python/losses/python/losses_impl.py).

<!-- Placeholder for "Used in" -->

This loss comes from `Least Squares Generative Adversarial Networks`
(https://arxiv.org/abs/1611.04076).

L = 1/2 * (D(G(z)) - `real_label`) ** 2

where D(y) are discriminator logits.

#### Args:


* <b>`discriminator_gen_outputs`</b>: Discriminator output on generated data. Expected
  to be in the range of (-inf, inf).
* <b>`real_label`</b>: The value that the generator is trying to get the discriminator
  to output on generated data.
* <b>`weights`</b>: Optional `Tensor` whose rank is either 0, or the same rank as
  `discriminator_gen_outputs`, and must be broadcastable to
  `discriminator_gen_outputs` (i.e., all dimensions must be either `1`, or
  the same as the corresponding dimension).
* <b>`scope`</b>: The scope for the operations performed in computing the loss.
* <b>`loss_collection`</b>: collection to which this loss will be added.
* <b>`reduction`</b>: A <a href="../../../../../tf/losses/Reduction"><code>tf.compat.v1.losses.Reduction</code></a> to apply to loss.
* <b>`add_summaries`</b>: Whether or not to add summaries for the loss.


#### Returns:

A loss Tensor. The shape depends on `reduction`.
