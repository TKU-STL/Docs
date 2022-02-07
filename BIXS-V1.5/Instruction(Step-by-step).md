# BIXS-V1.5 安裝流程
#### Step1: 將 Arduino UNO 與電腦連線

#### Step2: 打開 VScode 點選功能列中的Terminal

#### Step3: 在 Terminal 輸入 "```cd``` + 程式碼要存放的目錄"
#### 範例碼 
```
cd \User\Desktop
```

#### Step4: 在 Terminal 輸入 "```git clone``` + BIXS-Arduino-V1程式碼網址" 將 [BIXS-Arduino-V1](https://github.com/TKU-STL/BIXS-Arduino-V1) 程式碼下載至指定目錄
#### 範例碼 
```
git clone https://github.com/TKU-STL/BIXS-Arduino-V1
```

#### Step5: Ctrl+Shift+P 開啟 Command Palette 輸入 "```PlatformIO: Home```" 開啟PlatformIO介面

#### Step6: 點選 Open Project 選擇開啟剛剛下載的BIXS-Arduino-V1資料夾

#### Step7: Ctrl+Shift+P 開啟 Command Palette 輸入 "```PlatformIO: Build```" 確認程式是否Success

#### Step8: Ctrl+Shift+P 開啟 Command Palette 輸入 "```PlatformIO: Upalod```" 將程式燒入 Arduino UNO(成功會顯示Success)

#### Step8: 在 Command Palette 輸入 "PlatformIO: Upload" 將程式燒入 Arduino UNO(成功會顯示Success)

#### Step9: 先在麵包板進行接線測試零件是否正常運作，詳細圖片參照以下附圖
![image](https://github.com/TKU-STL/Docs/blob/main/BIXS-V1.5/Picture/BIXS.jpeg)

#### Step10: 將SD卡中除了config.txt之外的檔案刪除後插入記憶模組

#### Step11: 開啟 BIXS-V1.5 的電源

#### Step12: 打開XCTU 並將Xbee接收端插上電腦

#### Step13: 點選Discover radio devices 並點選對應的 port 然後按下 Finish(搜尋到裝置後會顯示在左側 Radio Modules之下)

#### Step14: 在Radio Modules選擇裝置後點開Configuration 確認設定是否正確(詳細設定請參照 Hardware.md)

#### Step15: 點選Consoles然後點選Open，若有資料傳入表示兩個Xbee成功連接

#### Step16: 確認在 XCTU 上傳入的資料是否合理
    1.BMP180高度
    2.IMU三軸中與重力加速度同向的加速度值      

#### Step17: 將BIXS-V1.5斷電後取出SD卡，確認其中的資料是否與Xbee回傳的資料相符

#### Step18: 確認零件都正常運作後，將零件焊上PCB

#### Step19: 重複 Step10~17

#### Step20: BIXS-V1.5安裝完成
