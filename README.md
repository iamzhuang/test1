# NXROBO Spark
<img src="http://wiki.ros.org/Robots/Spark?action=AttachFile&do=get&target=spark.png" width="300">
This repository contains the ROS wrapper of Sparks's driver plus various ROS applications.This is a meta-package.
本说明为初学者体验版，如需查看详细说明，请查看 [详细版本 Detailed version](https://github.com/iamzhuang/test1/blob/master/ORB.md)

## Table of Contents

* [功能包说明packages-overview](#功能包说明packages-overview)
* [使用usage](#使用usage)
* [镜像Mirror](#镜像Mirror)
* [视频展示Video](#视频展示Video)
## 功能包说明packages-overview

* ***src*** : Spark的源代码，包括底层配置，硬件驱动，和各个应用功能包等。
* ***doc*** : 软硬件依赖包。

## 使用usage

### 系统要求 Prequirement

* System:	Ubuntu 14.04+
* ROS Version:	indigo or kinetic(Desktop-Full Install) 

### 下载安装 Download and install

* 下载工作空间 Download the workspace:
```yaml
git clone https://github.com/NXROBO/spark.git
```
* 安装依赖库并 Install libraries and dependencies:
```yaml
cd spark
./onekey.sh
```
* 根据提示选择103 Choose NO.103
```yaml
103
```
### 编译 compile
```yaml
catkin_make
```
* 如果编译一切正常，可根据提示运行相关例程。If everything goes fine, test the examples as follow:
```yaml
./onekey.sh
```

## 镜像Mirror

We also provide a downloadable mirror whose all environments have been configured.
*  Download address: [spark_mirror](http://pan.baidu.com/s/1i4ZlH4p)

## 视频展示Video

1.Spark跟随 Spark-Follower

<a href="https://www.youtube.com/embed/XBBVnRQn_fg" target="_blank"><img src="http://img.youtube.com/vi/XBBVnRQn_fg/0.jpg" 
alt="follow-person" width="240" height="180" border="10" /></a>
```yaml
cd spark
source devel/setup.bash
roslaunch spark_follower bringup.launch
```

2.Spark建图 Spark-SLAM-Mapping

<a href="https://www.youtube.com/embed/XBBVnRQn_fg" target="_blank"><img src="http://img.youtube.com/vi/XBBVnRQn_fg/0.jpg" 
alt="follow-person" width="240" height="180" border="10" /></a>
```yaml
cd spark
source devel/setup.bash
roslaunch spark_slam 2d_slam_teleop.launch slam_methods_tel:=gmapping
```

3.Spark导航 spark-Navigation

<a href="https://www.youtube.com/embed/XBBVnRQn_fg" target="_blank"><img src="http://img.youtube.com/vi/XBBVnRQn_fg/0.jpg" 
alt="follow-person" width="240" height="180" border="10" /></a>
```yaml
cd spark
source devel/setup.bash
roslaunch spark_navigation amcl_demo_lidar_rviz.launch
```

4.Spark-RtabMap建图 spark-RtabMap-Mapping

<a href="https://www.youtube.com/embed/XBBVnRQn_fg" target="_blank"><img src="http://img.youtube.com/vi/XBBVnRQn_fg/0.jpg" 
alt="follow-person" width="240" height="180" border="10" /></a>
```yaml
cd spark
source devel/setup.bash
roslaunch spark_rtabmap spark_rtabmap_teleop.launch 
```


