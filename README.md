# DCN Final Project
## Introduction
This is the final deliverable of the DCN Final Project (SDN development). It contains 2 parts of codes in 3 files in `DCN-Spring2022-FinalProject-hl4151.jar`, which are:
* `Routing.java` & `ShortestPathSwitching.java`: Implementing layer-3 (Network layer) routing;
* `LoadBalancer.java`: Implementing load balance routing;

Besides, this file also contains a JAR file `FloodlightWithApps.jar`, which is the executable jar file of this project.

There are also records of project vulnerability, project testing & debugging methods, and also a detailed project report.

## Implementation
For implementation details, please refer to the project report, which contains the pseudocode for algorithms and implementation code & corresponding illustrations.

Simply speaking, the layer-3 routing is implemented using Dijkstra algorithm based on adjacency table. The load balance routing is based on identifying the protocol type, source, and destination addresses of incoming packets, and then combined with actions for ARP reply sending, TCP address rewriting rules, or TCP RESET sending.

## How to run?
To run this project, please make sure you have installed mininet. First, you should use command
```
java -jar FloodlightWithApps.jar -cf $someconfiguration$.prop
```
In which the .prop is the configuration file indicating the task this progarm is to execute.

After that, please start mininet with some topology configuration in another console, and wait until it has ARPed each host. After that, you can enter commands in the mininet console to execute some actions in mininet.

## Thank you!
Edited by Haochen Li (mailto: hl4151@nyu.edu), 05/16/2022.