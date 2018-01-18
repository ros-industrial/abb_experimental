# ABB Experimental

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
