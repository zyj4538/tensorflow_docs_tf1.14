page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.gan.gan_model

Returns GAN model outputs and variables.

``` python
tf.contrib.gan.gan_model(
    generator_fn,
    discriminator_fn,
    real_data,
    generator_inputs,
    generator_scope='Generator',
    discriminator_scope='Discriminator',
    check_shapes=True
)
```



Defined in [`contrib/gan/python/train.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/python/train.py).

<!-- Placeholder for "Used in" -->


#### Args:


* <b>`generator_fn`</b>: A python lambda that takes `generator_inputs` as inputs and
  returns the outputs of the GAN generator.
* <b>`discriminator_fn`</b>: A python lambda that takes `real_data`/`generated data`
  and `generator_inputs`. Outputs a Tensor in the range [-inf, inf].
* <b>`real_data`</b>: A Tensor representing the real data.
* <b>`generator_inputs`</b>: A Tensor or list of Tensors to the generator. In the
  vanilla GAN case, this might be a single noise Tensor. In the conditional
  GAN case, this might be the generator's conditioning.
* <b>`generator_scope`</b>: Optional generator variable scope. Useful if you want to
  reuse a subgraph that has already been created.
* <b>`discriminator_scope`</b>: Optional discriminator variable scope. Useful if you
  want to reuse a subgraph that has already been created.
* <b>`check_shapes`</b>: If `True`, check that generator produces Tensors that are the
  same shape as real data. Otherwise, skip this check.


#### Returns:

A GANModel namedtuple.



#### Raises:


* <b>`ValueError`</b>: If the generator outputs a Tensor that isn't the same shape as
  `real_data`.