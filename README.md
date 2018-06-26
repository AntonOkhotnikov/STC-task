## STC-task
Audio events classifier

### Files description:
* **create_train_set.ipynb** - creates and saves training set with 13 MFCC features for each time window (standard size is 25 ms and step is 10 ms, see *python_speech_features* documentation) in each file. All the files that are longer than 6 seconds are splitted to the 6 seconds subfiles and files shorter than 6 seconds are padded with zeros in the end.
* **train_model.ipynb** - loads training set and builds and fits Bidirectional LSTM model with 80 hidden units; saves the model.
* **prepare_test_set_and_predict.ipynb** - creates the testing set in the same way as the training set is done; loads saved model and predicts values for the testing set; saves result to the `result.txt`.
* **draft_create_train_set_and_bidir_LSTM.ipynb** - file is used for testing the ideas on the small amount of data.

### To reproduce the results
- Install *python_speech_features* library by running 
```
pip install python_speech_features
```
- Clone this repository in the same folder as **data_v_7_stc**
- Run in the next order 3 notebooks one by one:
1. *create_train_set.ipynb*
2. *train_model.ipynb*
3. *prepare_test_set_and_predict.ipynb*
- Results will be saved in the text file `result.txt`

### Libraries versions
- cython                    0.28.3
- ipython                   6.4.0
- jupyter                   1.0.0
- h5py                      2.8.0
- keras                     2.2.0
- matplotlib                2.2.2
- numpy                     1.12.1
- pandas                    0.23.1
- pip                       10.0.1
- python-speech-features    0.6
- scipy                     1.1.0
- tensorflow                1.8.0 

### Links used
* https://github.com/jameslyons/python_speech_features
* http://python-speech-features.readthedocs.io/en/latest/
* https://machinelearningmastery.com/sequence-classification-lstm-recurrent-neural-networks-python-keras/

### References
* http://www.diva-portal.org/smash/get/diva2:1030847/FULLTEXT01.pdf
* https://dspace.cc.tut.fi/dpub/bitstream/handle/123456789/22645/cakir.pdf
* http://www.cs.tut.fi/~sgn24006/PDF/L04-audio-classification.pdf

