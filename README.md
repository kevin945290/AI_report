# Google Colab－零成本玩轉深度學習
## 前言
最近在學深度學習HyperLPR計畫時，由於一直沒有比較合適的設備訓練深度學習的模型，所以在網上想找到提供模型訓練，經過一段時間的搜索，最終發現了一個谷歌的產品--Google Colaboratory。它幾乎可以實現零成本玩深度學習，達到快速訓練模型的目的。  

Google Colaboratory是Google開放的一款深度學習的研究工具，主要用於深度學習的開發和研究。這款工具現在可以免費使用，但暫時還是無法確定是不是永久免費。 Google Colab最大的好處是給了廣大的AI開發者免費的GPU和TPU使用！ GPU型號是Tesla K80！你可以在上面輕鬆地跑例如：Keras、Tensorflow、Pytorch等框架。

## Google Colab基本操作
網站:[Google Colab](https://colab.research.google.com/)  
進入Google Colab網站-> 歡迎使用 Colab
![image](https://github.com/kevin945290/AI_report/blob/main/1.png)

修改檔名，並點選"+程式碼"新增程式碼區塊
![image](https://github.com/kevin945290/AI_report/blob/main/2.png)

現在，我們就可以在程式碼框中輸入一些程式碼。這裡注意，如果我們直接輸入程式碼，系統就會當作Python程式碼執行。例如我們輸入：  
a = 1  
print(a)  
運行之後輸出框中會列印出"1"。
![image](https://github.com/kevin945290/AI_report/blob/main/3.png)

如果想去執行系統指令，只需要在指令前加感嘆號!。例如我們輸入：  
!ls  
![image](https://github.com/kevin945290/AI_report/blob/main/4.png)

## 前期配置
修改筆記本環境
![image](https://github.com/kevin945290/AI_report/blob/main/5.png)

硬件類型從CPU改成GPU
![image](https://github.com/kevin945290/AI_report/blob/main/6.png)

連接Google drive:首先在儲存格中輸入並執行以下命令，會出現2次校驗
![image](https://github.com/kevin945290/AI_report/blob/main/7.png)

會發現上面的程式碼的授權網站無法進入,因為版本過舊
![image](https://github.com/kevin945290/AI_report/blob/main/8.png)

掛載Google Drive程式碼：
![image](https://github.com/kevin945290/AI_report/blob/main/9.png)

會發現上面的程式碼的授權網站也無法進入
![image](https://github.com/kevin945290/AI_report/blob/main/A.png)

所以改用其他方式，一開始沒掛載雲端，如圖:
![image](https://github.com/kevin945290/AI_report/blob/main/B.png)

所以我們用了最新版本的掛載雲端方式，載入成功之後在左邊的檔案中多了一個dirve資料夾，如下圖:
![image](https://github.com/kevin945290/AI_report/blob/main/C.png)

掛載完後，我們可以用命令"!ls"查看
![image](https://github.com/kevin945290/AI_report/blob/main/D.png)

## 更改工作目錄
在Colab中cd指令是無效的，切換工作目錄使用chdir函數，執行完後，目前工作目錄會進入drive資料夾下。我們再使用!ls指令會發現系統輸出的是drive資料夾下的目錄
![image](https://github.com/kevin945290/AI_report/blob/main/E.png)

用" os.chdir('../') "，可回到上級目錄，執行完後，目前工作目錄會回到上級目錄。之後我們再使用!ls指令來觀察
![image](https://github.com/kevin945290/AI_report/blob/main/F.png)

## 運行自己的程式碼
### 1. 將.py檔案和其它必要的檔案上傳到Google Drive
![image](https://github.com/kevin945290/AI_report/blob/main/G.png)

### 2. 將工作目錄切換到.py檔案所在目錄
![image](https://github.com/kevin945290/AI_report/blob/main/H.png)

### 3. 運行程式碼
![image](https://github.com/kevin945290/AI_report/blob/main/I.png)

### 4. 注意事項  
Linux系統下檔案路徑使用'/'而不是'\'  

## 總結
1.可以把Google Colab看成是一台有GPU或TPU的Ubuntu虛擬機，只不過我們只能用命令列的方式操作它。你可以選擇執行系統指令，也可以直接寫執行python程式碼。  
2. 掛載完Google Drive，會在虛擬機器裡產生一個drive資料夾，直接將Google Drive當成是一塊硬碟即可。存取drive資料夾裡的文件，就是在存取你的Google Drive裡的文件。  
3. Colab最多連續使用12小時，超過時間系統會強制掐斷正在運作的程式並收回佔用的虛擬機器。 （好像再次連接到虛擬機器後，虛擬機器是被清空的狀態，需要重新配置和安裝庫等等）


