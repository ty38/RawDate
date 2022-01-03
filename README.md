# RawDate
Query Sumarry

SELECT SupplierID,SupplierName,SUM(TotalPrice) AS TotalPrice, SUM(IF (MONTH(PurchaseDate) = 10, Qty*PriceEach,0)) AS Oct, SUM(IF (MONTH(PurchaseDate) = 11, Qty*PriceEach,0)) AS Nov, SUM(IF (MONTH(PurchaseDate) = 12, Qty*PriceEach,0)) AS Des FROM tb_raw GROUP BY SupplierID
