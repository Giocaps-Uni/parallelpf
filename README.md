Parallel Particle Filter with OpenMP

-> OpenMp parallelization on the host cpu

-> Code built using colcon, version controlo with git on openmp branch

-> Dependencies: OpenMP package (added on CMakeLists.txt)

-> Application profiled with gprof (options -pg in CMakeLists.txt)
  -> gmon.out gets saved in the bag folder
