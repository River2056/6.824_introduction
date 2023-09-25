---
transition: slide-left
---

# Focus: 重點架構

- Storage 存儲
- Computation 邏輯運算
- Communication 通訊交流
    - RPC, gRPC...

---
transition: slide-up
---

# Main Topics 重點主題

- Fault Tolerance 故障容許度
    - availablity 可用性 ==> 透過replication實現
    - recoverability 回復性 ==> 透過logging/transactions以及durable storage實現
- Consistency 一致性
- Performance 效能
    - throughput 流量
    - latency 延遲

---
transition: slide-left
---

# Context
由Google的兩位工程師發表: Jeffrey Dean && Sanjay Ghemawat

要解決的問題: 將網路裡的 *所有* 網站生成index (web indexing), 方便用戶透過搜尋引擎快速查詢到想要的資料

想達成的目標: 簡單的介面讓非專業的分布式系統工程師, 也能輕鬆實現分佈式架構.

手段: 

- 將自定義的 `map()`, `reduce()` 傳進MapReduce框架裡, 框架會自行將輸入參數分佈到系統內所有機器上.

