# ABB Experimental

[ROS-Industrial][] ABB experimental meta-package.  See the [ROS wiki][] page for more information.

# Build
## Build from Source (developers only, not recommended)
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

[ROS-Industrial]: http://www.ros.org/wiki/Industrial
[ROS wiki]: http://ros.org/wiki/abb_experimental
[wstool]: http://wiki.ros.org/wstool
[catkin tools]: https://catkin-tools.readthedocs.io/en/latest/
