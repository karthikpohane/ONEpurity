![gitfrontlogo](https://github.com/karthikpohane/ONEpurity/assets/117158132/ce489d55-66a0-42fc-b4fe-9b3f6989dbbb)
#
<p>ONEpurity is a Vehicle Pollution Detection System is an innovative solution designed to combat vehicular emissions and environmental pollution through the utilization of cutting-edge technologies, including deep learning, Convolutional Neural Networks (CNNs), TensorFlow, and the SSD MobileNet V2 architecture. This system aims to provide real-time and efficient pollution detection capabilities, merging technology witr sustainability for a cleaner environment.</p>

## Table of Contents

<table>
    <th>Introduction</th>
    <th>Technologies Used</th>
    <th>Functionality</th>
    <th>Installation</th>
    <th>Usage</th>
    <th>Workflow</th>
    <th>Environmental Impact</th>
    <th>Contributing</th>
</table>

## Introduction.

<p>ONEpurity: a compelling synergy of technological innovation and environmental responsibility, poised to revolutionize the battle against vehicular emissions and their ecological repercussions. In the prevailing landscape of mounting pollution concerns, ONEpurity emerges as a trailblazing solution, redefining the approach to pollution control with its seamless integration of advanced technologies like deep learning, Convolutional Neural Networks (CNNs), TensorFlow, and the SSD MobileNet V2 architecture.</p>
<p>Amidst growing global awareness of air quality and environmental impact, the urgency to swiftly identify and counter vehicle-derived pollutants is paramount. ONEpurity's adeptness lies in its ability to swiftly process visual data from vehicle cameras and external sensors, promptly discerning contaminants like smoke, particulate matter, and poisonous gases. This speed is not only essential for immediate intervention but also crucial for guiding informed policy decisions, fostering sustainable practices.</p>
<p>Underpinning ONEpurity's prowess is its reliance on deep learning and CNNs, empowering it to unravel complex visual patterns and identify pollutants based on their distinct characteristics. Fueling this innovation is TensorFlow, a versatile machine-learning framework that ensures accuracy and scalability. Complementing this is the choice of the SSD MobileNet V2 architecture, seamlessly blending speed and precision for real-time object detection while optimizing resources.
ONEpurity's narrative extends beyond detection, transcending into proactive alert mechanisms for stakeholders and a catalyst for informed policies. As a fusion of human ingenuity and ecological mindfulness, ONEpurity illuminates the path toward a greener urban landscape, promising a more sustainable future for future generations. In a landscape where progress hinges on innovation, ONEpurity is a transformative force, igniting a cleaner, purer tomorrow by transcending mere pollution detection to foster a holistic ecological revival.</p>

## Technologies Used.
<ul>
    <li>Deep Learning</li>
    <li>Convolutional Neural Networks (CNNs)</li>
    <li>TensorFlow</li>
    <li>SSD MobileNet_V2</li>
</ul>

## Functionality.
<ul>
    <li><p><b>Data Collection:</b> Visual data is obtained from cameras on vehicles or external sensors, capturing the surroundings as the vehicle moves.</p></li>
    <li><p><b>Preprocessing:</b> Raw visual data is enhanced through resizing, normalization, and noise reduction to ensure quality and consistency.</p></li>
    <li><p><b>CNN Training:</b> A diverse dataset containing pollutant scenarios trains the CNN to differentiate between different pollutants by identifying their visual characteristics.</p></li>
    <li><p><b>Real-Time Detection:</b> Equipped with a trained CNN, the system processes incoming visual data in real-time, rapidly identifying and localizing pollutants within images or video streams.</p></li>
    <li><p><b>Alert and Reporting:</b> When pollutants are detected, the system triggers alerts to relevant stakeholders, such as authorities or drivers. This supports swift corrective actions and pollution control efforts.</p></li>
</ul>

## <h1>Installation.</h1>
<h4>Steps</h4>
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
