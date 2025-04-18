# audio-ml

The is an audio classification project. The goal is to use a pretrained model (YAMNet or VGGish) along with a Sequential model to classify the animal noise in an input .wav file. The ESC-50 dataset is used for training and testing; this is the most popular dataset for Environmental Sound Classification (ESC).

**Working Notebooks:**
- **yamnet.ipynb:** 
  - Low accuracy: 68.62%
    -  Followed tutorial to get to this point: https://www.tensorflow.org/tutorials/audio/transfer_learning_audio
  - TFLite model has a 92.5% accuracy! and a size of 15MB
  - Uses post-training quantization
  - **The quantized accuracy is 91.25% and the size is 4MB**
  - Another Colab notebook was needed for Quantization Aware training (because another version of Keras was needed); see next
 
- **yamnet_quant_aware_training.ipynb**
  - Same model structure as above, but different quantization method
  - The quantized accuracy is 90.0% and the size is 13.4MB
  - This is too large for our embedded device
- **yamnet_simple.ipynb:** YAMNet model into a simple Sequential model
  - Accuracy: 93.75%
  - TFLite model has a very low accuracy of 9.25%
- **yamnet_with_lstm.ipynb:** YAMNet model into a Sequential model using an LSTM layer
  - Slightly better accuracy than the simple model: 95.05%
  - We are avoiding complex models/layers to save on size

- **vggish.ipynb:** VGGish model into a Sequential model using an LSTM layer
  - Accuracy is 86.25% but the VGGish model itself is 288MB
  - This is too large, so we did not proceed with VGGish
