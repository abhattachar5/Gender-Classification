# Gender-Classification
A Gender Classifier based on the UKT Image dataset and a custom VGG CNN architecture 

# UKT Image Dataset 
- Consists of 20k+ face images in the wild (only single face in one image)
- Provides the correspondingly aligned and cropped faces
- Provides the corresponding landmarks (68 points)
- Images are labelled by age, gender, and ethnicity.
- The dataset can be downloaded from https://susanqq.github.io/UTKFace/  (Note: Please use the Aligned and Cropped Faces repository) 
- The labels of each face image is embedded in the file name, formated like [age]_[gender]_[race]_[date&time].jpg
- The images were seggregated by using the Gender code in the lables of each image. Please use the file **Preprocessing_File Copy_UKT Dataset** for seggregating the dataset into Male and Females


# Custom VGG Architecture
- Input Shape - 128 x 128
- Convolution Layer (32) 
- Convolution Layer (32)
- Pooling Layer (2x2)
- Convolution Layer (64)
- Convolution Layer (64)
- Pooling Layer (2x2)
- Convolution Layer (128)
- Convolution Layer (128)
- Pooling (2x2)
- Flatten Layer
- FUC (128) Relu
- Output Later (Output - 1) (Activation = Sigmoid; Loss = Binary Crossentropy; Optimiser = Adam)


# Using the Trained Model
- The trained model can be found in **Kaggle_Gender_Classifier2_128_CustomVGG_100epochs_09012020.h5
- Use the file **Video_Gender Predictor_CustomVGG_CNN** changing the model location in the file to use the gender predictor with the computer Webcam
