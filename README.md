# tensorflow_object-detection-API-tutorial-
This is a  tensorflow object detection API which uses MS coco data set. 
Dependencies
Tensorflow Object Detection API depends on the following libraries:

Protobuf 3+
Python-tk
Pillow 1.0
lxml
tf Slim (which is included in the "tensorflow/models/research/" checkout)
Jupyter notebook
Matplotlib
Tensorflow
Cython
cocoapi

# For CPU
pip install tensorflow
# For GPU
pip install tensorflow-gpu

COCO API installation
Download the cocoapi and copy the pycocotools subfolder to the tensorflow/models/research directory if you are interested in using COCO evaluation metrics. The default metrics are based on those used in Pascal VOC evaluation. To use the COCO object detection metrics add metrics_set: "coco_detection_metrics" to the eval_config message in the config file. To use the COCO instance segmentation metrics add metrics_set: "coco_mask_metrics" to the eval_config message in the config file.

git clone https://github.com/cocodataset/cocoapi.git
cd cocoapi/PythonAPI
make
cp -r pycocotools <path_to_tensorflow>/models/research/

Protobuf Compilation
The Tensorflow Object Detection API uses Protobufs to configure model and training parameters. Before the framework can be used, the Protobuf libraries must be compiled. This should be done by running the following command from the tensorflow/models/research/ directory:

# From tensorflow/models/research/
protoc object_detection/protos/*.proto --python_out=.

Testing the Installation
You can test that you have correctly installed the Tensorflow Object Detection
API by running the following command:

python object_detection/builders/model_builder_test.py


