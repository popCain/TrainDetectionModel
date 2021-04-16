# TrainDetectionModel
Training Naruto characters detctor with Tensorflow Object Detection API using Google Colab
<p float = "left">
  <img src="https://github.com/popCain/TrainDetectionModel/blob/main/image/result_1.png" width="500">
  <img src="https://github.com/popCain/TrainDetectionModel/blob/main/image/result_2.png" width="290">
</p>   

## Ⅰ Prepare training data  
You can use the [`RectLabel`](https://rectlabel.com/) to bulid your own training dataset easyly on MAC OS(No alternative found on windows).      
> Process Locally
  1. Get the XML_files(labels info) of each image 
  2. Convert XML_files to CSV file
> Process on Google Colab
  3. Convert `images+CSV_file` to tfrecord(Binary file)
## Ⅱ Upload to your google driven
Using the `ObjectDetectionAPI_Training_Naruto.ipynb`(Please pay attention to the Path or folder name)
## Ⅲ Download the finetuning checkpoint(Here used MobilenetV3+SSDLite model)
You can download the pretrained detection model in google [`object detection zoo`](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1_detection_zoo.md)
