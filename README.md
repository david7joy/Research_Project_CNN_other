# CNN

We will be implementing the building blocks of a convolutional neural network! Each function we implement will have detailed instructions that will walk us through the steps needed - Convolution functions, including:
Zero Padding
Convolve window
Convolution forward
Convolution backward 
Pooling functions, including:
Pooling forward
Create mask
Distribute value
Pooling backward 

<img width="604" alt="model" src="https://user-images.githubusercontent.com/30907520/35636467-d1eab914-0676-11e8-8155-34a9a4e0114a.png">


The main benefits of padding are the following:

- It allows you to use a CONV layer without necessarily shrinking the height and width of the volumes. This is important for building deeper networks, since otherwise the height/width would shrink as you go to deeper layers. An important special case is the "same" convolution, in which the height/width is exactly preserved after one layer.

- It helps us keep more of the information at the border of an image. Without padding, very few values at the next layer would be affected by pixels as the edges of an image.

<img width="574" alt="pad" src="https://user-images.githubusercontent.com/30907520/35636604-4fd60900-0677-11e8-87ae-33f1ac5e6117.png">

The pooling (POOL) layer reduces the height and width of the input. It helps reduce computation, as well as helps make feature detectors more invariant to its position in the input. The two types of pooling layers are:

- Max-pooling layer: slides an ( f,f) window over the input and stores the max value of the window in the output.
- Average-pooling layer: slides an ( f,f) window over the input and stores the average value of the window in the output.

<img width="775" alt="max_pool1" src="https://user-images.githubusercontent.com/30907520/35638763-a44c13ac-067d-11e8-8a35-84845c49b48c.png">
<img width="757" alt="a_pool" src="https://user-images.githubusercontent.com/30907520/35638775-ad778f1a-067d-11e8-9ffe-b40f07aed584.png">
