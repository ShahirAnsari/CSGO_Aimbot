# CSGO_Aimbot
Train yolo model on cs go game images to detect and shoot enemies

* The [default weights](https://pjreddie.com/media/files/darknet53.conv.74) file can be downloaded
and placed in the weights folder.
* Modify the generates_train.py file to accpet type of images you want to train on(png, jpg) which creates the data/train.txt file

> Traning can be done using the command 
> ./darknet.exe detector train data/object.data cfg/yolov3_custom.cfg darknet53.conv.74
