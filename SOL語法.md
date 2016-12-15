# SOL語法

### 修改表格的欄位 - ALTER TABLE

```
ALTER TABLE "table_name"
[改變方式];
```

###### 增加欄位

在資料庫**[3GPlatform]**的表格**[DevReqCommand]** 中增加欄位**[istarTime]**，種類為**[int]**

```
Go
ALTER TABLE [3GPlatform].[DevReqCommand] 
   ADD [istarTime] [int]  NULL
ALTER TABLE [3GPlatform].[DevReqCommand] 
   ADD [iendTime] [int]  NULL 
Go
```





------

### 刪除資料 - DELETE FROM

```
DELETE FROM "表格名"
WHERE "條件";
```

在資料庫**[3GPlatform]**的表格**[DevReqCommand]**中的**EventTime**欄位刪除**'2016-11-22 07:44:00.000'**的資料

```
DELETE FROM [3GPlatform].[dbo].[DevReqCommand]
WHERE EventTime = '2016-11-22 07:44:00.000';
```



------

### 插入資料 - INSERT INTO

```
INSERT INTO "表格名" ("欄位1", "欄位2", ...)
VALUES ("值1", "值2", ...);
```

在資料庫**[3GPlatform]**的表格**[DevReqCommand]**中的欄位插入對應的數值

```
INSERT INTO [3GPlatform].[dbo].[DevReqCommand] (DeviceID,EventTime,EventType,Channel,AddAudio,StartTime,EndTime,Dev_TimeBase)
VALUES( 10, '2016-11-22 07:44:00.000', 2, 1, 0,  '2016-11-22 07:43:45.000', '2016-11-22 07:44:15.000',  3600 )
```

```
INSERT INTO [3GPlatform].[dbo].[DevEventListlog](DeviceID,Device_SN,EventTime,EventType,Latitude,Longitude,Speed,GSensor_X,GSensor_Y,GSensor_Z)
VALUES(10, 'KL000735', '2016-11-22 07:44:00.000', 2, 0.0, 0.0, 0, -0.5, -0.06, -0.9)
```





