page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.gan.losses.combine_adversarial_loss

Combine adversarial loss and main loss.

``` python
tf.contrib.gan.losses.combine_adversarial_loss(
    gan_loss,
    gan_model,
    non_adversarial_loss,
    weight_factor=None,
    gradient_ratio=None,
    gradient_ratio_epsilon=1e-06,
    scalar_summaries=True,
    gradient_summaries=True
)
```



Defined in [`contrib/gan/python/losses/python/tuple_losses_impl.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/python/losses/python/tuple_losses_impl.py).

<!-- Placeholder for "Used in" -->

Uses `combine_adversarial_loss` to combine the losses, and returns
a modified GANLoss namedtuple.

#### Args:


* <b>`gan_loss`</b>: A GANLoss namedtuple. Assume the GANLoss.generator_loss is the
  adversarial loss.
* <b>`gan_model`</b>: A GANModel namedtuple. Used to access the generator's variables.
* <b>`non_adversarial_loss`</b>: Same as `main_loss` from
  `combine_adversarial_loss`.
* <b>`weight_factor`</b>: Same as `weight_factor` from
  `combine_adversarial_loss`.
* <b>`gradient_ratio`</b>: Same as `gradient_ratio` from
  `combine_adversarial_loss`.
* <b>`gradient_ratio_epsilon`</b>: Same as `gradient_ratio_epsilon` from
  `combine_adversarial_loss`.
* <b>`scalar_summaries`</b>: Same as `scalar_summaries` from
  `combine_adversarial_loss`.
* <b>`gradient_summaries`</b>: Same as `gradient_summaries` from
  `combine_adversarial_loss`.


#### Returns:

A modified GANLoss namedtuple, with `non_adversarial_loss` included
appropriately.
