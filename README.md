# Defect-Detection using-YOLO5

1. YOLO5
 Install
Python>=3.6.0 is required with all requirements.txt installed including PyTorch>=1.7:
  
 $ git clone https://github.com/ultralytics/yolov5
$ cd yolov5
$ pip install -r requirements.txt

2. Train Custom Data
Dataset Link:
https://www.kaggle.com/ravirajsinh45/real-life-industrial-dataset-of-casting-product


3. Create folder train_data
  then Create folders images and labels in train_data
  then create two folders in images:
  train and val
  add traing and validation images in that folder
  
5.  Create Labels using https://www.makesense.ai


![image](https://user-images.githubusercontent.com/34790064/128226356-b5ded02a-8c20-416e-a640-9ac7371a8912.png)


![image](https://user-images.githubusercontent.com/34790064/128226697-bfdaca23-f652-4b74-a5fa-cc28e4b72179.png)


Create Bounding Boxes for all images

![image](https://user-images.githubusercontent.com/34790064/128226975-efe520ef-87b2-4ce3-acff-9547ce8bf210.png)


Export Annotations in YOLO format:
Text files of Labela will be downloaded

6.save that text files in labels folder in different folder train and val
7.Upload train_data folder in foloowing notebook
https://github.com/ultralytics/yolov5
8. Create new.yaml file
  dit coco128.yaml file acoording to custom dataset
  nc=2
  names=['Dent','Hole']
  /content/yolov5/data/coco128.yaml
  9.# Train YOLOv5s on COCO128 for 3 epochs
!python train.py --img 640 --batch 16 --epochs 60 --data new.yaml --weights yolov5s.pt --cache

10. Inference
detect.py runs YOLOv5 inference on a variety of sources, downloading models automatically from the latest YOLOv5 release, and saving results to runs/detect.









