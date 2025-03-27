# Laravel 12 攔截並收集印出給定的變數呼叫並將其顯示在專用終端機視窗中

引入 soloterm 的 dumps 套件來擴增攔截並收集印出給定的變數呼叫並將其顯示在專用終端機視窗中，這樣就無需使用偵錯輸出來擾亂您的瀏覽器或應用程式介面回應。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令的 __solo:dumps__ 來執行一個攔截所有印出給定的變數呼叫的伺服器啟動。
```sh
$ php artisan solo:dumps
```

----

## 畫面截圖
![](https://i.imgur.com/Wrkmhia.png)
> 進入 **Tinker** 環境，印出給定的變數

![](https://i.imgur.com/0uOSTry.png)
> 輸出將被傳送到此終端機視窗
