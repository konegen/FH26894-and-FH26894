# Lab2: Wake Words-PC

## Record training data
At the beginning you need some data to train you `Wake Word` model. In the folder `'data/commands'` there are already prerecorded words you can use. If you want to use them, just put the folders with the commands into the `'recorded_data'` folder. Otherwise you can record some data for the training of your `Wake Word` model. Therefore you have to execute the `Record_training_data.ipynb`.

## Data augmentation
To generate more data for training the neural network, data augmentation is applied. Therefore we use the `Data_augmentation.ipynb` script. 4 different augmentation will applied to the data:
- Noise - add additional meaningless data to the audiodata
- Shift - randomly shift audiodata to the left or right
- Pitch - change pitch randomly
- Speed - speeds up or slows down the audio signal

Afterwards the augmented data get stored in the folder `augmented_data`. 

## Training a model
In the script `Train_model.ipynb`, the augmented data is loaded, preprocessed, and then a neural network is trained with this data. Afterwards the trained model is stored in the folder `models`.

## Execute the model
The script `Wake_Word_prediction.ipynb` is used to load the previously trained wake word model. Afterwards the wake words can be spoken and it is returned what was recognized by the model.
