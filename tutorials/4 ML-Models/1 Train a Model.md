## Model fit perms 

# Explanation of `model.fit()` Parameters

## `x`

- **Description**: Input data (features).
- **Type**: Numpy array, TensorFlow tensor, or list of arrays/tensors if the model has multiple inputs.
- **Example**: `x=X_train`

## `y`

- **Description**: Target data (labels).
- **Type**: Numpy array or TensorFlow tensor.
- **Example**: `y=y_train`

## `batch_size`

- **Description**: Number of samples per gradient update.
- **Type**: Integer. Default is `32`.
- **Example**: `batch_size=64`

## `epochs`

- **Description**: Number of epochs to train the model.
- **Type**: Integer. An epoch is an iteration over the entire `x` and `y` data provided.
- **Example**: `epochs=10`

## `verbose`

- **Description**: Verbosity mode, 0 (silent), 1 (progress bar), 2 (one line per epoch).
- **Type**: Integer. Default is `1`.
- **Example**: `verbose=1`

## `callbacks`

- **Description**: List of callbacks to apply during training.
- **Type**: List of `tf.keras.callbacks.Callback` instances.
- **Example**: `callbacks=[tensorboard_callback, early_stopping]`

## `validation_data`

- **Description**: Data on which to evaluate the loss and any model metrics at the end of each epoch.
- **Type**: Tuple `(x_val, y_val)` or tuple `(x_val, y_val, val_sample_weights)`.
- **Example**: `validation_data=(X_val, y_val)`

## `validation_split`

- **Description**: Fraction of the training data to be used as validation data.
- **Type**: Float between `0` and `1`.
- **Example**: `validation_split=0.1`

## `shuffle`

- **Description**: Whether to shuffle the training data before each epoch.
- **Type**: Boolean. Default is `True`.
- **Example**: `shuffle=True`

## `class_weight`

- **Description**: Optional dictionary mapping class indices (integers) to a weight (float) value to apply to the model's loss for each class.
- **Type**: Dictionary.
- **Example**: `class_weight={0: 1., 1: 2.}`

## `sample_weight`

- **Description**: Optional array of the same length as `x`, containing weights to apply to the model's loss for each sample.
- **Type**: Numpy array.
- **Example**: `sample_weight=np.ones(len(X_train))`

## `initial_epoch`

- **Description**: Epoch at which to start training (useful for resuming a previous training run).
- **Type**: Integer. Default is `0`.
- **Example**: `initial_epoch=3`

## `steps_per_epoch`

- **Description**: Total number of steps (batches of samples) before declaring one epoch finished and starting the next epoch.
- **Type**: Integer or `None`.
- **Example**: `steps_per_epoch=len(X_train) // batch_size`

## `validation_steps`

- **Description**: Total number of steps (batches of samples) to draw before stopping when performing validation at the end of every epoch.
- **Type**: Integer or `None`.
- **Example**: `validation_steps=len(X_val) // batch_size`
