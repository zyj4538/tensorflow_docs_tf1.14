page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.VariableDeviceChooser

## Class `VariableDeviceChooser`

Device chooser for variables.





Defined in [`contrib/framework/python/ops/variables.py`](https://github.com/tensorflow/tensorflow/tree/r1.14/tensorflow/contrib/framework/python/ops/variables.py).

<!-- Placeholder for "Used in" -->

When using a parameter server it will assign them in a round-robin fashion.
When not using a parameter server it allows GPU or CPU placement.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    num_tasks=0,
    job_name='ps',
    device_type='CPU',
    device_index=0,
    replica=None
)
```

Initialize VariableDeviceChooser.


#### Usage:

To use with 2 parameter servers:
  VariableDeviceChooser(2)

To use without parameter servers:
  VariableDeviceChooser()
  VariableDeviceChooser(device_type='GPU') # For GPU placement



#### Args:


* <b>`num_tasks`</b>: number of tasks.
* <b>`job_name`</b>: String, a name for the parameter server job.
* <b>`device_type`</b>: Optional device type string (e.g. "CPU" or "GPU")
* <b>`device_index`</b>: int.  Optional device index.  If left unspecified, device
  represents 'any' device_index.



## Methods

<h3 id="__call__"><code>__call__</code></h3>

``` python
__call__(op)
```






