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
