# crazyflie-pid-int
Trying different techniques for approximating the integral term of the crazyflie quadcopter's pid controller

I would like to compare the currently implemented rectangle rule integration technique with the trapezoid rule and Simpson's rule, with respect to their effects on a pilot's ability to hover the crazyflie.

Proposed test set up: Double blind test with 19 pilots attempting to hover 3 crazyflie quadcopters for a 15 second period. Pilots select the copter which seemed easiest to hover. Pilots do not know which integration technique is being tested, and assistants setting up the copters do not know, either. The experiment is repreated 3 times, with the integration techniques being switched from copter to copter, to contol for hardware differences. A Chi-squared statistic will be used to test the null hypothesis that there is no difference in pilot preference.
****************************************************************************
The above test was performed during the week of April 6 - 10, 2015, by calculus students at Shenandoah Valley Governor's School. The results of the 57 tials were

rectangle rule: 15,  Simpson's rule: 22,  trapezoid rule: 20

The Chi-squared statistic's value of 1.37, df=2, fell well short of the critical value of 5.99 needed to reject the null hypothesis.

Students noted, however, that the Simpson's rule copter could be identified by its yaw rotation, which they conjectured to be the result of the fact that the Simpson's rule pidUpdate changes only on every third call. It was suggested that a separate pidUpdate function be created for yaw, always using the rectangle rule, and then the tests should then be repeated.
