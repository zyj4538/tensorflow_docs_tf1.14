page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.seq2seq.GreedyEmbeddingHelper

## Class `GreedyEmbeddingHelper`

A helper for use during inference.

Inherits From: [`Helper`](../../../tf/contrib/seq2seq/Helper)



Defined in [`contrib/seq2seq/python/ops/helper.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/seq2seq/python/ops/helper.py).

<!-- Placeholder for "Used in" -->

Uses the argmax of the output (treated as logits) and passes the
result through an embedding layer to get the next input.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    embedding,
    start_tokens,
    end_token
)
```

Initializer.


#### Args:


* <b>`embedding`</b>: A callable that takes a vector tensor of `ids` (argmax ids),
  or the `params` argument for `embedding_lookup`. The returned tensor
  will be passed to the decoder input.
* <b>`start_tokens`</b>: `int32` vector shaped `[batch_size]`, the start tokens.
* <b>`end_token`</b>: `int32` scalar, the token that marks end of decoding.


#### Raises:


* <b>`ValueError`</b>: if `start_tokens` is not a 1D tensor or `end_token` is not a
  scalar.



## Properties

<h3 id="batch_size"><code>batch_size</code></h3>




<h3 id="sample_ids_dtype"><code>sample_ids_dtype</code></h3>




<h3 id="sample_ids_shape"><code>sample_ids_shape</code></h3>






## Methods

<h3 id="initialize"><code>initialize</code></h3>

``` python
initialize(name=None)
```




<h3 id="next_inputs"><code>next_inputs</code></h3>

``` python
next_inputs(
    time,
    outputs,
    state,
    sample_ids,
    name=None
)
```

next_inputs_fn for GreedyEmbeddingHelper.


<h3 id="sample"><code>sample</code></h3>

``` python
sample(
    time,
    outputs,
    state,
    name=None
)
```

sample for GreedyEmbeddingHelper.




