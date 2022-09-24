# FaceRec

### Face Recognition App that learns to recognise and verify your face


## Architecture microscope
- Trained using [Siamese Neural Network](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf)
- This model uses two sets of Neural Layers that receive two different images each. These two layers are completeley identical to each other (Like siamese twins), whose output is passed through the L1 distance layer.
- The images with the face to be verified are passed through one of the embedding layer (input embedding) and the images with both positive (image with face to be recognised) and negative(image containing faces other than the face to be recognised) are passed through the other layer (validation embedding).
- The L1 distance layer finds the absolute distance between the outputs of the twin neural nets to compare the amount of difference between the two images.
- The distance layer learns to find the distance between the false image and positive images so as to be able to verify the input accurately.


## Dataset open_file_folder
- The negatives were obtained from the [Labeled Faces in the Wild (LFW)](https://www.cs.cmu.edu/~rsalakhu/papers/oneshot1.pdf) dataset
- The positives were obtained using OpenCV to capture large number of images from the webcam

## Final UI

The model was deployed to give it's output on a simple app made using Kivy

![UI](/Assets/UI.png)
