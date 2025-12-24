
Project Title : **Lightweight CNN for Image Classification with Preprocessing,**
Augmentation, and Feature Visualization
First, open the provided Jupyter/Colab notebook the .ipynb or .py file for this project in your local environment and ensure a GPU runtime is enabled (in ths case it is in Google Colab: Runtime → Change runtime type → GPU).
Here, we used python programming code for this project here in the Google Colab Environment.
Then Install the required Python libraries (TensorFlow/Keras, NumPy, scikit-learn, OpenCV, Matplotlib, Seaborn) if they are not already available in the local producable environment.
And next the code Runs the initial cells that download CIFAR-10 dataset , then the code performs stratified sampling to create a 10,000-image subset, and automatically organize it into separate train, val, and test folders by class.
Next Execute the preprocessing cells in the following .ipynb file to enable CLAHE-based contrast enhancement, normalization, and data augmentation on our dataset which we created earlier from CIFAR-10 (random flips, rotations, translations, and zoom) inside the TensorFlow data pipeline.
Then Run the model-building and training cells to construct the lightweight CNN (three convolutional blocks with global average pooling) and train it on the prepared training set while monitoring validation performance with early stopping.
After training, run the evaluation cells to compute test accuracy, precision, recall, F1-score, and to generate the confusion matrix summarizing class-wise performance on the 1,500-image test data set.

Finally, we run the feature map visualization cells to produce plots of training/validation accuracy and loss over the continous running epochs and feature-map visualizations images from different convolutional layers, which illustrate what patterns the CNN has learned at each depth.
