# **Multi-Sensor Fusion for Scene Perception and Reconstruction: Integrating Visible Light, Infrared,** solid-LiDAR, and **IMU** 

## 1.1 project 2

To enhance the 3D perception capability of multi-sensor perception systems under low-visibility and smoke-interference conditions, an advanced multi-spectral fusion method integrating visible, infrared, LiDAR, and IMUs is proposed in this paper. First, a bi-level adversarial optimization network is presented to enhance infrared-visible image fusion capability, augmented by a saliency-driven pixel-wise loss (S-DW) to balance intensity distributions and improve visual naturalness for target detection. Second, a 2D-3D joint mapping module achieves real-time cross-modal alignment of visible, infrared, and LiDAR data. It employs inverse motion compensation for scan distortion mitigation and hierarchical photometric error optimization via PCA-based planar constraints and sparse direct alignment, enabling sub-pixel registration. Third, a dynamic spatio-temporal hash-indexed framework globally fuses multi-spectral point clouds (visible, infrared, LiDAR) through software-synchronized temporal alignment. It addresses asynchronous multi-modal data via bidirectional nearest neighbor (BNN) search for 2D-3D correspondences and jointly optimizes spatio-temporal and feature alignment. Collectively, these approaches enhance fused image quality, enable real-time cross-sensor calibration, and ensure globally consistent multi-scale mapping, advancing integrated perception in complex environments.Experimental results demonstrate the effectiveness of the proposed approach in complex environments, with significant improvements in accuracy and robustness compared to state-of-the-art methods. This work has potential applications in autonomous driving, robotics, and augmented reality.

The code of this algorithm will be made public after publication in the journal



## 1.2 Datasets

You can get the crane dataset on Baidu Netdisk through the following link Link:



Existing infrared and visible light datasets are difficult to use effectively in the evaluation and learning of target detection tasks. Most of these datasets directly or indirectly provide a set of infrared and visible image pairs, but they are difficult to meet the training requirements of deep neural networks, both in terms of data quality, resolution and quantity. In addition, some of the datasets lack the necessary pre-processing steps. To solve these problems, this paper proposes the Robust visual-infrared-Lidar and Imu(VILI) dataset, which not only provides infrared and visible image pairs with the highest resolution, but also pre-processes these image pairs for matching and correction, and also contains the point cloud information of the scene, as well as time synchronisation of all data types, which significantly improves the diversity and usefulness of the data.

**Table 1: Comparative analysis of different datasets**

| Scenes   | Numbers |
| -------- | ------- |
| Daytime  | 421     |
| night    | 41      |
| sunday   | 87      |
| rain     | 24      |
| foggy    | 30      |
| overcast | 2       |



The dataset is captured by robot platform and a time synchronisation multisensor system including an infrared camera, a visible light camera and a LiDAR is constructed to capture the multimodal information of the current scene. The parameters of the two cameras are as follows: the focal lengths of the infrared camera and the visible light camera are fIR=3.2mm and fIR=8mm, respectively; the resolution of the visible light image is 1920×1080 with a large field of view (FOV); the resolution of the infrared camera is 1280×960, and the infrared wavelength band used is 8-14μm. The farthest detection range of LIDAR is 450m, and the non-repeating scanning FOV is 70.4°*77.2°, the maximum echo beam is 3, the data rate of point cloud is 240,000 points per second, the detection accuracy is 2cm, the relevant parameters of inertial guidance is the use of BMI088 model, the maximum reading speed is 2000Hz.

[![image-20250422214243090](https://github.com/weiye51/Multi-Sensor-Fusion/blob/main/1.png)]



This chapter presents a real-world multimodal dataset spanning 3 hours, which fuses data from Infrared Vision, LiDAR, and IMU sensors, depicted in Figure 2.8. This dataset covers a wide variety of scenarios, including both indoor and outdoor settings, diverse illumination conditions, and multiple motion patterns. It is particularly rich in samples acquired under challenging circumstances, such as low-light, nighttime operations, and instances involving rapid motion. The dataset includes annotations for numerous object classes, encompassing prevalent dynamic and static targets: person, crowd, bicycle, electric vehicle, car, bus, building, vegetation, and obstacle.

**Table 2** objects in the datasets

| Object     | numbers |
| ---------- | ------- |
| People     | 143     |
| car        | 41      |
| bus        | 20      |
| Excavators | 15      |
| Bicycles   | 18      |
[
![image-20250422214506571](https://github.com/weiye51/Multi-Sensor-Fusion/blob/main/2.png)
]




