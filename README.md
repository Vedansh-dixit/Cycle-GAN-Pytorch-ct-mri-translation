# Cycle-GAN-Pytorch-ct-mri-translation
This repository uses Cycle GAN for unpaired image to image translation.
Abstract: 
Medical images have been widely used in clinics, providing visual representations of under-skin tissues in human body. By applying different imaging protocols, diverse modalities of medical images with unique characteristics of visualization can be produced. Considering the cost of scanning high-quality single modality images or homogeneous multiple modalities of images, medical image synthesis methods have been extensively explored for clinical applications.
Among them, deep learning approaches, especially generative adversarial networks (GANs) and Cycle-GAN, have rapidly become dominating for medical image synthesis in recent years.
A GAN requires little to no labelled data to obtain high-quality data that can be generated through competition between the generator and discriminator networks. Therefore, GANs are rapidly proving to be a state-of-the-art foundation, achieving enhanced performances in various medical applications.
CT scans use X-rays, which produce ionizing radiation. Research shows that this kind of radiation may damage DNA and lead to cancer. In this report, we have come up with a solution to convert MRI scan of an organ into CT scan and vice versa using Cycle Generative Adversarial Network (GAN).
 
**#Introduction:** 
As with most of the medical diagnosis, there are certain risks involved in CT scans also, though these risks are not there in MRI scan. One of the major drawbacks is the use of X-rays in CT scans, these X-rays can harm unborn babies in pregnant woman, it also exposes the body to the radiation that have its own ill effects. For the specific population which possess potential health risk after undergoing CT scans another option is MRI scan. MRI scan uses radio waves. So, for population who can't go under CT scan due to some condition/symptoms. we are providing a way to get CT scan through its translation from an MRI scan.
 
**Approach used: **
In order to solve our problem at first, we read about different type of scans available and selecting the ones with zero to little amount of risk. Once listed, MRI scan came on top. To solve the above problem, we tried to figure out a process by which we can translate CT scans to MRI scans and vice versa, i.e., we will have to convert one image into something else and that is when GAN comes in. We used the technique of cycle GAN which is used for unpaired image to image translation. 
GAN consists of 2 parts, one is generator which generates fake or synthetic images and the other part of cycle GAN is discriminator whose aim is to detect the real and fake images. The generator continuously improves its self and tries to fool the discriminator, it uses the technique of unsupervised learning to fool the discriminator.
For a successful and favourable result, we searched for a large enough dataset so we can improve our accuracy while not forcing machine to produce garbage data. Now after successfully collecting the data, we started training and testing the model in order to get the best results.
   
**Understanding about Cycle GAN and its working:** 
A Cycle GAN is designed for image-to-image translation, and it learns from unpaired training data. It gives us a way to learn the mapping between one image domain and another using an unsupervised approach.
A Cycle GAN is made of two types of networks: discriminators and generators. In this example, the discriminators are responsible for classifying images as real or fake (for both X and Y kinds of images). The generators are responsible for generating convincing, fake images for both kinds of images.

**Code:**
To implement the code follow the procedure mentioned in CT_CycleGAN.ipynb

**Dataset**
https://www.kaggle.com/datasets/darren2020/ct-to-mri-cgan


**Conclusion:** 
In conclusion we found a solution to our problem statement by using Cycle GAN to convert MRI and CT scans into one another. This in turn provides patients, doctors and researchers to translate CT scans into MRI scans and vice versa.

Our code is inspired by:
https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix
