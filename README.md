# Venture Funding with Deep Learning

This Jupyter notebook creates, trains, and evaluates three binary classification models using a deep neural network.  These models are used to predict whether the Alphabet Soup company's funding applicants will be successful.

Specifically, it carries out the following steps:
1. Prepares historical Alphabet Soup funding data by encoding and scaling the data as needed.
2. Compiles and evaluates a binary classification model using a neural network.
3. Optimizes the model, creating and evaluating two alternative models.

---

## Technologies

This Jupyter notebook makes use of the following Python libraries:
* Pandas
* TensorFlow 2.0
* Keras (high-level API for TensorFlow)

---

## Installation Guide

To use this notebook:
* Install Jupyter lab Version 2.3.1 and Python 3.7.
* Pandas should already be included in the dev environment distribution.  If not, install it.
* Install TensorFlow 2.0.  Keras is included with TensorFlow 2.0.

Open the notebook in Jupyter lab and you can rerun the analysis.

---

## Deep Neural Network Models

Overall, all three models performed similarly.  Alternative Model 1 was minimally better, but all had an accuracy of about 72.9-73% when evaluated using the test data.

### Original Model
#### Summary
```
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense (Dense)                (None, 58)                6786      
_________________________________________________________________
dense_1 (Dense)              (None, 29)                1711      
_________________________________________________________________
dense_2 (Dense)              (None, 1)                 30        
=================================================================
Total params: 8,527
Trainable params: 8,527
Non-trainable params: 0
_________________________________________________________________

```
#### Evaluation Results with Test Data
```
Original Model Results
268/268 - 0s - loss: 0.5545 - accuracy: 0.7294
Loss: 0.554536759853363, Accuracy: 0.7294460535049438
```

### Alternative Model 1
#### Summary
```
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense_3 (Dense)              (None, 39)                4563      
_________________________________________________________________
dense_4 (Dense)              (None, 19)                760       
_________________________________________________________________
dense_5 (Dense)              (None, 19)                380       
_________________________________________________________________
dense_6 (Dense)              (None, 1)                 20        
=================================================================
Total params: 5,723
Trainable params: 5,723
Non-trainable params: 0
```
#### Evaluation Results with Test Data
```
Alternative Model 1 Results
268/268 - 0s - loss: 0.5501 - accuracy: 0.7299
Loss: 0.5501484274864197, Accuracy: 0.729912519454956
```

### Alternative Model 2
#### Summary
```
Model: "sequential_2"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
dense_7 (Dense)              (None, 78)                9126      
_________________________________________________________________
dense_8 (Dense)              (None, 52)                4108      
_________________________________________________________________
dense_9 (Dense)              (None, 1)                 53        
=================================================================
Total params: 13,287
Trainable params: 13,287
Non-trainable params: 0
_________________________________________________________________
```
#### Evaluation Results with Test Data
```
Alternative Model 2 Results
268/268 - 0s - loss: 0.5626 - accuracy: 0.7293
Loss: 0.5626142621040344, Accuracy: 0.7293294668197632
```

---

## Contributors

Michael Danenberg

---

## License

MIT