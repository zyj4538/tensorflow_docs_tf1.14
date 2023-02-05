page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.SecondOrStepTimer

## Class `SecondOrStepTimer`

Timer that triggers at most once every N seconds or once every N steps.



### Aliases:

* Class `tf.compat.v1.estimator.SecondOrStepTimer`
* Class `tf.compat.v1.train.SecondOrStepTimer`
* Class `tf.compat.v2.estimator.SecondOrStepTimer`
* Class `tf.estimator.SecondOrStepTimer`
* Class `tf.train.SecondOrStepTimer`



Defined in [`python/training/basic_session_run_hooks.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/python/training/basic_session_run_hooks.py).

<!-- Placeholder for "Used in" -->

This symbol is also exported to v2 in tf.estimator namespace. See
https://github.com/tensorflow/estimator/blob/master/tensorflow_estimator/python/estimator/hooks/basic_session_run_hooks.py

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    every_secs=None,
    every_steps=None
)
```






## Methods

<h3 id="last_triggered_step"><code>last_triggered_step</code></h3>

``` python
last_triggered_step()
```




<h3 id="reset"><code>reset</code></h3>

``` python
reset()
```




<h3 id="should_trigger_for_step"><code>should_trigger_for_step</code></h3>

``` python
should_trigger_for_step(step)
```

Return true if the timer should trigger for the specified step.


#### Args:


* <b>`step`</b>: Training step to trigger on.


#### Returns:

True if the difference between the current time and the time of the last
trigger exceeds `every_secs`, or if the difference between the current
step and the last triggered step exceeds `every_steps`. False otherwise.


<h3 id="update_last_triggered_step"><code>update_last_triggered_step</code></h3>

``` python
update_last_triggered_step(step)
```






