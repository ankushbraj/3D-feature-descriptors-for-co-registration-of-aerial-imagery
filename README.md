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
## Implementation
#### The current code can incrementally register based on Iterative Closest point algorithm available on PCL documentation. The plan is use the code snippets in PCL tutorials available on official website and make small changes and visualize the results. The steps planned are,

- [x] Data acquisition - An input cloud and a reference cloud are fed into the algorithm.
- [x] Estimating Keypoints - pcl::SIFTKeypoint< PointInT, PointOutT >
- [ ] Describing keypoints using 3D Feature descriptors - pcl::FPFHEstimation< PointInT, PointNT, PointOutT >
- [ ] Correspondence Estimation - pcl::registration::CorrespondenceEstimation< PointSource, PointTarget, Scalar >
- [ ] Correspondence rejection - RANSAC pcl::registration::CorrespondenceRejectorSampleConsensus< PointT >
- [ ] Transformation Estimation - pcl::registration::TransformationEstimationSVD< PointSource, PointTarget, Scalar >
 
 
 ## Usage
```
1. Put three files in a folder with name, for ex :coreg
2. build 
3. cd build
4. put the .pcd in the build folder
5. ./coreg test[1-5].pcd
```

