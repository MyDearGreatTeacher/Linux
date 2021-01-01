#
```
https://linuxsecurity.com/
```
```
IP Chains - Linux Kernel 2.2.x Firewalling
Netfilter - Linux Kernel 2.4.x Firewalling
```
```
Linux Administrator's Security Guide
Linux Network Security  By Kurt Seifried kurt@seifried.org

https://www.linuxtopia.org/online_books/linux_administrators_security_guide/13_Linux_Network_Security.html
```
```

https://tldp.org/HOWTO/Security-HOWTO/network-security.html

```
# iptables之log日誌工具-ULOGD使用手記
```
iptables之log日誌工具-ULOGD使用手記
weixin_30762087的博客
https://blog.csdn.net/zhongbeida_xue/article/details/106057885
```
#
```
LINUX FIREWALLS ：善用 NFTABLES 等超強工具捍衛 LINUX 防火牆的安全性, 4/e (中文版) 
Linux Firewalls: Enhancing Security with nftables and Beyond, 4/e
Steve Suehring 王文燁  博碩文化  2019-09-12
ISBN: 9864344234   ISBN-13: 9789864344239
```
```
▶針對執行iptables或nftables的Linux防火牆，進行安裝、設定以及更新
▶遷移到nftables，或者使用新的iptables增強機制
▶管理複雜的多重防火牆設定
▶建立、除錯和最佳化防火牆規則
▶使用Samhain和其他工具來保護文件系統的完整性，以及監控網路和檢測入侵
▶增強系統以防禦埠掃描和其他攻擊
▶使用chkrootkit檢測惡意軟體rootkit和後門等漏洞
```
```
Part I 封包過濾以及基本安全措施

Chapter 1 封包過濾防火牆的預備知識
1.1 OSI 網路模型
1.1.1 連接導向和非連接的協定
1.1.2 下一步
1.2 IP 協定
1.2.1 IP 編址和子網劃分
1.2.2 IP 分片
1.2.3 廣播與多播
1.2.4 ICMP
1.3 傳輸層機制
1.3.1 UDP
1.3.2 TCP
1.4 位址解析協定（ARP）
1.5 主機名稱和 IP 位址
1.5.1 IP 位址和乙太網位址
1.6 路由：將封包從這裡傳輸到那裡
1.7 服務埠：通向您系統中程式的大門
1.7.1 一個典型的 TCP 連接：存取遠端站點
1.8 小結

Chapter 2 封包過濾防火牆概念
2.1 封包過濾防火牆
2.2 選擇一個預設的封包過濾策略
2.3 對一個封包的駁回（Rejecting）VS 拒絕（Denying）
2.4 過濾傳入的封包
2.4.1 遠端來源位址過濾
2.4.2 本地目的位址過濾
2.4.3 遠端來源埠過濾
2.4.4 本地目的埠過濾
2.4.5 傳入 TCP 的連接狀態過濾
2.4.6 探測和掃描
2.4.7 拒絕服務攻擊
2.4.8 來源路由封包
2.5 過濾傳出封包
2.5.1 本地來源位址過濾
2.5.2 遠端目的位址過濾
2.5.3 本地來源埠過濾
2.5.4 遠端目的埠過濾
2.5.5 傳出 TCP 連接狀態過濾
2.6 私有網路服務 VS 公有網路服務
2.6.1 保護不安全的本地服務
2.6.2 選擇執行的服務
2.7 小結

Chapter 3 iptables：傳統的 Linux 防火牆管理程式
3.1 IP 防火牆（IPFW）和 Netfilter 防火牆機制的不同
3.1.1 IPFW 封包傳輸
3.1.2 Netfilter 封包傳輸
3.2 iptables 基本語法
3.3 iptables 特性
3.3.1 NAT 表特性
3.3.2 mangle 表特性
3.4 iptables 語法
3.4.1 filter 表命令
3.4.2 filter 表目標擴展
3.4.3 filter 表匹配擴展
3.4.4 nat 表目標擴展
3.4.5 mangle 表命令
3.5 小結

Chapter 4 nftables:（新）Linux 防火牆管理程式
4.1 iptables 和 nftables 的差別
4.2 nftables 基本語法
4.3 nftables 特性
4.4 nftables 語法
4.4.1 表語法
4.4.2 規則鏈語法
4.4.3 規則語法
4.4.4 nftables 的基礎操作
4.4.5 nftables 檔案語法
4.5 小結

Chapter 5 建構和安裝獨立的防火牆
5.1 Linux 防火牆管理程式
5.1.1 自訂與購買：Linux 核心
5.1.2 來源位址和目的位址的選項
5.2 初始化防火牆
5.2.1 符號常數在防火牆範例中的使用
5.2.2 啟用核心對監控的支援
5.2.3 移除所有預先存在的規則
5.2.4 重置預設策略及停止防火牆
5.2.5 啟用迴路介面
5.2.6 定義預設策略
5.2.7 利用連接狀態繞過規則檢測
5.2.8 來源位址欺騙及其他不合法位址
5.3 保護被分配在非特權埠上的服務
5.3.1 分配在非特權埠上的常用本地 TCP 服務
5.3.2 分配在非特權埠上的常用本地 UDP 服務
5.4 啟用基本的、必需的網際網路服務
5.4.1 允許 DNS（UDP/TCP埠53） 
5.5 啟用常用 TCP 服務 147
5.5.1 Email (TCP SMTP埠25, POP埠110, IMAP埠143)
5.5.2 SSH（TCP埠22）
5.5.3 FTP (TCP埠20、21)
5.5.4 通用的 TCP 服務
5.6 啟用常用 UDP 服務
5.6.1 存取您 ISP 的 DHCP 伺服器（UDP埠67、68）
5.6.2 存取遠端網路時間伺服器（UDP埠123）
5.7 記錄被丟棄的傳入封包
5.8 記錄被丟棄的傳出封包
5.9 安裝防火牆
5.9.1 除錯防火牆腳本的小竅門
5.9.2 在啟動 Red Hat 和 SUSE 時啟動防火牆
5.9.3 在啟動 Debian 時啟動防火牆
5.9.4 安裝使用動態IP 位址的防火牆
5.10 小結

Part II 進階議題、多個防火牆和邊界網路

Chapter 6 防火牆的最佳化
6.1 規則組織
6.1.1 從阻止高位埠流量的規則開始
6.1.2 使用狀態模組進行 ESTABLISHED 和 RELATED 匹配
6.1.3 考慮傳輸層協定
6.1.4 儘早為常用的服務設置防火牆規則
6.1.5 使用網路資料流來決定，在哪裡為多個網路介面設置規則
6.2 用戶自定義規則鏈
6.3 最佳化的範例
6.3.1 最佳化的 iptables 腳本
6.3.2 防火牆初始化
6.3.3 安裝規則鏈
6.3.4 建構用戶自定義的 EXT-input 和 EXT-output 規則鏈
6.3.5 tcp-state-flags
6.3.6 connection-tracking
6.3.7 local-dhcp-client-query 和 remote-dhcp-server-response
6.3.8 source-address-check
6.3.9 destination-address-check
6.3.10 在 iptables 中記錄丟棄的封包
6.3.11 最佳化的 nftables 腳本
6.3.12 防火牆初始化
6.3.13 建構規則檔案
6.3.14 在 nftables 中記錄丟棄的封包
6.4 最佳化帶來了什麼
6.4.1 iptables 的最佳化
6.4.2 nftables 的最佳化
6.5 小結

Chapter 7 封包轉發
7.1 獨立防火牆的侷限性
7.2 基本的閘道器防火牆的設置
7.3 LAN 安全問題
7.4 可信家庭 LAN 的設定選項
7.4.1 對閘道器防火牆的 LAN 存取
7.4.2 對其他 LAN 的存取：在多個 LAN 間轉發本地流量
7.5 較大型或不可信 LAN 的設定選項
7.5.1 劃分位址空間來建立多個網路
7.5.2 透過主機、位址或埠範圍限制內部存取
7.6 小結 

Chapter 8 網路位址轉換
8.1 NAT 的概念背景
8.2 iptables 和 nftables 中的NAT 語義
8.2.1 來源位址 NAT
8.2.2 目的位址 NAT
8.3 SNAT 和私有 LAN 的例子
8.3.1 偽裝發往網際網路的 LAN 流量
8.3.2 對發往網際網路的 LAN 流量應用標準的 NAT
8.4 DNAT、LAN 和代理的例子
8.4.1 主機轉發
8.5 小結

Chapter 9 除錯防火牆規則
9.1 常用防火牆開發技巧
9.2 列出防火牆規則
9.2.1 iptables 中列出表的例子
9.2.2 nftables 中列出表的例子
9.3 直譯系統日誌
9.3.1 syslog 設定
9.3.2 防火牆日誌訊息：它們意謂著什麼
9.4 檢查開放埠
9.4.1 netstat -a [ -n -p -A inet ]
9.4.2 使用fuser 檢查一個綁定在特定埠的處理序
9.4.3 Nmap
9.5 小結

Chapter 10 虛擬專用網路
10.1 虛擬專用網路概述
10.2 VPN 協定
10.2.1 PPTP 和 L2TP
10.2.2 IPSec
10.3 Linux 和 VPN 產品
10.3.1 Openswan/Libreswan
10.3.2 OpenVPN
10.3.3 PPTP
10.4 VPN 和防火牆
10.5 小結

Part III iptables 和nftables 之外的事

Chapter 11 入侵檢測和響應
11.1 檢測入侵
11.2 系統可能遭受入侵時的症狀
11.2.1 體現在系統日誌中的跡象
11.2.2 體現在系統設定中的跡象
11.2.3 體現在檔案系統中的跡象
11.2.4 體現在用戶帳號中的跡象
11.2.5 體現在安全稽核工具中的跡象
11.2.6 體現在系統性能方面的跡象
11.3 系統被入侵後應採取的措施
11.4 事故報告
11.4.1 為什麼要報告事故
11.4.2 報告哪些類型的事故
11.4.3 向誰報告事故
11.4.4 報告事故時應提供哪些資訊
11.5 小結

Chapter 12 入侵檢測工具
12.1 入侵檢測工具包：網路工具
12.1.1 交換機和集線器以及您為什麼應該關心它
12.1.2 ARPWatch
12.2 Rootkit 檢測器
12.2.1 執行 Chkrootkit
12.2.2 當 Chkrootkit 報告電腦已被感染時應如何處理
12.2.3 Chkrootkit 和同類工具的侷限性
12.2.4 安全地使用 Chkrootkit
12.2.5 什麼時候需要執行 Chkrootkit
12.3 檔案系統完整性
12.4 日誌監控
12.4.1 Swatch
12.5 如何防止入侵
12.5.1 勤安防
12.5.2 勤更新
12.5.3 勤測試
12.6 小結

Chapter 13 網路監控和攻擊檢測
13.1 監聽乙太網
13.1.1 三個實用工具
13.2 TCPDump：簡單介紹
13.2.1 獲得並安裝 TCPDump
13.2.2 TCPDump 的選項
13.2.3 TCPDump 表達式
13.2.4 TCPDump 進階功能
13.3 使用 TCPDump 捕獲特定的協定
13.3.1 在現實中使用 TCPDump
13.3.2 透過 TCPDump 檢測攻擊
13.3.3 使用 TCPDump 記錄流量
13.4 使用 Snort 進行自動入侵檢測
13.4.1 獲取和安裝 Snort
13.4.2 設定 Snort
13.4.3 測試 Snort
13.4.4 接收警報
13.4.5 關於 Snort 的最後思考
13.5 使用 ARPWatch 進行監控
13.6 小結

Chapter 14 檔案系統完整性
14.1 檔案系統完整性的定義
14.1.1 實用的檔案系統完整性
14.2 安裝 AIDE
14.3 設定 AIDE
14.3.1 建立 AIDE 設定檔案
14.3.2 AIDE 設定檔案的範例
14.3.3 初始化 AIDE 資料庫
14.3.4 調度 AIDE 自動地執行
14.4 用 AIDE 監控一些壞事
14.5 清除 AIDE 資料庫
14.6 更改 AIDE 報告的輸出
14.6.1 獲得更詳細的輸出
14.7 在 AIDE 中定義巨集
14.8 AIDE 的檢測類型
14.9 小結

Appendix A 安全資源
A.1 安全資訊資源
A.2 參考資料和常見問題解答（FAQ）

Appendix B 防火牆範例與支援腳本
B.1 第 5 章為獨立系統建構的 iptables 防火牆
B.2 第 5 章中為獨立系統建構的 nftables 防火牆
B.3 第 6 章中經過最佳化的 iptables 防火牆
B.4 第 6 章的 nftables 防火牆
```

#
```

```
#
```
Linux iptables 速查手冊
作者： Gregor N. Purdy   譯者： 林長毅  歐萊禮    2004/10/15
觀念
　　應用
　　設定 iptables
　　連線追蹤
　　統計
　　網路位址轉譯（NAT）
　　來源位址轉譯（SNAT）與偽裝
　　目的位址轉譯（DNAT）
　　透明代理
　　負載均攤
　　乏態與具態防火牆
　　常用工具
　　iptables 命令參考
　　求助
　　iptables 的子命令
　　篩選條件與處置作為
　　工具命令參考
　　iptables-restore
```
