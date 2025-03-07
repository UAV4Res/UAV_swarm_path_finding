# Code structure
The application is visualized using pygame. The purpose of some important code files is presented as follows.
+ ```main.py```: File to run this application
+ ```gen_test.py```: This file creates and interface to create a custom test case.
+ ```utils.py```: This file contains the algorithm of our project. Most path finding algorithm functions and math, geometry classes can be found in this file.
+ ```output.txt```: This file contains the metrics of each test case.
In the folder ```simulation-scenarios```, we have the code to visualize each algorithm. The name of each file corresponding to the name of the algorithm run by the file.

# How to use
## Create test
+ Before using the project, make sure you have python installed on your computer.
+ Install requirement:
```
pip install numpy==2.2.3 pygame==2.6.1
```
+ To use the project, we first need to create a test. To do this, we can run ```gen_test.py``` by:
```
python gen_test.py
```
+ After that, the terminal will ask you to enter some parameters, some paramter may hard to understand:
  + cell_radius: This parameter define the radius of the field which uavs can connect to each others.
  + uav_distance: This represent the remain distance which the uav can fly.
  + time_charge: Charging time of the uav
  + dis_threshold: This distance make the uav dont stay too far from the base, make sure the uav can fly to the base.
    
+ After enter all the parameters, a window would appear. This window will have four mode: gray, red, white, number, green, and blue. To change between modes, press q.
  + gray mode: You can draw the gray color represent the area that uav dont need to scan by hold left click and move the mouse.
  + red mode: You can draw the red color represent unreachable area by hold left click and move the mouse.
  + white mode: You can draw the white color represent unscanned area by hold left click and move the mouse.
  + number: You can set priority of each cell by hold left click and move the mouse. To increase the priority, press s. To decrease the priority, press a.
  + green and blue mode: You can left click on a cell to change it to the color corresponding to the mode. The choosen cell in green mode represent the cell uavs start scanning and the choosen cell in blue mode represent the base cell
+ After draw the map. Press enter to save the map.
## Run the algorithm
+ After you create the test. You can just run the main file:
```
python main.py
```
Path finding process will be visualized with each algorithm. The output metric will be saved in ```output.txt```. The format look like this:
```
type = randomUAV, num_of_uavs = 7, time = 62.449999999997736, cost = 313435.79999999324, data = 
 [{0: 0}]
```
Here we have ```type``` show algorithm is used in the test, ```num_of_uavs``` represent number of uavs, ```time``` represent the total time the algorithm takes. ```cost``` represent the total time to each uav with difference priority. 
# Reference
Tsunami: https://www.researchgate.net/publication/379603814_Tsunami_Scalable_Fault_Tolerant_Coverage_Path_Planning_for_UAV_Swarms 
