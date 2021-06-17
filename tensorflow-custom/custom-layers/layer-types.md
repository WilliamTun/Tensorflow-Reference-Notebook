# Common layers
Layer is a class that collects parameters to encapsulate:
- state (variables - eg weight and constant) 
- computation (forward pass - eg Y = weight * X + constant)

to achieve the layers purpose. 

## Convolutional
- Conv1D/2D/3D
- SeparableConv2D
- DepthwiseConv2D
## Recurrent
- LSTM
- GRU
## Pooling
- MaxPooling2D
- AveragePooling2D
- GlobalAveragePooling2D
## Merge
- Add
- Subtract
- Multiply
## Activation
- LeakyReLU
- PReLU
- ELU
## Core
- Activation
- Lambda
- Input
- Dense
- Dropout
- BatchNormalization