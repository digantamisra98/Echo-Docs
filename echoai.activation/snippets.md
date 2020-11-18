# Snippets

#### Code Examples:

Sample scripts are provided in [Smoke\_tests](/Smoke_tests) folder.

**PyTorch**:

```python
# import PyTorch
import torch

# import activation function from echoAI
from echoAI.Activation.Torch.mish import Mish

# apply activation function
mish = Mish()
t = torch.tensor(0.1)
t_mish = mish(t)
```

**TensorFlow Keras**:

```python
#import tensorflow
import tensorflow as tf
from tensorflow.keras import layers
from tensorflow.keras.layers import Dense, Flatten

# import activation function from echoAI
from echoAI.Activation.TF_Keras.custom_activation import Mish

model = tf.keras.Sequential([
    layers.Flatten(),
    layers.Dense(128, input_shape=(784,)),
    Mish(), # use the activation function
    layers.Dense(64, activation='relu'),
    layers.Dense(10, activation='softmax')])

# Compile the model
model.compile(optimizer = "adam", loss = "mean_squared_error", metrics = ["accuracy"])

# Fit the model
model.fit(x = X_train, y = y_train, epochs = 3, batch_size = 128
```

