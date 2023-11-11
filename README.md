![traffic-signal](https://github.com/Git-init-2022/Yolov3-pretrained-model/assets/107217455/1998b15a-faa3-45d4-98e8-8c29f0834299)


<h1 align="center">Smart Traffic Signal Control</h1>

<div align="center">

[![Python version](https://img.shields.io/badge/python-3.7-blue.svg)](https://www.python.org/downloads/release/python-370/)
[![License: Apache 2](https://img.shields.io/badge/License-Apache-yellow.svg)](https://www.apache.org/licenses/LICENSE-2.0)

<h4>This Smart Traffic Signal Control uses live images from the cameras at traffic junctions for traffic density calculation using YOLO object detection and sets the signal timers accordingly, thus reducing the traffic congestion on roads, providing faster transit to people, and reducing fuel consumption.</h4>

</div>

-----------------------------------------
### Inspiration

* Traffic congestion is becoming one of the critical issues with the increasing population and automobiles in cities. Traffic jams not only cause extra delay and stress for the drivers but also increase fuel consumption and air pollution. 

* According to the [TomTom Traffic Index](https://www.tomtom.com/en_gb/traffic-index/ranking/), 3 of the top 10 countries facing the most traffic congestion are in India viz. Mumbai, Bengaluru, and New Delhi.  People are compelled to spend hours stuck in traffic jams, wasting away their precious time commuting. Current traffic light controllers use a fixed timer and do not adapt according to the real-time traffic on the road.

* In an attempt to reduce traffic congestion, we developed an improved traffic management system in the form of a Computer Vision-based traffic light controller that can autonomously adapt to the traffic situation at the traffic signal. The proposed system sets the green signal time adaptively according to the traffic density at the signal and ensures that the direction with more traffic is allotted a green signal for a longer duration of time as compared to the direction with lesser traffic. 

------------------------------------------
### Implementation Details

This project can be broken down into 3 modules:

1. `Vehicle Detection Module` - This module is responsible for detecting the number of vehicles in the image received as input from the camera. More specifically, it will provide as output the number of vehicles of each vehicle class such as car, bike, bus, truck, and rickshaw.

2. `Signal Switching Algorithm` - This algorithm updates the red, green, and yellow times of all signals. These timers are set bases on the count of vehicles of each class received from the vehicle detection module and several other factors such as the number of lanes, average speed of each class of vehicle, etc. 

3. `Simulation Module` - A simulation is developed from scratch using [Pygame](https://www.pygame.org/news) library to simulate traffic signals and vehicles moving across a traffic intersection.

Read more about object detection model used, working of the algorithm, and development of simulation [here](./Adaptive_Traffic_Signal_Timer_Implementation_Details.pdf).

------------------------------------------
### Demo

* `Vehicle Detection`

![vehicle-detection](https://github.com/Git-init-2022/Yolov3-pretrained-model/assets/107217455/78e4d217-1349-473a-8bb4-5a2f78044af5)


<br> 

* `Signal Switching Algorithm and Simulation`

<p>
      <img src="https://github.com/Git-init-2022/Yolov3-pretrained-model/blob/efa7e6121ac28b566efb13ea7bbe50f191a5040d/Demo%20(1).gif"/>
</p>

------------------------------------------
### Prerequisites

1. [Python 3.7](https://www.python.org/downloads/release/python-370/)
2. [Microsoft Visual C++ build tools](http://go.microsoft.com/fwlink/?LinkId=691126&fixForIE=.exe.) (For Windows only)

------------------------------------------
### Installation

* Step I: Clone the Repository
```sh
      $ git clone https://github.com/mihir-m-gandhi/Adaptive-Traffic-Signal-Timer
```

* Step II: Download the weights file from [here](https://drive.google.com/file/d/1flTehMwmGg-PMEeQCsDS2VWRLGzV6Wdo/view?usp=sharing) and place it in the Adaptive-Traffic-Signal-Timer/Code/YOLO/darkflow/bin directory

* Step III: Install the required packages
```sh
      # On the terminal, move into Adaptive-Traffic-Signal-Timer/Code/YOLO/darkflow directory
      $ cd Adaptive-Traffic-Signal-Timer/Code/YOLO/darkflow
      $ pip install -r requirements.txt
      $ python setup.py build_ext --inplace
```

* Step IV: Run the code
```sh
      # To run vehicle detection
      $ python vehicle_detection.py
      
      # To run simulation
      $ python simulation.py
```

------------------------------------------
### Contributors

G John Caleb - [John-caleb](https://github.com/orgs/Git-init-2022/people/John-caleb)

R Sai Krishna - [saikrish02](https://github.com/orgs/Git-init-2022/people/saikrish02)

B Jyothi Swaroop Reddy - [JyothiSwaroopReddy07](https://github.com/orgs/Git-init-2022/people/JyothiSwaroopReddy07)

------------------------------------------
### Acknowledgement

We would like to extend our sincere thanks to our mentor Mrs.Kamakshi Prasad for her kind help and valuable advice. Her support and constant supervision were imperative for the successful completion of this project. We would also like to express our special gratitude and thanks to Mrs. Kavita Kelkar, the subject-matter expert for this project, for her valuable inputs and guidance.   

------------------------------------------
### License
This project is licensed under the Apache License 2.0 - see the [LICENSE](./LICENSE) file for details.
