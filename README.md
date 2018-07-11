# ABB Experimental

## ROS Distro Support

|         | Indigo | Jade | Kinetic |
|:-------:|:------:|:----:|:-------:|
| Branch  | [`indigo-devel`](https://github.com/ros-industrial/abb_experimental/tree/indigo-devel) | [`indigo-devel`](https://github.com/ros-industrial/abb_experimental/tree/indigo-devel) | [`kinetic-devel`](https://github.com/ros-industrial/abb_experimental/tree/kinetic-devel) |
| Status  |  supported | supported |  supported |
| Version | [version](http://repositories.ros.org/status_page/ros_indigo_default.html?q=abb_experimental) | [version](http://repositories.ros.org/status_page/ros_jade_default.html?q=abb_experimental) | [version](http://repositories.ros.org/status_page/ros_kinetic_default.html?q=abb_experimental) |

## Travis - Continuous Integration

Status: [![Build Status](https://travis-ci.org/ros-industrial/abb_experimental.svg?branch=kinetic-devel)](https://travis-ci.org/ros-industrial/abb_experimental)

## ROS Buildfarm

|         | Indigo Source | Indigo Debian | Jade Source | Jade Debian |  Kinetic Source  |  Kinetic Debian |
|:-------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|:-------------------:|
| abb_experimental | [![not released](http://build.ros.org/buildStatus/icon?job=Isrc_uT__abb_experimental__ubuntu_trusty__source)](http://build.ros.org/view/Isrc_uT/job/Isrc_uT__abb_experimental__ubuntu_trusty__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Ibin_uT64__abb_experimental__ubuntu_trusty_amd64__binary)](http://build.ros.org/view/Ibin_uT64/job/Ibin_uT64__abb_experimental__ubuntu_trusty_amd64__binary/) | [![not released](http://build.ros.org/buildStatus/icon?job=Jsrc_uT__abb_experimental__ubuntu_trusty__source)](http://build.ros.org/view/Jsrc_uT/job/Jsrc_uT__abb_experimental__ubuntu_trusty__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Jbin_uT64__abb_experimental__ubuntu_trusty_amd64__binary)](http://build.ros.org/view/Jbin_uT64/job/Jbin_uT64__abb_experimental__ubuntu_trusty_amd64__binary/) | [![not released](http://build.ros.org/buildStatus/icon?job=Ksrc_uX__abb_experimental__ubuntu_xenial__source)](http://build.ros.org/view/Ksrc_uX/job/Ksrc_uX__abb_experimental__ubuntu_xenial__source/) | [![not released](http://build.ros.org/buildStatus/icon?job=Kbin_uX64__abb_experimental__ubuntu_xenial_amd64__binary)](http://build.ros.org/view/Kbin_uX64/job/Kbin_uX64__abb_experimental__ubuntu_xenial_amd64__binary/) |


[![support level: community](https://img.shields.io/badge/support%20level-community-lightgray.png)](http://rosindustrial.org/news/2016/10/7/better-supporting-a-growing-ros-industrial-software-platform)

[ROS-Industrial][] ABB experimental meta-package.  See the [ROS wiki][] page for more information.


## Contents

This repository contains packages that will be migrated to the [abb][] repository after they have received sufficient testing.
The contents of these packages are subject to change, without prior notice.
Any available APIs are to be considered unstable and are not guaranteed to be complete and / or functional.


## Build
### Build from Source (developers only, not recommended)
This build methods uses:
 - [wstool][] for rosinstall.
 - [catkin tools][] for building.
This package depends on the following ros dependencies that are not included in the source build method, so they will need to be installed:
```
sudo apt install ros-kinetic-industrial-core ros-kinetic-moveit
```
Now build the abb_experimental package:
```
mkdir -p abb_experimental_ws/src
cd abb_experimental_ws/src
git clone -b kinetic-devel git@github.com:ros-industrial/abb_experimental.git
wstool init .
wstool merge abb_experimental/abb_experimental.rosinstall
wstool update
catkin build
```

[ROS-Industrial]: http://wiki.ros.org/Industrial
[ROS wiki]: http://wiki.ros.org/abb_experimental
[abb]: https://github.com/ros-industrial/abb
[wstool]: http://wiki.ros.org/wstool
[catkin tools]: https://catkin-tools.readthedocs.io/en/latest/
