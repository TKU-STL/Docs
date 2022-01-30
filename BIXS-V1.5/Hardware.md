# Introduction to BIXS-V1.5: Hardware
![image](https://github.com/TKU-STL/Docs/blob/main/BIXS-V1.5/Picture/BIXS.jpeg)
## Arduino UNO
* 系統機載電腦
* 供電
    * 可透過USB連接埠、電源輸入插座、Vin腳位提供電源
    * 供應的電壓限制為6V至20V (建議輸入7V-12V)
* 本次任務用到的腳位有SDA, SCL, A4, A5, Vin, GND, RX0, TX0
* RESET
    * 當程式執行有問題時，可按reset鈕重新執行燒錄程式
* 注意事項
    * 進行燒錄時記得先將RX, TX腳位斷開以防燒錄失敗
## XBEE Pro 3
* 主要傳輸模組
* XCTU為其使用介面
* SMA 外螺內針
* 注意事項
    * 容易脫離轉接板導致使用異常，發射時可用膠帶捆住
    * 接上轉接板時須注意方向問題
- [購買網址](https://www.ruten.com.tw/item/show?21312138233975)
### 設定
<img src="https://github.com/TKU-STL/Docs/blob/main/BIXS-V1.5/Picture/messageImage_1643524873609.jpg" alt="Cover" width="80%"/></div>

* 發送端(ROUTER或END_DEVICE)
   * ID:數字隨意但需跟接收端一樣
   * JV:Enabled[1]
   * CE:不動(Join Network[0])
   * DH:0
   * DL:0
   * NI:自取(英文)
   * SP:1F4 ->定義睡眠花費時間(可以不設定此項)
* 接收端(COORDINATOR)
   * ID:數字隨意但需跟發送端一樣
   * JV:不動
   * CE: Enabled[1](Form Network[1]) ->將此XBEE設為coordinator
   * DH:不動，有改的話發送端也要改
   * DL:不動，有改的話發送端也要改
   * NI:自取(預設的空白刪乾淨)
   * SP:1F4 ->定義睡眠花費時間(可以不設定此項)

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
    * 盡量與航電艙保持水平
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
- [購買網址](https://shopee.tw/product/10708564/4655497306?smtt=0.4892717-1643482313.9)

## 分電盤
* Vin可承受12V電壓
* 分別有3v, 5v輸出
* 確定連接正確再按下開關
* 注意事項
    * 正負極務必接對，否則有起火燃燒的可能
    * 使用三用電表測試時小心不要形成短路否則有起火燃燒的可能
* 淡水鴻吉電子材料行購買

## 天線
* 地面站
    * SMA定向平板天線
    * 增益值:14DBi
    * 支援頻率:2.4GHz
* 發送端
    * SMA內螺內孔全向增益雙頻天線
    * 增益值:6DBi
    * 支援頻率:2.4/5GHz
    * 長度:19.5cm
* 注意事項
    * 定向天線須隨時面向發送端指向位置以確保資料傳輸完整
* 購買網址
    - [平板天線](https://www.ruten.com.tw/item/show?21901449881377)
    - [發送端](https://www.ruten.com.tw/item/show?21615456125288)

## SMA頭饋線
* 天線延長線，根據任務所需挑選長度
* 注意事項
    * 購買前務必確認接頭是否符合(內螺內孔+外螺內針)
    * 若是無法搭配可使用轉接頭
* 光華商場購買(訂製)

## 4w 2.4G功率放大器
* 加強地面站訊號接收，增加傳輸最遠距離
* 一頭接平板天線，一頭接XBEE
* 需電池供電，連接成功時指示燈亮起(可用3s 11.1V電池)
* 購買網址
    - [功率放大器](https://www.ruten.com.tw/item/show?22139393914871)
    - [3s電池](https://www.ruten.com.tw/item/show?22140462188749)
    
## PCB
* 需先畫好線路圖再送廠商打樣
* 送出前記得反覆確認線路及開洞位置正確
- [購買網址](https://www.ruten.com.tw/item/show?21928008865324)

