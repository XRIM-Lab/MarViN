# MARViN: Mobile AR Dataset with Visual-Inertial Data

### [Homepage](https://lck666666.github.io/research/MARViN/index.html) | [Paper](https://ieeexplore.ieee.org/document/10536574)

**MARViN: Mobile AR Dataset with Visual-Inertial Data** <br>
[Changkun Liu](https://lck666666.github.io)\*, Yukun Zhao\* and [Tristan Braud](https://braudt.people.ust.hk/index.html) <br>
<em>* equal contribution</em><br>
The Hong Kong University of Science and Technology<br>
Virtual Reality and 3D User Interfaces Abstracts and Workshops (VRW), 2024<br>


You can download the MARViN dataset [link](https://hkustconnect-my.sharepoint.com/:f:/g/personal/cliudg_connect_ust_hk/Ek76M4OIy31KrNrizKxlEbIBvlXNQVLv2Ft3vtL9EphwWw?e=3bDJSo). 


```
MARViN
├── atrium
│   ├── seqxx
│        ├── image.jpg
│        ├── ARKit/ARCore.txt
│        ├── GyroscopeData.txt
│        ├── GPSData.txt
│        ├── AccelerometerData.txt
│        ├── MagnetometerData.txt
│   ├── test.txt
│   └── train.txt
├── ....
│
└── stairs
│   ├── seqxx
│        ├── image.jpg
│        ├── ARKit/ARCore.txt
│        ├── GyroscopeData.txt
│        ├── AccelerometerData.txt
│        ├── MagnetometerData.txt
│   ├── test.txt
│   └── train.txt
```
Note that due to the low gps accuracy of indoor scenes, we do not provide gps data in the seqs of indoor scenes.

# Pose Format
We provide txt poses files.
For test/train.txt poses files:
```image_name x y z qw qx qy qz```.

```x, y, z``` are camera to world coordinates.
6DoF poses in test/train.txt follow the COLMAP coordinate system.

For ARKit/ARCore.txt poses files:
```image_name x y z qw qx qy qz```.

```x, y, z``` are camera to world coordinates.
6DoF poses in ARKit/ARCore.txt follow the Unity coordinate system.

Unity -> COLMAP:
```y -> -y, qy -> -qy```

# Sensor Data Format

We provide txt sensor data files, which include gyroscope, GPS, accelerometer and magnetometer data respectively. 

* Gyroscope data

  For GyroscopeData.txt files: 

  ```image_name qw qx qy qz```

  The quaternion follows the Unity coordinate system and represents the device's orientation. 

* GPS data

  For GPSData.txt files:

  ```image_name x y z```

  ```x, y, z``` are latitude, longitude and altitude respectively.

* Accelerometer data

  For AccelerometerData.txt files: 

  ```image_name x y z```

  ```x y z``` are last measured linear acceleration of a device in three-dimensional space following the Unity coordinate system.

* Magnetometer data

  For MagnetometerData.txt files:

  ```image_name trueHeading```

  ```trueHeading``` is the heading in degrees relative to the geographic North Pole.


# Data Capture App based on Unity
Our Data Capture App is [opensource](https://github.com/yukunzhao998/DataCapture), please cite this paper and star this repo if you find our dataset or data capture app is helpful. Thanks!
<h3 id="citation">Citation</h3>
		<pre class="citation-code"><code><span>@INPROCEEDINGS{10536574,
  author={Liu, Changkun and Zhao, Yukun and Braud, Tristan},
  booktitle={2024 IEEE Conference on Virtual Reality and 3D User Interfaces Abstracts and Workshops (VRW)}, 
  title={MARViN: Mobile AR Dataset with Visual-Inertial Data}, 
  year={2024},
  volume={},
  number={},
  pages={532-538},
  keywords={Performance evaluation;Visualization;Solid modeling;Three-dimensional displays;Pose estimation;User interfaces;Cameras;Visual localisation Dataset—Camera pose regression—Visual-Inertial Odometry—Visual positioning system;Computer Vision—Augmented Reality},
  doi={10.1109/VRW62533.2024.00103}}</code></pre>
