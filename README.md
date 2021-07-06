# CSGO_Aimbot
Train yolo model on cs go game images to detect and shoot enemies

* The [default weights](https://pjreddie.com/media/files/darknet53.conv.74) (darknet53.conv.74) file can be downloaded
and placed in the weights folder.
* Modify the generates_train.py file to accept type of images you want to train on(png, jpg) which creates the data/train.txt file
* You can create a validation file (valid.txt) to if you want but we can always test it manually after training.

* Training can be done using the command.
> *./darknet.exe detector train data/object.data cfg/yolov3_custom.cfg weights/darknet53.conv.74*
