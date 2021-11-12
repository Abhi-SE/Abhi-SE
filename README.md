# Federated-Learning #

## Federated Learning on Handwritten Digit MNIST Dataset ##

- **Dataset** : 
The Handwritten MNIST Dataset contains 70,000 images which include 60,000 training images and 10,000 testing images. Each example is a 28x28 grayscale image which is associated with 10 different classes. This dataset is divided into 5 training batches and 1 test batch. The batch size is 10,000.

- **Execution Process** : 
For the execution of image classification of Handwritten MNIST data using Federated Learning, we have manually dividing the data of training of 60000 images into 5 devices and later on trained on 12000 images for each devices and aggregated them into one single global model.

  - **Manual Process** : 
  The data is first divided into 5 clients, having 10,000 training images each. The images are normalized. Thereafter we instantiated the client models. For every client, the test images are common (10,000). For this we have used Adam optimizer and Sparse Categorical Cross Entropy as a loss function. Next we train our client models and extract out the test accuracy for each client. Next we use the federated learning for training our client models for 50 communication rounds. Here we extracted the weights of each model and assigned the mean average of the weights to every model and train again. Thereafter we have trained without using federated learning and record the results.
  
    Following are the results before updating the parameters:
  
  | Clients  | Training Accuracy On Individual Data(in %) |  Testing Accuracy on Individual Data(in %) |
  | ------------- | ------------- | ------------ |
  | Client1  | 78.18  | 81.84 |
  | Client2  | 77.75  | 80.75 |
  | Client3  | 77.93  | 81.7 |
  | Client4  | 78.75  | 79.11 |
  | Client5  | 78.15  | 78.86 |
 
 
  We have found that the accuracy of the model which was trained using federated learning gives accuracy 87.40% while without federated learning the accuracy is around 84%. So federated learning not only provides privacy but also gives more accurate results in a fast manner.



