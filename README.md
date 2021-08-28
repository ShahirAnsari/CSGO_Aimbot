# CSGO_Aimbot

Overview to train for images
* Place images in object/data foler.
* Place default weights in main directory
* Modify data/object.data and data/object.names file.
* Modify cfg/yolo.config file.
* Run generate.py program that create data.train.txt file.
* Run darknet.exe to start training.


Directory and Files definition



* `data/object.names` - Contains number of classes,location of train.txt,valid.txt file and location of folder to store training_weights(create the training_weights folder manually in darknet directory).
*  `data/object.names` - Contains the names of the classes to train on. One class per line.
*  `data/object` - Contains images and label to train on.
*  `data/train.txt` - Contains locations of all file to be trained on. i.e. all file in `data/object` folder

All the above folder and files are to be placed in your `darknet/data` folder.

Configuration file : `cfg/yolov3_CSGO.cfg`

Modification to the config fle.
* Comment the batch and subdivision under testing.
* batch -  64  `(decrease or increase according to how much your pc can handle.)`
* subdivision - 64  `(decrease or increase according to how much your pc can handle. Subdivision <= Batch.`
* classes - 2  `(Your number of classes)`
* max_batches - 4000 `(2000*classes)`
* filter - 21  `(classes+5)*3 i.e (2+5)*3`
* random - 0/1 `1- if you have different size images,0-If all images are of same size`







Train yolo model on cs go game images to detect and shoot enemies

* The [default weights](https://pjreddie.com/media/files/darknet53.conv.74) (darknet53.conv.74) file can be downloaded
and placed in the weights folder.
* Modify the generates_train.py file to accept type of images you want to train on(png, jpg) which creates the data/train.txt file
* You can create a validation file (valid.txt) to if you want but we can always test it manually after training.

* Training can be done using the command.
 
     `./darknet.exe detector train data/object.data cfg/yolov3_custom.cfg weights/darknet53.conv.74*`


The next part is converting the model to tensorflow and detect objects on images and videos.

