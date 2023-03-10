page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.gan.losses.wargs.acgan_generator_loss

ACGAN loss for the generator.

``` python
tf.contrib.gan.losses.wargs.acgan_generator_loss(
    discriminator_gen_classification_logits,
    one_hot_labels,
    weights=1.0,
    scope=None,
    loss_collection=tf.GraphKeys.LOSSES,
    reduction=losses.Reduction.SUM_BY_NONZERO_WEIGHTS,
    add_summaries=False
)
```



Defined in [`contrib/gan/python/losses/python/losses_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/python/losses/python/losses_impl.py).

<!-- Placeholder for "Used in" -->

The ACGAN loss adds a classification loss to the conditional discriminator.
Therefore, the discriminator must output a tuple consisting of
  (1) the real/fake prediction and
  (2) the logits for the classification (usually the last conv layer,
      flattened).

#### For more details:


* <b>`ACGAN`</b>: https://arxiv.org/abs/1610.09585


#### Args:


* <b>`discriminator_gen_classification_logits`</b>: Classification logits for generated
  data.
* <b>`one_hot_labels`</b>: A Tensor holding one-hot labels for the batch.
* <b>`weights`</b>: Optional `Tensor` whose rank is either 0, or the same rank as
  `discriminator_gen_classification_logits`, and must be broadcastable to
  `discriminator_gen_classification_logits` (i.e., all dimensions must be
  either `1`, or the same as the corresponding dimension).
* <b>`scope`</b>: The scope for the operations performed in computing the loss.
* <b>`loss_collection`</b>: collection to which this loss will be added.
* <b>`reduction`</b>: A <a href="../../../../../tf/losses/Reduction"><code>tf.compat.v1.losses.Reduction</code></a> to apply to loss.
* <b>`add_summaries`</b>: Whether or not to add summaries for the loss.


#### Returns:

A loss Tensor. Shape depends on `reduction`.



#### Raises:


* <b>`ValueError`</b>: if arg module not either `generator` or `discriminator`
* <b>`TypeError`</b>: if the discriminator does not output a tuple.