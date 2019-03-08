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

# Cmake older version installation

```
wget http://www.cmake.org/files/v3.12/cmake-3.12.1.tar.gz 
tar -xvzf cmake-3.12.1.tar.gz 
cd cmake-3.12.1/ 
./configure 
make
```
now you dont need to install cmake (using sudo make install), instead you can set the path to point at this cmake 

```
export PATH=~/Downloads/cmake-3.12.3/bin:$PATH
```


# g++ stuff
when you build ros melodic, make sure that your g++ supports c++11
This command shows which g++ I am using 
```
ls  -ltr /usr/bin/g++
```
This will change the compiler to whatever you want 
```
sudo ln -sf /usr/bin/g++-7 /usr/bin/g++
```
