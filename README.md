# Plant-Disease-Image-Classifier

Project Objective: Build Plant disease prediction system where we will train a CNN for Image classification. After training the model, we will build a simple StremLit web application where the user can upload a plant image and predict with that trained model about what that particular plant disease. Once we have the StreamLit app, it will be dockerised and deployed as a Docker container for better standards.

User can browse and paste their plant image files from their local device. After pressing "Classify" button, the model will classify the image into the classes.

Workflow:

1. Data curation - since this is a image classification task, we need proper image data in which case a Kaggle dataset will be used (will need Kaggle JSON file whch contains our Kaggle account credentials and kind of load it in Python and get the dataset through an API)

--> Link for Kaggle dataset: https://kaggle.com/datasets/abdallahalidev/plantvillage-dataset

--> Google Colab is the environment which will be used as it provides built-in GPU support compared to Jupyter notebook environment.

2. Data Processing - we will work with an image data generator class from TensorFlow where we will load the image data from the directory with appropriate classes and make it suitable for the CNN to learn from it.

3. Train-Test Split - build a pipeline for training data generator and other one for validation generator (interlinked with the image data generator method used).

4. CNN Training - Build the CNN with appropriate convolutional layers and all the dense layer required

5. Model Evaluation - once the model has been trained, we will evaluate and make sure that the model is working well and has decent accuracy.

6. StreamLit Web App - Once all the steps present in the workflow are completed, we will save the model as a file and once this model has been saved, we can build a StreamLit web app around this where we will export the trained file and load it in the StreamLit web app Python script where the user can upload their image of the plant from their device and get a prediction of classification class by the model.

7. Dockerise - create a dockerfile that has a list of instructions to build a docker image. Once the docker image has been built, we will create Docker containers out of this and can push this to some Docker repository (DockerHub) or can put it on Azure or AWS container registries.
