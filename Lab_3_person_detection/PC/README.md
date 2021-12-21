## Requirements
All frameworks needed to use this project are located in the requirements.txt file. These can be installed as follows:
```
pip install -r requirements.txt
```

## Prepare training data
At the beginning you need to download the COCO dataset and extract the required data from the dataset. For this the script `1_Prepare_training_data.ipynb` is executed.


## Training a model
In the script `2_Train_person_detection_model.ipynb`, the extracted data is loaded and then a neural network is trained with this data. Afterwards the trained model is stored in the folder `model`.


## Execute the model
The script `3_Person_detection.ipynb` is used to load the previously trained  model. Afterwards a window with the camera streams opens and the images of the camera get predicted from the model.
