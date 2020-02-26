## <a name="withholding-tax-codes-to-msdyn_withholdingtaxcodes"></a>源泉徴収税コードを msdyn_withholdingtaxcodes へ

このテンプレートは、Finance and Operations アプリと Common Data Service 間でデータを同期します。

Finance and Operations フィールド | タイプのマッピング | その他の Dynamics 365 フィールド | 既定値
---|---|---|---
WITHHOLDINGCODE | = | msdyn_name | 
WITHHOLDINGTAXNAME | = | msdyn_description | 
WITHHOLDINGTAXROUNDOFF | = | msdyn_roundoff | 
WITHHOLDINGTAXROUNDOFFTYPE | >< | msdyn_roundofftype | 
CURRENCYCODEID | = | msdyn_currency.isocurrencycode | 
WITHHOLDINGTAXBASE | >< | msdyn_taxableamountorigin | 
