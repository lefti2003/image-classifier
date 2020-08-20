# image-classifier
Python application that can train an Image Classifier on a dataset, then predict new images using the trained model
There are 4 files in this repository.
1. Image Classifier Project.html
  This is a html file of an ipython jupyter notebook for an Image Classifier. The Classifier performs certain functions such as
  1. Load Data
  2. Defines Transforms for training, validation and testing sets
  3. Load Data sets for training, validation and testing
  4. Define a default Network vgg16 for this case.
  5. Train the network-> print the epochs, train loss, Validation loss, Validation Accuracy
  6. Test the network->  print the epochs, train loss, Test loss, Test Accuracy
  7. Save the checkpoint
  8. Load the checkpoint
  9. Image preprocessing
  10. Class Prediction and Sanity Checking
2. Image Classifier Project.ipynb
  This is the ipython jupyter notebook for the above mentioned Image Classifier
3. train.py
  This is a python script that will train a new network on a dataset and save the model as a checkpoint.
  Usage 1 (Basic):python train.py data_directory
  Usage 2 (Save checkpoints) :python train.py data_directory --save_dir save_directory
  Usage 3 (Choose architecture):python train.py data_dir --arch "vgg13"
  Usage 4 (Set hyperparameters):python train.py data_dir --learning_rate 0.01 --hidden_units 512 --epochs 20
  Usage 5 (Use GPU for training):python train.py data_dir --gpu
4. predict.py
 This is a python script that uses a trained network to predict the class for an input image.
  Usage 1 (Basic):python predict.py /path/to/image checkpoint
  Usage 2 (Return K most likely classes): python predict.py input checkpoint --top_k 3
  Usage 3 (use a mapping of categoris to real names): python predict.py input checkpoint --category_names cat_to_name.json
  Usage 4 (Use GPU for inference): python predict.py input checkpoint --gpu
