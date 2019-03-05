# Cmake_lab
Stuff for Cmake 

# Cmake flags 
```
mkdir build
cd build
cmake ..
cmake -LA | awk '{if(f)print} /-- Cache values/{f=1}'
```
You can do this with a GUI 

```
sudo apt-get install cmake-curses-gui
ccmake ..
```
when you want to build OpenCV for a limitted embedded system use this 
```
 cmake -D CMAKE_BUILD_TYPE=Release -D CMAKE_INSTALL_PREFIX=/usr/local -D WITH_FFMPEG=0 -D WITH_CUDA=OFF ..
```
