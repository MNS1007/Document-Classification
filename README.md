# Document-Classification
Task : The goal is to classify the document images into 16 types as proposed in the IndoML Datathon contest.
Base Data : 16,000 Images
Additional Data (Augumented Data)  : 16,000 Images (clockwise 90 degrees rotated images (Base Data was rotated and added as it was observed that some images were rotated in the original dataset)
Total Images : 32,000
Train - Cross Validation Split : 80:20
Procedure : 
The images were processed so as to create five seperate datasets
i. Header part of all images
ii. Footer of all images
iii. Left Body of all images
iv. Right Body of all images
v. And the original full image dataset

Each of the five datasets were trained in 5 seperate models :  Same Architecture 
Architecture of our CNN :
4 Convolutional layers (Conv2D + MaxPooling) + 2 Dense Layers 
input image size: 128*128
Conv2D-> MaxPooling2D -> Conv2D -> MaxPooling2D -> Conv2D -> MaxPooling2D -> Conv2D -> MaxPooling2D -> Dropout -> Flatten -> Dense -> Dense

All the output probabilities were then stacked to form new array which was then fed as the input for our final model. (Sequential Model)

Final Model Architecture 
Sequential Model
Dense -> Dropout -> BatchNorm -> Dense -> Dropout -> Dense

Final Training Accuracy : 90.35
Test F1 Score : 0.725

Final Competiton Rank : 38 out of 102.

Team Members:
Sharath S R
Suraj S 
Nithin Skantha M 

