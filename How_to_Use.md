✅ 1. Prepare and Connect the Developer Kit

The easiest way to get started is by using the **Jetson Orin Nano Developer Kit**.

📦 Basic Components:

- Orin Nano module (pre-installed on the board)  
- Carrier board (for I/O connections)  
- Heatsink + cooling fan  
- microSD card or NVMe SSD (for OS installation)  
- Power adapter (5V 4A or 20V USB-C PD)  
- Keyboard, mouse, HDMI monitor  

🧷 Connection Steps:

1. Flash the OS image (JetPack) onto a microSD card or NVMe SSD  
2. Insert the storage device into the board  
3. Connect HDMI monitor, keyboard, and mouse  
4. Connect power → Jetson will automatically boot  
5. On first boot, set up the Ubuntu environment  

---

✅ 2. Install JetPack

**JetPack** is a bundle of the OS and NVIDIA’s AI libraries for Jetson boards.

📥 Installation Steps:

1. Install [NVIDIA SDK Manager](https://developer.nvidia.com/nvidia-sdk-manager) on your PC  
2. Boot the Jetson board into recovery mode  
3. Connect the board to your PC via USB  
4. In SDK Manager, select JetPack and flash the device (includes Ubuntu, CUDA, cuDNN, etc.)

※ The developer kit usually comes with JetPack pre-installed, so you can boot right away with just a microSD card.

---

✅ 3. Set Up Development Environment

Jetson Orin Nano runs a typical Ubuntu Linux system, so most standard tools work as expected.

📦 Recommended Tools:

- Python 3 / pip  
- OpenCV  
- PyTorch or TensorFlow  
- Jupyter Notebook (optional)  
- VS Code (supports remote access)

```
bash

sudo apt update
sudo apt install python3-pip python3-opencv
pip3 install torch torchvision
```

---

✅ 4. Running AI / Vision Programs  
Jetson includes a **GPU and AI engine (Tensor Cores)** that can accelerate tasks like the following:

📌 Example 1: Real-time Object Detection (YOLO)

```
bash

git clone https://github.com/AlexeyAB/darknet.git
cd darknet
make
./darknet detector demo cfg/coco.data cfg/yolov4.cfg yolov4.weights
```

📌 Example 2: Camera Input Using OpenCV

```
python

import cv2

cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read()
    cv2.imshow("Camera", frame)
    if cv2.waitKey(1) == 27:  # Press 'Esc' to exit
        break

cap.release()
cv2.destroyAllWindows()
```

---

✅ 5. Expanding for Application Use

Jetson Orin Nano can be connected to various devices and utilized for different types of projects:

| Device       | Description                                          |
|--------------|------------------------------------------------------|
| **CSI Camera** | High-speed video input via MIPI interface            |
| **USB Camera** | Simple plug-and-play connection                      |
| **LiDAR**      | Distance sensor for robotics and autonomous driving |
| **IMU**        | Measures orientation and velocity (used in drones, robots) |
| **GPIO**       | Controls for LEDs, motors, sensors                  |
| **ROS**        | Compatible with Robot Operating System              |
