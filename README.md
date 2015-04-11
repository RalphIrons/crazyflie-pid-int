# crazyflie-pid-int
Trying different techniques for approximating the integral term of the crazyflie quadcopter's pid controller

I would like to compare the currently implemented rectangle rule integration technique with the trapezoid rule and Simpson's rule, with respect to their effects on a pilot's ability to hover the crazyflie.

Proposed test set up: Double blind test with 19 pilots attempting to hover 3 crazyflie quadcopters for a 15 second period. Pilots select the copter which seemed easiest to hover. Pilots do not know which integration technique is being tested, and assistants setting up the copters do not know, either. The experiment is repreated 3 times, with the integration techniques being switched from copter to copter, to contol for hardware differences. A Chi-squared test will test the null hypothesis that there is no difference in pilot preference.
