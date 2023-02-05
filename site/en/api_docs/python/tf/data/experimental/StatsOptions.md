page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.data.experimental.StatsOptions

## Class `StatsOptions`

Represents options for collecting dataset stats using `StatsAggregator`.



### Aliases:

* Class `tf.compat.v1.data.experimental.StatsOptions`
* Class `tf.compat.v2.data.experimental.StatsOptions`
* Class `tf.data.experimental.StatsOptions`



Defined in [`python/data/experimental/ops/stats_options.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/data/experimental/ops/stats_options.py).

<!-- Placeholder for "Used in" -->

You can set the stats options of a dataset through the `experimental_stats`
property of <a href="../../../tf/data/Options"><code>tf.data.Options</code></a>; the property is an instance of
<a href="../../../tf/data/experimental/StatsOptions"><code>tf.data.experimental.StatsOptions</code></a>. For example, to collect latency stats
on all dataset edges, use the following pattern:

```python
aggregator = tf.data.experimental.StatsAggregator()

options = tf.data.Options()
options.experimental_stats.aggregator = aggregator
options.experimental_stats.latency_all_edges = True
dataset = dataset.with_options(options)
```

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__()
```






## Properties

<h3 id="aggregator"><code>aggregator</code></h3>

Associates the given statistics aggregator with the dataset pipeline.


<h3 id="counter_prefix"><code>counter_prefix</code></h3>

Prefix for the statistics recorded as counter.


<h3 id="latency_all_edges"><code>latency_all_edges</code></h3>

Whether to add latency measurements on all edges. Defaults to False.


<h3 id="prefix"><code>prefix</code></h3>

Prefix to prepend all statistics recorded for the input `dataset` with.




## Methods

<h3 id="__eq__"><code>__eq__</code></h3>

``` python
__eq__(other)
```




<h3 id="__ne__"><code>__ne__</code></h3>

``` python
__ne__(other)
```






