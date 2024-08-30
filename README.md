# Mathable-AI-Score-Calculator

Individual project for the Computer Vision course, taken in the 1st year of the Artificial Intelligence master program at the Faculty of Mathematics and Computer Science, University of Bucharest.

The project consisted of using multiple computer vision methods in order to calculate the scores of two players during multiple iterations of the board game Mathable. A multitude of images were given (regular, rotated, and perspective views), depicting the the players' placed tokens as well as the state of the game board during the players' moves. Further details about the datasets containing these images can be consulted [here](https://tinyurl.com/CV-2024-Project1).

<details>
<summary><h4>Visual details about the game and the datasets (also found in the "details.pdf" file inside the "Project details" directory):</h4></summary>

![image](https://github.com/user-attachments/assets/259c5885-e049-44ee-9dc7-68f621577fa8)
![image](https://github.com/user-attachments/assets/d6f86a69-a3e3-415c-8e3c-f1e55b1f92ec)
</details>

The approach taken to realize this project involved the use of the following computer vision methods:
- **template matching**: in the beginning, templates of each token and type of board tile were extensively cropped, so as to recognize the newly placed token in each player's move
- **SIFT features**: in order to "straighten" rotated and perspective images of the board
- **projective transformations**: used alongside SIFT features
> Note: for further details about the project solution, please consult the "documentation.pdf" file in the "Documentation" directory

This project solution achieved **correct results on all of the given input data** (see the link to the datasets from above).
