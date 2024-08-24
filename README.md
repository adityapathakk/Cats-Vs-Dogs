# Project: Classifier for Cats and Dogs
### Tech-Stack: Deep Learning in Python
- <b>Libraries:</b> Tensorflow, Keras, OpenCV, Matplotlib, Pandas
- <b>Concepts:</b> CNNs, Data Augmentation, Transfer Learning, Data Visualisation
- <b>Tools</b>: Google Colab, Kaggle, VS Code

I developed this <s>FOR FUN</s> to revise Deep Learning fundamentals using the popular classification problem - <i><b>Cats Vs Dogs</b></i>!<br>
If you'd like to upvote/comment/copy this notebook on Kaggle, here's the link to my <a href = "https://www.kaggle.com/code/adityapathak03/comprehensive-guide-to-cnns-with-cats-vs-dogs">Comprehensive Guide to CNNs with Cats Vs Dogs</a>!

# Project Methodology & Details

### 1. Importing Libraries and Loading Dataset
The dataset used for this project can be found <a href = "https://www.kaggle.com/datasets/salader/dogs-vs-cats">here</a>. It is a popular dataset with a file size of 1GB.<br>
Refer to the picture below to see some of the libraries that were used.

<img width="1130" alt="Screenshot 2024-08-24 at 3 47 56 PM" src="https://github.com/user-attachments/assets/b17e5429-a8f4-4e35-a3d0-d137a746a597">

#### 1.1 Data Normalisation
A ```process``` function was defined to maintain the pixel values of the images in the dataset between 0 and 1 as opposed to 0 and 255.

<img width="1130" alt="Screenshot 2024-08-24 at 3 51 10 PM" src="https://github.com/user-attachments/assets/0c62e818-3038-42fa-8518-d59683f77b78">

### 2. Data Visualisation
I observed some of the images present in the dataset.
<p float="left">
  <img width="700" alt="Screenshot 2024-08-24 at 4 21 30 PM" src="https://github.com/user-attachments/assets/8ba52f1a-2539-4c7e-aa3d-13cd628880ac">
  <img width="700" alt="Screenshot 2024-08-24 at 3 54 01 PM" src="https://github.com/user-attachments/assets/eb0a9c08-475a-4cbd-9abe-002094a62636">
</p>

### 3. Developing Simple CNNs
I developed 5 simple CNNs with increasing complexity -

- Model 1 is a basic CNN for introductory purposes.
- Model 2 shows how Batch Normalisation and Dropout increase validation accuracy quite a bit. This is a type of regularisation.
- Model 3 tries L1 regularisation, while Model 4 tries L2 regularisation.
- Model 5 is a complex CNN that does quite well. It has a lot of convolutional layers that can gather a lot of information from the dataset.

Take a look below for some snapshots of the models and their training process -
<p float="left">
  <img width="1315" alt="CNN Model 1" src="https://github.com/user-attachments/assets/e558b751-c9c0-4df2-b625-e87064af8470">
  <img width="700" alt="CNN Model 2" src="https://github.com/user-attachments/assets/3f63157e-5230-4c78-82a3-212f01cb7357">
  <img width="700" alt="CNN Model 3" src="https://github.com/user-attachments/assets/a6583ef6-010b-4433-8a7d-6e1d1f320481">
  <img width="700" alt="CNN Model 4" src="https://github.com/user-attachments/assets/86aa741a-1b76-4a7e-9199-99b34077527f">
  <img width="700" alt="CNN Model 5" src="https://github.com/user-attachments/assets/4422f8f2-bb83-4c3e-a003-722e4964c774">
</p>
Out of all these, Model 5 performed the best, with <b>both training accuracy and validation accuracy reaching > 91%</b>!

### 4. CNN with Augmented Data
Using some simple data augmentation layers like ```RandomFlip```, ```RandomRotation```, ```RandomZoom```, ```RandomTranslation```, and ```RandomContrast```, implemented a CNN with augmented data.

<img width="700" alt="Screenshot 2024-08-24 at 11 44 42 PM" src="https://github.com/user-attachments/assets/1fec0e30-36ad-4fa9-990b-3faf5dd19b9e">

### 5. Transfer Learning - VGG16
Harnessed the popular pre-trained model VGG16 to achieve extremely accurate results.
<p float="left">
  <img width="700" alt="Screenshot 2024-08-24 at 11 46 40 PM" src="https://github.com/user-attachments/assets/0c2c6fc5-fb18-42b5-9f49-67e71490f24d">
  <img width="700" alt="Screenshot 2024-08-24 at 11 47 46 PM" src="https://github.com/user-attachments/assets/b075ed20-66ae-4f26-ae0f-d83f778d3ee5">
</p>

### 6. Visualized Accuracy with Graphs
Plotted graphs for training accuracy vs validation accuracy and training loss vs validation loss for all the models

![image](https://github.com/user-attachments/assets/dff73ade-ff40-487d-8acf-4c1548259bb6)

### 7. Making Predictions
2 images were selected at random. After resizing, predictions were made using the VGG model. They were correct :D 

<img width="750" alt="Screenshot 2024-08-24 at 11 52 19 PM" src="https://github.com/user-attachments/assets/e368a71e-7d82-4fa2-8e7c-50cd25a46e25">

### 8. Closing Note
- If you observe the model fitting process of some models (for example, CNN Model #4), then you'll notice that the model reached a certain peak in accuracy during training, but when the number of epochs ended, it was nowhere near that peak. To fix this, we can use callback functions like 'Early Stopping' and 'Model Checkpoint'.
- You have to be extremely patient with Deep Learning. You have to keep evaluating model performance, fine-tune/update weights/layers and just find out what works and what doesn't. All this can be time-consuming, but it has to be done! So don't worry about taking your time.

# Thanks!
For checking this out. I hope you learnt something new here!
