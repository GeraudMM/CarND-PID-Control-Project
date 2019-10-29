[image1]: Driving_PID.png "Intro Pic"

# CarND-PID-Control-Project
In this project we'll implement a PID controller in C++ to maneuver a vehicle around the track from the Behavioral Cloning Project!

![Driving Example][image1] 

### Introduction

The simulator will provide you the cross track error (CTE) and the velocity (mph) in order to compute the appropriate steering angle.

One more thing. The speed limit has been increased from 30 mph to 100 mph. Get ready to channel your inner Vin Diesel and try to drive SAFELY as fast as possible! NOTE: you don't have to meet a minimum speed to pass.

### Description

In this project, I implemented a PID controller for the steering of the car along the track. I modified the three parameters Kp, Ki & Kd by hand until I got a satisfying result. I finally choose Kp = 0.1, Ki = 0.03 & Kd = 1.2.
We can try to intelligently tune the parameters knowing how they will affect our system:
 - Kp is the proportional gain and is multiplied bu the error.A high proportional gain results in a large change in the output for a given change in the error. If the proportional gain is too high, the system can become unstable. In contrast, a small gain results in a small output response to a large input error, and a less responsive or less sensitive controller.
 - Ki is the integral gain and is multiplied by the accumulated error. The integral term accelerates the movement of the process towards setpoint and eliminates the residual steady-state error that occurs with a pure proportional controller. However, since the integral term responds to accumulated errors from the past, it can cause the present value to overshoot the setpoint value
 - Kd is the derivative gain and is multiplied by the the derivative of the error. Derivative action predicts system behavior and thus improves settling time and stability of the system.
 
Finally, I tried to implement a controller for the car's speed but I couldn't find a good set of parameters so I stopped for the moment.
In conclusion, some improvements are needed if we want good regulation without too many oscillations. Perhaps one of the possibilities would be to implement the [SIMC method](http://folk.ntnu.no/skoge/publications/2012/skogestad-improved-simc-pid/PIDbook-chapter5.pdf) to smooth our system's curve.

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
