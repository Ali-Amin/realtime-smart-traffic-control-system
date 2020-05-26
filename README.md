# Smart Traffic Control System using Digital Image Processing
An automated traffic control system for junction. Written completely in `python3` using digital image processing concepts written from scratch (no `opencv`)

<i>Junction dataset can be found at here ![url](https://personal.ie.cuhk.edu.hk/~ccloy/downloads_qmul_junction.html)</i>

## The system is capable of automating this junction
![image](https://github.com/Ali-Amin/smart-traffic-system-using-dip/blob/master/assets/frame3.png)

<br>
Using the finite state machine below, the system can take an input of:
<br>

- current frame
- immediate previous frame
- background
- current state of the junction

and will output which state to go to next

![image](https://github.com/Ali-Amin/smart-traffic-system-using-dip/blob/master/assets/fsm_diagram.png)

where the states denote the following:
- <b>State 1</b>: Main road is lit green, uturns and sideways road are lit red
- <b>State 2</b>: Uturns are green and all others are red</b>
- <b>State 3</b>: The sideways road is lit green and all others are red</b>

## Limitations
- Traffic video cannot be directly used for testing since cars will not respond to feedback from the model
- Each region has a different size, meaning that 1 car in each region will have a different average value in each one, but this is worked-around by using different decision boundary values for each region
