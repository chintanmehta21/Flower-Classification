# Flower-Classification

### Description
This project was a part of the Kaggle's "[Petals to the Metal](https://www.kaggle.com/c/tpu-getting-started/overview) - Flower Classification on TPU" competition. The main purpose of the development process was classifying 104 types of flowers. We developed this highly effective model using Effnet and ExceptionNet algorithms. 

### Data
 - Dataset of 104 types of flowers has been used
 - Dataset has been drawn from 5 different public Datasets
 - Some classes are very narrow, containing only a particular sub-type of flower (e.g. pink primroses) while other classes contain many sub-types (e.g. wild roses)
 - This entire data is in TFRecord format
 - The TFRecord format is a container format frequently used in Tensorflow to group and shard data data files for optimal training performace
 - Each file contains the id, label (the class of the sample, for training data) and img (the actual pixels in array form) information for many images
 -  * train/*.tfrec - training samples, including labels
    * val/*.tfrec - pre-split training samples w/ labels intended to help with checking your model's performance on TPU. The split was stratified across labels
    * test/*.tfrec - samples without labels - you'll be predicting what classes of flowers these fall into
    * sample_submission.csv - a sample submission file in the correct format
    * id - a unique ID for each sample
    * label - (in training data) the class of flower represented by the sample
 - Link to the Datasets : 
 -  * [192 x 192 Dataset](https://drive.google.com/file/d/1a6LfrNf9ex-6vYLzhGVJUQ83z3zbJwpx/view?usp=sharing)
 -  * [224 x 224 Dataset](https://drive.google.com/file/d/1jH4B0VJGbkhADyy2gmoW-wH7avH1CGk6/view?usp=sharing)
 -  * [331 x 331 Dataset](https://drive.google.com/file/d/1FjXO2ct4dU30kU4lLzaiLoMl2a2fcWva/view?usp=sharing)
 -  * [512 x 512 Dataset](https://drive.google.com/file/d/1P0JO2Dk9SeK8m-QMn9YYEo4IqqsHr0LE/view?usp=sharing)

### Features
 - Uses EffNet and ExceptionNet algorithm to classify the flowers
 - Training and Testing is performed in the 80:20 ratio
 - Image size used for training and testing is 512x512
 - Batch size for training is 16 images
 - The model has a f1 score of 0.964 i.e. accuracy of 96%
