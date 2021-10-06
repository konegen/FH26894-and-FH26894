## Record training data
At the beginning you need some data to train your `Wake Word` model. There is already a prerecorded dataset which can be downloaded [here](http://download.tensorflow.org/data/speech_commands_v0.02.tar.gz). Unzip the data and put the different folders you want to use as `Wake Words` into the folder `'data/commands'`. 

Otherwise you can record some data for the training of your `Wake Word` model. Therefore you have to execute the `Record_training_data.ipynb`.


## Data augmentation
To generate more data for training the neural network, data augmentation is applied. Therefore we use the `Data_augmentation.ipynb` script. 4 different augmentation will applied to the data:
- Noise - Add additional meaningless data to the audiodata
- Shift - Randomly shift audiodata to the left or right
- Pitch - Change pitch randomly
- Speed - Speeds up or slows down the audio signal

Afterwards the augmented data get stored in the folder `augmented_data`. 


## Training a model
In the script `Train_model.ipynb`, the augmented data is loaded, preprocessed, and then a neural network is trained with this data. Afterwards the trained model is stored in the folder `models`.

Otherwise there are already prerecorded commands in the `'data/commands'` folder. These can also be used to train a net with the `Train_model_prerecorded.ipynb` script.


## Execute the model
The script `Wake_Word_prediction.ipynb` is used to load the previously trained wake word model. Afterwards the wake words can be spoken and it is returned what was recognized by the model.