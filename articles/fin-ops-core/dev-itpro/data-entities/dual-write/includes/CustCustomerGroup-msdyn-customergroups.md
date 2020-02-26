## <a name="customer-groups-to-msdyn_customergroups"></a>顧客グループを msdyn_customergroups へ

このテンプレートは、Finance and Operations アプリと Common Data Service 間でデータを同期します。

Finance and Operations フィールド | タイプのマッピング | その他の Dynamics 365 フィールド | 既定値
---|---|---|---
CUSTOMERGROUPID | = | msdyn_groupid | 
DESCRIPTION | = | msdyn_description | 
ISSALESTAXINCLUDEDINPRICE | >< | msdyn_issalestaxincludedinprice | 
PAYMENTTERMID | = | msdyn_paymenttermid.msdyn_name | 
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn_clearingperiodpaymenttermname.msdyn_name | 
