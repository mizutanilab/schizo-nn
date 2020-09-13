# Schizophrenia-mimcking layer
This layer seems to outperform fully connected layer. We have experienced it in many examples.

## How to use the schizophrenia layer in your network
1. Download 'schizo.py' file to your working directory where your *.py file is placed.
2. Replace 'Dense' layer with Schizo layer like this: 
```
import schizo as Schizo
model = keras.Sequential([
  layers.Flatten(),
  Schizo(512, reduction_ratio=0.5, form='diagonal', activation='relu', kernel_initializer='he_normal'),
  # layers.Dense(512, activation='relu', kernel_initializer='he_normal'),
  layers.Dense(num_class, activation='softmax')
])
```
In this example, the Dense hidden layer were commented out to replace it with a Schizo layer of 50% parameter reduction. You can set the reduction ratio using arguemnt 'reduction_ratio'. Parameter reduction of 50-80% seems to give good results. We recommend 50% as a first choice. 

## Sciprts used for generating our figures
