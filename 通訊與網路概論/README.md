# 通訊與網路概論


## SISCO router 設定
<img src="./img/img-1.png">

### 指令目錄
<a href="#user-content--通用指令">通用指令</a> - <a href="#user-content--設定ip">設定ip</a> - <a href="#user-content--設定靜態路由ip">設定靜態路由ip</a> - <a href="#user-content--顯示路由ip">顯示路由ip</a> - <a href="#user-content--設定DGW">設定DGW</a> - <a href="#user-content--儲存狀態指令">儲存狀態指令</a>

### ※ 通用指令
| 指令   | 模式 | 解釋                                     |
| ------ | ---- | ---------------------------------------- |
| enable | >    | 進入Privileged Mode[#]                   |
| conf t | #    | 進入Global Configuration Mode[(config)#] |

### ※ 設定ip
| 指令               | 模式         | 解釋                        |
| ------------------ | ------------ | --------------------------- |
| interface [port]   | (config)#    | 進入Specific Interface Mode |
| ip add [ip] [mask] | (config-if)# | 設定interface的ip和mask     |
| no shutdown        | (config-if)# | 儲存設定                    |

### ※ 設定靜態路由ip
#### 靜態路由
| 指令                                | 模式      | 解釋                       |
| ----------------------------------- | --------- | -------------------------- |
| ip route [fIp網段] [fMask] [tIp]    | (config)# | 目標fIp網段的封包，丟向tip |
| no ip route [fIp網段] [fMask] [tIp] | (config)# | 移除該static條目           |

### ※ 顯示路由ip
| 指令          | 模式 | 解釋               |
| ------------- | ---- | ------------------ |
| show ip route | #    | 顯示連接路由ip表格 |

### ※ 設定OSPF
| 指令                                    | 模式             | 解釋                                  |
| --------------------------------------- | ---------------- | ------------------------------------- |
| router ospf [ProcessId]                 | (config)#        | 進入touter Mode(ProcessId設1)         |
| network [ip網段] [反向mask] area [area] | (config-touter)# | 設定OSPF IP (直連的都要設定，area設0) |
| no router ospf [ProcessId]              | (config)#        | 刪除該Process(裡面的ospf都會被刪掉)   |

### ※ 設定DGW
| 指令                    | 模式      | 解釋    |
| ----------------------- | --------- | ------- |
| ip default-gateway [ip] | (config)# | 設定DGW |

### ※ 顯示設定狀態
| 指令     | 模式 | 解釋         |
| -------- | ---- | ------------ |
| show run | #    | 顯示設定狀態 |

### ※ 儲存狀態指令
| 指令                               | 模式 | 解釋                     |
| ---------------------------------- | ---- | ------------------------ |
| sh running-config                  | #    | 儲存設定到running-config |
| copy running-config startup-config | #    | 儲存設定到startup-config |
| show ip route                      | #    | show route table         |