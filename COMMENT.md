# HW1
A Practical Self-Adaptive Rendezvous Protocol in Cognitive Radio Ad Hoc Networks
## Summary
在cognitive radio ad-hoc networks(CRAHNs)中，當兩個使用者在通道會合時可以進行通訊，然而在真實狀況中會合成功率會受可用通道狀態變化、通道衝突等影響。本文提出分析模型框架可解決影響會合成功率的問題，也提出Self-Adaptive Rendezvous Protocol來適應動態的網路。模擬測試的結果能提高使用者在通道會合成功率、縮短會合延遲時間並降低壅塞發生。
## Strength （優點）
1.過去論文只探討channel-hopping sequence以確保成功會合，卻未解決實際狀況中通道內碰撞和使用者壅塞的問題，本文發現過去忽略的問題並分析blind rendezvous schemes假設的特殊情況，最後提出新框架解決問題。
2.新框架能夠選擇最佳化的STTR，並隨著網路狀況做動態更新。過大的STTR會增加會合成功率，但會有低效率的封包傳送速度及雍塞發生的問題。
3.提出的協定不使用任何不實際的假設，模擬的結果比過去的協定在真實場景中有更高的匯合成功率、短的會合延遲、低雍塞。
## Weakness （缺點問題漏洞）

## Comments（改善方法）
