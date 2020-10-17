# BADMINTON MATCH VIDEO ANALYSIS USING YOLOV3, PYTORCH AND MXNET MODEL ARCHITECTURES

*Completed by: <br />
  Nethra Viswanathan <br />
  Deepika <br />
  Saimonika Kalasamudram <br />*
  
## Proposals achieved as part of the project:

Please find below the output achieved out of the objectives mentioned in the proposal document for a short badminton singles match video:
1.	Recognition and classification of the 2 opponents with distinct name labels, say Player 1 and Player 2 - **Player1 and Player 2 are detected with bounding boxes**
2.	Recording and displaying the Start time and end time of the match - **Timer keeps running throughout the match video.**
3.	Displaying the number of hits made by each player  - **Instead of displaying the number, HIT is highlighted on every hit.**
4.	Displaying the number of out of the boundary hits (AWAYs) made by each player during the course of match - **Instead of displaying the number, AWAY is highlighted on every AWAY hit by the player.**
5.	Visualization of the trajectory of the shuttlecock - **Shuttlecock is detected in every frame of the video with a bounding box.**



## Deliverables of the Project:

The code works well in Google Colab Pro. Hence it is recommended to execute the code in Colab Pro.In case the code needs to be run in local system, steps are provided for the purpose as well. The complete set of folders mentioned below are downloaded from Onedrive link by the code in this notebook for further processing.

All the annotated image files and videos have not been placed in deliverables due to space constraint.

1. **Folder "data"** : Contains all the training and test images for both the above mentioned models
2. **data/annotations/labels** : Contains all the frame numbers and labels in a txt file for training and validation of MXNet model for detection of hits 
3. **data/MXNetvideos** : Contains the training videos of badminton match for MXNet model (detection of hits)
4. **data/MXNetframe**s : Contains the frames of all the videos present in the above folder as the model trains on images and not videos directly. The folder also contains the frames of the test videos.
5.**data/Test** : Contains the test videos for testing the MXNet model (detection of hits). The model will pick the test videos from here for detection of hits and AWAYs.
6. **data/Test_Results**: Both the models (MXNet and YOLOv3) place the resultant videos of tested videos in this path. The yolo result of player and shuttlecock detection is saved as "<Videoname>_detected.mp4" and the combined result of both the models is saved in "results.mp4". his folder shiuld be empty while we execute the testing script.
7. **data/Saved_test_results**: Contains the backup of currently saved test results as the TEST_RESULTS folder is supposed to be empty while executing the code
8. **data/splits**: Contains the video names and corresponding frame numbers in  3 different text files - train, val and test for training, validation and testing of the MXNet model for detection of hits. The test.txt file is populated through code with the video file name and frame numbers of the frames extracted from the test video uploaded in TEST folder.
9. **data/YoloTrainingImages**: Contains the training images of YoloV3 model for object detection ,  the annotation csv file and the annotation text file in YOLO format "data_train.txt"
10. **models/vision/experiments/0000**: Contains the weights calculated for 19 epochs of the MXNet model , scores.txt containing the scores of accuracy for each epoch, log file and a tensorboard event folder "tb" which records the trining sumamry in tensorboard format.
11. **models/YoloV3**: Contains tensorboard logs  in "logs" folder,  the base model files of keras yolo3 with weights in "keras_yolo3" folder
12. **models/vision/experiments/0000/tbpyt**: Contains the weights of Pytorch model as a result of 3 methods of training alomng with event logs for Tensorboard.

## Project Tasks and Code Agenda:


1.   **Detection of Players and Shuttlecock**

      *   Package Installation
      *   Import statements
      *   File Path declarations
      *   Class definitions
      *   Stand alone Funtion definitions
      *   Training code
      *   Detection code

2.   **Detection of Hits and Aways in the game**

      *   Package Installation
      *   Import statements
      *   File Path declarations
      *   Class definitions
      *   Stand alone Funtion definitions
      *   Training code
      *   Detection code
