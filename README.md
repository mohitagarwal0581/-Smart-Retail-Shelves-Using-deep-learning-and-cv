# -Smart-Retail-Shelves-Using-deep-learning-and-cv
TensorFlow’s Object Detection API have been used to detect the products that are kept on the shelves using cameras. We have used some pre-trained models (e.g. Faster_RCNN_Inception_V2 model) to train the classifier to classify different objects by using the dataset of images of different products. The training has been done until the loss consistently drops below 0.05 and which is around 40000 steps. 
## Modules
<ul>
<li><b>Dataset Preparation Module:</b> This module deals with collection of images which
constitutes of the dataset.</li>
<li><b>Training Preparation Module:</b> This module deals with preparing of the dataset for
training purposes which includes labelling of images and creating the label map.</li>
<li><b>Training and Testing the Classifier Module:</b> In this module, the actual training of
dataset begins and once the training is completed then the testing of classifier is
done.</li>
</ul>
<ul>
<li><h3>Dataset Preparation Module:</h3>
1. TensorFlow needs various pictures of an instance to put-in a highly accurate identifier
classifier.<br>
2. For a classifier to become strong training needs to be done. The pictures which are
trained will be having snaps of instances in the picture along with the wanted
instances, and thundering states should be there.<br>
3. The dataset that we have taken consists of two products.<br>
4. For our Product Identifier classifier, we will be having two varieties of Chocolates
(Dairy milk and Perk). We have taken about 150 pictures of each chocolate, and there
are many non-desired instances in the images.<br>
5. Then, we took about another 50 pictures with both chocolates in the picture. We want
to be able to detect the chocolates when they’re overlapping, so we made sure to have
the chocolates be overlapped in many images.<br>
6. Here are some examples of images containing chocolates:
<img src="srsdocs/dataset1.PNG">
<img src="srsdocs/dataset2.PNG"></li>
  </ul>
  <ul>
<li><h3>Training Preparation Module:</h3></li>
  <li>1. LabelImg of the objects in the images is done so that classifier can identify objects
in the images.<br>
2. For labelling we have used LabelImg.<br>
3. An .XML file will be saved by labelimg that contains the data which is labelled i.e.
(the coordinates and dimensions) for every picture.<br>
4. These .xml files would be used to generate TFRecords. These are put-in to the TF.<br>
5. With the images labelled, now a csv file is generated from all the xml files.<br>
6. This file contains the coordinates of the target instances in every picture of the
dataset.<br>
7. In the Tfrecord file, an ID number is assigned for every instance.<br>
8. Now, label map file is created.<br>
9. A map with a label tells the trainer that each item is to specify a mapping of the
    class names to the class ID numbers.<br></li>
  </ul>
