# Feature based automatic registration of aerial imagery using Point cloud library (PCL)

## 3D Feature Descriptors suitable for Registration based on Performance
  [Documentation for choosing the Feature discriptors with KPI ](https://docs.google.com/document/d/1rlW5H1NrMiBt6rW-jM73dyxy5JrsuGpSkpbSgFH9KK4/edit?usp=sharing1)

## Feature Descriptors available in C++ Repo
1. [CSHOT](http://vision.disi.unibo.it/research/80-shot)
2. [PPF Hist](https://gitlab.com/caro-sdu/covis)

## Feature Descriptors available in PCL
1. [ROPS](http://pointclouds.org/documentation/tutorials/rops_feature.php)
2. [FPFH](http://pointclouds.org/documentation/tutorials/fpfh_estimation.php)
3. [PFH](http://pointclouds.org/documentation/tutorials/pfh_estimation.php)

#### The project is carried out to use PCL library: conduct and test experiments on Registration and 3D discriptors

## Note
1. The official tutorials and latest PCL are incompatible with each other.
2. Some of the tutorials are updated in PCL ["/doc/tutorials/content/sources"](https://github.com/PointCloudLibrary/pcl). 
3. The PCL has changed the format to .PCD, but all datasets are in .PLY format
4. In order to use .PLY file from all famous datasets, convert the file using PCL tools "PLY to PCD"

## Dependencies
This project has the following dependencies: 
```
QT Creator
C++
OpenCV (3.4.4 and above)
Point Cloud Library (PCL)
VTK (5.10 and above)
```
