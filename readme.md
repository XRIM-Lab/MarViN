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

# Pose Format
We provide txt poses files.
For test/train.txt poses files:
```image_name x y z qw qx qy qz```.

```x, y, z``` are camera to world coordinates.
Our 6DoF poses follow the COLMAP coordinate system.

For ARKit/ARCore.txt poses files:
```image_name x y z qx qy qz qw```.

```x, y, z``` are camera to world coordinates.
