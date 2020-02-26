## <a name="fiscal-calendar-period-to-msdyn_fiscalcalendarperiods"></a>会計カレンダー期間を msdyn_fiscalcalendarperiods へ

このテンプレートは、Finance and Operations アプリと Common Data Service 間でデータを同期します。

Finance and Operations フィールド | タイプのマッピング | その他の Dynamics 365 フィールド | 既定値
---|---|---|---
COMMENTS | = | msdyn_comments | 
ENDDATE | = | msdyn_enddate | 
MONTH | >< | msdyn_month | 
CALENDAR | = | msdyn_fiscalcalendar.msdyn_calendar | 
QUARTER | >< | msdyn_quarter | 
SHORTNAME | = | msdyn_shortname | 
STARTDATE | = | msdyn_startdate | 
TYPE | >< | msdyn_fiscalperiodtype | 
PERIODNAME | = | msdyn_periodname | 
FISCALYEAR | = | msdyn_fiscalcalendaryear.msdyn_name | 
CALENDAR | = | msdyn_fiscalcalendaryear.msdyn_fiscalcalendarname | 
