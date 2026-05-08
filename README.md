The data notebook contains the data preperation.
We use the haarcascades algorithm to crop out faces from the images which is honestly not that great. It doesnt recognize a lot of the faces. 
Then we apply some data augmentation to make sure that the model doesnt overfit.
I've optimised the training, the best i can. I tried using a lr scheduler but it wasnt working.

If u wanna improve performance, maybe try a wavelet tranform before prediction for better feature extraction.
The model has ~8.5 million parameters and is a classic CNN model.
