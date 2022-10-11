<h1 align="center">
  <br>
 :house_with_garden: Beating Boston Housing Kaggle Competition. :european_post_office: <br>
</h1>

<p align="center">
  <a href="#about-paper">About Competition</a> •
  <a href="#about-methods">About Methods</a> •
  <a href="#result">Result</a> •
  <a href="#feedback">Feedback</a>
</p>

## About Competition
We're going to use the Boston Housing dataset and to teach a model to predict the MEDV (median value) from the other features. The train.csv file contains the MEDV value, but the test.csv doesn't. Then we export our predictions for MEDV into a csv file, following the format in the provided sampleSubmission.csv file. The predictions will be scored against a held-out dataset.

## About Methods
I've used a simple three-layer fully-connected neural network:
```python
model4 = tf.keras.Sequential([
                              tf.keras.layers.Dense(100, activation = 'relu'),
                              tf.keras.layers.Dense(100, activation = 'relu'),
                              tf.keras.layers.Dense(1)
])

model4.compile(optimizer = tf.keras.optimizers.Adam(lr = 0.001),
               loss = 'mse',
               metrics = 'mae')

model4.fit(df, target, 
                      epochs = 1200,                     
                      verbose = 0,
                      callbacks=[PrintSmile()])
```



## Result
> **Note**
> Because that's a late submission, you'll not see me on leaderboard. So I publish result here as a screenshot. You can rerun this model and check the result.

![result](https://github.com/boramorka/usercontent/blob/main/boston-housing/kaggle_submission.png?raw=true)

## Feedback
:person_in_tuxedo: Feel free to send me feedback on [Telegram](https://t.me/boramorka). Feature requests are always welcome. 

:abacus: [Check my other projects.](https://github.com/boramorka)