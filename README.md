# Uni-CV-Projects

Individual projects for the Computer Vision course, taken in the 1st year of the Artificial Intelligence master program at the Faculty of Mathematics and Computer Science, University of Bucharest.

## Mathable Score Calculator

The project consisted of calculating the scores of two players during multiple iterations of the board game Mathable. A multitude of images were given (regular, rotated, and perspective views), showing the players' placed tokens as well as the state of the game board during the players' moves.

Click [here](https://tinyurl.com/CV-2024-Project1) to see the datasets, as well as other project details.

<details>
<summary><h4>Images depicting the game and the datasets:</h4></summary>

![image](https://github.com/user-attachments/assets/259c5885-e049-44ee-9dc7-68f621577fa8)
![image](https://github.com/user-attachments/assets/d6f86a69-a3e3-415c-8e3c-f1e55b1f92ec)
</details>

The approach taken to realize this project involved the use of the following computer vision methods:
- **template matching**: in the beginning, templates of each token and type of board tile were extensively cropped, so as to recognize the newly placed token in each player's move
- **SIFT features**: in order to "straighten" rotated and perspective images of the board
- **projective transformations**: used alongside SIFT features
> Note: for further details about the project solution, please consult [this path](https://github.com/alexsasu/Uni-CV-Projects/tree/main/Mathable%20Score%20Calculator/Documentation) inside the repository

This project solution achieved **correct results on all of the given input data** (see the link to the datasets from above).

## Video Surveillance of On-Street Parking Spaces

The goal of this project was to solve four tasks tied to the surveillance of diagonal on-street parking spaces and two traffic lanes:
- Task 1: determine which parking spaces are occupied and which are not, from an image and a txt file of the given parking spaces
- Task 2: the same requirements as task 1, but this time checking all of the parking spaces instead of just a few given ones
- Task 3: tracking a specific car during a short video of up to one minute
- Task 4: identify how many cars are stopped at a red traffic light at the last frame of a similarly lengthy video to the ones at task 3

Click [here](https://tinyurl.com/CV-2024-Project2) to see the datasets, as well as other project details.

<details>
<summary><h4>The 10 parking spaces of interest and the two lanes:</h4></summary>

![image](https://github.com/user-attachments/assets/317655a8-856a-40b1-9586-42388da442f2)
</details>

In order to solve this project, the following methods were employed:
- For all of the tasks, a pretrained version of the **YOLOv9** model was used, namely the **YOLOv9e** detection model from the [Ultralytics](https://docs.ultralytics.com/models/yolov9/) website
- Tasks 1 & 2: because the model had trouble detecting parking spaces that were farther away, a manual cropping of the last 5 spaces was made and then fed to the model
- Task 3: the tracking was made by calculating **IoU scores** at each frame between the last retained bounding box and all of the bounding boxes detected in the current frame 
- Task 4: similarly to tasks 1 and 2, a multitude of croppings were made in order for the model to more accurately detect farther away cars, and only the last frame of the video was taken into account
> Note: for further details about the project solution, please consult [this path](https://github.com/alexsasu/Uni-CV-Projects/tree/main/Video%20Surveillance%20of%20On-Street%20Parking%20Spaces/Documentation) inside the repository
