# RoadSignsDetectionYOLOv8
<div id="header" align="center">
  <a href="https://yolovision.ultralytics.com/">
<img src="asset\title-banner-yolov8.png" width="100%"/>
</a>
</div>

<!DOCTYPE html>
<html lang="it">
<body>
  <h1>Road Signs Detection with YOLOv8</h1>
  <p>
    <strong>Abstract:</strong>
    <br>
    
This project aims to develop a road sign identification system based on artificial vision. The system will be able to detect and classify road signs in real time, providing useful information to drivers and autonomous driving systems.
  </p>
  <h2>Goal</h2>
  <p>
    <br>
    The objective of the project is the development of a road sign identification system based on artificial vision that is:
<ul>
<li>Accurate: The system must be able to detect and classify traffic signs with high precision, even in poor visibility conditions.</li>
<li>Fast: the system must be able to process images in real time, in order to provide useful information to drivers and autonomous driving systems.</li>
<li>Robust: The system must be robust to variations in light, weather conditions and traffic conditions.</li>
</ul>
  </p>
  <h2>Tools</h2>
  <p>
    <br>
    <ul>
      <li>
        <strong>Python:</strong>
        Python is a general-purpose programming language that has been widely used for developing computer vision applications. Python offers a number of advantages for developing computer vision applications.
        <br>
        <br>
       <div align="center"> 
         <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/800px-Python-logo-notext.svg.png" width="100"></img>
       </div>
      </li>
    </ul>
    In the context of traffic sign detection project, Python is used to:
<ul>
<li>
  <strong>Training the YOLOv8 model:</strong>
  The YOLOv8 model will be trained in Python using the Ultralytics YOLOv8 library.
</li>
</ul>
<br>
<br>

 <strong> <li>YOLOv8 is a computer vision model for object detection developed by Ultralytics.</strong>
 It was released in 2022 and is considered one of the most accurate and fastest models available.
YOLOv8 is based on a convolutional neural network architecture called Darknet-53. The network consists of 53 convolution layers, each of which is followed by a max-pooling unit.
YOLOv8 can detect and classify objects in real time. It was trained on an image and video dataset that includes a variety of objects, including people, vehicles, animals and everyday objects.
In the context of the traffic sign detection project, YOLOv8 is used to:
<ul>
<li>Traffic sign detection: YOLOv8 will be used to detect and classify traffic signs in images and videos.</li>
To use YOLOv8 for traffic sign detection, you need:

<li>Download the YOLOv8 model: The YOLOv8 model is available for download from the Ultralytics website.</li>
<li>Prepare the dataset: The dataset must include images and videos of traffic signs.</li>
<li>Train the model: The YOLOv8 model can be trained using the prepared dataset.</li>
Once the YOLOv8 model is trained, it can be used to detect traffic signs in images and videos.
</ul>
</p>
  <h2>Code implementation</h2>
  <p>Below is a description of the code used to implement the project in Google Colab:</p><br>
  <img src="asset\code-img\import-lib.png" alt="Import lib" width="100%"><br>
  <p>As a first step we import the basic libraries such as os for the file paths, glob and IPython.display to show the results of the train in the subsequent steps.</p><br>

  <img src="asset\code-img\check-gpu.png" alt="Check gpu" width="100%"><br>
  <p>To verify the correct access status to the GPU we install the nvidia-smi library.</p><br>
  
  <img src="asset\code-img\mounted-drive.png" alt="Mounted Google Drive" width="100%"><br>
  <p>We use Colab's compatibility with Google Drive to access the account on which the dataset on which to create our model is present.</p><br>
  
  <img src="asset\code-img\install-yolo.png" alt="Install yolo" width="100%">
  <img src="asset\code-img\check-install.png" alt="Check yolo" width="100%"><br>
  <p>We install references to the latest version of YOLOv8 and verify correct installation.</p><br>

  <img src="asset\code-img\start-train.png" alt="Start train" width="100%"><br>
  <p>At this point we have all the necessary tools to start training the model using YOLOv8's Train mode.
   The current configuration involves training the model in 10 epochs using the default image size, i.e. 640.</p><br>

  <img src="asset\code-img\resume-train.png" alt="Resume train" width="100%"><br>
  <p>For the purposes of the project, a further train of the model was carried out once the dataset had been expanded.</p><br>
  
   <img src="asset\code-img\print-matrix.png" alt="Resume train" width="100%"><br>
   <img src="asset\code-img\check-model-prevision.png" alt="Check model" width="100%">
   <img src="asset\code-img\print-validation.png" alt="Print prevision" width="100%">
  <p>Once the model has been trained, we proceed with viewing the results. We print the confusion matrix, the prediction tests and the train graphs to determine whether the expected results have actually been achieved.</p><br>

  <img src="asset\code-img\valid-model.png" alt="Valid model" width="100%"><br>
  <p>The next step is data validation, taking advantage of YOLOv8's Validation mode, a fundamental step for the machine learning pipeline, as it allows you to evaluate the quality of the trained models.</p><br>

  <img src="asset\code-img\prediction.png" alt="Predict model" width="100%"><br>
  <p>Finally we use the product model for prediction on our data. In our case we used the model for the detection of road signs in a video in which there are real cases.<p><br>


  
</body>
</html>
