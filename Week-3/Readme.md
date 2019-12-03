
Validation accuracy for Base Network - 82.75

Model Definition

# Define the model
from keras.layers import SeparableConv2D
model = Sequential()
# 3x3 depthwise separable conv2d with same padding
model.add(SeparableConv2D(filters = 128, kernel_size=3, padding= 'same', activation = 'relu', input_shape = (32, 32, 3)))
# 32
model.add(BatchNormalization())
# 3x3 depthwise separable conv2d
model.add(SeparableConv2D(filters = 128, kernel_size=3, activation = 'relu')) 
# 30
model.add(BatchNormalization())
model.add(Dropout(0.2))
# 3x3 depthwise separable conv2d with dropout
model.add(SeparableConv2D(filters = 128, kernel_size=3, activation = 'relu'))
# 28
model.add(BatchNormalization())
model.add(Dropout(0.2))
# max-pool
model.add(MaxPooling2D(pool_size=(2, 2))) 
# 14
# 3x3 depthwise separable conv2d with same padding
model.add(SeparableConv2D(filters = 80, kernel_size=3, padding = 'same', activation = 'relu')) 
# 14
model.add(BatchNormalization())
model.add(Dropout(0.2))
# 3x3 depthwise separable conv2d with dropout
model.add(SeparableConv2D(filters = 96, kernel_size=3, activation = 'relu'))
# 12
model.add(BatchNormalization())
model.add(Dropout(0.2))
# 3x3 depthwise separable conv2d with dropout
model.add(SeparableConv2D(filters = 128, kernel_size=3, activation = 'relu')) 
# 10
model.add(BatchNormalization())
model.add(Dropout(0.3))
# max-pool
model.add(MaxPooling2D(pool_size=(2, 2))) 
# 5
# 3x3 depthwise separable conv2d with dropout
model.add(SeparableConv2D(filters = 160, kernel_size=3, activation = 'relu')) 
# 3
model.add(Dropout(0.3))
# 3x3 conv2D with softmax
model.add(SeparableConv2D(filters = num_classes, kernel_size=3, activation = 'softmax')) 
# 1
# flatten
model.add(Flatten())
# Compile the model
model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])

Log

Epoch 1/50
390/390 [==============================] - 75s 193ms/step - loss: 1.4373 - acc: 0.4735 - val_loss: 1.1007 - val_acc: 0.6034
Epoch 2/50
390/390 [==============================] - 72s 184ms/step - loss: 0.9793 - acc: 0.6500 - val_loss: 1.0542 - val_acc: 0.6264
Epoch 3/50
390/390 [==============================] - 72s 184ms/step - loss: 0.8455 - acc: 0.7007 - val_loss: 0.8893 - val_acc: 0.6905
Epoch 4/50
390/390 [==============================] - 71s 182ms/step - loss: 0.7571 - acc: 0.7335 - val_loss: 0.8121 - val_acc: 0.7256
Epoch 5/50
390/390 [==============================] - 71s 181ms/step - loss: 0.6873 - acc: 0.7581 - val_loss: 0.7307 - val_acc: 0.7506
Epoch 6/50
390/390 [==============================] - 71s 181ms/step - loss: 0.6374 - acc: 0.7770 - val_loss: 0.7020 - val_acc: 0.7602
Epoch 7/50
390/390 [==============================] - 71s 181ms/step - loss: 0.6003 - acc: 0.7896 - val_loss: 0.6455 - val_acc: 0.7754
Epoch 8/50
390/390 [==============================] - 71s 181ms/step - loss: 0.5710 - acc: 0.7997 - val_loss: 0.6635 - val_acc: 0.7693
Epoch 9/50
390/390 [==============================] - 71s 181ms/step - loss: 0.5469 - acc: 0.8092 - val_loss: 0.6412 - val_acc: 0.7847
Epoch 10/50
390/390 [==============================] - 71s 181ms/step - loss: 0.5216 - acc: 0.8167 - val_loss: 0.7010 - val_acc: 0.7656
Epoch 11/50
390/390 [==============================] - 71s 181ms/step - loss: 0.5049 - acc: 0.8223 - val_loss: 0.6743 - val_acc: 0.7716
Epoch 12/50
390/390 [==============================] - 71s 181ms/step - loss: 0.4908 - acc: 0.8264 - val_loss: 0.6417 - val_acc: 0.7855
Epoch 13/50
390/390 [==============================] - 71s 182ms/step - loss: 0.4728 - acc: 0.8337 - val_loss: 0.6266 - val_acc: 0.7905
Epoch 14/50
390/390 [==============================] - 71s 181ms/step - loss: 0.4584 - acc: 0.8377 - val_loss: 0.6046 - val_acc: 0.7996
Epoch 15/50
390/390 [==============================] - 71s 182ms/step - loss: 0.4441 - acc: 0.8449 - val_loss: 0.6316 - val_acc: 0.7912
Epoch 16/50
390/390 [==============================] - 71s 183ms/step - loss: 0.4358 - acc: 0.8460 - val_loss: 0.6777 - val_acc: 0.7727
Epoch 17/50
390/390 [==============================] - 71s 183ms/step - loss: 0.4223 - acc: 0.8509 - val_loss: 0.5666 - val_acc: 0.8102
Epoch 18/50
390/390 [==============================] - 71s 182ms/step - loss: 0.4140 - acc: 0.8538 - val_loss: 0.6100 - val_acc: 0.8029
Epoch 19/50
390/390 [==============================] - 71s 183ms/step - loss: 0.4010 - acc: 0.8576 - val_loss: 0.6740 - val_acc: 0.7869
Epoch 20/50
390/390 [==============================] - 72s 184ms/step - loss: 0.3943 - acc: 0.8599 - val_loss: 0.5879 - val_acc: 0.8122
Epoch 21/50
390/390 [==============================] - 72s 184ms/step - loss: 0.3857 - acc: 0.8626 - val_loss: 0.6130 - val_acc: 0.8039
Epoch 22/50
390/390 [==============================] - 72s 184ms/step - loss: 0.3771 - acc: 0.8657 - val_loss: 0.5679 - val_acc: 0.8150
Epoch 23/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3702 - acc: 0.8665 - val_loss: 0.6225 - val_acc: 0.8055
Epoch 24/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3628 - acc: 0.8704 - val_loss: 0.5949 - val_acc: 0.8081
Epoch 25/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3535 - acc: 0.8738 - val_loss: 0.6009 - val_acc: 0.8183
Epoch 26/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3486 - acc: 0.8764 - val_loss: 0.5713 - val_acc: 0.8219
Epoch 27/50
390/390 [==============================] - 71s 181ms/step - loss: 0.3441 - acc: 0.8759 - val_loss: 0.6306 - val_acc: 0.8010
Epoch 28/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3360 - acc: 0.8811 - val_loss: 0.7309 - val_acc: 0.7854
Epoch 29/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3336 - acc: 0.8821 - val_loss: 0.6346 - val_acc: 0.8046
Epoch 30/50
390/390 [==============================] - 71s 181ms/step - loss: 0.3290 - acc: 0.8816 - val_loss: 0.6276 - val_acc: 0.8076
Epoch 31/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3258 - acc: 0.8840 - val_loss: 0.6023 - val_acc: 0.8176
Epoch 32/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3170 - acc: 0.8865 - val_loss: 0.5767 - val_acc: 0.8204
Epoch 33/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3131 - acc: 0.8886 - val_loss: 0.6397 - val_acc: 0.8112
Epoch 34/50
390/390 [==============================] - 71s 182ms/step - loss: 0.3044 - acc: 0.8919 - val_loss: 0.6576 - val_acc: 0.8006
Epoch 35/50
390/390 [==============================] - 72s 184ms/step - loss: 0.3065 - acc: 0.8899 - val_loss: 0.6095 - val_acc: 0.8176
Epoch 36/50
390/390 [==============================] - 71s 183ms/step - loss: 0.3042 - acc: 0.8894 - val_loss: 0.6104 - val_acc: 0.8183
Epoch 37/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2985 - acc: 0.8928 - val_loss: 0.6566 - val_acc: 0.8062
Epoch 38/50
390/390 [==============================] - 71s 183ms/step - loss: 0.2911 - acc: 0.8949 - val_loss: 0.6165 - val_acc: 0.8179
Epoch 39/50
390/390 [==============================] - 72s 184ms/step - loss: 0.2905 - acc: 0.8957 - val_loss: 0.5721 - val_acc: 0.8249
Epoch 40/50
390/390 [==============================] - 72s 184ms/step - loss: 0.2849 - acc: 0.8974 - val_loss: 0.6253 - val_acc: 0.8142
Epoch 41/50
390/390 [==============================] - 72s 184ms/step - loss: 0.2839 - acc: 0.8975 - val_loss: 0.6053 - val_acc: 0.8182
Epoch 42/50
390/390 [==============================] - 71s 181ms/step - loss: 0.2824 - acc: 0.8981 - val_loss: 0.6103 - val_acc: 0.8166
Epoch 43/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2745 - acc: 0.9014 - val_loss: 0.6197 - val_acc: 0.8164
Epoch 44/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2719 - acc: 0.9025 - val_loss: 0.6048 - val_acc: 0.8227
Epoch 45/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2701 - acc: 0.9029 - val_loss: 0.6313 - val_acc: 0.8229
Epoch 46/50
390/390 [==============================] - 71s 181ms/step - loss: 0.2674 - acc: 0.9038 - val_loss: 0.7484 - val_acc: 0.7893
Epoch 47/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2610 - acc: 0.9052 - val_loss: 0.6052 - val_acc: 0.8222
Epoch 48/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2637 - acc: 0.9059 - val_loss: 0.5655 - val_acc: 0.8349
Epoch 49/50
390/390 [==============================] - 71s 182ms/step - loss: 0.2598 - acc: 0.9054 - val_loss: 0.6467 - val_acc: 0.8175
Epoch 50/50
390/390 [==============================] - 71s 181ms/step - loss: 0.2550 - acc: 0.9091 - val_loss: 0.5686 - val_acc: 0.8344


