# Crontab指令

## 1. Linux Cron 指令

    crontab -l    列出該使用者擁有的 crontab 指令

    crontab -e   編輯該使用者的 crontab 指令

    crontab -r    將使用者的 crontab 全部清除！（ 小心使用 ）

    crontab -u   改變排程的執行身分: crontab -u user filename


## 2.編寫方法

基本上，我們只需要按照『分鐘』、『小時』、『日期』、『月份』、『星期』五個欄位輸入，最後加上 command 即可。 


分鐘： 0-59
小時： 0-23
日期： 1-31
月份： 1-12
星期： 0-6
* 代表任意。

比如說我有個想要執行的 test.sh 檔，然後我希望每天凌晨十二點都可以執行一次，那麼我就要寫下以下指令：
```
* 0 * * * sh /home/clay/test.sh
```
如果我有個 test.py 的 Python 程式希望可以每 5 分鐘執行一次，那麼我可以寫下：
```
*/5 * * * python3 /home/clay/test.py
```
最好使用『絕對路徑』來指向要執行的檔案比較好哦。


## 設定預設開啟軟體
```
export VISUAL=vim
export EDITOR=vim
```