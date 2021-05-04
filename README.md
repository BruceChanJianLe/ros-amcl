# ROS Adaptive Monte Carlo Localizer

This repository demonstrates the usage of using Adaptive Monte Carlo Localization.  

## Reinitializing AMCL

When your robot is lose in a map, you may trigger the below command to populate the map with particles.  

```bash
rosservice call /global_localization
```
You may wish to drive your robot around for the particles to coverge to the correct position.  

## Reference
- AMCL Demo [link](https://www.youtube.com/watch?v=tqWnQUIoVUQ)
- AMCL Notes [link](https://husarion.com/tutorials/ros-tutorials/9-map-navigation/)
