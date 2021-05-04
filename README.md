# ROS Adaptive Monte Carlo Localizer

This repository demonstrates the usage of using Adaptive Monte Carlo Localization.  

## Reinitializing AMCL

When your robot is lose in a map, you may trigger the below command to populate the map with particles.  

```bash
rosservice call /global_localization
```
You may wish to drive your robot around for the particles to coverge to the correct position.  

## AMCL Params

- `scan`: Laser scan topic.

- `global_frame_id`: Frame name of global frame, usually it's map

- `odom_frame_id`: Frame name of odom.

- `base_frame_id`: Frame name of base.

- `odom_model_type`: Method of how your navigates options are diff/omni ,but use fixed algorithms with -corrected suffix. Example: "diff-corrected".

- `update_min_d`: Translational movement required before performing a filter update.

- `update_min_a`: Rotational movement required before performing a filter update.

- `min_particles`: Minimum allowed number of particles. How many of laser scan points is used to estimate position, if you have changing environment consider enlarging this param.

- `tf_broadcast`: Decide if publish the transform between the global frame and the odometry frame.

- `initial_pose_x`: Initial pose mean (x), you should set this param different than "0.0" only if place where robot starts navigation is different than start point for map. If it's small distance you should leave this as "0.0".

- `initial_pose_y`: Initial pose mean (x). Use this the same way as initial_pose_x.

- `initial_pose_a`: Initial pose mean (yaw). Use this the same way as initial_pose_x.


## Reference
- AMCL Demo [link](https://www.youtube.com/watch?v=tqWnQUIoVUQ)
- AMCL Params [link](https://husarion.com/tutorials/ros-tutorials/9-map-navigation/)
