# isic_melanoma_contest_task3

Disease classification model for ISIC 2018: Skin Lesion Analysis Towards Melanoma Detection – Task 3.

The original data set of 10K images were rotated by 90 degrees x 3 and then zoomed by 20% resulting in 80K total images. The data was then divided into training and validation sets of 64K (80%) and 16K (20%). Note that the augmented images were separated between the training and validation sets to prevent data leakage.

The data was then trained on VGG16, InceptionV3, and ResNet50 models using Keras. The best performing model was based on ResNet50 which is shown on the attached Jupyter Notebook.

The ResNet50 model was trained for 1 epoch / 514 seconds on a GTA 1080ti GPU, resulting in the following performance:

					Loss	  Accuracy
			Training	0.3958	  0.8576
			Validation	0.4438	  0.8516

The model was also achieved a classification accuracy of 81.7% based on the ISIC contest validation data set of 193 images.

Final results for the 1,512 test images will be available on 07/29/2018.
