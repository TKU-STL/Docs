# Introduction to BIXS-V1.5: Hardware
![image](https://github.com/TKU-STL/Docs/blob/main/BIXS-V1.5/Picture/BIXS.jpeg)
## XBEE Pro 3
* 主要傳輸模組
* XCTU為其使用介面
* SMA 外螺內針
* 注意事項
    * 容易脫離轉接板導致使用異常，發射時可用膠帶捆住
    * 接上轉接板時須注意方向問題
- [購買網址](https://www.ruten.com.tw/item/show?21312138233975)

## XBee Explorer Dongle sparkfun
* 地面站所需轉接板
* 注意事項
    * 與電腦連接過久容易資料讀取異常，若有問題可先拔掉重新連接
- [購買網址](https://www.taiwaniot.com.tw/product/xbee-explorer-dongle/)

## YwRobot Studio XBEE 傳輸擴展板
* 腳位連接
    * RX腳位接Arduino TX腳位
    * TX腳位接Arduibo RX腳位
    * VCC接5V
    * GND接GND
- [購買網址](https://www.ruten.com.tw/item/show?22151558253582)

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
* 相關網址
    - [購買](https://www.taiwaniot.com.tw/product/9dof-imu-breakout-lsm9ds1-sparkfun/)
    - [Library](https://github.com/sparkfun/SparkFun_LSM9DS1_Arduino_Library)

## MicroSD 記錄模組 (GY-Openlog Cleanflight naze32 F3 blackbox)
* 腳位連接
    * RXI接Arduino TXI腳位
    * vcc接5v
    * GND接GND
* 儲存容量可到32G
* 注意事項
    * 第一次插入記憶卡上電後，內存卡上將生產config.txt文件
    * 發射前記得將前面測試的資料刪除
- [購買網址](https://www.taiwaniot.com.tw/product/gy-openlog-cleanflight-naze32-f3-blackbox-%E9%BB%91%E5%8C%A3%E5%AD%90-microsd-%E8%A8%98%E9%8C%84%E6%A8%A1%E7%B5%84-uart-%E9%80%9A%E8%A8%8A/)

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
* Vin可承受12V電壓
* 分別有3v, 5v輸出
* 確定連接正確再按下開關
* 注意事項
    * 正負極務必接對，否則有起火燃燒的可能
    * 使用三用電表測試時小心不要形成短路否則有起火燃燒的可能
* 淡水鴻吉電子材料行購買

