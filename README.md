# Collect object detection results on MS COCO dataset
A quick and dirty patch over YOLO2 to ficilicate the collection of object detection results on MS COCO dataset.
 1. Checkout **the yolo-coco-result branch** of this repository, compile the code and download the weight file according to https://pjreddie.com/darknet/yolo/.
 2. List absolute paths of all the MS COCO image files into a text file ```find `pwd` -name "*.jpg" > image_files.txt```, where ``` `pwd` ``` is the directory that contains MS COCO image dirs `train2014`, `val2014` and `test2014`.
 3. Put `image_files.txt` in the darknet proejct directory and run `./darknet detect cfg/yolo.cfg yolo.weights data/dog.jpg > coco_detection_result` to collect the result.

![Darknet Logo](http://pjreddie.com/media/files/darknet-black-small.png)

#Darknet#
Darknet is an open source neural network framework written in C and CUDA. It is fast, easy to install, and supports CPU and GPU computation.

For more information see the [Darknet project website](http://pjreddie.com/darknet).

For questions or issues please use the [Google Group](https://groups.google.com/forum/#!forum/darknet).
