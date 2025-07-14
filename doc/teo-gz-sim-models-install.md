## teo-gz-sim-models: Installation from Source Code

First install the dependencies:

- [Install CMake 3.12+](https://github.com/roboticslab-uc3m/installation-guides/blob/master/docs/docs/install-cmake.md)
- [Install YCM 0.11+](https://github.com/roboticslab-uc3m/installation-guides/blob/master/docs/docs/install-ycm.md)

### Install the Models

Our software integrates the previous dependencies. Note that you will be prompted for your password upon using '''sudo''' a couple of times:

```bash
cd
mkdir -p repos; cd repos
git clone https://github.com/roboticslab-uc3m/teo-gz-sim-models.git
cd teo-gz-sim-models; mkdir build; cd build
cmake ..
make -j$(nproc); sudo make install; cd
```

For additional `teo-gz-sim-models` options use ccmake instead of cmake.

### Install YARP plugins for Gazebo

These SDF models integrate dynamically loaded plugins designed for interoperating the Gazebo environment from YARP. To make this possible, you need to build and install the [robotology/gz-sim-yarp-plugins](https://github.com/robotology/gz-sim-yarp-plugins) repository. Refer to their installation guides for instructions.
