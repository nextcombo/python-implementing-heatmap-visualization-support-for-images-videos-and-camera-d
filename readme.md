# [python] Implementing Heatmap Visualization Support for Images, Videos, and Camera Detection Based on YOLOv12

YOLOv12 Grad-CAM Visualization Tool This tool is based on the YOLOv12 model and integrates Grad-CAM technology to achieve object detection.

## YOLOv12 Grad-CAM Visualization Tool

This tool is based on the YOLOv12 model, combined with Grad-CAM technology to achieve visual analysis of object detection. It supports image, video, and real-time camera processing.

### Notes

The project uses the YOLOv12-1.0 model for testing and verification, not the Turbo model. Additionally, as YOLOv12-1.0 does not currently directly support GPUs like the RTX 2080 or earlier models, it will prompt an error when running. Please use this early update version of YOLOv12, which supports the RTX 2070 GPU.

### Functional Characteristics

-

Supports multiple Grad-CAM methods.

-

Real-time camera processing

-

Video file processing

-

Image file processing

### Environmental Requirements

-

Python 3.10+

-

The computer must have a NVIDIA graphics card and support for the CUDA environment.

### Installation Steps

1.

Create a virtual environment to install YOLOv12 (recommended)

```
wget https://github.com/Dao-AILab/flash-attention/releases/download/v2.7.3/flash_attn-2.7.3+cu11torch2.2cxx11abiFALSE-cp311-cp311-linux_x86_64.whl
conda create -n yolov12 python=3.11
conda activate yolov12
pip install -r requirements.txt
pip install -e .

-

1

-

2

-

3

-

4

-

5

```

Please note that the above is a Linux installation guide, for Windows, refer to https://blog.csdn.net/FL1623863129/article/details/145760810 for installation.
2. Clone repository

```
Download the source code for YOLOv12-gradcam.
cd yolov12-gradcam

-

1

-

2

```

1.

Install dependencies

```
pip install -r requirements.txt

-

1

```

### Quick Start

1. Image Processing

```
from Yolov12Heatmap import *
model = Yolov12Heatmap(weight='yolov12n.pt')
result = model('test.jpg')
cv2.imshow('result', result)
cv2.waitKey(0)

-

1

-

2

-

3

-

4

-

5

-

6

```

![[python] Implementing heatmap visualization based on YOLOv12 to support image, video, and camera detection.](01-d00f81ed.png)

#### 2. Video Processing

```
from Yolov12Heatmap import *
model = Yolov12Heatmap(weight='yolov12n.pt')
model.start_video('test.mp4')

-

1

-

2

-

3

-

4

```

![[python] Implementing heatmap visualization based on YOLOv12 to support image, video, and camera detection.](02-fd4b2865.png)

#### 3. Real-time Camera

```
from Yolov12Heatmap import *
model = Yolov12Heatmap(weight='yolov12n.pt')
model.start_camera(0) # 0 represents the default camera

-

1

-

2

-

3

-

4

```

### Parameter Configuration

Additional parameter adjustments require reading the code in the Yolov12Heatmap.py file for modification.


## Payment

Here is a pay link on Stripe ( https://buy.stripe.com/3cs8yP7sY87d0vu9AB ). Please contact me lonlonago@foxmail.com after funding $89, and I will send you a complete data files , thank you!

![111.png](111.png)
