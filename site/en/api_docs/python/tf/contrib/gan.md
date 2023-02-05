page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# Module: tf.contrib.gan

TF-GAN is a lightweight library for training and evaluating GANs.



Defined in [`contrib/gan/__init__.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/gan/__init__.py).

<!-- Placeholder for "Used in" -->

In addition to providing the infrastructure for easily training and evaluating
GANS, this library contains modules for a TFGAN-backed Estimator,
evaluation metrics, features (such as virtual batch normalization), and losses.
Please see README.md for details and usage.

## Modules

[`estimator`](../../tf/contrib/gan/estimator) module: TF-GAN estimator module.

[`eval`](../../tf/contrib/gan/eval) module: TF-GAN evaluation module.

[`features`](../../tf/contrib/gan/features) module: TFGAN features module.

[`losses`](../../tf/contrib/gan/losses) module: TFGAN losses and penalties.

## Classes

[`class ACGANModel`](../../tf/contrib/gan/ACGANModel): An ACGANModel contains all the pieces needed for ACGAN training.

[`class CycleGANLoss`](../../tf/contrib/gan/CycleGANLoss): CycleGANLoss contains the losses for `CycleGANModel`.

[`class CycleGANModel`](../../tf/contrib/gan/CycleGANModel): An CycleGANModel contains all the pieces needed for CycleGAN training.

[`class GANLoss`](../../tf/contrib/gan/GANLoss): GANLoss contains the generator and discriminator losses.

[`class GANModel`](../../tf/contrib/gan/GANModel): A GANModel contains all the pieces needed for GAN training.

[`class GANTrainOps`](../../tf/contrib/gan/GANTrainOps): GANTrainOps contains the training ops.

[`class GANTrainSteps`](../../tf/contrib/gan/GANTrainSteps): Contains configuration for the GAN Training.

[`class InfoGANModel`](../../tf/contrib/gan/InfoGANModel): An InfoGANModel contains all the pieces needed for InfoGAN training.

[`class RunTrainOpsHook`](../../tf/contrib/gan/RunTrainOpsHook): A hook to run train ops a fixed number of times.

[`class StarGANModel`](../../tf/contrib/gan/StarGANModel): A StarGANModel contains all the pieces needed for StarGAN training.

## Functions

[`acgan_model(...)`](../../tf/contrib/gan/acgan_model): Returns an ACGANModel contains all the pieces needed for ACGAN training.

[`cyclegan_loss(...)`](../../tf/contrib/gan/cyclegan_loss): Returns the losses for a `CycleGANModel`.

[`cyclegan_model(...)`](../../tf/contrib/gan/cyclegan_model): Returns a CycleGAN model outputs and variables.

[`gan_loss(...)`](../../tf/contrib/gan/gan_loss): Returns losses necessary to train generator and discriminator.

[`gan_model(...)`](../../tf/contrib/gan/gan_model): Returns GAN model outputs and variables.

[`gan_train(...)`](../../tf/contrib/gan/gan_train): A wrapper around `contrib.training.train` that uses GAN hooks.

[`gan_train_ops(...)`](../../tf/contrib/gan/gan_train_ops): Returns GAN train ops.

[`get_joint_train_hooks(...)`](../../tf/contrib/gan/get_joint_train_hooks): Returns a hooks function for joint GAN training.

[`get_sequential_train_hooks(...)`](../../tf/contrib/gan/get_sequential_train_hooks): Returns a hooks function for sequential GAN training.

[`get_sequential_train_steps(...)`](../../tf/contrib/gan/get_sequential_train_steps): Returns a thin wrapper around slim.learning.train_step, for GANs.

[`infogan_model(...)`](../../tf/contrib/gan/infogan_model): Returns an InfoGAN model outputs and variables.

[`stargan_loss(...)`](../../tf/contrib/gan/stargan_loss): StarGAN Loss.

[`stargan_model(...)`](../../tf/contrib/gan/stargan_model): Returns a StarGAN model outputs and variables.

