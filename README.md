# UrbanSound Classification with CNN and RNN
![cnn_rnn_logs](https://user-images.githubusercontent.com/55723894/99321383-af0d5480-283b-11eb-8c82-374953c13669.jpeg)
### Table of Contents
* [About the Project](#about-the-project)
* [Built With](#built-with)
* [Usage](#usage)
* [NoteBooks](#notebooks)
* [Contact](#contact)

### About the Project
This project is about applying deep learning technologies to classify the sound files. Also this is a course project for 
my graduate study in the deep learning theories taught by [Dr. Emad Mohammed](https://scholar.google.com/citations?user=hJPaK90AAAAJ&hl=en) in the Lakehead 
University in 2019.

### Built With
The project code is written in python in Jupyter Notebook. It could also be implemented on Google Colaboratory, and the file path needs to be modified based 
on the dataset folder in the google drive.   
* [Tensorflow](https://www.tensorflow.org/)
* [Keras](https://keras.io/guides/)
* [Numpy](https://numpy.org/)
* [Scikit-Learn](https://scikit-learn.org/stable/)
* [Pandas](https://pandas.pydata.org/)
* [Librosa](https://librosa.org/)
* [Matplotlib](https://matplotlib.org/)

### Movitation
UrbanSound8K dataset is not a new dataset for the classification challenge. There have been several researches conducted based on this dataset with the 
machine learning algorithms from 2014-2016. However, this project is not to examine the previous research result or to copy the publication result into the 
notebook. Instead, I use this dataset to implement all the deep learning technologies I've learnt from the class, so this project contains a full workflow 
from the raw data processing to final deep learning model construction including CNN, RNN, Transfer Learning and Functional API, etc. 

### Dataset
Due to the large size of the dataset, I cannot upload it to the github repo. but the dataset could be 
downloaded from this [link](https://urbansounddataset.weebly.com/urbansound8k.html). The dataset has 8732 audio files of urban sounds in .wav format and 
all stats information of the dataset is saved a meta-data file named as "UrbanSound8K.csv". This csv file is also the entry point of the data preprocessing 
in the notebook. 

Sound classes:
0 = air_conditioner
1 = car_horn
2 = children_playing
3 = dog_bark
4 = drilling
5 = engine_idling
6 = gun_shot
7 = jackhammer
8 = siren
9 = street_music

Sound labels: air_conditioner, car_horn, children_playing, dog_bark, drilling, engine_idling, gun_shot, jackhammer, siren, street_music.

### Notebooks
To use the notebooks posted in this repo, please check some modifications as follows: 
1. The original data are split into 10 folders which is setup to examine the experiment result in the publication. But to use the notebooks in the repo, 
please merge all 10 folders into one folder and change the path in the notebook to link the metadata file.
2. The data pipeline includes a series of transformation from original wmv files to final trainable data.So the transformed data are saved in the binary
files at each stage, but due to the size limit, it's not updated in the repo and the same binary files could be generated via running the Data Processing 
notebook.
3. RNN & CNN Modeling notebook runs based on all the data generated by the Data Processing notebook including both split and non-split dataset. There are 
four binary files that could be generated in the Data Processing notebook for the model training and the details are as follows: 
- api_rnn_tensor_nosplit: one binary file containing all sound data for RNN training without any split ((x_train, y_train) = api_rnn_tenor_nosplit)
- api_cnn_tensor_nosplit: one binary file containing all sound data for CNN training without any split ((x_train, y_train) = api_cnn_tenor_nosplit)
- api_rnn_tensor: one binary file containing all sound data for RNN training with a split 80% for train and 20% for validation 
((x_train, y_train, x_val, y_val) = api_rnn_tenor)¶
- api_cnn_tensor: one binary file containing all sound data for RNN training with a split 80% for train and 20% for validation 
((x_train, y_train, x_val, y_val) = api_cnn_tenor) 

### Contact
C.Young: kyang3@lakehadu.ca

Project Link: https://github.com/mlmaster1995/UrbanSound-Classification_CNN_RNN


 
