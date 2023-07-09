# NNCodec
Here, I'm learning, where we can use NNCodec.  
I'm using NNCodec then presented in 2022  
Page of article:  https://arxiv.org/abs/2210.13438; PDF: https://arxiv.org/pdf/2210.13438.pdf.  

This is block of encoder:  
![Block of encoder](https://github.com/NikSuPNU/NNCodec/blob/main/encoder.png)

Total params: 3,220,976;  
Trainable params: 3,220,976;  
Non-trainable params: 0.  

The encodec uses several blocks:  
  --Conv1D (Applies a 1D convolution over an input signal composed of several input planes.)  
  
  --Elu (Applies the Exponential Linear Unit (ELU) function, element-wise, as described in the paper: Fast and Accurate Deep Network Learning by Exponential Linear Units (ELUs). https://pytorch.org/docs/stable/generated/torch.nn.ELU.html)  
  
  --LSTM (Applies a multi-layer long short-term memory (LSTM) RNN to an input sequence. https://pytorch.org/docs/stable/generated/torch.nn.LSTM.html)  

Also used in the codec "Residual neural network" https://en.wikipedia.org/wiki/Residual_neural_network.  


