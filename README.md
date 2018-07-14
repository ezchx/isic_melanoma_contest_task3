# isic_melanoma_contest_task3

Disease classification model for ISIC 2018: Skin Lesion Analysis Towards Melanoma Detection – Task 3.

The original data set of 10K images was augmented by rotating 90 degrees x 3 for 40K total images These images were then zoomed by 20% for 80K total images. The images were then divided into training and validation sets of 64K (80%) and 16K (20%). Note that the augmented images were not mixed between the training and validation sets to prevent data leakage.

The original model was based on the Keras ResNet50 pre-trained ImageNet library. After replacing the 1K classification dense layer with a 7 classification dense layer, ALL of the layers were trained on the 80k images with a learning rate of 0.00003. The final model was trained on a GTA 1080ti for 1 epoch / 514 seconds, resulting in the following performance:

					Loss	  Accuracy
			Training	0.3958	  0.8576
			Validation	0.4438	  0.8516

The model was then run on the contest validation data of 193 images resulting in an accuracy of 81.7%. Final results for the 1,512 test images will be available on 07/29/2018.
