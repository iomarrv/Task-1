# Task-1
import numpy as np
x = np.arrange(1,1001)
y = x * 2
print(x)
print(y)

import tensorflow as tf
model = tf.keras.sequential ([
tf.keras.layers.Dense(1),
tf.keras.layers.Dense(10),
tf.keras.layers.Dense(10),
tf.keras.layers.Dense(1)
])
model.compile(optimizer='adam' , loss = 'mse')
model.fit(x,y, epochs =200)
model.predict(np.array([500]))
