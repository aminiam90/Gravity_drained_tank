# Gravity_drained_tank
Identification and PID control of a nonlinear two drained tanked gravity based process in Matlab GUI environment. 



Objective: Identification and PID control of a nonlinear two drained tanked gravity based process in Matlab GUI environment. 

How to run: Download the zip file. Open and run `Gravity_drained_tank.m'. In case of size incompatibility set your screen resoulution to 1680*1050. 

How it works: The process has two modes: (i) Open loop, (ii) Closed loop (ii). In the open-loop operation the upper tank has an 'Inlet flowrate' which can be set manually. 
At the bottom, there is also a 'Disturbance flow rate' which can also be set. The user can set these two parameters and click on the Simulate botton and observe the level of 
the bottom tank. 

Step 1. Pulse test for System identification: To identify the system and fit a linear model (either first order or second order) one should click on the 'Pulse Test' menu.
In the next menu, the paramters of a pulse test is aksed from the user. By clicking `OK' the pulse test is run and the output data is shown and stored automatically. 
Note that this step should be performed while the system is open loop. In the figure, the open-loop system is shown by a red cross on the feedback loop.

Step 2. Fitting model: After conducting the Pulse Test, we will fit a model to the process. So click on the 'Fit Model' menu on top. 
There exist four options to fit a model to the process. Once an option is selected some initial range for the uknown model parameter is asked. 
The software does its best to come up with good initial parameters, so best practice is to leave the initial parameters as they are. 
The model is shortly shown on the screen. If the model is statisfactory the user can select yes. Otherwise, the another pulse test and fit model may be required. 

Step 3. Tuning controller parameters: Once a model is fit to the obtained data, click on the 'Tuning paranmeters' menu. 
There are a variety of different methods to tune P, PI, and PID parameters. By selecting the desired method, controller parameters are shown. 
Then, one can change the system mode from 'manual mode' to the selected controller and enter the computed controller parameters. 

Step 4. Set point tracking: Now, one can the desired set point and evaluate the performance of the designed controller. 
Simply set the set point below the system model, and click on the 'simulate' button. 


What model is used for the Gravity drained Tank? 

dh(1)=(-2.5*(h(1))^(0.5)+inlet)/10;
dh(2)=(2.5*h(1)^(0.5)-2.5*(h(2))^(0.5)-dis)/10;

where h(1) is the level of upper tank, h(2) is the level of lower tank, inlet is the 'inlet flowrate' of the upper tank, dist is the 'outlet flowrate' of the bottom tank.
Other constatn parameters are related to the size of the tanks. 

