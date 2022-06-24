---
title: 航海作成エンティティ
description: この記事では、航海作成データ エンティティに関する情報を提供します。これは作業航海を作成する際に必要なデータ エンティティをグループ化します。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: cb2e2f53942015caf9462692515f24deb9689aed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873901"
---
# <a name="voyage-creation-entities"></a>航海作成エンティティ

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

航海作成データ エンティティは、作業航海を作成する際に必要なデータ エンティティをまとめてグループ化します。 ユーザーまたはユーザーの配送業者は、これらのデータ エンティティを使用して、既存の購入者注文や移動オーダー明細行を参照する、航海、出荷コンテナー、フォリオ、航海明細行のレコードを作成できます。

## <a name="voyages-itmtableentity"></a>航海 (ITMTableEntity)

航海は入荷品の移動を表し、陸揚原価の最高レベルの原価領域として機能します。 これは、船舶、出発港、行先港に関連するヘッダー レベルの情報を含みます。 `ITMTableEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 配送方法 | ITMTable.DlvModeId | Nvarchar(10) | 無効 | 無効 |
| ブローカーのアドバイス | ITMTable.ITMBrokerAdvised | 日時 | 無効 | 無効 |
| 顧客の予定 | ITMTable.ITMCustomerAppointment | 日時 | 無効 | 無効 |
| 倉庫で出荷 | ITMTable.ITMDelAtWarehouse | 日時 | 無効 | 無効 |
| 出荷指示 | ITMTable.ITMDeliveryInstructions | 日時 | 無効 | 無効 |
| 出発日 | ITMTable.ITMDepartureDate | 日時 | 無効 | 無効 |
| リリースされた商品 | ITMTable.ITMGoodsReleased | 日時 | 無効 | 無効 |
| 現地輸送日 | ITMTable.ITMLocalTransportDate | 日時 | 無効 | 無効 |
| 現地輸送時刻 | ITMTable.ITMLocalTransportTime | Int | 無効 | 無効 |
| 元の船荷証券が送信されました | ITMTable.ITMOriginalBOLSebt | 日時 | 無効 | 無効 |
| 元のドキュメントを受領しました | ITMTable.ITMOriginalDocsReceived | 日時 | 無効 | 無効 |
| 発注書のステータス | ITMTable.ITMPurchStatus | Int | 無効 | 無効 |
| 確認日 | ITMTable.ITMVerificationDate | 日時 | 無効 | 無効 |
| 関税エントリ識別子 | ITMTable.ShipCustomsEntryId | Nvarchar(20) | 無効 | 無効 |
| 出荷日 | ITMTable.ShipDate | 日時 | 無効 | 無効 |
| Description | ITMTable.ShipDescription | Nvarchar(60) | 無効 | 無効 |
| ドキュメント受領 | ITMTable.ShipDocReceived | Int | 無効 | 無効 |
| 推定出荷日 | ITMTable.ShipEstDlvDate | 日時 | 無効 | 無効 |
| 出荷港での ETA | ITMTable.ShipEstPortDate | 日時 | 無効 | 無効 |
| 出荷元港 | ITMTable.ShipFromPort | Nvarchar(20) | 無効 | 無効 |
| 航空貨物運送/船荷証券の保管 | ITMTable.ShipHAWB | Nvarchar(20) | 無効 | 無効 |
| 航海 | ITMTable.ShipId | Nvarchar(20) | **有** | **有** |
| 予約参照番号 | ITMTable.ShipIdExternal | Nvarchar(20) | 無効 | 無効 |
| 輸送テンプレート | ITMTable.ShipJourneyId | Nvarchar(20) | 無効 | 無効 |
| 現地配送業者 | ITMTable.ShipLocalForwarder | Nvarchar(20) | 無効 | 無効 |
| マスター航空貨物運送/船荷証券 | ITMTable.ShipMAWB | Nvarchar(20) | 無効 | 無効 |
| 測定 | ITMTable.ShipMeasurement | Numeric(32, 6) | 無効 | 無効 |
| 測定単位 | ITMTable.ShipMeasurementUnit | Int | 無効 | 無効 |
| パレット数 | ITMTable.ShipNoOfPallets | Int | 無効 | 無効 |
| 保留中の航海 | ITMTable.ShipPending | Int | 無効 | 無効 |
| 備考 | ITMTable.ShipRemarks | Nvarchar(MAX) | 無効 | 無効 |
| レンタル | ITMTable.ShipRental | Int | 無効 | 無効 |
| 航海状態 | ITMTable.ShipStatusId | Nvarchar(20) | 無効 | 無効 |
| 数値の一致 | ITMTable.ShipTallyInNumber | Nvarchar(20) | 無効 | 無効 |
| 出荷先港 | ITMTable.ShipToPort | Nvarchar(20) | 無効 | 無効 |
| 評価日 | ITMTable.ShipValuationDate | 日時 | 無効 | 無効 |
| 出荷会社 | ITMTable.ShipVendAccount | Nvarchar(20) | 無効 | 無効 |
| 船舶 | ITMTable.ShipVesselId | Nvarchar(20) | 無効 | **有** |
| 外部航海 ID | ITMTable.ShipVoyage | Nvarchar(20) | 無効 | 無効 |

### <a name="number-sequences-for-voyages"></a>航海の番号順序

航海の共有番号順序によって、航海 ID の割り当てを制御します。

**航海 ID** (`ShipId`) 値としてデータ エンティティに渡す値は、更新する既存のレコードの識別に使用します。 そのレコードが存在しない場合は、手動入力を許可するように割り当て済みの番号順序を構成しているかどうかによって動作が異なります。

- 手動入力が有効である場合、渡された値を使用する新しいレコードが作成されます。
- 手動入力が有効でない場合、渡された値の代わりに、割り当て済みの番号順序が含む次の番号を使用します。

航海 ID としてインポートしたプレースホルダー値は、インポート セッション中に保持されます。 この動作によって、プレースホルダーを参照する出荷コンテナーと航海明細行を航海に確実に含ませ、番号順序から割り当てた値を反映するように、それらを更新できます。

### <a name="automatic-cost-transactions"></a>自動原価トランザクション

Microsoft Dynamics 365 Supply Chain Management の **自動原価** ページから、自動原価を航海に追加できます (**陸揚原価 \> 原価計算 \> 自動原価**)。 また、自動原価のレコードは、陸揚原価が対応する各原価領域に対して 。原価トランザクション データ エンティティを使用して作成することもできます。

Supply Chain Management で構成した自動原価は、航海明細行の作成時に航海に適用されます。 ヘッダー レコードを明細行情報に関連付けるまで、レコードに対するコストは表示されません。

## <a name="shipping-containers-itmcontainersentity"></a>出荷コンテナー (ITMContainersEntity)

出荷コンテナーは、商品を輸送する物理的なコンテナーを表します。 この物理的なコンテナーは、海上輸送の輸送コンテナーまたは航空輸送の単一パレットである可能性があります。 出荷コンテナーは、出荷コンテナー ID、シール番号、出荷コンテナー タイプに関連するヘッダー レベルの情報を含みます。 (出荷コンテナー タイプは寸法情報を提供します。) `ITMContainersEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 出発日 | ITMContainers.ITMDepartureDate | 日時 | 無効 | 無効 |
| 現地輸送日 | ITMContainers.ITMLocalTransportDate | 日時 | 無効 | 無効 |
| 現地輸送時刻 | ITMContainers.ITMLocalTransportTime | Int | 無効 | 無効 |
| 元の航海 | ITMContainers.OrigShipId | Nvarchar(20) | 無効 | 無効 |
| 実重量 | ITMContainers.ShipActualWeight | Numeric(32, 6) | 無効 | 無効 |
| ブローカーのアドバイス | ITMContainers.ShipBrokerAdvised | 日時 | 無効 | 無効 |
| 出荷コンテナー | ITMContainers.ShipContainerId | Nvarchar(20) | **有** | **有** |
| 出荷コンテナー タイプ | ITMContainers.ShipContainerTypeId | Nvarchar(20) | 無効 | 無効 |
| 単位タイプ | ITMContainers.ShipContainerUnitTypeId | Nvarchar(10) | 無効 | 無効 |
| レンタルに変換済 | ITMContainers.ShipConvertedToRental | Int | 無効 | 無効 |
| 顧客の予定 | ITMContainers.ShipCustomerAppointment | 日時 | 無効 | 無効 |
| 出荷日 | ITMContainers.ShipDate | 日時 | 無効 | 無効 |
| 倉庫で出荷 | ITMContainers.ShipDelAtWarehouse | 日時 | 無効 | 無効 |
| 出荷指示 | ITMContainers.ShipDeliveryInstructions | 日時 | 無効 | 無効 |
| 試験証明書適用日 | ITMContainers.ShipECAppliedDate | 日時 | 無効 | 無効 |
| 試験証明書有効期限 | ITMContainers.ShipECExpiryDate | 日時 | 無効 | 無効 |
| 試験証明書番号 | ITMContainers.ShipECNum | Nvarchar(20) | 無効 | 無効 |
| 試験証明書受領日 | ITMContainers.ShipECReceivedDate | 日時 | 無効 | 無効 |
| 推定出荷日 | ITMContainers.ShipEstDlvDate | 日時 | 無効 | 無効 |
| 出荷港での ETA | ITMContainers.ShipEstPortDate | 日時 | 無効 | 無効 |
| 積込予定日 | ITMContainers.ShipExpectedLoadingDate | 日時 | 無効 | 無効 |
| 出荷元港 | ITMContainers.ShipFromPort | Nvarchar(20) | 無効 | 無効 |
| 商品の説明 | ITMContainers.ShipGoodsDesc | Nvarchar(60) | 無効 | 無効 |
| リリースされた商品 | ITMContainers.ShipGoodsReleased | 日時 | 無効 | 無効 |
| GPS トラッカー ユニット | ITMContainers.ShipGPSUnit | Nvarchar(30) | 無効 | 無効 |
| 航空貨物運送/船荷証券の保管 | ITMContainers.ShipHAWB | Nvarchar(20) | 無効 | 無効 |
| 航海 | ITMContainers.ShipId | Nvarchar(20) | **有** | **有** |
| 輸送テンプレート | ITMContainers.ShipJourneyId | Nvarchar(20) | 無効 | 無効 |
| 現地配送業者 | ITMContainers.ShipLocalForwarder | Nvarchar(20) | 無効 | 無効 |
| 測定 | ITMContainers.ShipMeasurement | Numeric(32, 6) | 無効 | 無効 |
| 測定単位 | ITMContainers.ShipMeasurementUnit | Int | 無効 | 無効 |
| カートン数 | ITMContainers.ShipNoOfCartons | Numeric(32, 6) | 無効 | 無効 |
| 元の船荷証券が送信されました | ITMContainers.ShipOriginalBOLSebt | 日時 | 無効 | 無効 |
| 元のドキュメントを受領しました | ITMContainers.ShipOriginalDocsReceived | 日時 | 無効 | 無効 |
| シール番号 | ITMContainers.ShipOurSealNum | Nvarchar(20) | 無効 | 無効 |
| 使用済 | ITMContainers.ShipPendingUsed | Int | 無効 | 無効 |
| 発注書のステータス | ITMContainers.ShipPurchStatus | Int | 無効 | 無効 |
| 冷却タイプ | ITMContainers.ShipRefrigerationTypeId | Nvarchar(10) | 無効 | 無効 |
| 備考 | ITMContainers.ShipRemarks | Nvarchar(MAX) | 無効 | 無効 |
| レンタル | ITMContainers.ShipRental | Int | 無効 | 無効 |
| 返品可能 | ITMContainers.ShipReturnable | Int | 無効 | 無効 |
| 航海状態 | ITMContainers.ShipStatusId | Nvarchar(20) | 無効 | 無効 |
| 出荷会社シール番号 | ITMContainers.ShipTheirSealNum | Nvarchar(20) | 無効 | 無効 |
| 出荷先港 | ITMContainers.ShipToPort | Nvarchar(20) | 無効 | 無効 |
| 確認日 | ITMContainers.ShipVerificationDate | 日時 | 無効 | 無効 |
| 船舶 | ITMContainers.ShipVesselId | Nvarchar(20) | 無効 | **有** |

### <a name="voyage-id-validation"></a>航海 ID の検証

番号順序は出荷コンテナー ID を制御しません。 それは、使用された航海のコンテキストでのみ一意です。

出荷コンテナー エンティティ (`ITMContainersEntity`) を航海エンティティ (`ITMTableEntity`) から独立して使用する場合、**航海 ID** (`ShipId`) 値を航海テーブルの既存のレコードと一致させる必要があります。 そうしない場合はインポートが失敗します。

出荷コンテナー エンティティ (`ITMContainersEntity`) と航海エンティティ (`ITMTableEntity`) を同じインポート セッションの一部として使用する場合、出荷コンテナーの前に航海エンティティを作成する必要があります。 そうしない場合は、**航海 ID** (`ShipId`) の値を正常に検証できません。 **航海 ID** (`ShipId`) 値にプレースホルダー値を使用する場合、同じプレースホルダーを出荷コンテナー エンティティの **航海 ID** (`ShipId`) 値として使用する場合にのみ、関連付けを作成できます。

### <a name="other-field-validations"></a>その他のフィールド検証

次の表は、陸揚原価設定テーブルに対して検証する出荷コンテナー テーブル (`ITMContainers`) が含むフィールドを示します。 さらに、既存の値を読み取り、有効な値を環境で確実に受け取れるように配送業者が使用する、陸揚原価データ エンティティも示します。

| ITMContainers テーブルが含むフィールド | 陸揚原価データ エンティティ |
|---|---|
| 出荷コンテナー タイプ | ITMShippingContainerTypeEntity |
| 商品の説明 | ITMGoodsDescriptionEntity |
| 冷却タイプ | ITMShippingContainerRefrigerationTypeEntity |

## <a name="folios-itmfolioentity"></a>フォリオ (ITMFolioEntity)

フォリオは、税関申告で使用する、出荷コンテナーが含む品目のグループを表します。 フォリオはヘッダー レベルの情報を含み、これは関税ブローカーと商品の説明に関連付けられています。 `ITMFolioEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| ブローカーのアドバイス | ITMFolioTable.ShipBrokerAdvised | 日時 | 無効 | 無効 |
| 貨物制御番号 | ITMFolioTable.ShipCargoControlNumber | Nvarchar(20) | 無効 | 無効 |
| 顧客の予定 | ITMFolioTable.ShipCustomerAppointment | 日時 | 無効 | 無効 |
| 関税ブローカー | ITMFolioTable.ShipCustomsBroker | Nvarchar(20) | 無効 | 無効 |
| 関税 ID | ITMFolioTable.ShipCustomsId | Nvarchar(60) | 無効 | 無効 |
| 会社 | ITMFolioTable.ShipDataArea | Nvarchar(4) | 無効 | **有** |
| 倉庫で出荷 | ITMFolioTable.ShipDelAtWarehouse | 日時 | 無効 | 無効 |
| 出荷指示 | ITMFolioTable.ShipDeliveryInstructions | 日時 | 無効 | 無効 |
| ドキュメント受領 | ITMFolioTable.ShipDocReceived | Int | 無効 | 無効 |
| 推定出荷日 | ITMFolioTable.ShipEstDlvDate | 日時 | 無効 | 無効 |
| 出荷港での ETA | ITMFolioTable.ShipEstPortDate | 日時 | 無効 | 無効 |
| 輸出者 | ITMFolioTable.ShipExporterId | Nvarchar(20) | 無効 | 無効 |
| Name | ITMFolioTable.ShipExporterName | Nvarchar(60) | 無効 | 無効 |
| フォリオ日付 | ITMFolioTable.ShipFolioDate | 日時 | 無効 | 無効 |
| フォリオ | ITMFolioTable.ShipFolioId | Nvarchar(20) | **有** | **有** |
| 出荷元港 | ITMFolioTable.ShipFromPort | Nvarchar(20) | 無効 | 無効 |
| 商品の説明 | ITMFolioTable.ShipGoodsDesc | Nvarchar(60) | 無効 | 無効 |
| リリースされた商品 | ITMFolioTable.ShipGoodsReleased | 日時 | 無効 | 無効 |
| 航空貨物運送/船荷証券の保管 | ITMFolioTable.ShipHAWB | Nvarchar(20) | 無効 | 無効 |
| 航海 | ITMFolioTable.ShipId | Nvarchar(20) | 無効 | **有** |
| 測定 | ITMFolioTable.ShipMeasurement | Numeric(32, 6) | 無効 | 無効 |
| 測定単位 | ITMFolioTable.ShipMeasurementUnit | Int | 無効 | 無効 |
| カートン数 | ITMFolioTable.ShipNoOfCartons | Numeric(32, 6) | 無効 | 無効 |
| 元の船荷証券が送信されました | ITMFolioTable.ShipOriginalBOLSebt | 日時 | 無効 | 無効 |
| 元のドキュメントを受領しました | ITMFolioTable.ShipOriginalDocsReceived | 日時 | 無効 | 無効 |
| 発注書のステータス | ITMFolioTable.ShipPurchStatus | Int | 無効 | 無効 |
| 備考 | ITMFolioTable.ShipRemarks | Nvarchar(MAX) | 無効 | 無効 |
| 航海状態 | ITMFolioTable.ShipStatusId | Nvarchar(20) | 無効 | 無効 |
| 税率コード | ITMFolioTable.ShipTariffCode | Nvarchar(10) | 無効 | 無効 |
| 出荷先港 | ITMFolioTable.ShipToPort | Nvarchar(20) | 無効 | 無効 |
| 評価日 | ITMFolioTable.ShipValuationDate | 日時 | 無効 | 無効 |
| 確認日 | ITMFolioTable.ShipVerificationDate | 日時 | 無効 | 無効 |
| 仕入先 | ITMFolioTable.VendAccount | Nvarchar(20) | 無効 | 無効 |

### <a name="number-sequences-for-folios"></a>フォリオの番号順序

フォリオの番号順序は、フォリオ ID の割り当てを制御します。

**フォリオ ID** (`FolioId`) 値としてデータ エンティティに渡す値は、更新する既存のレコードの識別に使用します。 そのレコードが存在しない場合は、手動入力を許可するように割り当て済みの番号順序を構成しているかどうかによって動作が異なります。

- 手動入力が有効である場合、渡された値を使用する新しいレコードが作成されます。
- 手動入力が有効でない場合、渡された値の代わりに、割り当て済みの番号順序が含む次の番号を使用します。

フォリオ ID としてインポートしたプレースホルダー値は、インポート セッション中に保持されます。 この動作によって、プレースホルダーを参照する航海明細行を正しく関連付け、番号順序で割り当てた値を反映するように、それらを更新します。

### <a name="field-validations"></a>フィールドの検証

フォリオ テーブル (`ITMFolioTable`) の **商品の説明** フィールドを、同じ名前の陸揚原価設定テーブルに対して検証します。 配送業者は、`ITMGoodsDescriptionEntity` 陸揚原価データ エンティティを使用して既存の値を読み取り、有効な値を環境で確実に受け取ります。

## <a name="voyage-lines-for-purchase-orders-itmpurchaselineentity"></a>発注書の航海明細行 (ITMPurchaseLineEntity)

航海明細行は、その航海が含む単一の発注書明細行を表します。 この関係付けは、**発注書番号** と **購買明細行番号** フィールドによって確立します。 航海明細行は、航海、出荷コンテナー、フォリオに対して作成した以前の各レコードを参照します。 `ITMPurchaseLineEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 通貨 | ITMLine.CurrencyCode | Nvarchar(3) | 無効 | 無効 |
| 正味金額 | ITMLine.LineAmountMST | Numeric(32, 6) | 無効 | 無効 |
| 購買注文明細行番号 | ITMLine.RefRecId | Numeric(32, 6) | **有** | 無効 |
| 出荷コンテナー | ITMLine.ShipContainerId | Int | 無効 | 無効 |
| 会社 | ITMLine.ShipDataArea | Nvarchar(20) | **有** | 無効 |
| 申告数量 | ITMLine.ShipDeclaredQty | Nvarchar(4) | 無効 | 無効 |
| フォリオ | ITMLine.ShipFolioId | Numeric(32, 6) | 無効 | 無効 |
| 航海 | ITMLine.ShipId | Nvarchar(20) | **有** | 無効 |
| 品目番号 | ITMLine.ShipItemId | Nvarchar(20) | 無効 | 無効 |
| 測定 | ITMLine.ShipMeasurement | Nvarchar(20) | 無効 | 無効 |
| 測定単位 | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | 無効 | 無効 |
| カートン数 | ITMLine.ShipNoOfCartons | Int | 無効 | 無効 |
| 位置 | ITMLine.ShipPosition | Numeric(32, 6) | 無効 | 無効 |
| Quantity | ITMLine.ShipQty | Int | 無効 | 無効 |
| 発注書番号 | ITMLine.TransRefId | Numeric(32, 6) | **有** | 無効 |
| 単位 | ITMLine.UnitId | Int | 無効 | 無効 |
| ボリューム | ITMLine.Volume | Nvarchar(10) | 無効 | 無効 |
| 重量 | ITMLine.Weight | Numeric(32, 6) | 無効 | 無効 |

## <a name="voyage-lines-for-transfer-orders-itmtransferlineentity"></a>移動オーダーの航海明細行 (ITMTransferLineEntity)

航海明細行は、その航海が含む単一の移動オーダー明細行を表します。 この関係付けは、**移動オーダー番号** と **移動明細行番号** フィールドによって確立します。 航海明細行は、航海、出荷コンテナー、フォリオに対して作成した以前の各レコードを参照します。 `ITMTransferLineEntity` エンティティは、この機能に対応しています。 次の表に、このエンティティを構成するフィールドとマッピングを示します。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 通貨 | ITMLine.CurrencyCode | Nvarchar(3) | 無効 | 無効 |
| 正味金額 | ITMLine.LineAmountMST | Numeric(32, 6) | 無効 | 無効 |
| 出荷コンテナー | ITMLine.ShipContainerId | Int | 無効 | 無効 |
| 会社 | ITMLine.ShipDataArea | Nvarchar(20) | **有** | 無効 |
| 申告数量 | ITMLine.ShipDeclaredQty | Nvarchar(4) | 無効 | 無効 |
| フォリオ | ITMLine.ShipFolioId | Numeric(32, 6) | 無効 | 無効 |
| 航海 | ITMLine.ShipId | Nvarchar(20) | **有** | 無効 |
| 品目番号 | ITMLine.ShipItemId | Nvarchar(20) | 無効 | 無効 |
| 測定 | ITMLine.ShipMeasurement | Nvarchar(20) | 無効 | 無効 |
| 測定単位 | ITMLine.ShipMeasurementUnit | Numeric(32, 6) | 無効 | 無効 |
| カートン数 | ITMLine.ShipNoOfCartons | Int | 無効 | 無効 |
| 位置 | ITMLine.ShipPosition | Numeric(32, 6) | 無効 | 無効 |
| Quantity | ITMLine.ShipQty | Int | 無効 | 無効 |
| 移動明細行番号 | ITMLine.TransferLineNumber | Numeric(32, 6) | **有** | 無効 |
| 移動オーダー番号 | ITMLine.TransRefId | Numeric(32, 6) | **有** | 無効 |
| 単位 | ITMLine.UnitId | Int | 無効 | 無効 |
| ボリューム | ITMLine.Volume | Nvarchar(10) | 無効 | 無効 |
| 重量 | ITMLine.Weight | Numeric(32, 6) | 無効 | 無効 |

### <a name="reference-table"></a>参照テーブル

航海明細行は、オープン状態の入庫注文明細行との関連付けによって作成します。 この明細行は、発注書に含まれる場合もあれば、移動オーダーの受け取りトランザクションである場合もあります。 航海明細行テーブル (`ITMLine`) の `RefTableId` フィールドは、テーブル番号を参照して、明細行が関連付けられた注文タイプを指定します。 データを作成しているテーブルで特定のテーブル番号を参照している場合、それらの値に基づいてエンティティを分割します。

参照テーブル (`RefTableId`) とトランザクション タイプ (`TransType`) の値は、陸揚原価購買注文明細行エンティティまたは陸揚原価移動明細行エンティティの選択で暗黙的に含まれます。

### <a name="validation"></a>検証

航海明細行は、航海レコード、出荷コンテナー レコード、フォリオ レコードを、直接参照します。 これらの参照レコードの作成に使用するエンティティとは独立して、購入明細行エンティティ (`ITMPurchaseLinesEntity`) や移動明細行エンティティ (`ITMPurchaseLinesEntity`) を使用する場合、**航海 ID** (`ShipId`)、**出荷コンテナー** (`ShipContainerId`)、**フォリオ** (`ShipFolioId`) の値を、対応するテーブルが含む既存のレコードと一致させる必要があります。 そうしない場合はインポートが失敗します。

いずれかの明細行エンティティを同じインポート セッションの一部として使用している場合、これらの他のエンティティを航海明細行より前に作成する必要があります。 そうしない場合は、この値を正常に検証できません。 航海番号やフォリオ番号にプレースホルダー値を使用する場合、同じプレースホルダーを航海明細行エンティティの航海番号やフォリオ番号として使用する場合にのみ、関連付けを作成できます。

発注書や移動オーダー注文明細行を、すでに既存の航海明細行に割り当てている場合、新しい航海明細行は作成されません。 注文明細行を新しい航海に割り当てる前に、現在の航海から削除する必要があります。

### <a name="order-line-identification"></a>注文明細行 ID

航海明細行は、**レコード ID** (`RefRecId`)、**在庫分析コード ID** (`InventDimId`)、**在庫トランザクション ID** (`InventTransId`) 値を直接参照します。 現在、データ エンティティの使用時に、これらの値を含める必要はありません。 代わりに、注文明細行番号を含める必要があります。 注文明細行番号と注文番号を一緒に使用することで、それらの参照値を識別できるようになります。

### <a name="voyage-line-quantity"></a>航海明細行の数量

航海明細行は注文明細行に直接関連付けられているため、エンティティを使用して入力する **数量** (`ShipQty`) 値は、値を一致させる必要があります。 発注書明細行または移動明細行のいずれかの数量に対して、検証を実行します。 検証に失敗すると、そのレコードは処理されません。

### <a name="calculated-fields"></a>計算済フィールド

**重量** と **容量** の計算フィールドには、データ エンティティによって受け取った値を指定できます。 値を指定しない場合、システム値を使用できるなら、これらのフィールドをシステム値を使用して更新します。 陸揚原価に関して、この値は次の方法で計算します。

- *重量* = *数量* × *品目の総重量*
- *容量* = *数量* × (*品目の総奥行* × *品目の総高さ* × *品目の総幅*)

## <a name="sequencing"></a>優先順位

このテーブル間の依存関係のため、最初に航海レコードを作成する必要があります。 航海明細行は、航海、出荷コンテナー、フォリオの作成後にのみ作成できます。

検証の警告を発生させずに航海を作成するためには、システムはエンティティを次の順序で処理する必要があります。

1. 航海 (`ITMTableEntity`)
1. 出荷コンテナー (`ITMContainersEntity`)
1. フォリオ (`ITMFolioTableEntity`)
1. 航海明細行 (`ITMPurchaseLinesEntity` または `ITMTransferLinesEntity`)
