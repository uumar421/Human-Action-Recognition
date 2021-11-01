# Human-Action-Recognition
Human activity recognition, or HAR for short, is a broad field of study concerned with identifying
the specific movement or action of a person based on sensor data.

Movements are often typical activities performed indoors, such as walking, talking, standing, and sitting. 
They may also be more focused activities such as those types of activities performed in a kitchen or on a factory floor.

The sensor data may be remotely recorded, such as video, radar, or other wireless methods.
Alternately, data may be recorded directly on the subject such as by carrying custom hardware or smart phones that have accelerometers and gyroscopes.

We will discover the problem of human activity recognition and the deep learning methods that are achieving state-of-the-art performance on this problem.

  - Activity recognition is the problem of predicting the movement of a person, often indoors, based on sensor data, such as an accelerometer in a smartphone.
  - Streams of sensor data are often split into subs-sequences called windows, and each window is associated with a broader activity, called a sliding window approach.
  - Convolutional neural networks and long short-term memory networks, and perhaps both together, are best suited to learning features from raw sensor data and predicting the       associated movement.

## Project Summary
 An android application is built that uses the phone camera to record a video and predict the activity being performed. As backend, a model consisting of Convolutional Neural Network (CNN) is deployed. The CNN model comprises mainly of 2D convolutional layers with relu activations, followed by 2D max pooling layers. The dataset used for training consists of 11 folders (which are also the classes). The classes are as follows: 
 
 1. Breakdancing 
 2. Calligraphy 
 3. Celebrating 
 4. Claypotterymaking
 5. Climbingarope 
 6. Cookingoncampfire 
 7. Eatingicecream 
 8. Golfdriving 
 9. Pushup 
 10. Raisingeyebrows 
 11. Ridingscooter
 
 
### Link to dataset:
 
        https://drive.google.com/u/0/uc?export=download&confirm=-fln&id=1TPHNa6iwwJr0i9JmzN-c3YAf_tn7cwKz
        
  The dataset is split for training (80%) and validation (20%).

### Summary of CNN_Model:

![image](https://user-images.githubusercontent.com/69485235/139669743-4f1e5186-006d-401f-9726-0269c0f4dfbd.png)

- Adam Optimizer and Sparse Categorical Crossentropy loss function are used in the CNN. 
- The model is trained for a total of 10 epochs. After that, the model starts to overfit.
- The overall validation accuracy after 10th epoch is 98.58%. The training and validation loss and accuracy are plotted using matplotlib
- The model is saved in h5 format. Using the model, prediction is made on a youtube video by providing the URL of the video to the network.
- The h5 model is then transformed into tf.lite format in order to use it with android application.
- Android application is created in Android Studio (SDK) using Java programming language.
- The android application uses the camera of phone and predicts the activity (label) being performed in it.

## Interface of the Android Application:
![image](https://user-images.githubusercontent.com/69485235/139670105-3305f44d-74a5-4c0d-bd4e-ddd6ec1c38bd.png)


