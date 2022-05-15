Use sign-detection.ipynb

The repo utilizes the YOLOv5 architecture with modifications for our use.
https://github.com/ultralytics/yolov5

There is a current issue regarding version incompatibility between the version of YOLOv5 we used and Torch.
Please refer to https://github.com/ultralytics/yolov5/issues/6948 for fixing this issue.

<h1>Examples</h1>
<img src="https://github.com/nathan-lai-engineering/sign-detection/blob/main/readme-images/example%201.PNG?raw=true">
Above, frame displaying detection of stop sign

</br>
</br>
<img src="https://github.com/nathan-lai-engineering/sign-detection/blob/main/readme-images/example%202.PNG?raw=true">
Above, frame displaying detection of speed limit including number on sign

</br>
</br>
<img src="https://github.com/nathan-lai-engineering/sign-detection/blob/main/readme-images/example%203.PNG?raw=true">
Above, frame displaying false sign detection by YOLOv5, but caught by EasyOCR as urdbl (unreadable)

<h1>Usage</h1>

<h3>Setup</h3>
Enters the YOLOv5 directory and double checks the device used for detection

<h2>Inference</h2>
<h3>1. Parameters</h3>
The cell where things such as directory and other settings can be adjusted for the rest of inference.
Requires setting up a videos folder if not using an existing one already.

<h3>2. Functions</h3>
Utility functions to be used later on

<h3>3. Detection</h3>
The call to the YOLOv5 architecture to perform inference on a set up videos as denoted in the paramters cell.

<h3>4. Process Labels</h3>
Post-processes the raw output from YOLOv5 to fill in gaps, remove outliers, and group together detections.

<h3>5. OCR</h3>
Runs OCR on groupings of detections to verify results from YOLOv5 and assign speed limit numbers.

<h3>6. Generate snippet highlights</h3>
Creates video snippets of every grouping of detection for ease of double checking

<h3>7. Generate results</h3>
Creates a more human readable csv for detections

<h2>8. Generate videos</h3>
Creates a full video with bounding boxes of detections.
