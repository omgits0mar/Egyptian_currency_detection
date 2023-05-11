# Egyptian Banknotes Detection using YOLOv8 Model

This project uses the YOLO (You Only Look Once) model trained on the [EgyptIris dataset](https://www.kaggle.com/datasets/egyptiris/egyptian-currency) to detect and recognize Egyptian banknotes. 

## Data Preprocessing

Before training the YOLO model, we first preprocessed the data to put it in the format required by YOLO. This was done using a Python script called `data-preprocessing-script`. The script took the raw data from the dataset and converted it into the following format: <path_to_image> <x1>,<y1>,<x2>,<y2>,<class_id>


where:

- `<path_to_image>` is the path to the image file.
- `<x1>,<y1>` are the coordinates of the top-left corner of the bounding box.
- `<x2>,<y2>` are the coordinates of the bottom-right corner of the bounding box.
- `<class_id>` is the ID of the class (i.e., the banknote denomination).

The output of the `data-preprocessing-script` is a file called `data.txt`, which contains the formatted data.

## Training the YOLO Model

Once the data was preprocessed, we trained the YOLOv8 model using the following hyperparameters:

- Batch size: 16
- Subdivision: 16
- Learning rate: 0.001
- Momentum: 0.9
- Decay: 0.0005
- Number of iterations: 25
- Number of classes: 5 (for the five banknote denominations)


## Results

The following is a real-live video demonstrating the sample run of the project with me testing it :)

<video width="640" height="360" controls autoplay loop>
  <source src="img-2013_slowed_Trim.mp4">
</video>


[Real-Time currency detection](https://github.com/omgits0mar/Egyptian_currency_detection/assets/63152481/175d9f8c-808f-4d1e-aec7-b5eb3c369daa)


## Conclusion

In conclusion, this project demonstrates the use of YOLO for banknote detection and recognition on the Egyptian currency dataset. The trained model can be used in real-world applications, such as banknote counting machines and ATM machines but it is mainly used in our project to help visually impaired people recognize and know what money they have and also how much by counting them.

## Note :

This repo and code feature is an open source python notebook part of the graduation project App `Smart Vision for Visually impaired` which aims to help visually impaired people sense and know what is going around by using AI, Computer Vision and Deeplearning to create powerfull features in a mobile app that could help those everyone in needs
This App is currently in developing of some features as :
1. Optical characater recognition (OCR) for reading text in many languages.
2. Friends face recognition using Siamese one-shot learn
3. **Currency detection (Egyptian banknotes ✅) using YOLO object detection and EGYPT-IRIS dataset**
4. Image Caption and Scene Recognition of surroundings usind Pre-trained large models.
5. Voice commands (Trigger words detection) for choosing which feature the patiant wants by voice in the application
6. Object detection filtered by text and depth estimating the distance of this object using OpenAi's ClipSeg and Intel's DPT models.
Though in this notebook doesnot feature the real-time extraction as these are used in the app only.
