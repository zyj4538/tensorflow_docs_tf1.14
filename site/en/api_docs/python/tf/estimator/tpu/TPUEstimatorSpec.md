page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.estimator.tpu.TPUEstimatorSpec

## Class `TPUEstimatorSpec`

Ops and objects returned from a `model_fn` and passed to `TPUEstimator`.



### Aliases:

* Class `tf.compat.v1.estimator.tpu.TPUEstimatorSpec`
* Class `tf.contrib.tpu.TPUEstimatorSpec`
* Class `tf.estimator.tpu.TPUEstimatorSpec`



Defined in [`python/estimator/tpu/tpu_estimator.py`](https://github.com/tensorflow/estimator/tree/master/tensorflow_estimator/python/estimator/tpu/tpu_estimator.py).

<!-- Placeholder for "Used in" -->

See `EstimatorSpec` for `mode`, `predictions`, `loss`, `train_op`, and
`export_outputs`.

For evaluation, `eval_metrics `is a tuple of `metric_fn` and `tensors`, where
`metric_fn` runs on CPU to generate metrics and `tensors` represents the
`Tensor`s transferred from TPU system to CPU host and passed to `metric_fn`.
To be precise, TPU evaluation expects a slightly different signature from the
<a href="../../../tf/estimator/Estimator"><code>tf.estimator.Estimator</code></a>. While <a href="../../../tf/estimator/EstimatorSpec#eval_metric_ops"><code>EstimatorSpec.eval_metric_ops</code></a> expects a
dict, <a href="../../../tf/estimator/tpu/TPUEstimatorSpec#eval_metrics"><code>TPUEstimatorSpec.eval_metrics</code></a> is a tuple of `metric_fn` and `tensors`.
The `tensors` could be a list of `Tensor`s or dict of names to `Tensor`s. The
`tensors` usually specify the model logits, which are transferred back from
TPU system to CPU host. All tensors must have be batch-major, i.e., the batch
size is the first dimension. Once all tensors are available at CPU host from
all shards, they are concatenated (on CPU) and passed as positional arguments
to the `metric_fn` if `tensors` is list or keyword arguments if `tensors` is
a dict. `metric_fn` takes the `tensors` and returns a dict from metric string
name to the result of calling a metric function, namely a `(metric_tensor,
update_op)` tuple. See `TPUEstimator` for MNIST example how to specify the
`eval_metrics`.

`scaffold_fn` is a function running on CPU to generate the `Scaffold`. This
function should not capture any Tensors in `model_fn`.

`host_call` is a tuple of a `function` and a list or dictionary of `tensors`
to pass to that function and returns a list of Tensors. `host_call` currently
works for train() and evaluate(). The Tensors returned by the function is
executed on the CPU on every step, so there is communication overhead when
sending tensors from TPU to CPU. To reduce the overhead, try reducing the
size of the tensors. The `tensors` are concatenated along their major (batch)
dimension, and so must be >= rank 1. The `host_call` is useful for writing
summaries with <a href="../../../tf/contrib/summary/create_file_writer"><code>tf.contrib.summary.create_file_writer</code></a>.

## Properties

<h3 id="mode"><code>mode</code></h3>




<h3 id="predictions"><code>predictions</code></h3>




<h3 id="loss"><code>loss</code></h3>




<h3 id="train_op"><code>train_op</code></h3>




<h3 id="eval_metrics"><code>eval_metrics</code></h3>




<h3 id="export_outputs"><code>export_outputs</code></h3>




<h3 id="scaffold_fn"><code>scaffold_fn</code></h3>




<h3 id="host_call"><code>host_call</code></h3>




<h3 id="training_hooks"><code>training_hooks</code></h3>




<h3 id="evaluation_hooks"><code>evaluation_hooks</code></h3>




<h3 id="prediction_hooks"><code>prediction_hooks</code></h3>






## Methods

<h3 id="as_estimator_spec"><code>as_estimator_spec</code></h3>

``` python
as_estimator_spec()
```

Creates an equivalent `EstimatorSpec` used by CPU train/eval.




