# Introduction to BIXS-V1.5: Hardware
![image](https://github.com/TKU-STL/Docs/blob/main/BIXS-V1.5/Picture/BIXS.jpeg)
## XBEE Pro 3
* 主要傳輸模組
* XCTU為其使用介面
* SMA 外螺內針
* 注意事項
    * 容易脫離轉接板導致使用異常，發射時可用膠帶捆住
    * 接上轉接板時須注意方向問題
## XBee Explorer Dongle sparkfun
* 地面站所需轉接板
* 注意事項
    * 與電腦連接過久容易資料讀取異常，若有問題可先拔掉重新連接
## YwRobot Studio XBEE 傳輸擴展板
* 腳位連接
    * RX腳位接Arduino TX腳位
    * TX腳位接Arduibo RX腳位
    * VCC接5V
    * GND接GND
## 九軸IMU (SparkFun LSM9DS1)
* 可測量數據
    * 3軸加速度 (刻度可設置為±2,4,8,16 g)
    * Roll, Pitch, Yaw (支援±245,500,2000°/ s)
    * 3軸磁力 (標度範圍±4,8,12,16高斯)
* 腳位連接
    * SCL接Arduino SCL腳位
    * SDA接Arduino SDA腳位
    * VCC接3.3v
    * GND接GND
* 注意事項
    * 儀器上有標示x/y/z軸方向
## MicroSD 記錄模組 (GY-Openlog Cleanflight naze32 F3 blackbox)
* 腳位連接
    * RXI接Arduino TXI腳位
    * vcc接5v
    * GND接GND
* 儲存容量可到32G
* 注意事項
    * 第一次插入記憶卡上電後，內存卡上將生產config.txt文件
    * 發射前記得將前面測試的資料刪除
## BMP180
* 高度計
* 腳位連接
    * SDA接A4
    * SCL接A5
    * VIN接3.3v
    * GND接GND
* 注意事項
    * 根據經驗此儀器壞掉機率較高，焊接時加熱時間盡量減短
    * 此儀器為氣壓型高度計，需測量到外界氣壓才會是準確的高度




## 分電盤

