Parallel Particle Filter with OpenMP

-> OpenMp parallelization on the host cpu

-> Code built using colcon, version control with git on openmp branch

-> Dependencies: OpenMP package [added in CMakeLists.txt]

-> Application can be profiled with gprof [added option -pg in CMakeLists.txt]
  -> gmon.out saved in the bag folder [demo_pf/]


To run, in the pf folder run (for every terminal):

# source /opt/ros/foxy/setup.bash
# source install/setup.bash

in one terminal, launch rviz2:

# rviz2

in another terminal, launch the node using:

# ros2 launch particle_filter demo_particlelaunch.xml

in another terminal launch the bag play using:

# ros2 bag play rosbag2_2023_05_19-15_38_30/

In rviz2, add the map, odometry & posearray (by topic)

--------------------------------------------------------

To profile the application with gprof, run a bag play. When the recording has
finished, close the node, go in the demo_pf/ folder and run

# gprof ../build/particle_filter/pf_node gmon.out > analysis.txt

This command gets hooked to the application "pf_node" (the executable of the
node) and writes results on the file "analysis.txt"
