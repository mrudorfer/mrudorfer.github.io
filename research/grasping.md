## robotic grasping of unknown objects


During my postdoc at University of Birmingham I worked on project BURG - benchmarking and understanding robotic grasping.
In contrast to grasping previously known objects, where we could rely on a 3d model to find suitable grasps, we now focused on grasping unseen objects even from unknown categories - and yet we only considered mostly rigid objects, as with deformables it can get much more complicated!
On the one hand we developed methods to grasp novel objects, but on the other hand we also explored how to make robotics research more reproducible by means of benchmarks.

### learning to grasp

With our partners Tatiana, Antonio and Fabio from Torino we developed an efficient end-to-end learning strategy to generate 6-DOF parallel-jaw grasps starting from a partial point cloud of an object. Our approach does not exploit any geometric assumption, it is instead guided by a principled multi-task optimization objective that generates a diverse set of grasps by combining contact point sampling, grasp regression, and grasp evaluation.

![grasping](/assets/img/l2g-grasp-video.gif)

We evalauted the method both in simulation as well as with real robot experiments and found that the numbers were very different.
This inspired me to further explore how the grasps in simulation and the real world deviate.

### robotic grasping experiments in simulation and real world

Markus from our project partner in Vienna and I developed a toolkit, which allows to set up the exact same grasping scenarios in the real world as well as the simulated environment.
To achieve this, we used a combination of printable templates indicating the object positions and Augmented Reality.

![burg-toolkit](/assets/img/burg-toolkit.png)

Using this toolkit, we could try different grasps and record the differences in the outcomes of simulated and real trials.
Although in our pilot study with two exemplary scenarios the overall success rates were similar, we found that there were a lot of errors in both ways - with the simulation sometimes over- and sometimes underestimating the real performance.
This is an important finding, as often we use simulated grasping trials to train our models and making the training data more realistic would effectively reduce the sim-2-real gap when applying those models in the real world!


<hr/>
#### related publications

- A. Alliegro, M. Rudorfer, F. Frattin, A. Leonardis and T. Tommasi, **‘End-to-end learning to grasp via sampling from object point clouds,’** in IEEE Robotics and Automation Letters, vol. 7, no. 4, pp. 9865-9872, Oct. 2022. [Paper](https://arxiv.org/abs/2203.05585), [Code](https://github.com/antoalli/L2G/)
- M. Rudorfer, M. Suchi, M. Sridharan, M. Vincze and A. Leonardis, **‘BURG-Toolkit: Robot Grasping Experiments in Simulation and the Real World,’** ICRA Workshop on Releasing Robots into the Wild, 2022. [Project Page](https://mrudorfer.github.io/burg-toolkit/)
- A. Vick, M. Rudorfer and V. Vonasek, **‘Benchmark concept for industrial pick&place applications,’** IOP Conference Series:
Materials Science and Engineering, vol. 1140, no. 1, 2021. [Paper](https://doi.org/10.1088/1757-899X/1140/1/012014)
