# TrainDetectionModel
Training Naruto characters detctor with Tensorflow Object Detection API using Google Colab
<p float = "left">
  <img src="https://github.com/popCain/TrainDetectionModel/blob/main/image/result_1.png" width="500">
  <img src="https://github.com/popCain/TrainDetectionModel/blob/main/image/result_2.png" width="290">
</p>   

## Prepare training data  
* Use the [`RectLabel`](https://rectlabel.com/) to bulid your own training dataset easyly on MAC OS(No alternative found on windows).    
* Extract [`sub-dataset`](https://github.com/popCain/getSubsetFromCOCO) from COCO Dataset(Needed category only)
> Process Locally
  1. Get the XML_files(labels info) of each image 
  2. Convert XML_files to CSV file
> Process on Google Colab
  3. Convert `images+CSV_file` to tfrecord(Binary file)
## Upload to your google driven
Using the `ObjectDetectionAPI_Training_Naruto.ipynb`(Please pay attention to the Path or folder name)
## Configuring the development environment
Download the Google Object Detection API Library([Reference](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1.md)).
## Download the finetuning checkpoint(Here used MobilenetV3+SSDLite model)
You can download the pretrained detection model in google [`object detection zoo`](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md)
## Modify the config file
Different Model correspond to different cofig_file(In `"models/research/object_detection/samples/configs/"`)    
*[Note]: Can not modify the parameter of **`val.record`**, you may need to download and  edit it locally with  correct path of test dataset.*     
## Begin training
Spend different amounts of time according to the specified number of training steps      
* *[Note]: Interruption of the connection with remote google GPU may occurred, dont't worry about it, we have saved the training processing file in the `training folder`, we can ignore the interruption and continue training from the breakpoint*
## Training result view from Tensorboard
<p float = "left">
  <img src="https://github.com/popCain/TrainDetectionModel/blob/main/image/loss.png" width="300">
  <img src="https://github.com/popCain/TrainDetectionModel/blob/main/image/mAP.png" width="500">
</p>  

## Export the frozen graph based on training checkpoint
Reference to my another repository([exportMobileNet_SSDSeries](https://github.com/popCain/exportMobileNet_SSDSeries))
## You can convert the exportd `Frozen graph` to the [CoreML data format](https://github.com/popCain/TFtoCoreML)
## Apply the model to your iOS APP([reference](https://github.com/popCain/ObjectDetection_iOS))
