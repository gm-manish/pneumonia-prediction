
# Instruction for Running the Code

Step 1: Download the Data From the Given [Source](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)<br>

Step 2: Open the Notebook and Use Runall. (Since there is a considerable number of parameters, there may be high usage of CPU and GPU.)<br>

Note that: We have also used model checkpointing if there is failure in training.

# Pneumonia Prediction using Chest X-ray

Libraries Used:

1. `tensorflow`
2. `pillow`
3. `matplotlib`


Model Used: CNN model

Input Shape:

Used `ImageDataGenerator` from Tensorflow for creating image to specific sizes i.e. 150x150x3.

# Model 1 Architecture
Architecture:

1. Layer 1 <br>
    1.1 32 Filters with 3x3 Stride taking 150x150x3 input.<br>
    1.2 Batch Normalization. <br>
    1.3 Max pooling with pool size of 2x2.<br>
    
2. Layer 2<br>
   2.1 64 Filters with 3x3 Stride taking data from Layer 1.<br>
   2.2 Batch Normalization. <br>
   2.3 Max pooling with pool size of 2x2.<br>
   
3. Layer 3<br>
    3.1 128 Filters with 3x3 Stride taking data from Layer 2.<br>
    3.2 Batch Normalization. <br>
    3.3 Max Pooling with Pool size of 2x2.<br>

4. Flattening Layers (Takes image and changes to single dimension)

5. Dense Layer 1 with 2048 nodes and dropout of 0.2

6. Dense Layer 2 with 512 nodes and dropout of 0.2

7. Dense Layer 3 with 128 nodes and dropout of 0.2

8. Dense Layer 4 with 32 nodes and dropout of 0.2

9. Final Layer with 1 Sigmoid activation.

All Layers except final layer has `RELU` activation function.

# Model 2 Architecture

Architecture:

1. Layer 1 <br>
    1.1 16 Filters with 3x3 filter size taking 150x150x3 input.<br>
    1.2 Batch Normalization. <br>
    1.3 Max pooling with pool size of 2x2.<br>
    
2. Layer 2<br>
   2.1 32 Filters with 3x3 filter size taking data from Layer 1.<br>
   2.2 Batch Normalization. <br>
   2.3 Max pooling with pool size of 2x2.<br>
   
3. Layer 3<br>
    3.1 64 Filters with 3x3 filter size taking data from Layer 2.<br>
    3.2 Batch Normalization. <br>
    3.3 Max Pooling with Pool size of 2x2.<br>

4. Layer 3<br>
    3.1 128 Filters with 3x3 filter size taking data from Layer 2.<br>
    3.2 Batch Normalization. <br>
    3.3 Max Pooling with Pool size of 2x2.<br>

5. Flattening Layers (Takes image and changes to single dimension)

6. Dense Layer 1 with 2048 nodes and dropout of 0.2

7. Dense Layer 2 with 1024 nodes and dropout of 0.2

8. Dense Layer 3 with 512 nodes and dropout of 0.2

9. Dense Layer 4 with 256 nodes and dropout of 0.2

10. Dense Layer 4 with 128 nodes and dropout of 0.2

11. Dense Layer 4 with 64 nodes and dropout of 0.2

12. Dense Layer 4 with 32 nodes and dropout of 0.2

13. Dense Layer 4 with 16 nodes and dropout of 0.2

14. Final Layer with 1 Sigmoid activation.

All Layers except final layer has `RELU` activation function.



