# Eurobot2019
ICRS's Eurobot Entry 2019

## ROS Tutorials
Please please *please* go through the publisher/subscriber and service/client tutorials as found [here](http://wiki.ros.org/ROS/Tutorials) before editing any nodes.

## Merges
Before merging a completed branch, please bring it up at the next weekly meeting (Wednesdays 2pm in the lab) so that we can confirm that it is ready to be merged. This way we can make some test branches to check that there are no obvious bugs when interacting with other nodes.

## Branch Layout
There are 5 main branches which each have separate sub branches for each node within them. The layout (as planned so far) is as follows:
```
master
├── drop_module_node
    │   ├── drop_node
    │   ├── colour_select_node
├── pickup_module_node
    │   ├── store_node
    │   ├── pickup_node
    │   ├── finalise_position_node
├── path_planning_module_node
    │   ├── localisation_module_node
    │   |   ├── camera_node
    │   |   ├── lidar_node
    │   ├── path_following_node
    │   ├── motor_control_node
├── collision_avoidance_module_node
    │   ├── <tbc>
├── tactics_module_node
    │   ├── <tbc>
```

If a branch doesn't exist and is outlined here, feel free to create it. If a branch doesn't exist and is not outlined here, but you think it should be, contact Nick on Slack.

## Catkin Packages
Each module branch should have its own catkin package (drop, pickup, path_planning, localisation, collision_avoidance and tactics). All other nodes should be made in the CMakeLists.txt of the module it belongs to *as a separate executable*. If any packages are missing please contact Nick on Slack.
