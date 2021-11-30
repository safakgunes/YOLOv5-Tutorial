# Yolov5-Tutorial
Yolov5 training and detection tutorial

## What is YOLO?
* YOLO is an algorithm that uses neural networks to provide real-time object detection. This algorithm is popular because of its speed and accuracy. It has been used in various applications to detect traffic signals, people, parking meters, and animals.

![YOLO](https://raw.githubusercontent.com/safakgunes/Yolov5-Tutorial/main/img_results.png)


## Create an environment

* Update pip with the following command.
```bash
$ python -m pip install --upgrade pip
```
* Create an enviroment.
```bash 
$ conda create --name yolov5 
```
* Activate this environment
```bash
$ conda activate yolov5
```
## Requirements

* Open the yolov5 directory
```bash
$ cd <yolov5_dir>
```
* Setup requirements
```bash
 $ pip install -r requirements.txt
```
* Make sure you have cuda and cudnn installs

## Train

* Make sure environment activated. Go to yolov5 directory.
```bash
$ cd <yolov5_dir>
```

* can be use as shown below.

```bash
$ python train.py --data coco.yaml --cfg yolov5s.yaml --weights '' --batch-size 64
                                         yolov5m                                40
                                         yolov5l                                24
                                         yolov5x                                16
```       
* Run commands below
```bash
% python train.py --data ./data/coco128.yaml --cfg ./models/yolov5s.yaml  --batch 64
```
* You can see the training results and  weights, enter the directory below in the yolov5 folder.

```bash
$ cd <yolov5_dir>/runs/train
```
## Detect

* can be use as shown below.

```bash
$ python detect.py --source 0  # webcam
                            img.jpg  # image
                            vid.mp4  # video
                            path/  # directory
                            path/*.jpg  # glob
                            'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                            'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```
* Run commands below

```bash
$ python detect.py --source ../img.png --weights ./runs/train/exp/weights/best.pt --conf 0.5
```                                 
*  You can see the detection results, enter the directory below in the yolov5 folder.     

```bash
$ cd <yolov5_dir>/runs/detect
```


                                 
                                 
