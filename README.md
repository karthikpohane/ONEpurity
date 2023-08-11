# ONEpurity
![1 (1)](https://github.com/karthikpohane/ONEpurity/assets/117158132/dca7bfef-a188-4e12-ad8b-11021a796596)

<p>This set of Notebooks provides a complete set of code to be able to train and leverage your own custom object detection model using the Tensorflow Object Detection API. This accompanies the Tensorflow Object Detection course on my <a href="https://www.youtube.com/c/nicholasrenotte">YouTube channel</a>. 

![Screenshot 2023-08-11 134231](https://github.com/karthikpohane/ONEpurity/assets/117158132/75ddf39d-2268-4ed1-9c75-80ed3846ca6a)

![Screenshot 2023-08-11 134108](https://github.com/karthikpohane/ONEpurity/assets/117158132/79a4d901-a47c-4577-9138-1608b748aa88)
![Screenshot 2023-08-11 134108](https://github.com/karthikpohane/ONEpurity/assets/117158132/20e19fc5-8941-48a4-8014-1e819f684516)
![Screenshot 2023-08-11 134231](https://github.com/karthikpohane/ONEpurity/assets/117158132/6cb5eb51-851a-4daf-b2cf-6a86b0dee96a)
![one (1)](https://github.com/karthikpohane/ONEpurity/assets/117158132/b12d6ba1-705d-4230-9fdb-92a1bf2f0a82)

## Steps
<br />
<b>Step 1.</b> Clone this repository: https://github.com/karthikpohane/ONEpurity/
<br/><br/>
<b>Step 2.</b> Create a new virtual environment 
<pre>
python -m venv tfod
</pre> 
<br/>
<b>Step 3.</b> Activate your virtual environment
<pre>
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 
</pre>
<br/>
<b>Step 4.</b> Install dependencies and add virtual environment to the Python Kernel
<pre>
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=tfodj
</pre>
<br/>
<b>Step 5.</b> Collect images using the Notebook <a href="https://github.com/karthikpohane/ONEpurity/blob/main/1.%20Image%20Collection.ipynb">1. Image Collection.ipynb</a> - ensure you change the kernel to the virtual environment as shown below
<img src="https://imgur.com/qSsLcBi"> 
<br/>
<b>Step 6.</b> Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders. <br/>
\TFODCourse\Tensorflow\workspace\images\train<br />
\TFODCourse\Tensorflow\workspace\images\test
<br/><br/>
<b>Step 7.</b> Begin training process by opening <a href="https://github.com/karthikpohane/ONEpurity/blob/main/2.%20Training%20and%20Detection.ipynb">2. Training and Detection.ipynb</a>, this notebook will walk you through installing Tensorflow Object Detection, making detections, saving and exporting your model. 
<br /><br/>
<b>Step 8.</b> During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.  
<img src="https://i.imgur.com/FSQFo16.png">
If not, resolve installation errors by referring to the <a href="https://github.com/karthikpohane/ONEpurity/blob/main/README.md">Error Guide.md</a> in this folder.
<br /> <br/>
<b>Step 9.</b> Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics. 
<img src="https://i.imgur.com/K0wLO57.png"> 
<br />
<b>Step 10.</b> You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g. 
<pre> cd Tensorlfow/workspace/models/my_ssd_mobnet/eval</pre> 
and open Tensorboard with the following command
<pre>tensorboard --logdir=. </pre>
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
<br />
