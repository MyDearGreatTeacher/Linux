# nping 工具:
```
https://nmap.org/nping/
https://linux.die.net/man/1/nping
http://blog.sina.com.cn/s/blog_c02c69f10101gl27.html
```
```
Nping is an open source tool for network packet generation, response analysis and response time measurement. 
Nping can generate network packets for a wide range of protocols, allowing users full control over protocol headers. 

While Nping can be used as a simple ping utility to detect active hosts, 
it can also be used as a raw packet generator for network stack stress testing, 
ARP poisoning, Denial of Service attacks, route tracing, etc.

Nping's novel echo mode lets users see how packets change in transit between the source and destination hosts. 
That's a great way to understand firewall rules, detect packet corruption, and more.

Nping has a very flexible and powerful command-line interface that grants users full control over generated packets. 


Nping是一個用於生成網路包、分析響應和測量響應時間的開源工具。
Nping可以生成多種協定的網路資料包，可以讓使用者自由填充協定頭的欄位。
其不僅可以作為簡單的ping工具來檢測存活主機，還可以作為用於網路棧壓力測試的原始報文生成器、ARP攻擊、拒絕服務攻擊、路由跟蹤等。
Nping的新穎Echo mode可使使用者看到資料包在源主機和目標主機之間傳輸的過程中的變化情況，
其是獲悉防火牆規則、檢測資料包損壞等的非常好的方法。
```
### Nping的特性Nping's features
```
Nping有一個非常靈活和功能強大的命令列介面，使得使用者可以完全控制生成的資料包。

Nping的特性包括：
自訂的TCP，UDP，ICMP和ARP報文生成；
支援多個目標主機；
支援多目標埠；
對non-root使用者採用非特權模式；
Echo mode用於高級故障診斷和發現；
支援乙太網幀生成；
支持IPv6；
支援Linux、Mac OS和微軟Windows作業系統；
路由跟蹤能力；
高可定制；
免費和開源。
     Nping開始於2009年的“穀歌代碼之夏”專案，雖然它已經在很多方面使用，
     但它仍處於開發的早期階段，使得其可能包含很多bug，且一些功能還沒有實現

Nping's features include:

Custom TCP, UDP, ICMP and ARP packet generation.
Support for multiple target host specification.
Support for multiple target port specification.
Unprivileged modes for non-root users.
Echo mode for advanced troubleshooting and discovery.
Support for Ethernet frame generation.
Support for IPv6 (currently experimental).
Runs on Linux, Mac OS and MS Windows.
Route tracing capabilities.
Highly customizable.
Free and open-source.
```
### nping攻擊攻擊測試

攻擊指令:
```
nping --tcp-connect --rate=9000 - c 900000 --quiet 192.168.1.1 
```
命令說明:
```
--tcp-connect 使用tcp 連線模式進行攻擊，如果要加快發送速度，也可以改用--udp 。
--rate=9000 :每秒鐘發送9000 組封包，至於能不能產生9000 組封包，取決攻擊機的能力及網路頻寬。
-c 900000 : 重複執行這個動作900000 回。
--quiet 使用靜音模式，只顯示必要訊息。
```
