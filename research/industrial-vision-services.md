## service-based architectures for machine vision

This is the work I did during my PhD. 
Find the abstract here:

The growing trend towards high-mix and low-volume production demands more
flexible and reconfigurable control for assembly systems. In unstructured or less structured environments, object detection and pose estimation is a key capability to enable industrial robotics applications such as grasping, handling and assembling.

The integration and interconnectivity of such automation functions is fostered by Industry 4.0 through the adoption of service-based ecosystems.
The main objective of this thesis is to create a service-based framework for
robust object detection and pose estimation in manufacturing environments. This could resemble a viable alternative to traditional machine vision systems such as smart cameras and embedded PCs, which are challenged by the high diversity and fast-paced progress in the field of object detection and pose estimation.

We approach this problem in three steps. In the first step, we propose a framework and demonstrate that it is realizable. It has a REST /gRPC interface that allows to handle all detection methods uniformly. A virtualization strategy enables upscaling and easy deployment, and the new OPC UA vision specification is exploited for integration of the detector services into the production environment.

![industrial vision services](/assets/img/thesis-gist.png)

In a second step, we examine three exemplary object detection and pose estimation methods and prove that they can be integrated into the framework. This boils down to automatic training from a CAD model and parameterization without expert knowledge, which is possible for two of the three methods. Regarding the third method – a Deep Learning approach – we demonstrate that synthetic images can be generated from the model to enable training, but further measures are required to attain the desired pose accuracy.

![render and compose](/assets/img/render-and-compose.png)

Finally, in a third step, we characterize the framework to identify its strengths and weaknesses compared to conventional machine vision systems. We perform a scenario-based analysis to determine certain quality attributes and find that both system types have their justification. The proposed service-based framework enables more efficient resource utilization, has a better configurability, maintainability and availability. On the other hand, conventional systems have better timing behavior and do not require such elaborate security measures. Timing, resource utilization and reusability are moreover strongly affected by the chosen detection method. Given a particular application, our characterization helps to identify the most suitable system type.

Altogether, in this work we have contributed a novel type of vision system and
demonstrated that it is a viable alternative for object detection and pose estimation applications. The framework structure as well as the identified architectural trade-offs can furthermore be generalized to other machine vision or automation tasks. Promising future research directions include facilitating the training of Deep Learning methods, quantifying architectural trade-offs in case studies, and integrating other vision applications to create an ecosystem of vision services.


<hr/>
#### related publications

- M. Rudorfer, **‘Towards robust object detection and pose estimation as a service for manufacturing industries,’** PhD thesis, TU Berlin. [Thesis](https://doi.org/10.14279/depositonce-11302)
- M. Rudorfer, L. Neumann and J. Krüger, **‘Towards learning 3d object detection and 6d pose estimation from synthetic data,’** in 2019 24th IEEE International Conference on Emerging Technologies and Factory Automation (ETFA), IEEE, 2019, pp. 1540–1543.
- O. Kröger, J. Guhl, O. Heimann, M. Katanacho, C. Niebuhr, M. Rudorfer, T. Özkaya, J. Wassermann, J. Hügle, T. Pannen and J. Krüger, **‘A service-oriented robotic manufacturing system: Lessons learned from participating in the world robot challenge 2018,’** in Tagungsband des 4. Kongresses Montage Handhabung Industrieroboter, Springer, 2019, pp. 44–53.
- M. Rudorfer, C. Krause, A. Vick and J. Krüger, **‘Dienstebasierte Architekturen für Robotersysteme [service-based architectures for robot systems],’** Fortschritt-Berichte Fertigungstechnik: Produktion 2030 - Wandel in der Automatisierungstechnik, 2019.
- M. Rudorfer, T. J. Pannen and J. Krüger, **‘A case study on granularity of industrial vision services,’** in Proceedings of the 2nd International Symposium on Computer Science and Intelligent Control, Best Student Paper Award, 2018, pp. 1–6
- M. Rudorfer and J. Krüger, **‘Industrial image processing applications as orchestration of web services,’** Procedia CIRP, vol. 76, pp. 144–148, 2018.
- M. Rudorfer and M. Chemnitz, **‘Dienstebasierte Integration objekt-spezifischer Lageerkennungsalgorithmen am Beispiel eines roboterbasierten Greifszenarios [service-based integration of object-specific pose detection methods for a robotic grasping scenario],’** Fortschritt-Berichte Fertigungstechnik: Industrie 4.0 - Wertsch  ̈opfungspotenziale in der dienstebasierten Produktion, 2018.
- A. Vick, C. Horn, M. Rudorfer and J. Krüger, **‘Control of robots and machine tools with an extended factory cloud,’** in 2015 IEEE World Conference on Factory Communication Systems (WFCS), IEEE, 2015, pp. 1–4.