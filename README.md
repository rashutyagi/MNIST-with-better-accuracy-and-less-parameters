# MNIST-with-better-accuracy-and-less-parameters

# I was able to get the accuracy of 99.40 in 15th epoch and using 10540 trainable parameters


In this repository I have tried to acheive an accuracy of 99.40% on MNIST data using only 10k parameters.

In this code the strategy which I used is that I used The MaxPooling immediately after my first convolution and used maxpooling again after 4 more convolutions and this helped my to reduce the number of parameters which I was using before.In addition to that I have used the dropouts and Batchnormalizations also along with the above mentioned concept.


Model architecture is like 

Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_153 (Conv2D)          (None, 26, 26, 16)        144       
_________________________________________________________________
batch_normalization_124 (Bat (None, 26, 26, 16)        64        
_________________________________________________________________
dropout_110 (Dropout)        (None, 26, 26, 16)        0         
_________________________________________________________________
max_pooling2d_23 (MaxPooling (None, 13, 13, 16)        0         
_________________________________________________________________
conv2d_154 (Conv2D)          (None, 11, 11, 32)        4640      
_________________________________________________________________
batch_normalization_125 (Bat (None, 11, 11, 32)        128       
_________________________________________________________________
dropout_111 (Dropout)        (None, 11, 11, 32)        0         
_________________________________________________________________
conv2d_155 (Conv2D)          (None, 11, 11, 10)        330       
_________________________________________________________________
batch_normalization_126 (Bat (None, 11, 11, 10)        40        
_________________________________________________________________
dropout_112 (Dropout)        (None, 11, 11, 10)        0         
_________________________________________________________________
conv2d_156 (Conv2D)          (None, 9, 9, 16)          1456      
_________________________________________________________________
batch_normalization_127 (Bat (None, 9, 9, 16)          64        
_________________________________________________________________
dropout_113 (Dropout)        (None, 9, 9, 16)          0         
_________________________________________________________________
conv2d_157 (Conv2D)          (None, 7, 7, 16)          2320      
_________________________________________________________________
batch_normalization_128 (Bat (None, 7, 7, 16)          64        
_________________________________________________________________
dropout_114 (Dropout)        (None, 7, 7, 16)          0         
_________________________________________________________________
max_pooling2d_24 (MaxPooling (None, 3, 3, 16)          0         
_________________________________________________________________
conv2d_158 (Conv2D)          (None, 1, 1, 10)          1450      
_________________________________________________________________
batch_normalization_129 (Bat (None, 1, 1, 10)          40        
_________________________________________________________________
dropout_115 (Dropout)        (None, 1, 1, 10)          0         
_________________________________________________________________
flatten_20 (Flatten)         (None, 10)                0         
_________________________________________________________________
activation_20 (Activation)   (None, 10)                0         
=================================================================
Total params: 10,740
Trainable params: 10,540
Non-trainable params: 200



After evaluation the logs are like this 

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 16s 267us/step - loss: 0.5288 - acc: 0.8548 - val_loss: 0.1277 - val_acc: 0.9780
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 8s 133us/step - loss: 0.2703 - acc: 0.9165 - val_loss: 0.0905 - val_acc: 0.9844
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 8s 130us/step - loss: 0.2147 - acc: 0.9334 - val_loss: 0.0609 - val_acc: 0.9883
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 8s 127us/step - loss: 0.1854 - acc: 0.9397 - val_loss: 0.0553 - val_acc: 0.9899
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 8s 127us/step - loss: 0.1674 - acc: 0.9421 - val_loss: 0.0474 - val_acc: 0.9911
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 8s 133us/step - loss: 0.1538 - acc: 0.9463 - val_loss: 0.0431 - val_acc: 0.9915
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 8s 130us/step - loss: 0.1446 - acc: 0.9479 - val_loss: 0.0354 - val_acc: 0.9915
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 8s 131us/step - loss: 0.1340 - acc: 0.9512 - val_loss: 0.0344 - val_acc: 0.9929
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 8s 133us/step - loss: 0.1281 - acc: 0.9529 - val_loss: 0.0317 - val_acc: 0.9933
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 8s 132us/step - loss: 0.1225 - acc: 0.9530 - val_loss: 0.0286 - val_acc: 0.9928
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 8s 129us/step - loss: 0.1206 - acc: 0.9526 - val_loss: 0.0276 - val_acc: 0.9935
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 8s 126us/step - loss: 0.1166 - acc: 0.9535 - val_loss: 0.0284 - val_acc: 0.9932
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 8s 128us/step - loss: 0.1142 - acc: 0.9546 - val_loss: 0.0258 - val_acc: 0.9928
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 8s 134us/step - loss: 0.1124 - acc: 0.9543 - val_loss: 0.0262 - val_acc: 0.9929
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 8s 135us/step - loss: 0.1095 - acc: 0.9546 - val_loss: 0.0251 - val_acc: 0.9940
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 8s 133us/step - loss: 0.1085 - acc: 0.9547 - val_loss: 0.0255 - val_acc: 0.9923
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 8s 136us/step - loss: 0.1043 - acc: 0.9558 - val_loss: 0.0247 - val_acc: 0.9936
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 8s 132us/step - loss: 0.1058 - acc: 0.9543 - val_loss: 0.0233 - val_acc: 0.9936
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 8s 127us/step - loss: 0.1044 - acc: 0.9545 - val_loss: 0.0237 - val_acc: 0.9931
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 8s 130us/step - loss: 0.1027 - acc: 0.9553 - val_loss: 0.0233 - val_acc: 0.9939
<keras.callbacks.History at 0x7fc17dca7400>


# I was able to get the accuracy of 99.40 in 15th epoch and using 10540 trainable parameters
