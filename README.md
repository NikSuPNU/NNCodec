# NNCodec
Here, I'm learning, where we can use NNCodec.
I'm using NNCodec then presented in 2022
Page of article:  https://arxiv.org/abs/2210.13438; PDF: https://arxiv.org/pdf/2210.13438.pdf'

This is block of encoder:
![Block of encoder](https://github.com/NikSuPNU/NNCodec/blob/main/encoder.png)

Summary of NNCodec:

SEANetEncoder(
  (model): Sequential(
    (0): SConv1d(
      (conv): NormConv1d(
        (conv): Conv1d(1, 32, kernel_size=(7,), stride=(1,)), 288 params
        (norm): Identity(), 0 params
      ), 288 params
    ), 288 params
    (1): SEANetResnetBlock(
      (block): Sequential(
        (0): ELU(alpha=1.0), 0 params
        (1): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(32, 16, kernel_size=(3,), stride=(1,)), 1,568 params
            (norm): Identity(), 0 params
          ), 1,568 params
        ), 1,568 params
        (2): ELU(alpha=1.0), 0 params
        (3): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(16, 32, kernel_size=(1,), stride=(1,)), 576 params
            (norm): Identity(), 0 params
          ), 576 params
        ), 576 params
      ), 2,144 params
      (shortcut): SConv1d(
        (conv): NormConv1d(
          (conv): Conv1d(32, 32, kernel_size=(1,), stride=(1,)), 1,088 params
          (norm): Identity(), 0 params
        ), 1,088 params
      ), 1,088 params
    ), 3,232 params
    (2): ELU(alpha=1.0), 0 params
    (3): SConv1d(
      (conv): NormConv1d(
        (conv): Conv1d(32, 64, kernel_size=(4,), stride=(2,)), 8,320 params
        (norm): Identity(), 0 params
      ), 8,320 params
    ), 8,320 params
    (4): SEANetResnetBlock(
      (block): Sequential(
        (0): ELU(alpha=1.0), 0 params
        (1): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(64, 32, kernel_size=(3,), stride=(1,)), 6,208 params
            (norm): Identity(), 0 params
          ), 6,208 params
        ), 6,208 params
        (2): ELU(alpha=1.0), 0 params
        (3): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(32, 64, kernel_size=(1,), stride=(1,)), 2,176 params
            (norm): Identity(), 0 params
          ), 2,176 params
        ), 2,176 params
      ), 8,384 params
      (shortcut): SConv1d(
        (conv): NormConv1d(
          (conv): Conv1d(64, 64, kernel_size=(1,), stride=(1,)), 4,224 params
          (norm): Identity(), 0 params
        ), 4,224 params
      ), 4,224 params
    ), 12,608 params
    (5): ELU(alpha=1.0), 0 params
    (6): SConv1d(
      (conv): NormConv1d(
        (conv): Conv1d(64, 128, kernel_size=(8,), stride=(4,)), 65,792 params
        (norm): Identity(), 0 params
      ), 65,792 params
    ), 65,792 params
    (7): SEANetResnetBlock(
      (block): Sequential(
        (0): ELU(alpha=1.0), 0 params
        (1): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(128, 64, kernel_size=(3,), stride=(1,)), 24,704 params
            (norm): Identity(), 0 params
          ), 24,704 params
        ), 24,704 params
        (2): ELU(alpha=1.0), 0 params
        (3): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(64, 128, kernel_size=(1,), stride=(1,)), 8,448 params
            (norm): Identity(), 0 params
          ), 8,448 params
        ), 8,448 params
      ), 33,152 params
      (shortcut): SConv1d(
        (conv): NormConv1d(
          (conv): Conv1d(128, 128, kernel_size=(1,), stride=(1,)), 16,640 params
          (norm): Identity(), 0 params
        ), 16,640 params
      ), 16,640 params
    ), 49,792 params
    (8): ELU(alpha=1.0), 0 params
    (9): SConv1d(
      (conv): NormConv1d(
        (conv): Conv1d(128, 256, kernel_size=(10,), stride=(5,)), 328,192 params
        (norm): Identity(), 0 params
      ), 328,192 params
    ), 328,192 params
    (10): SEANetResnetBlock(
      (block): Sequential(
        (0): ELU(alpha=1.0), 0 params
        (1): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(256, 128, kernel_size=(3,), stride=(1,)), 98,560 params
            (norm): Identity(), 0 params
          ), 98,560 params
        ), 98,560 params
        (2): ELU(alpha=1.0), 0 params
        (3): SConv1d(
          (conv): NormConv1d(
            (conv): Conv1d(128, 256, kernel_size=(1,), stride=(1,)), 33,280 params
            (norm): Identity(), 0 params
          ), 33,280 params
        ), 33,280 params
      ), 131,840 params
      (shortcut): SConv1d(
        (conv): NormConv1d(
          (conv): Conv1d(256, 256, kernel_size=(1,), stride=(1,)), 66,048 params
          (norm): Identity(), 0 params
        ), 66,048 params
      ), 66,048 params
    ), 197,888 params
    (11): ELU(alpha=1.0), 0 params
    (12): SConv1d(
      (conv): NormConv1d(
        (conv): Conv1d(256, 512, kernel_size=(16,), stride=(8,)), 2,098,176 params
        (norm): Identity(), 0 params
      ), 2,098,176 params
    ), 2,098,176 params
    (13): SLSTM(
      (lstm): LSTM(512, 512, num_layers=2), 4,202,496 params
    ), 4,202,496 params
    (14): ELU(alpha=1.0), 0 params
    (15): SConv1d(
      (conv): NormConv1d(
        (conv): Conv1d(512, 128, kernel_size=(7,), stride=(1,)), 459,008 params
        (norm): Identity(), 0 params
      ), 459,008 params
    ), 459,008 params
  ), 7,425,792 params
), 7,425,792 params
=======================================================================
Total params: 3,220,976
Trainable params: 3,220,976
Non-trainable params: 0
-----------------------------------------------------------------------
