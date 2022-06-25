# BrainTumorDetection

Brain tumor detection using deep learning

Clone the repository and run the jupyter notebook, or run it on Google Colab at [BrainTumorDetector.ipynb](https://colab.research.google.com/drive/1t8JFIeIObGaqmGUMW0NZuOnxQfPNYGFk?usp=sharing) or download and use the fine-tuned models in the [release](https://github.com/giuseppebrb/BrainTumorDetection/releases) page.

In the notebook file we're going to build a computer vision model to detect brain tumors. In order to perform that, we'll be using [PyTorch](https://pytorch.org) and in particular we'll start from the [YOLOv5](https://github.com/ultralytics/yolov5) architecture to perform fine-tuning for this task. For building our models will be used the small version (YOLOv5s).

Furthermore, we'll use this dataset from Kaggle called "[Brain Tumor Object Detection Dataset](https://www.kaggle.com/datasets/davidbroberts/brain-tumor-object-detection-datasets)" which already includes the labels and the bounding boxes that will be used to train the model.
It counts 1.274 images of MRI scans of the brain taken on 3 different axes:

| Axial       | Coronal     | Sagittal    |
| ----------- | ----------- | ----------- |
| ![00022_75.jpg](https://i.imgur.com/BdcTZOO.jpg)      |![59 (8).jpg](https://i.imgur.com/lH96GA2.jpg)        |      ![00002_166.jpg](https://i.imgur.com/9rCqylE.jpg)       |

The output of the models will render a bounding box around tumors (if any) or around structures that could be mistaken as a tumor but they are not. Confidence score of the prediction will be shown as well.

The image below shows 3 predictions on MRI of different patient, one for each plane.
![output](https://i.imgur.com/sk2Vh1s.jpg)
