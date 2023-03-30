# HW2
Predicting the effect of home Wi-Fi quality on QoE
## Summary
Whenever Wi-Fi quality being poor will degrades the Quality of Experience (QoE).
Detecting Wi-Fi quality degrades QoE before users call is extremely important for residential Internet Service Providers (ISPs).
In theis paper, their goal is to develop a system that runs on commodity access points (APs) to assist ISPs in detecting when Wi-Fi degrades QoE.
Thier contributions include developing a method to detect instances of poor QoE based on the passive observation of Wi-Fi quality metrics and applying their predictors of QoE given Wi-Fi quality to Wi-Fi metrics available on commodity APs with low errors collected customers of a large residential ISP. Our results show that QoE is good most of the time.ISPs can use the fraction of poor QoE samples to identify stations with frequent poor QoE due to Wi-Fi.
## Strength （優點）
1.They build a system for ISPs to detect when home Wi-Fi quality degrades QoE before QoE degrades.
2.To reduce the tests with real users, they measure application quality metrics and use state of the art methods to translate QoS into QoE as captured by the degradation of mean opinion scores(DMOS).
3.They vary the medium availability at the AP by introducing interference from Wi-Fi or non-Wi-Fi sources.
4.They use four applications to predict various Wi-Fi scenario.
5.They use a set of 20 different audio samples recommended by ITU-T for speech quality assessment to sumulatate real environment.
6.They map application QoS metrics into an estimated QoE, and denote the application QoS to QoE model as a function.

## Weakness （缺點問題漏洞）
1.They excute automated tests with some applications.They use the command line to perform RTC tests with a pre-recorded audio/video sample.The setup closely resembles a real user environment. However,The setting is still slightly off in a real environment.
2.They denote the applicaation QoS to QoE model as a function. But the models output an estimate of the absolute MOS. The estimate of MOS is uncertainly accurate for the customer QoE.
3.The difference in frequency between applications is due to the application sensitivity to the Wi-Fi impairments.On other predictors, this only occurs when they also observe interference.
## Comments（改善方法）
1.The expiriment uses the pre-recorded audio/vedio streams, they should consider transmission delay in a real scenes.
2.Making the experiment for contrasting QoE and estimate of the absolute MOS by model. Analyze both of them relative and deviation.
3.They have to consider interference of Wi-Fi, and conquer it.
