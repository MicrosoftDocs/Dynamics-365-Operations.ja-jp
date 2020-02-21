## <a name="mapping-tables"></a>テーブルのマッピング

### <a name="mapping-types"></a>マッピング タイプ

さまざまな異なるマッピング タイプがあります。 次の表は、テンプレート テーブルで使用される記号について説明します。

| 記号 | 説明 |
|--------|-------------|
| >  | 一方向 |
| >> | 一方向、データはプロセス内で変換されます。 |
| =  | 双方向 |
| >< | 双方向、データはプロセス内で変換されます。 |
| << | 一方向、データはプロセス内で変換されます。 |

### <a name="filters"></a>フィルター

ソースフィルタとリバースソースフィルタによって、どの行が同期されるかが決まります。

### <a name="default-values"></a>既定値

同期されたフィールドが Finance and Operations テーブルやその他の Dynamics 365 テーブルのいずれかに存在しない場合は、同期されたテーブルに既定の値が割り当てられます。 場合によっては、デフォルト値は、共通データモデル内の属性値へのルックアップである整数となります。 たとえば、共通データモデル の 取引先担当者 テーブルでは、 [**address1_addresstypecode**](../data-entities/dual-write/customer-mapping.md#customers-v3-to-contacts) の既定値は **3** です。 共通データモデルでは、 [address1AddressTypeCode](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/contact#address1AddressTypeCode) に対する **3** の値は **プライマリー アドレス** です。 
