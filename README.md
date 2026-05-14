The data notebook contains the data preperation.
We use the haarcascades algorithm to crop out faces from the images which is honestly not that great. It doesnt recognize a lot of the faces. 
Then we apply some data augmentation to make sure that the model doesnt overfit.
I've optimised the training, the best i can. I tried using a lr scheduler but it wasnt working.

If u wanna improve performance, maybe try a wavelet tranform before prediction for better feature extraction.
The model has ~8.5 million parameters and is a classic CNN model.



1. Data Collection
    The data collection part is a bit more tricky than we would think because a huge huge hugeee part of F1 driver images have their faces covered by their helmets and in many photos their driving their car, in all these cases the face of the driver would not be visible, which is why we need a huge amount of scrapped data(~2000 images) per driver. After applying the haarcascades, it reduces to a few hundred images. The data has been scrapped from getty images using fatkun image scrapper.

2. Data Processing
   The data collected is filled with garbage images where the face is not visible. Apply haarcascades and save only images with a face and 2 eyes.
   Then manually go over the chosen images and delete all images that is not of the particular driver.
   Applying a wavelet tranform might help improve accuracy.

4. Model
   The model I have implemented is a CNN with a few layers. It performs relatively well on the data and it worked well on images i pulled from the internet which were not part of the testing data nor the training data.

   


