# EDU 
Contents  
---
Thread: 
--
  We use spatial enhancement filtering technology to make up for the semantic gap, and propose an enhanced ense U-Net (E-DU), which aims to be applied to multi-modal medical image segmentation, so as to improve the segmentation performance and efficiency.  
--
Methods: 
--
  Before the combination of encoder and decoder features, we replace the traditional skip connection with multi-scale denoise enhancement (MDE) module. The encoder features need to be convoluted by the line depth of spatial enhancement filter and then combined with the decoder features. We propose a simple and efficient deep full convolution network structure E-DU, which can not only fuse semantically different features, but also denoise and enhance the feature map.  
--
Module structure：
--
![image](https://user-images.githubusercontent.com/101448564/158799383-b6e0c42e-a360-4bb0-8dc8-194031264d30.png)  
--
Demand:  
--
  This research is carried out on the Linux workstation equipped with GPU. The software platform is based on Python 3.7, and the proposed algorithms are implemented based on pytorch 1.7.1 framework. GPU is used to accelerate the training in the training process.   
--
The module uses： 
--
import os  
import cv2  
import numpy as np  
import pandas as pd  
import matplotlib.pyplot as plt  
.... 
--
Data Source：
--
![image](https://user-images.githubusercontent.com/101448564/158796655-25ad677d-f91b-4146-a141-79a5fe8b2019.png)  
--
The dataset we selected can be briefly described as follows.  
  Data 1 is a dataset composed of tuberculosis foci, which contains 138 X-Ray images of tuberculosis patients before and after treatment, 58 of which are abnormal pictures (with tuberculosis manifestations) and 80 normal pictures.  
  Data 2 contains 888 cases of low-dose lung CT image data, including 1186 nodules. The number of slices contained in each image will vary with various patients, scanning machines and scanning layer thickness.  
  Data 3 is the brain tumor MR data set. It consists of 220 high grade gliomas (HGG) and 54 low grade gliomas (LGG).  
  Data 4 is a microscope image modal data set, including 2D and 3D delayed video sequences of fluorescent anti staining nuclei or cells moving on or immersed in the substrate, a total of 30 cases (60 images).  
  Data 5 is a microscope pathological image dataset composed of skin lesions, which can be used to identify lesions such as melanoma, actinic keratosis and basal cell carcinoma in skin lesion images, with a total of 2594 images.  
  Data 6 is a dataset composed of 10000 polyps.  
  Data 7 is a retinal fundus angiography dataset about pathological myopia (PM), including color fundus retinal images of 1200 subjects, 400 training, verification and test datasets respectively   
--
Reselt：
--
![image](https://user-images.githubusercontent.com/101448564/158796529-9867c591-0462-4dc5-a65a-8a8e03cc6c18.png)  
  The segmentation efficiency results show that the convergence speed of E-DU is the fastest, and the addition of MDE module can effectively save peak memory usage (PMU) and average time per step (ATS).
--

