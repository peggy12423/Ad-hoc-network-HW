# HW1
A Practical Self-Adaptive Rendezvous Protocol in Cognitive Radio Ad Hoc Networks
## Summary
在cognitive radio ad-hoc networks(CRAHNs)中，當兩個使用者在通道會合時可以進行通訊，然而在真實狀況中會合成功率會受可用通道狀態變化、通道衝突等影響。本文提出分析模型框架可解決影響會合成功率的問題，也提出Self-Adaptive Rendezvous Protocol來適應動態的網路。模擬測試的結果能提高使用者在通道會合成功率、縮短會合延遲時間並降低壅塞發生。
## Strength （優點）
1.過去論文只探討channel-hopping sequence以確保成功會合，卻未解決實際狀況中通道內碰撞和使用者壅塞的問題，本文發現過去忽略的問題並分析blind rendezvous schemes假設的特殊情況，最後提出新框架解決問題。
2.新框架能夠選擇最佳化的STTR，並隨著網路狀況做動態更新。過大的STTR會增加會合成功率，但會有低效率的封包傳送速度及雍塞發生的問題。
3.提出的協定不使用任何不實際的假設，模擬的結果比過去的協定在真實場景中有更高的匯合成功率、短的會合延遲、低雍塞。
4.分析會合過程的兩大主要問題：channel status changing during the channel-hopping和data packet congestion caused by rendezvous，利用Poisson分布定義參數，取得發生問題的機率。
5.將TTR、ETTR、MTTR等多項參數整理成表格，閱讀公式時可以參照表格知道參數意義。
6.過去很少有論文考慮節點移動性的影響，本文將CRAHN中的PU和SU視為CH期間的靜態節點，考慮到channel-hopping期間SU不可用channel的狀況。
7.提出序列調整機制，避免不在彼此的感應範圍內的SU發送者同時跳到相同channel上，造成碰撞而導致會合延遲或失敗。
## Weakness （缺點問題漏洞）
1.在密集節點大流量的CRAHN中，文中提到的四個因素會同時影響channel的可用狀態，但未提到會合成功率及TTR的影響程度。
2.本文通過智能推理可能的場景並動態調整參數，然而實際場景的狀況可能面臨新的狀況，導致參數的設定不符合場景需求。
3.在本文提出的RTS碰撞避免方法中，加入Not-Clear-To-Send來通知發送者，正在爭奪同一個接收者，本文未討論NCTS封包丟失而造成的狀況。
4.在模擬實驗中，PU和SU隨機分佈在模擬區域內，並未測試特定分布狀況的模擬結果。
5.當 SU 的封包大小增加時，會合協議都會獲得更好的性能，卻會導致傳輸時間增加而影響數據傳輸的性能，兩者之間的權衡參數仍是未知。
## Comments（改善方法）
1.探討如何利用更多的數據來訓練和優化自適應模型，以提高協議的效率和準確性。
