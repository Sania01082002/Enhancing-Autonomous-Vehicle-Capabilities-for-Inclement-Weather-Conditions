# Enhancing-Autonomous-Vehicle-Capabilities-for-Inclement-Weather-Conditions
# Abstract
Autonomous vehicles face significant challenges in adverse weather conditions, where
sensor performance is often degraded due to factors like rain, snow, and fog. This project
evaluates the effectiveness of object detection algorithms within a sensor fusion system designed to enhance perception in such environments. Individual sensors, including LiDAR,
radar, and cameras, experience reduced visibility, impacting their ability to ensure safe
navigation. To address this, we train an object detection model on a MATLAB-generated
dataset and compare its performance against a conventional algorithm. We evaluate the
influence of various detection algorithms on real-time decision-making by simulating sensor fusion across different weather conditions. The study aims to determine which model
is more robust and adaptive, ultimately improving the reliability of autonomous driving
in inclement weather.
# Backgraound and Problem Statement
- Autonomous vehicles rely on advanced sensor systems to perceive their environment accurately and make safe driving decisions. Sensors such as cameras, LiDAR, and radar play a pivotal role in detecting objects, identifying lanes, and estimating distances. However, adverse weather conditions such as rain, fog, and snow significantly degrade the performance of these individual sensors. Cameras are affected by poor lighting and radar,though robust in challenging weather, lacks the resolution required for detailed perception. These limitations pose a significant challenge to the development and deployment of autonomous vehicles. To address this issue, sensor fusion has emerged as a promising solution. By integrating data from multiple sensors, sensor fusion enhances robustness,
accuracy, and reliability, enabling autonomous vehicles to operate effectively even in unfavourable conditions.
- Adverse weather conditions like rain, fog, and snow degrade the performance of singlesensor systems in autonomous vehicles, leading to unreliable object detection and impaired
decision-making. Cameras suffer from reduced visibility, radar faces noise and clutter,
and LiDAR experiences signal attenuation. These limitations compromise safety-critical
tasks such as obstacle avoidance and path planning. To ensure reliable perception and
safe operation in all conditions, advanced sensor fusion techniques are needed to enhance
system robustness.
# Overview
## Python-Related Work
### 1. Sensor fusion and preprocessing
- Converted radar data from polar to Cartesian coordinates using NumPy.
- Mapped 3D radar points to the 2D camera image plane with numpy.linalg.
- Overlaid radar points as red dots on camera images using OpenCV’s cv2.circle.
- Stored fused images with annotations for object detection.
- Aligned camera and radar timestamps using a Pandas time index for synchronization.
### 2. Object Detection in Adverse Weather
- Simulated rain using OpenCV with white dashed lines of adjustable intensity.
- Simulated fog by reducing contrast, adding a gray overlay, and applying Gaussian blur.
- Used Faster R-CNN, pre-trained on COCO, fine-tuned in PyTorch with torch.optim.
- Trained on 100 nuScenes camera frames labeled with vehicles over multiple
epochs.
- Processed weather-affected frames, drawing bounding boxes with cv2.rectangle.
## Transition from Python to MATLAB
The initial phase of the project was implemented in Python, where Faster R-CNN was
used for object detection under normal and adverse weather conditions, and geometric
sensor fusion aligned Camera, Radar, and LiDAR data. However, Python lacked real-time
multi-object tracking, dynamic environments, and sensor degradation models, making it
insufficient for evaluating JPDA performance.
To overcome these limitations, the project transitioned to MATLAB, which provides
real-time driving scenario simulation using the Automated Driving Toolbox and Simulink.
MATLAB enables dynamic multi-object tracking, sensor noise modeling, and motion
estimation, allowing for a more comprehensive evaluation of JPDA tracking performance
in adverse weather.
## MATLAB-Related Work
- Developed an AV model in Simulink with a sensor fusion system in a virtual
environment.
- Integrated camera and radar data using the JPDA algorithm for robust tracking.
- Clustered radar data with DBSCAN for effective object grouping.
- Detected vehicles initially with the ACF algorithm from camera frames.
- Extracted lane detections from forward-facing camera frames.
- Retrained YOLOv2 on a generated dataset as an alternative to ACF.
- Tested the model under simulated rain and fog conditions.
- Evaluated performance using F1 score and recall rate to assess detection credibility.
# Objectives
- Simulate a sensor fusion system integrating Radar and Camera data to test its
effectiveness for autonomous vehicle safety in adverse weather conditions.
- Model weather scenarios, including rain and fog, within a simulation environment.
- Assess the performance of ACF and YOLO in challenging weather conditions to
determine the more accurate object detection algorithm.
- Evaluate the sensor fusion system’s performance by validating vehicle detection
accuracy under the selected algorithm.
# Methodology
## Dataset Selection
This initial step involved selecting an appropriate dataset to support the simulation of
sensor fusion and object detection in adverse weather conditions. The nuScenes mini
dataset was chosen, comprising radar and camera data, due to its comprehensive coverage
of real-world driving scenarios. This dataset’s richness in diverse environmental data
made it ideal for testing the robustness of autonomous vehicle (AV) perception under
simulated rain and fog. The simulation environment utilized Python IDLE, leveraging
the nuScenes-devkit to efficiently extract radar and camera data, ensuring a seamless
workflow for subsequent analysis and fusion tasks.
