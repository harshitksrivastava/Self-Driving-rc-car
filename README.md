# Self-Driving-rc-car
The objective of this project is to explain the development and functioning of the self-driving RC car which uses Raspberry Pi. 
A Pi Camera is mounted along with the ultrasonic sensor to provide the data from the real world to the RC car. 
The car combines several algorithms for stop sign detection, traffic-light detection and obstacle avoidance to provide for the autonomous driving.

The car has following units:
1. Input unit:- Camera module, ultrasonic
module attached to the Raspberry Pi.
2. Processing unit:- A computer on the same
network is made server using TCP protocol. It
receives image data and distance data from pi via
a serial communication . A neural network
prediction for steering control also runs on the
this computer, this predicted command is carried
out by Arduino via a USB connection.
3. Object detection:- The object detection unit
gets simplified to a certain extent with the use of
Haar feature-based cascade classifiers for object
detection. The ultrasonic sensor mounted on the
front-base of the car detect the object distancewith the help of the transceiver mechanism.
4. Neural Network:- Neural network plays a
vital role in training the remote controlled car
and to adapt the dynamic varied situations. The
main advantage of using neural network is that
once the network is trained, it solely has to load
trained parameters afterward, thus prediction
becomes very quick. The neural network is fed
with the continuous video calibration from the
camera mounted on the RC car. However, only
the lower half of the input image is used for
training and prediction. There are 38,400
(320×120) nodes in the input layer and 32
nodes each in two hidden layers. The number of
nodes in the hidden layer is chosen fairly
arbitrary. Eventually, there area unit four nodes
within the output layer where every node
corresponds to the RC car’s steering control
instructions: forward, reverse, left and right.
(Note that the reverse control click is not used
in the project, but it is still included in the
output layer)
