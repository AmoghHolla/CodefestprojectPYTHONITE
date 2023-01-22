1. As you all know, in our world, many people easy manage to doze off or feel drowsy while driving for longer periods of time, or when
people come home after long work shifts they tend to feel sleepy. Such incedents dont only can cause severe injuries, but also several
deaths when such people encounter accidents. This issues has become so huge that around 1 in every 25 people get caught up in such a 
situation and more that 40% of accidents happen due to this issue.

My main inspiration to do this was because recently on the road in front of my apartment, a recent accident had occured and the first though that came to my mind was "I need to stop this issue" and soon after I came to this idea.

by knowing this u probably know that my main theme is Transportation.

Now coming on the solution. So I am making a driver drowsiness detection system that tracks down whether the driver's eyes are open
or closed using various modules and libraries including OPEN.cv, Tensorflow, Keras and obviously my main language is python.

Now next coming to its practicality, this soultion is very practical and the main reason is because this can be runned on any device,
therfore much more easily available rather than using sensors whihc you have to wear etc. 

And then we have why this solution is innovative. Firstly, even if such a for of detection may exist the implementation has not been done 
which I am doing here in my project.


About my files:


Model:
This script is a machine learning model that classifies images of eyes as open or closed. It uses the Keras library, which is a high-level neural networks API, running on top of TensorFlow.

The script defines a generator function that takes as input a directory, and returns a generator that can be used to load image data from the directory. The generator is set up with some default parameters, such as rescaling the pixel values of the images to the range of 0-1, grayscaling the images, and returning the images in the form of batches of a specified batch size.

The script then defines the model architecture using the Keras Sequential API. The model consists of several convolutional layers, max pooling layers, dropout layers, and a dense layer. The convolutional layers are used to extract features from the images, the max pooling layers are used to reduce the dimensionality of the feature maps, the dropout layers are used to prevent overfitting, and the dense layer is used to perform the final classification.

The script then compiles the model by specifying the optimizer, loss function, and metrics. The optimizer is set to Adam, the loss function is set to categorical cross-entropy, and the metrics are set to accuracy.

The script then fits the model to the data using the fit () method, specifying the training data, validation data, number of epochs, and steps per epoch.

Finally, the script saves the trained model to a file named 'cnnCat2.h5' in the 'models' directory using the save () method.



This script is a Drowsiness Detector that uses computer vision and machine learning techniques to detect drowsiness in a person. The script uses the OpenCV library for computer vision, the Keras library for machine learning, and the Pygame library for playing a sound alarm.

The script defines a class called "DrowsinessDetector" with several methods. The constructor method "init" initializes some variables used in the class. It also initializes the mixer library, loads an alarm sound and a video capture from the default camera, loads a pre-trained model for eye state prediction, and loads classifiers for detecting faces, left eyes, and right eyes.

The "process_eyes" method takes an eye image as input and processes it for prediction by converting it to grayscale, resizing it, normalizing it, reshaping it in a format suitable for the model, and adding a new dimension to it.

The "predict" method takes an eye image as input and uses the pre-trained model to predict whether the eye is open or closed. It returns a label "Open" or "Closed" accordingly.

The "__monitor" method is the main loop of the program, it captures a video frame, detects the face, eyes, applies the predict method on the eyes, and increment the score if both eyes are closed. 

It also draws rectangles around the eyes and face on the frame and display the label on the frame. If the score reaches a certain threshold, the alarm sound is played.





