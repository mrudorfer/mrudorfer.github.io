## robotic assembly

Using robots for autonomous assembly of products with small lot sizes and high variety is an open challenge that gets a lot of research attention.
This is fostered by competitions such as the World Robot Challenge in Japan in which we took part in 2018 with our team **BerlinAUTs**.

<iframe width="500" height="281" src="https://www.youtube.com/embed/K0bYMBEZO54" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<hr/>
### the challenge

The World Robot Competition comprised a couple of different challenges seeking for robots that can be helpful in desaster scenarios, enable the future convenience stores, clean public toilets or leverage industrial manufacturing. Along with 15 other teams, we took part in the assembly challenge.

There were four tasks in total. The first task required to master a set of independent assembly operations, like peg-in-hole, screwing, or strapping a rubber belt onto two pulleys. The second task was a preparation for the assembly. It mimicked a bin-picking scenario where the robot had to pick certain parts according to the set list and place them into a kitting tray. Finally, the tasks three and four dealt with the assembly of the belt drive unit (see manual assembly [here](https://www.youtube.com/watch?v=NNSmNDf3PK0)). The fourth task mimicked a high-mix low-volume production scheme, which requires to dynamically switch between several variants of the product. The teams had to cope with surprise variants that were only specified 24 hours before the competition trial.

![image](/assets/img/wrc-kitting.png)

<hr/>
### our approach

We aimed for a robot system with maximum flexibility. It led us to a service-based architecture for our robot system. Each component could be programmed and controlled individually. A gRPC interface then enabled the communication. The complexity was putting all these things together for testing, which we actually accomplished only a few weeks before the competition. But once everything was in place, we could program the actual tasks on a very high abstraction layer. Many changes of the task would not need any reprogramming of the robot, instead we would simply adjust some config files.

![image](/assets/img/wrc-system-overview.png)

Some other changes were directly compensated by the system itself. For example, we did not need fixed positions for task-related parts such as the taskboard, the kitting trays or the bins. Instead, we had placed markers at relevant positions. Recognizing their positions was enough to navigate the robot close to its target. With the robot-mounted camera, we could use visual servoing to make minor pose adjustments for achieving the desired accuracy.

![image](/assets/img/wrc-taskboard.jpg)

As funding for this project was limited we had to compensate missing resources with creativity. Some tasks required two robot arms (e.g. holding a nut near a hole while placing a screw from the other side). We had only one available, so we mounted a second gripper on the table that could help with some of these operations. However, there remained several tasks we simply could not accomplish. We tried to come up with partial solutions that would at least give us a fraction of the points. In the end, we could achieve a solid 10/16 ranking at the competition. And we learned a lot. It was a great experience, we grew together as a team, made new friends and got to know a bit of Japanese culture.

![image](/assets/img/wrc-berlinauts.png)


<hr/>
#### publications

- F. Von Drigalski, C. Schlette, M. Rudorfer, N. Correll, J. C. Triyonoputro, W. Wan, T. Tsuji and T. Watanabe, **‘Robots assembling machines: Learning from the world robot summit 2018 assembly challenge,’** Advanced Robotics, vol. 34, no. 7-8, pp. 408–421, 2020. [Paper](https://arxiv.org/abs/1911.05884)
- O. Kröger, J. Guhl, O. Heimann, M. Katanacho, C. Niebuhr, M. Rudorfer, T. Özkaya, J. Wassermann, J. Hügle, T. Pannen and J. Krüger, **‘A service-oriented robotic manufacturing system: Lessons learned from participating in the world robot challenge 2018,’** in Tagungsband des 4. Kongresses Montage Handhabung Industrieroboter, Springer, 2019, pp. 44–53.