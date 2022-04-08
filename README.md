# LIBs of VSLAM

## Eigen

```bash
mkdir build && cd build
cmake ..
sudo make install
```
    
## Pangolin
  
```bash
mkdir build && cd build
cmake ..
make
sudo make install
```
  
## Sophus
  
```bash
mkdir build && cd build
cmake ..
make
sudo make install
```
  
## Ceres-solver
  
```bash
sudo apt install libgoogle-glog-dev libgflags-dev
sudo apt install libatlas-base-dev
sudo apt install libsuitesparse-dev

mkdir build && cd build
cmake ..
make -j3
make test
sudo make install
```
  
## g2o
  
```bash
sudo apt install libsuitesparse-dev qtdeclarative5-dev qt5-qmake libqglviewer-dev-qt5

mkdir build && cd build
cmake ..
make
sudo make install
```
  

## OpenCV
  
```bash
sudo apt install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev libx264-dev libatlas-base-dev gfortran libgtk2.0-dev libjpeg-dev libpng-dev

mkdir build && cd build
cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..
sudo make -j4
sudo make install
```
  
- The Last Steps
```bash
sudo gedit /etc/ld.so.conf.d/opencv.conf
# Add
  /usr/local/lib

sudo ldconfig
sudo gedit /etc/bash.bashrc
# Add
  PKG_CONFIG_PATH=$PKG_CONFIG_PATH:/usr/local/lib/pkgconfig
  export PKG_CONFIG_PATH
      
source /etc/bash.bashrc
sudo updatedb
```
  
## Others Libs

```bash
sudo apt update
sudo apt upgrade
sudo apt install build-essential cmake
```
