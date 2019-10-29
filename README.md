[image1]: Driving_PID.png "Intro Pic"

# CarND-PID-Control-Project
In this project we'll implement a PID controller in C++ to maneuver a vehicle around the track from the Behavioral Cloning Project!

![Driving Example][image1] 

### Introduction

The simulator will provide you the cross track error (CTE) and the velocity (mph) in order to compute the appropriate steering angle.

One more thing. The speed limit has been increased from 30 mph to 100 mph. Get ready to channel your inner Vin Diesel and try to drive SAFELY as fast as possible! NOTE: you don't have to meet a minimum speed to pass.

### Description

### Files description

The script files are in the `src` folder. All the other files or folders are there to ensure we can run the program successfully. 
Here are the main script files:
 
 - `PID.h` & `PID.ccp` contain the class for the PID controller.
 
 - `main.cpp` is of course the main script but take also care of the protocol.
 
 ### Getting Started

This project involves the Term 2 Simulator from Udacity which can be downloaded [here](https://github.com/udacity/self-driving-car-sim/releases).

Download the CarND-PID-Control [repo](https://github.com/udacity/CarND-PID-Control-Project) or my own [repo](https://github.com/GeraudMM/CarND-PID-Control-Project).

Then install uWebSocketIO.
The Udacity repository includes two files that can be used to set up and install [uWebSocketIO](https://github.com/uWebSockets/uWebSockets) for either Linux or Mac systems. For windows you can use either Docker, VMware, or even [Windows 10 Bash on Ubuntu](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/) to install uWebSocketIO.

Once the install for uWebSocketIO is complete, the main program can be built and run by doing the following from the project top directory.

1. mkdir build
2. cd build
3. cmake ..
4. make
5. ./pid


Then you only need to open the executable file in the `Term 2 Simulator` folder and launch the project to watch the car evovle.

### Other Important Dependencies

* cmake >= 3.5
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
