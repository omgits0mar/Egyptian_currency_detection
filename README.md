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


## Inference

To test the YOLO model, we ran it on a set of test images. The output of the model is a set of bounding boxes around the banknotes in the image. We then used OpenCV to draw the bounding boxes on the image and labeled them with the corresponding banknote denomination.

## Conclusion

In conclusion, this project demonstrates the use of YOLO for banknote detection and recognition on the Egyptian currency dataset. The trained model can be used in real-world applications, such as banknote counting machines and ATM machines but it is mainly used in our project to help visually impaired people recognize and know what money they have and also how much by counting them.


