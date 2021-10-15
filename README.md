# EVA7
1) Data Generation strategy:-The Random number is getting generated using the 'Range' and 'Random' function in Python. The list of random number is then converted into a trensor to be passed on to the network for comparing with the actual labels. This will help us arrive at the number of correct predictions.

2) Input Combination:-The image from the MNIST database and the random number have been combined at the output layer.

3) Result evaluation:-The predictions are compared to the actual labels to arrive at the number of correct predictions. There are 2 methods to arrive at the number.  1) **prediction.argmax(dim=1).eq(labels)** 2) write a function **def get_num_correct(prediction, labels):    return prediction.argmax(dim=1).eq(labels).sum().item()**.

4) The Neural Network predicted 1 correct label. The prediction values were compared with the actual labels to arrive at the result.

5) Loss function is the method to calculate the prediction error that occurs as part of arriving at correct predictions. We need to minimize this error using an optimization function. We have to deal with the  **Classification** loss in the model since we are dealing with categorical values(predicting 0-9 digits). We have used **Cross Entropy loss** as the loss fucntion as it is the most commonly used and a preferred loss fucntion for classification problems. Another loss function that can be used for binary classification is **Hinge Loss** but for that target values need to be in the set {-1, 1} which is not in our case.

![Screenshot (15)](https://user-images.githubusercontent.com/57353992/137544223-3b518361-09a9-4245-8d5d-914430369286.png)
