page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.gan.gan_train_ops

Returns GAN train ops.

``` python
tf.contrib.gan.gan_train_ops(
    model,
    loss,
    generator_optimizer,
    discriminator_optimizer,
    check_for_unused_update_ops=True,
    is_chief=True,
    **kwargs
)
```



Defined in [`contrib/gan/python/train.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/python/train.py).

<!-- Placeholder for "Used in" -->

The highest-level call in TF-GAN. It is composed of functions that can also
be called, should a user require more control over some part of the GAN
training process.

#### Args:


* <b>`model`</b>: A GANModel.
* <b>`loss`</b>: A GANLoss.
* <b>`generator_optimizer`</b>: The optimizer for generator updates.
* <b>`discriminator_optimizer`</b>: The optimizer for the discriminator updates.
* <b>`check_for_unused_update_ops`</b>: If `True`, throws an exception if there are
  update ops outside of the generator or discriminator scopes.
* <b>`is_chief`</b>: Specifies whether or not the training is being run by the primary
  replica during replica training.
* <b>`**kwargs`</b>: Keyword args to pass directly to `training.create_train_op` for
  both the generator and discriminator train op.


#### Returns:

A GANTrainOps tuple of (generator_train_op, discriminator_train_op) that can
be used to train a generator/discriminator pair.
