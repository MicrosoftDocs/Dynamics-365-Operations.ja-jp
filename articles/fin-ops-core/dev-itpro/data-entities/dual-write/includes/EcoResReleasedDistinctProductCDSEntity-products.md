## <a name="cds-released-distinct-products-to-products"></a>CDS リリース済の特徴的製品から製品へ

このテンプレートは、Finance and Operations アプリと Common Data Service 間でデータを同期します。

Finance and Operations フィールド | タイプのマッピング | その他の Dynamics 365 フィールド | 既定値
---|---|---|---
PRODUCTNUMBER | >> | msdyn_productnumber | 
PRODUCTNAME | >> | name | 
PRODUCTDESCRIPTION | >> | description | 
ITEMNUMBER | >> | msdyn_itemnumber | 
CURRENCYCODE | >> | transactioncurrencyid.isocurrencycode | 
SALESUNITSYMBOL | >> | defaultuomid.msdyn_symbol | 
SALESPRICE | >> | price | 
UNITCOST | >> | currentcost | 
PRODUCTTYPE | >> | producttypecode | 
SALESUNITDECIMALPRECISION | >> | quantitydecimal | 0
ISCATCHWEIGHTPRODUCT | >> | msdyn_iscatchweight | 
PRODUCTCOLORID | >> | msdyn_productcolor.msdyn_productcolorname | 
PRODUCTCONFIGURATIONID | >> | msdyn_productconfiguration.msdyn_productconfiguration | 
PRODUCTSIZEID | >> | msdyn_productsize.msdyn_productsize | 
PRODUCTSTYLEID | >> | msdyn_productstyle.msdyn_productstyle | 
