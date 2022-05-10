Use sign-detection.ipynb

The repo utilizes the YOLOv5 architecture with modifications for our use.
https://github.com/ultralytics/yolov5

There is a current issue regarding version incompatibility between the version of YOLOv5 we used and Torch.
Please refer to https://github.com/ultralytics/yolov5/issues/6948 for fixing this issue.

Cells Explained

Setup
Enters the YOLOv5 directory and double checks the device used for detection

Inference
1. Parameters
The cell where things such as directory and other settings can be adjusted for the rest of inference.
Requires setting up a videos folder if not using an existing one already.

2. Functions
Utility functions to be used later on

3. Detection
The call to the YOLOv5 architecture to perform inference on a set up videos as denoted in the paramters cell.

4. Process Labels
Post-processes the raw output from YOLOv5 to fill in gaps, remove outliers, and group together detections.

5. OCR
Runs OCR on groupings of detections to verify results from YOLOv5 and assign speed limit numbers.

6. Generate snippet highlights
Creates video snippets of every grouping of detection for ease of double checking

7. Generate results
Creates a more human readable csv for detections

8. Generate videos
Creates a full video with bounding boxes of detections.
