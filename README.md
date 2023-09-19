Parallel Particle Filter with OpenMP

-> OpenMp parallelization on the host cpu

-> Code built using colcon, version controlo with git on openmp branch

-> Dependencies: OpenMP package (added on CMakeLists.txt)

-> Application profiled with gprof (options -pg in CMakeLists.txt)
  -> gmon.out gets saved in the bag folder

Functions running (relatively) slow: (from gmon analysis)
% time     n seconds
61.86      0.60     0.60     1020     0.59     0.65  RayMarching::calculateRays(Particle_t*, float*, Map_t*, Cloud_t*, int, float*)
  6.19      0.66     0.06     1020     0.06     0.11  RayMarching::calculateWeights(Particle_t*, float*, float*, Map_t*, Cloud_t*, int, int)
