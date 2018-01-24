# AMSGrad-Tensorflow
Simple Tensorflow implementation of [AMSGrad](https://openreview.net/pdf?id=ryQu7f-RZ)

## Hyperparameter
* For the default hyperparameter, we set it to the best value in the [experiment](https://fdlm.github.io/post/amsgrad/)
* `learning_rate` = 0.01
* `beta1` = 0.9
* `beta2` = 0.99
* Depending on which network you are using, performance may be good at `beta2 = 0.999 (default)`

## Usage
```python
  from AMSGrad import AMSGrad
  
  train_op = AMSGrad(learning_rate=0.01, beta1=0.9, beta2=0.99, epsilon=1e-8).minimize(loss)
```

## Network Architecture
```python
  x = fully_connected(inputs=images, units=100)
  x = relu(x)
  logits = tf.layers.dense(inputs=x, units=10)
```
## Result (iteration = 3M)
### lr=0.1, beta1=0.9, beta2=various


### lr=0.01, beta1=0.9, beta2=various

## Author
Junho Kim
