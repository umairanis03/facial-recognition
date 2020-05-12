# Masked Face Recognition
## :memo: How does a facial recognition system works?
> 1.**Face detection:** first, the system has to identify the part of the image or the video that represents the face.
> 2. **Pre-processing:** the data has to be transformed into a normalized, monolith format (the images have to be of the same resolution, levels of zoom, brightness, orientation, etc.). It is also often referred to as feature normalization.
> 3. **Feature extraction:** the system has to extract meaningful data from the facial images, identifying the most relevant bits of data and ignoring all of the “noise.” It’s also referred to as encoding.
> 4. **Face recognition:** the actual process of matching unique data features to each individual. The underlying principle here is called object classification.
## :memo:Deep face recognition using imperfect facial data
> 1. Paper [Link](https://www.sciencedirect.com/science/article/pii/S0167739X18331133)
> 2. Studies the performance of Deep Methods for partial face recognition
> 3. Experiments are based on CNN based architecture along with the pre-trained VGG-Face model through which we extract features for machine learning.
> 4. Cosine similarity and SVM has been used as classifiers
> 5. Several experiments conducted using both adding individual face parts and not adding them to the training set
> 6. The experiment claims to reach 90% accuracy in both the cases
> 7. Adding partial faces images to the training dataset boosted the accuracy 
> 8. Cosine Similarity seems to be better measure than SVMs for the respective task
> 
> ![](https://ars.els-cdn.com/content/image/1-s2.0-S0167739X18331133-gr11.jpg)

---
## :memo:Occlusion Robust Face Recognition Based on Mask Learning With Pairwise Differential Siamese Network
> 1. [Link](http://www.ijircce.com/upload/2016/april/60_Occlusion.pdf) to the article
> 2. Human visual system pays attention to the non-occluded facial areas for recognition (and ignores the occluded areas), the paper propose to discard feature elements that have been corrupted by occlusions
> 3. To learn the correspondence between occluded facial regions and corrupted feature elements, we develop a novel pairwise differential siamese network (PDSN) structure with a mask generator module that takes pairwise images (one is a clean face and the other is an occluded one of the same identity) as input.
> 4. Our mask generator will identify those feature elements that are harmful for the recognition as well as far from its genuine values as corrupted ones.
> 5.  Given the feature of a face image with block bj occluded, denoted as f(xj ), how to learn a mask generator Mθ whose output is multiplied with the f(xj ) to mask out those corrupted elements.
> 6.  The core mask generator module Mθ in our PDSN is expected to output a mask whose element is a real value in [0, 1] and is multiplied with the input contaminated feature to diminish its corrupted elements: ˜f(xij) = Mθ(·)f(xij)
> 7. A fixed mask is extracted from every trained mask generator Mθ and build a dictionary accordingly.
> 8. After getting the mask, the final features can be calculated. The similarity score between two samples can be calculated using Cosine Similarity.
> ![](https://i.imgur.com/dYA1EK3.png)



## :memo: Efficient Detection of Occlusion prior to Robust Face Recognition [Link](http://downloads.hindawi.com/journals/tswj/2014/519158.pdf)
>1. The proposed approach consists of first detecting and segmenting occluded parts (e.g., sunglasses/scarves) and then applying face recognition on the non-occluded facial regions
>2. the presence of occlusion is first analysed in the patch-level using Gabor wavelets, PCA and SVM.
>3. Then we segment the occluded part more precisely from the other facial regions by a generalized Potts model Markov random field (GPM-MRF) 
>4. After the computation of an occlusion mask indicating which pixel in a face image is occluded, we propose a variant of local Gabor binary pattern histogram sequences (LGBPHS) [11] to efficiently represent occluded faces by excluding features extracted from the occluded pixels
>![](https://i.imgur.com/8qeRbgX.png)

## :memo: Occlusion invariant Face Recognition [Link](http://www.ijircce.com/upload/2016/april/60_Occlusion.pdf)
![](https://i.imgur.com/1cRY7F7.png)




 
