# Stratified-k-fold-Cross-Validation with Ensemble Deep Learning for Image Classification using Keras
This python program demonstrates image classification with stratified k-fold cross validation technique with 5 deep learning models for image classification. Libraries required are keras, sklearn and tensorflow.
* The DS.zip file contains a sample dataset that I have collected from Kaggle.com. It consists of three folders (Train, Test, and Validation) and each of these three folders consists of folders according to class labels (e.g., circles, triangles, and squares).
* Checkout the code in **stratified_K_fold_CV_ensemble_deep_learning.ipynb** notebook.
* There are 5 DL models in the code and the best 3 performing models are selected for the final ensemble soft voting. The model_1 is a custom model, model_2 (Xception), model_3 (DenseNet201), model_4 (VGG16), and model_5 (InceptionResNetV2). 
* Change the batch size, epoch, and the structure of the CNN models according to your needs. Here, some naive values are provided without any hyper-parameter tuning.
* Change the contents of DS folder according to your dataset/images. But initially keep all the images inside the sub-folders of the "train" folder. The program will take care of splitting the test images and validation images inside the code. Also, don't forget to rename your sub-folders inside train, test and validation folder according to your classes.
# Results
* In the following figure, the average accuracy, precision, and f1-score of the k-fold CV is illustrated for the 5 DL models.
![image](https://user-images.githubusercontent.com/27827295/204691256-cc9996c9-d977-41d5-8a06-7f23257ad483.png)
* The top 3 DL models are selected as the final models to be used in the ensemble technique. In this case model_2 (Xception), model_3 (DenseNet201), model_5 (InceptionResNetV2). In the test data, the ensemble of the 3 models performs better than the individual models.
