# audio-ml

The is an audio classification project. The goal is to use a pretrained model (YAMNet or VGGish) along with a Sequential model to classify the animal noise in an input .wav file. The ESC-50 dataset is used for training and testing; this is the most popular dataset for Environmental Sound Classification (ESC).

**Working Notebooks:**
- **yamnet original.ipynb:** YAMNet model into a Sequential model
  - accuracy ~93%
  - unable to save as a working TFLite model
- **yamnet with lstm.ipynb:** YAMNet model into a Sequential model using an LSTM layer
  - slightly better accuracy than original (~95.5%)
- **yamnet (using tutorial).ipynb:** YAMNet model into a Sequential model using Google's tutorial
  - low accuracy (around 67%)
  - TFLite model has a 97.5% accuracy!

- **vggish.ipynb:** VGGish model into a Sequential model using an LSTM layer
  - accuracy around 88% but a very large model
