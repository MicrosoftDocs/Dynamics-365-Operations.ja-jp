## <a name="currencies-to-transactioncurrencies"></a>通貨を transactioncurrencies へ

このテンプレートは、Finance and Operations アプリと Common Data Service 間でデータを同期します。

ソース フィルター: ((CURRENCYCODE != "999"))

Finance and Operations フィールド | タイプのマッピング | その他の Dynamics 365 フィールド | 既定値
---|---|---|---
CURRENCYCODE | = | isocurrencycode | 
NAME | = | currencyname | 
SYMBOL | = | currencysymbol | 
なし | >> | exchangerate | 1
