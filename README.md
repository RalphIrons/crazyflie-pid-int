# crazyflie-pid-int
Trying different techniques for approximating the integral term of the crazyflie quadcopter's pid controller

I would like to compare the currently implemented rectangle rule integration technique with the trapezoid rule and Simpson's rule, with respect to their effects on logged motor thrust and accelerometer data.

Proposed test set up: suspend crazyflie between two supports using string through built-in expansion holes. Crazyflie rotates only around pitch axis (y axis?). Log data on all motors and accelerometer data on pitch axis (y axis?). With crazyflie flying level, lift rear end up until vertical, then release. Do this a total of 4 times. Recharge crazyflie. Flash firmware implementing a new integration technique, then repeat test.
