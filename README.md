# TeachableMachine

This is a GitHub Repository for using [Teachable Machine](https://teachablemachine.withgoogle.com/train) with StreamLit cloud. 

You will need to: 
* modify `labels.txt` 
* create and upload the `keras_model.h5` 

These are the two outputs from exporting a teachable machine image recognition model, as a Tensorflow Keras model. 

Once you have cloned this repo and added the two files, you can create an app from it on [Streamlit Cloud](https://streamlit.io/cloud)

Steps in [Teachable Machine](https://teachablemachine.withgoogle.com/train):
* Pick 2 objects and train a classification model.
* Once trained, do the following:
  1. Export model
  2. Pick Tensorflow (NOT Tensorflow.js, JavaScript is bad.) > Keras
  3. Click download model. (this will take a few minutes.)
  4. Click the fork button on GitHub (create a copy of the repository)
  5. Navigate to your labels.txt (on your repository fork) > Edit file > Change the names of the classes to your objects (eg: 0 mug 1 pencil)

Issues:
* Incompatible Tensorflow version (2.12) in Streamlit Cloud: Requires min. 2.16.2
* Tensorflow version 2.16.2 is unable to run the `keras_model.h5`. Bugs found.
