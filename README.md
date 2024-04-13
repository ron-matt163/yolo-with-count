# Automated Shelf Monitoring System
We have built a Robust Shelf Monitoring system that helps supermarket staff maintain accurate inventory details, re-stock items efficiently and on time, and tackle the problem of misplaced items where an item is accidentally placed at a different location. Our product aims to serve as a store manager that alerts the owner about items that need re-stocking and misplaced items.
## [Training the model:](https://models.roboflow.com/object-detection/yolov4)
* Unzip the labelled dataset from [kaggle](https://www.kaggle.com/datasets/rohanjosephmathew/grocery-shelf-status-analysis) and store it to your google drive.
* Follow the tutorial and update the training parameters in `custom-yolov4-detector.cfg` file in /darknet/cfg/ directory.
* `filters = (number of classes + 5) * 3 ` for each yolo layer.
* `max_batches = (number of classes) * 2000`

## [Steps to run the prediction colab notebook](https://colab.research.google.com/drive/1Y50cpgrfe_KgBfrqTIULw1GOb3sG3f1I#scrollTo=C5aYHDUZqtkw):
1. Install the required dependencies; pymongo,dnspython.
2. Clone the darknet repository and the required python scripts.
3. Mount the google drive containing the weight file.
4. Copy the pre-trained weight file to the yolo content directory.
5. Run the `detect.py` script to peform the prediction.
## Presenting the predicted result.
  The `detect.py` script has the option to send SMS notifications to the shopkeepers. We have built a front-end for building the phone book for collecting the details of the shopkeepers. It also displays the latest prediction results and model accuracy.
