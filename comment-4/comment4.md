# HW4
Moving Tag Detection via Physical Layer Analysis for Large-Scale RFID Systems

## Summary
With the rapid proliferation of RFID-based applications, RFID tags have been deployed into various applications in increasingly large numbers. The RFID systems are deployed to monitor a large number of RFID tags. The RFID systems are usually required to track the
movement of all tags in a real-time approach. A critical issue in such type of tag monitoring is to efficiently distinguish the motion status of all tags, including stationary or moving. 
In this paper, they propose a real-time approach to detect the moving tags in the monitoring area. We achieve the time efficiency by decoding collisions from the physical layer. Experiment result shows that when monitoring 1000 tags, our solution can accurately detect the moving tags while reducing 80% time compared with the state-of-art solutions.

## Strength （優點）
1. They are the first to propose a moving tag detection scheme for tag monitoring by leveraging the physical-layer features.
2. They solution is able to accurately detect the motion status of all tags, by referring to the physical-layer features.
3. They implemented a prototype system and evaluated its performance in realistic settings.
4. They study to extract physical-layer features from 2-collision and 3-collision slots. That can efficiently resolve all the tags in the collision slots and identify more tags in a frame.
5. They use a matrix to depict the phase distribution of the two-dimensional phase profiles. With this scheme, the tags can be accurately detected.

## Weakness （缺點問題漏洞）
1. Due to manufacturing imperfection, BLF varies among different tags. But in the paper, it does not mention what is different between tags. 
2. Since the time interval between the RN16 period and the EPC-ID period is very small, this paper considers the position and wireless environment as unchanged. However, it is uncertain whether omitting the EPC-ID signal will affect the extraction of physical-layer features.


## Comments（改善方法）
1. In this paper, it is necessary to design experiments to detect the differences among tags and determine whether such differences would affect the efficiency of detecting tag motion status.
2. Experimental design is employed to determine whether different positions and wireless environments affect the extraction of physical-layer features. The experiments are conducted to compare the results when including the EPC-ID signal and when omitting the EPC-ID signal.

