# Lungs-Cancer-Detection-using-CNN-Model
## About Data Set:

The Iraq-Oncology Teaching Hospital/National Center for Cancer Diseases (IQ-OTH/NCCD) lung cancer dataset was collected in the above-mentioned specialist hospitals over a period of three months in fall 2019. It includes CT scans of patients diagnosed with lung cancer in different stages, as well as healthy subjects. IQ-OTH/NCCD slides were marked by oncologists and radiologists in these two centers. The dataset contains a total of 1097 images .These cases are grouped into three classes: normal, benign, and malignant. The CT scans were originally collected in DICOM format(Digital Imaging and Communications in Medicine standard). All images were de-identified before performing analysis. Written consent was waived by the oversight review board. The study was approved by the institutional review board of participating medical centers. Each scan contains several slices. The number of these slices range from 80 to 200 slices, each of them represents an image of the human chest with different sides and angles. The 110 cases vary in gender, age, educational attainment, area of residence and living status. Some of them are employees of the Iraqi ministries of Transport and Oil, others are farmers and gainers. Most of them come from places in the middle region of Iraq, particularly, the provinces of Baghdad, Wasit, Diyala, Salahuddin, and Babylon.

## About Model:

A CNN model was trained using this data and the architecture of the model was optimized using techniques such as dropout, Adam optimizer and early stopping. 
The model was then validated using a separate test dataset.The first preprocessing of the dataset is done by rescaling and resizing. Rescaling is done by making all the pixel values between 0 and 1 while resizing is done by changing image size to 256x256.Then we split it into the train, validate which is 80%, 20%, respectively, test data of 60 images(20 of each class) is separated at the start and made them shuffle randomly. We made batches of size 81. And images size is 256x256.
Our CNN model consists of six convolution layers of 32, 64, 64, 64,128,128 filters respectively and 6 max-pooling layers of size (2, 2) and then one hidden layer in fully connected layer with 64 node. Except the output layer, in all layers Relu activation used. As it is the multiclass classification problem, so softmax is used in output layer as activation function.

## About Front End:
To build the front-end of the application, Flask was used to create an interactive web interface that allows users to upload an image of a lung and receive a prediction on whether the case is malignant, benign or normal.
Main page of our website look like this as shown below: <br />
![mainpage](https://github.com/Tayyba-Salamat/Lungs-Cancer-Detection-using-CNN-Model/assets/110371081/873fe92b-ce2e-4c8b-8892-85121eb836fb)
<br />
 
After getting started, user will be redirected to the following page: <br />
![sec](https://github.com/Tayyba-Salamat/Lungs-Cancer-Detection-using-CNN-Model/assets/110371081/d4e62476-b818-40b0-b7e5-eadc50f763bc)

<br />
 
And classification interfaces for classes are: <br />
![third](https://github.com/Tayyba-Salamat/Lungs-Cancer-Detection-using-CNN-Model/assets/110371081/dd88064f-22e0-4c78-88f0-16b255997dc9)
<br />
![fourth](https://github.com/Tayyba-Salamat/Lungs-Cancer-Detection-using-CNN-Model/assets/110371081/96ef80aa-06bb-4e78-ae05-50950722bcf3)

 
<br />
Result:
Validation and training loss by using this CNN model, we achieved till 0.05.Till 15 epochs, we achieved accuracy of almost 98% without over fitting as shown in the given graph  <br />
![los](https://github.com/Tayyba-Salamat/Lungs-Cancer-Detection-using-CNN-Model/assets/110371081/f3325267-5dcc-4217-8338-6a5f403dd6bc)

<br />
![Acc](https://github.com/Tayyba-Salamat/Lungs-Cancer-Detection-using-CNN-Model/assets/110371081/37699947-daa0-446f-877a-f85a44b8583b)


 
