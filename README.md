# isic_melanoma_contest_task3

Disease classification model for ISIC 2018: Skin Lesion Analysis Towards Melanoma Detection – Task 3.

The original data set of 10K images was augmented by rotating 90 degrees x 3 = 40K images. All of these images were then zoomed by 20% = 80K images. The images were then divided into training and validation sets of 64K (80%) and 16K (20%). Note that the augmented images were not mixed between the training and validation sets to prevent data leakage.

The data was then trained on the Keras VGG16, InceptionV3, and ResNet50 models. The best performing model was the ResNet50 which is detailed on the attached Jupyter Notebook.

The final model was trained on a GTA 1080ti for 1 epoch / 514 seconds, resulting in the following performance:

					Loss	  Accuracy
			Training	0.3958	  0.8576
			Validation	0.4438	  0.8516

The model was then run on the contest validation data of 193 images resulting in an accuracy of 81.7%. Final results for the 1,512 test images will be available on 07/29/2018.
