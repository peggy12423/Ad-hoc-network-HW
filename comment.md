# HW1
A Practical Self-Adaptive Rendezvous Protocol in Cognitive Radio Ad Hoc Networks

## Summary
In cognitive radio ad-hoc networks, two users rendezvous on a common available channel to realize communications. However, the theoretical rendezvous successful rate may suffer from the available channel status changing, collisions on channels, congestion at users, and target users unavailability in practical scenarios.
The authors propose analytical models for each possible factor which affecting rendezvous rate.They also proposes the self-adaptive protocol which can adapt to the dynamic network.The protocal includes modules for channel state changing and data packet congestion.Furthermore, a collision avoidance mechanism and rendezvous delay compensation method are mentioned. Simulation results show that the method can enhance the rendezvous rate of the users in the channel, shorten the delay time of the rendezvous, and avoid the occurrence of congestion.

## Strength （優點）
1.Most existing rendezvous papers focus on success-guaranteed channel-hopping(CH) sequence design. They do not solve the problem of collisions on channels and congestion at users. The authors discover these problems that have been ignored before, and analyze 
impratical assumptions for blind rendezvous. Finally, they propose a new framework that can address these issues in practical scenarios.
2.In the proposed protocol, they calculate the optimal STTR and update it dynamically based on the environmental changes.A long STTR can lead to a high rendezvous success rate but a low performance of data transmissions and congestion occur.
3.The proposed protocol does not use any impractical assumptions, and the simulation results have higher rendezvous efficiency, shorter rendezvous delay, and lower collision rate than before in real scenarios.
4.Analyze two main problems in rendezvous process: channel status changing during the channel-hopping and data packet congestion caused by rendezvous.Follow the Poisson distribution to define parameters and calculate the probability of occurrence of problems.
5.They organize multiple parameters such as TTR, ETTR, MTTR into a table, and you can refer to the table to know the meaning of the parameters when reading the formula.
6.In the past, there are few papers considered the influence of nodes’ mobility. In this paper, primary users(PUs) and secondary users(SUs) in CRAHN are regarded as static nodes during channel-hopping.considering the situation that SU is unavailable during channel-hopping.A channel will become unavailable to a SU in some situation.
7.A sequence adjustment mechanism is proposed to avoid two SU senders that are not in each other's sensing range hop to the same channel at the same time. That will resulting in collisions, delay or failure of rendezvous.

## Weakness （缺點問題漏洞）
1.In a dense-node high-traffic CRAHN, the four factors usually affect the channel status simultaneously, but it does not mention successful rate of rendezvous and degree of influence.
2.By intelligently reasoning the possible scenarios and adjusting parameters dynamically. However, the practical scenario may face some new situation. The setting of parameter may not confront to the scenario requirements.
3.In the RTS collision avoidance method proposed in this paper, Not-Clear-To-Send(NCTS) notify the sender that someone is competing for the same receiver. They do not discuss the situation caused by NCTS packet loss.
4.In the simulation experiment, PUs and SUs are randomly distributed in the simulation area, and the simulation results of specific distribution conditions are not experienced.
5.When the packet size of SU increases, the rendezvous protocolS will gain better performance. But they cause increasing transmission time and impacting the performance of data transmissions. The trade-off parameters between the two are still unknown.

## Comments（改善方法）
1.Observe the status of the channel.In addition, analyze the successful rendezvous rate and the corresponding TTR.
2.They have to operate the experiment in real scene to know the relevant parameter settings.
3.A Time-out mechanism can be designed to retransmit NCTS packets after a certain time.
4.According to the specific distribution requirements, the protocol proposed in this paper is experimentally verified.
5.Experiment the transmission time of different packet sizes and the performance of the rendezvous protocol to obtain the optimal trade-off parameters.
