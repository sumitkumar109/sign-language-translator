## DESIGN AND IMPLEMENTATION  

### Dataset: 
A user defined dataset has been used for this project. A total of 125 images, around 25 images, is used for each of the classes. This dataset contains a total of 5 symbols that are:  hello, yes, no, I Love You and thanks, which are quite useful while dealing with the real time application.

### Algorithm Used:

YOLO or You Only Live Once is a very clever algorithm, It is really good at detecting where and what objects are present in the given image or video by just looking once at the picture or the video. 

### Working of YOLO:
**Neural Networks :** YOLO is powered by the Neural Networks, they are a special type of computer algorithm. Neural networks are named so because they are modeled after our brains, and are engineered to detect patterns. YOLO itself is a Convolutional Neural Network (CNN), a type of neural network, which is very good at detecting patterns in images.

**Neural Network Layers:** Neural networks are made up of layers, and CNNs are made of mostly convolutional layers. It is like sliding a filter over an image, and each layer is progressively more complex. The filter here is the numbers we are using to multiply. Basically, we look at one part of the input image, apply the filter, and use the sum of the result to get a convolved feature. If we think of the image being grayscale, each number is how bright that pixel is. The early layers may slide across filters designed to find edges, corners, and shapes, but later layers may detect more complex features like limbs, faces, and entire objects.

**Pooling Layers:** Pooling is much simpler, and also similar to convolution. Instead of detecting features, pooling is meant to lighten the load on the network by reducing its spatial size. It basically reduces the size of the inputs provided to the convolutional layers, with normally two methods:

**Max Pooling:** Max pooling is the first type, wherein you take the biggest number in each cell of the image.

**Average Pooling:**  The second type of pooling, wherein you average all the numbers in each cell of the image.

**Activation Layers:**  Activation layers are key for a neural network. At each step, we must define the output which will be the input for the next step (or the actual output at the very end). YOLO uses ReLU (Rectified Linear Unit). ReLU activation is used at each convolutional step, and not the pooling ones, since they are just meant to lighten the load. Basically, ReLU works by modifying the output so anything less than 0 becomes zero, and everything else is raw output.

**Figuring out where objects are:**
YOLO first will divide a given image or frame of a video into N number of squares. Then, each grid cell detects objects in it and predicts a number of bounding boxes, and confidence scores for those boxes (a bounding box is just it predicting where objects are and placing a box around it). After that, it takes the confidence scores high enough to likely be an object, and predicts what that object is, based on training data. This means you can only detect an object with YOLO after giving it a dataset of objects. This allows us to detect objects and predict what they are.

### Model Analysis:

**YOLO architecture :** An object detector is designed  in such a way to create features from input images which is then used to feed these features through a prediction system. It draws boxes around the objects and then gradually  predicts their classes. The YOLO model was the first object detector which enabled the connection of the procedure of predicting bounding boxes with class labels in an end to end differentiable network.

**There are 3 main components of the YOLO network:**
**Backbone:** A convolutional neural network, this aggregates and forms image features at different granularities.
**Neck:** A series of layers are present  to mix and combine image features which is then gradually passed forward to prediction.
**Head:** Consumes features from the neck and takes box and class prediction steps.

**YOLO Training Procedures:** Training procedures are equally important and is required in order to end the performance of an object detection system.
1. Data Augmentation - This makes transformations to the basic training data in order to expose the model to a wider range of semantic variation than the training set in isolation.
2. Loss Calculations - From the constituent loss functions, YOLO calculates a total loss function.

### Results:
<p float="left">
<img src="https://github.com/sumitkumar109/sign-language-translator/blob/main/data/images/Hello.png" width="250" height="250" />
<img src="https://github.com/sumitkumar109/sign-language-translator/blob/main/data/images/ILoveYou.png" width="250" height="250" />
<img src="https://github.com/sumitkumar109/sign-language-translator/blob/main/data/images/Yes.png" width="250" height="250" />
<img src="https://github.com/sumitkumar109/sign-language-translator/blob/main/data/images/No.png" width="250" height="250" />
<img src="https://github.com/sumitkumar109/sign-language-translator/blob/main/data/images/ThankYou.png" width="250" height="250" />
</p>
