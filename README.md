# Jiayuqin_xuepingleng_final_project
This is the official implementation for MMEFace: Multi Model Ensemble learning for masked Face recogniti, which serves as final project for 2023 Spring CSE 666 course.

Our presentation slides can be found at:https://docs.google.com/presentation/d/19fWdYpEYsqADUVlaaAtgxd1jBGpHGdlckR4PzneMoas/edit?usp=sharing

Face recognition is a research topic of significant importance in both academia and industry, encompassing a wide range of applications. Despite the remarkable success of deep learning algorithms in face recognition, the identification of occluded faces remains a challenging issue that demands attention. This paper presents a novel occluded face recognition system utilizing both real-world and artificially generated occluded face images. We conduct a comparative analysis of five distinct vision deep learning models and employ model ensemble techniques to leverage the strengths of each model while mitigating their weaknesses. Our approach achieves an accuracy of 84.07 percent, surpassing the previous state-of-the-art performance of 60.80 percent.

To generate the images for training and validation, you need to:

1 download the dataset from: https://drive.google.com/open?id=1UlOk6EtiaXTHylRUx2mySgvJX9ycoeBp
Extract the file and move the folder ./AFDB_face_dataset under ./self-built-masked-face-recognition

2 run ./wear_mask_to_face/add_mask_dataset_generation.ipynb. This step manually wear masks on face images and creates a folder add_mask_face_dataset under ./self-built-masked-face-recognition.

This process might take a long time, the preprocessed dataset is available at:

Densenet: https://drive.google.com/file/d/1V7Y9dFA1RylH_OhLHwnMFjb3j9H9-mjt/view?usp=sharing, 

MobileNet: https://drive.google.com/file/d/1fUmDLZaEoE92m9VwuCpcirRrH9VAPa0Y/view?usp=sharing, 

InceptionNet: https://drive.google.com/file/d/1hL80bKFaQS4QSVhLir351uY3fu8dCKPv/view?usp=sharing,

ResNet: https://drive.google.com/file/d/1wDHLEmlJeAQlrDYylf8A72qemkBry3jK/view?usp=sharing

To produce the result present in our paper, you need to:

1 cd add_mask_dataset_generation

2 train four models using densenet.ipynb, inceptionnet.ipynb,  mobilenet.ipynb or resnet.ipynb, we also provide the pretrained checkpoints densenet_model.pth,inception_model.pth, mobilenet.ckpt and resnet.ckpt, the inference code is also in the same jupyter notebooks. From this, you can generate predictions on test dataset.

3 run ensemble.ipynb to generate predictions of ensemble model, other experiment results can also be found in this notebook.
