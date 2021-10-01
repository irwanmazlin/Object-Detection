# Object Detection and OCR Projects
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE)

This project implement object detection with YOLOv4 and tensorflow. YOLOv4 use deep convolutional neural network to object object detection. I take the initiave use this library to perform detection, the OCR on lisence plate, cropping the detection and vehicle detection.

Here the Result of the project after perform the ocr and vehicle detection using th is library.

## Lisence Plate Detection

##### the cropping of the project
<p align="center"><img src="OCR using YOLOV4/ocr/objectcrop.png" width="640"\></p>


##### Final output of this project

:covid19)


## Vehicle Detection

<p align="center"><img src="vehicle detection/tensorflow-yolov4-tflite/data/result2.jpg" width="640"\></p>


## Getting Started
To get started, yyou are required to install the dependencies via pip. In this project we are using Google Colab as a platform to complete this projects. 

### Prerequisites
* Tensorflow 2.3.0rc0
* pytesseract
* opencv


## Download pre-trained YOLOv4 weights.

My object detection uses YOLOv4 to perform the detection. I am using the existing pre-trained model (YOLOv4) that able to detect the car plate and vehicle. Attachment below is the link to download the model for car plate detection and vehicle detection. 

License Plate Detection : https://drive.google.com/file/d/1EUPtbtdF0bjRtNjGv436vDY28EN5DXDH/view?usp=sharing

Car Detection : https://drive.google.com/open?id=1cewMfusmPjYWbrnuJRuKhPMwRe_b9PaT

### Performance
<p align="center"><img src="data/performance.png" width="640"\></p>

### copy the following syntax to run in terminal or cloud

```bash
# Convert darknet weights to tensorflow
## yolov4
python save_model.py --weights ./data/yolov4.weights --output ./checkpoints/yolov4-416 --input_size 416 --model yolov4 


python detect.py --weights ./checkpoints/yolov4-tiny-416 --size 416 --model yolov4 --image 'YOUR DATA' 

```
If you want to run yolov3 or yolov3-tiny change ``--model yolov3`` in command

#### Output for vehicle detection

##### Yolov4 of this project

##### the cropping of the project
<p align="center"><img src="vehicle detection/tensorflow-yolov4-tflite/data/vehicle/vehiclecrop0.png" width="250"\></p>
<p align="center"><img src="vehicle detection/tensorflow-yolov4-tflite/data/vehicle/vehiclecrop0.png" width="250"\></p>
<p align="center"><img src="vehicle detection/tensorflow-yolov4-tflite/data/vehicle/vehiclecrop0.png" width="250"\></p>






### References

   My project is inspired by these previous fantastic YOLOv4 implementations:
  * [Yolov4 tflite](https://github.com/hunglc007/tensorflow-yolov4-tflite)
  
