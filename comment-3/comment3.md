# HW3
SenSpeed: Sensing Driving Conditions to Estimate Vehicle Speed in Urban Environments
## Summary
Sometimes, GPS is unavailable or inaccurate in urban environments. In the paper, they utilizes smartphone sensors to sense natural driving conditions to achieve high estimation accuracy and solve this problem. They propose an accurate vehicle speed estimation system, SenSpeed, which senses natural driving conditions in urban environments. SenSpeed can identify three useful reference points, including making turns, vehicle stopping, and passing through uneven road surfaces, to measure and eliminate the errors caused by directly using phone's accelerometer readings for speed estimation. Their extensive experiments driving in two different cities over one month time period show that SenSpeed can estimate the vehicle speed in real-time with a low average error of 1.32mph, while achieving 0.75mph during the offline estimation. Whereas the average error of GPS is 3.1mph and 2.8mph respectively.

## Strength （優點）
1. The paper mentions about accurate vehicle speed estimation could make those vehicle-speed dependent applications more reliable under complex traffic systems in urban environments.
2. Using GPS continuously drains the phone battery quickly and the acceleration errors can lead to large deviations, so they using smartphone sensors to estimate the vehicle speed.
3. They consider a sensing approach, which uses smartphone sensors to sense natural driving conditions, to derive the vehicle speed without requiring any additional hardware.
4. They have considered that the solution should be lightweight and computational feasible on smartphones, because the speed estimation should be real-time and accurate.
5. According to the finding that the changes of the acceleration error are very small, so they develop a vehicle speed estimation system, SenSpeed, which it senses the unique features in natural driving conditions through simple smartphone sensors to facilitate vehicle speed estimation.

## Weakness （缺點問題漏洞）
1. They show the vehicle speed estimation through real road driving experiments in two different cities, but there is diverse scenario in prctical world. The experiment in only two different cities may be too limited.
2. They study the impact of the acceleration error on the speed estimation results obtained from the integral of the phone's accelerometer readings, but the accelerometer readings are noisy and affected by various driving environments. The sensor readings may cause serious errors in the estimation results.
3. SenSpeed system has to use the accelerometer for the vehicle acceleration and the gyroscope for the vehicle angular speed. If one of them is not available, it may caused the system estimated the vehicle speed inaccurately.

## Comments（改善方法）
1. Analyze the conditions of the two experimental cities. Add more urban scenarios to the experiment for increasing the diversity of experimental scenes.
2. They should capture as many as possible time points, called reference points, which can be calculated acceleration errors between each two adjacent points. After knowing these acceleration errors, the integral values can be corrected to get closer to the true speeds.
3. They must use alternatives in case of equipment failure, such as installing other equipment to evaluate the acceleration and the angular speed.
