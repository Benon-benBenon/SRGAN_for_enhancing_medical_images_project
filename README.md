# Deep Learning for Medical Image Super-Resolution Methods and Applications

## Abstract

Digital image processing is a fundamental foundation in medical imaging technologies. The super-
resolution method has emerged as a technique that provides sustainable solutions for poor quality
and low-resolution images. Super-resolution is an algorithm-based method that upscales single or
multiple low-resolution images into high-resolution images without losing important features. It
has many applications in different fields, including satellite imaging technology, medical imaging,
and remote sensing. Using this method helps medical imaging industries avoid wasting resources
on manufacturing image acquisition devices. Additionally, the super-resolution method helps such
industries manufacture less expensive medical devices used in imaging medicine.

Therefore, throughout this study, different techniques of image processing in medical imaging,
especially the super-resolution technique, are explained in detail, along with their advantages and
applications in medical imaging operations. Moreover, the implementation of the super-resolution
method using machine learning and deep neural network technology has been discussed, including
its limitations in the field of healthcare.

## Data Processing

Data preparation and exploratory data analysis are primary tasks that should be done to ensure
that data are well-organized and are in an appropriate format. In this project, X-ray images are
used; therefore, data are processed in such a way that they will have low-resolution data points
and high-resolution data points.

Processing of data is essential for the super-resolution adversarial network because it uses data
with different characteristics (high-resolution real data and low-resolution noise data). The gen-
erator part of SRGAN requires noise as input, while the discriminator network uses real data as
well as noise data as their input. Remember that SRGAN is composed of two networks: the
generator and the discriminator.

The dataset used in this super-resolution task contains 5863 chest X-ray images, totaling 1GB
of data, categorized as normal and pneumonia. However, to implement super resolution with
a sufficient amount of data for training, the two groups mentioned above are combined before
splitting the dataset into training and testing sets. Chest X-ray images were gathered and chosen
from retrospective cohorts of pediatric patients aged one to five years old from Guangzhou Women
and Children’s Medical Center, Guangzhou [1].

Since the SRGAN model utilizes both low-resolution and high-resolution images together, we
downsampled high-resolution images to low resolution using Lanczos filter. The goal of this
downsampling is to have a pair of folders, one containing high-resolution images and the other
for low-resolution images. This means that the training set consists of two folders: one for low-
resolution images and one for high-resolution images, and the testing set has a low-resolution
image test folder and a high-resolution images test folder.

In this implementation, the dataset is processed by forming pairs of folders containing low-
resolution images and high-resolution images. The **first pair** is **[(32 × 32), (128 × 128)]**, the
**second pair** is **[(64 × 64), (256 × 256)]**, and the **third pair** is **[(128 × 128), (512 × 512)]**. For
each pair mentioned here, the first tuple of the pair is low-resolution images, while the second
tuple is high-resolution images. The SRGAN model used in this project is dynamically changing
based on the pair of images used to train the model. This property allows this SRGAN model to
be flexible for input to provide an appropriate super resolution image as an output.

Data for this project **[LINK](https://drive.google.com/file/d/1HS6dIclJpob4WNNndftxYgzJ9fAVC2u4/view?usp=sharing)**

