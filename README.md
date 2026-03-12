# yolo_object_detection_pi4
Raspberry Pi 4B- Bookworm Debian 12 64 Bit- Yolov11n ncnn object detection requirements and code 

Inside the requirements.txt files you can find the versions of the libraries that needs to be installed.

--Steps to install ultralytics--
mkdir yolo
cd yolo
sudo apt update
sudo apt upgrade
python -m venv --system-site-packages venv
source yolo/bin/activate
pip install ultralytics ncnn /if stuck try again until finishes
yolo detect predict model=yolo11n.pt
yolo export model=yolo11n.pt format=ncnn /if you are stuck and get an error try running "pip install ultralytics==8.3.70 torch==2.5.0 torchvision==0.20" then re run the command
pip install numpy==1.26.4
python yolo_detect.py --model=yolo11n_ncnn_model --source=picamera0 --resolution=1280x720
