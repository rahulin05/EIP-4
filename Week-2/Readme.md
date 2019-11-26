Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 15s 257us/step - loss: 0.3395 - acc: 0.8780 - val_loss: 0.0653 - val_acc: 0.9796
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 9s 156us/step - loss: 0.1514 - acc: 0.9391 - val_loss: 0.0475 - val_acc: 0.9849
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 9s 155us/step - loss: 0.1323 - acc: 0.9444 - val_loss: 0.0410 - val_acc: 0.9863
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 9s 154us/step - loss: 0.1188 - acc: 0.9482 - val_loss: 0.0330 - val_acc: 0.9903
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 10s 159us/step - loss: 0.1143 - acc: 0.9486 - val_loss: 0.0318 - val_acc: 0.9898
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 9s 155us/step - loss: 0.1054 - acc: 0.9518 - val_loss: 0.0250 - val_acc: 0.9923
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 9s 154us/step - loss: 0.0991 - acc: 0.9542 - val_loss: 0.0249 - val_acc: 0.9920
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 9s 154us/step - loss: 0.0991 - acc: 0.9523 - val_loss: 0.0262 - val_acc: 0.9922
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 9s 152us/step - loss: 0.0977 - acc: 0.9526 - val_loss: 0.0265 - val_acc: 0.9926
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 9s 153us/step - loss: 0.0935 - acc: 0.9547 - val_loss: 0.0266 - val_acc: 0.9925
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 9s 155us/step - loss: 0.0916 - acc: 0.9551 - val_loss: 0.0235 - val_acc: 0.9928
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 9s 154us/step - loss: 0.0888 - acc: 0.9559 - val_loss: 0.0232 - val_acc: 0.9932
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 9s 153us/step - loss: 0.0910 - acc: 0.9549 - val_loss: 0.0251 - val_acc: 0.9934
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 9s 155us/step - loss: 0.0862 - acc: 0.9570 - val_loss: 0.0268 - val_acc: 0.9928
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 9s 157us/step - loss: 0.0836 - acc: 0.9565 - val_loss: 0.0244 - val_acc: 0.9933
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 9s 154us/step - loss: 0.0865 - acc: 0.9556 - val_loss: 0.0266 - val_acc: 0.9937
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 9s 156us/step - loss: 0.0865 - acc: 0.9560 - val_loss: 0.0216 - val_acc: 0.9943
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 9s 155us/step - loss: 0.0818 - acc: 0.9580 - val_loss: 0.0235 - val_acc: 0.9935
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 9s 155us/step - loss: 0.0836 - acc: 0.9581 - val_loss: 0.0246 - val_acc: 0.9938
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 9s 155us/step - loss: 0.0838 - acc: 0.9565 - val_loss: 0.0233 - val_acc: 0.9933
Out[37]:
<keras.callbacks.History at 0x7f59ee57f278>
In [38]:
score = model.evaluate(X_test, Y_test, verbose=0)
print(score)
[0.023308577030837295, 0.9933]

Stratergy - removed  the use of bias in each Conv2D layer. Removed last two batch normalization

