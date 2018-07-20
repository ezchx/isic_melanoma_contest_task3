# isic_melanoma_contest_task3

Disease classification model for ISIC 2018: Skin Lesion Analysis Towards Melanoma Detection – Task 3.

The original data was augmented by rotating and zooming the images as well as adding and deleting certain images to improve and balance out the classification sets. Augmented images as well as images with identical legion identifiers https://forum.isic-archive.com/t/task-3-supplemental-information/430 were separated between training and validation sets to minimize data leakage.

The images were trained on the Keras VGG16, InceptionV3, and ResNet50 models. The best performing model was based on ResNet50 which is shown on the attached Jupyter Notebook.

The ResNet50 model was trained for 1 epoch / 281 seconds on a GTA 1080ti GPU, resulting in the following performance:

					Loss	  Accuracy
			Training	0.7592	  0.7234
			Validation	0.7210	  0.7381

The model achieved a classification accuracy of 77.6% based on the ISIC contest validation data set of 193 images.

Final results for the ISIC 1,512 test images will be available when the contest concludes on 07/29/2018.
