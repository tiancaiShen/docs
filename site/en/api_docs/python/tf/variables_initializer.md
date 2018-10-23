

page_type: reference
<style> table img { max-width: 100%; } </style>


<!-- DO NOT EDIT! Automatically generated file. -->


# tf.variables_initializer

### Aliases:

* `tf.initializers.variables`
* `tf.variables_initializer`

``` python
tf.variables_initializer(
    var_list,
    name='init'
)
```



Defined in [`tensorflow/python/ops/variables.py`](https://www.github.com/tensorflow/tensorflow/blob/r1.7/tensorflow/python/ops/variables.py).

See the guide: [Variables > Variable helper functions](../../../api_guides/python/state_ops#Variable_helper_functions)

Returns an Op that initializes a list of variables.

After you launch the graph in a session, you can run the returned Op to
initialize all the variables in `var_list`. This Op runs all the
initializers of the variables in `var_list` in parallel.

Calling `initialize_variables()` is equivalent to passing the list of
initializers to `Group()`.

If `var_list` is empty, however, the function still returns an Op that can
be run. That Op just has no effect.

#### Args:

* <b>`var_list`</b>: List of `Variable` objects to initialize.
* <b>`name`</b>: Optional name for the returned operation.


#### Returns:

An Op that run the initializers of all the specified variables.