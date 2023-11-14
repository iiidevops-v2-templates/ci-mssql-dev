## Microsoft SQL Server Linux 2019
:warning: 此範本為開發用資料庫，不包含master、slave以及headless svc，請勿作為Production使用  
:information_source: 資料庫資料不提供儲存功能， 因此若本專案有任何commit更動都會導致原本的資料庫資料遺失，請commit前一定要注意(這資料庫並無掛載volume，因此無法救回)。

## 取出及管理資料庫資料
若在開發過程中想要將目前的資料庫資料匯入或取出, 請使用支援 SQL Server 的工具程式處理 Exp. [HeidiSQL](https://www.heidisql.com/)

## 支援自動讀入.sql匯入語法
##### sql範例檔位於：專案根目錄底下的 db/test.sql.sample，如果要自動匯入此範本資料庫內容，將檔案後綴的.sample刪除即可

##### 以下是腳本中進行的主要操作：

##### 建一個名為[test]的資料庫，並在該資料庫中創建一個名為Users的表格，該表格包含一個自動增量的主鍵（UserId）。
##### 請注意，這只是一個簡單的範例。您可以根據實際需要修改表格結構和插入的數據。

## 資料庫連結獲取方式 及 簡易驗證方式
##### 刪除檔案後綴的.sample，或是上傳.sql檔至專案內的db資料夾中，平台即會偵測到變更並觸發自動化CI流程，待pipeline完成後，可在實證環境得到連線資料，可以使用各式支援MSSQL工具連線，例如：HeidiSQL、DBeaver、SQLite Database Browser，
##### 以下使用HeidiSQL為例示範：
![image](https://i.imgur.com/L5h9gxR.png)
##### 可以查詢到匯入的test資料庫及Users表格：
![image](https://i.imgur.com/5xd0v6e.png)