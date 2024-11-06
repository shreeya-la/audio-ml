# audio-ml

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
