# Text-generation-using-LSTM
Character-level text generation using simple LSTM model in Pytorch

This notebook illustrates a LSTM network to generate new piece of text at character level.
It is part of Udacity's Computer Vision and Deep learning Nanodegrees.

The model was trained on GPU using Tolstoi's Anne Karenina masterpiece. The model is then able to generate new text based on the text from the book.
The full dataset (Tolstoi's novel) has a total of nearly 2bn characters which is split between training and validation (10%). The model is fed with batches of size (128, 100) characters. 

Hyperparameters of the model architecture can be defined for testing purpose :
- number of LSTM layers
- hidden unit dimensions

The output is generated character by character. A prime word is given to the trained model to initiate the process. Topk is used to improve the quality of the output while introducing some randomness.

## Results

I trained a 3-layer model with 1024 hidden diensions for 25 epochs which provides convincing results. A simpler model version can be trained more rapidely (2 layers, 512 hidden dimension) while still delivering good results. Saved weights for the deeper model are available in the repo.

![](assets/sample_output.PNG)
