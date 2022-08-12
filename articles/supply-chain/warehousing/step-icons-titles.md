---
title: Warehouse Management モバイル アプリのステップ アイコンとタイトルの割り当て
description: この記事では、Warehouse Management モバイル アプリの新しいタスク フローまたはカスタマイズされたタスク フローに対してステップ アイコンとタイトルを割り当てる方法について説明します。
author: Mirzaab
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 2ed2baff1851eba488233c050cef1f8f73b6bcee
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067305"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a>Warehouse Management モバイル アプリのステップ アイコンとタイトルの割り当て

[!include [banner](../includes/banner.md)]

この記事では、Warehouse Management モバイル アプリの新しいタスク フローまたはカスタマイズされたタスク フローに対してステップ アイコンとステップ タイトルを割り当てる方法について説明します。

次の図は、Warehouse Management モバイル アプリにステップ アイコンとタイトルがどのように表示されるかを示しています。

![Warehouse Management モバイル アプリのステップ アイコンとステップ タイトルの例。](media/step-icon-example.png "Warehouse Management モバイル アプリのステップ アイコンとステップ タイトルの例")

## <a name="turn-this-feature-on-or-off"></a>この機能のオン/オフの切り替え

この記事で説明する機能を使用するには、*新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル* 機能がシステムで有効になっている必要があります。 Supply Chain Management 10.0.25 では、この機能は必須なため、オフにすることはできません。 10.0.25 より以前のバージョンを使用している場合、管理者は [機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *新しい倉庫アプリのユーザー設定、アイコン、ステップ タイトル* を検索して、この機能をオンまたはオフにすることができます。

## <a name="standard-step-ids-classes-and-icons"></a>標準的なステップ ID、クラス、アイコン

タスク フローの各ステップはステップ ID で識別され、各ステップ ID には対応するステップ クラスがあります。 ステップ アイコンおよびタイトルは各ステップ クラスで指定されます。

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a>ステップ ID とステップ クラス

次の表に、現在使用可能なすべてのステップ ID と、それに対応するステップ クラスの一覧を示します。 基本入力フィールドの制御名がステップ ID として使用されます。

これらのステップ ID およびクラスがどのように使用されるかを示す例については、この記事で後述する [例: カスタム フローへのステップ アイコンとタイトルの割り当て](#example) セクションの `WHSMobileAppStepInfoBuilder.stepId()` メソッドの実装を参照してください。

| ステップ ID | ステップ クラス |
|-|-|
| BatchDisposition | WHSMobileAppStepBatchDisposition |
| 配送業者 | WHSMobileAppStepCarrier |
| CatchWeight | WHSMobileAppStepCatchWeight |
| CatchWeightQtyOutboundWeight | WHSMobileAppStepCatchWeight |
| CatchWeightTag | WHSMobileAppStepCatchWeightTag |
| CatchWeightTagWeight | WHSMobileAppStepCatchWeightTagWeight |
| ChangeWarehouseSuccess | WHSMobileAppStepChangeWarehouseSuccess |
| CheckDigit | WHSMobileAppStepCheckDigit |
| ClusterId | WHSMobileAppStepClusterId |
| ClusterPickQtyVerification | WHSMobileAppStepQtyVerification |
| ClusterPosition | WHSMobileAppStepClusterPosition |
| ConfigId | WHSMobileAppStepConfigId |
| 確認書 | WHSMobileAppStepConfirmation |
| ConsolidateFromLicensePlateId | WHSMobileAppStepConsolidateFromLicensePlateId |
| ConsolidateLPConfirmation | WHSMobileAppStepConsolidateLPConfirmation |
| ConsolidateToLicensePlateId | WHSMobileAppStepConsolidateToLicensePlateId |
| ContainerType | WHSMobileAppStepContainerType |
| CountingReasonCode | WHSMobileAppStepCountingReasonCode |
| CycleCountingAddLPOrFinish | WHSMobileAppStepCycleCountingAddLPOrFinish |
| CycleCountQty1 | WHSMobileAppStepCycleCountQty |
| CycleCountQty2 | WHSMobileAppStepCycleCountQty |
| CycleCountQty3 | WHSMobileAppStepCycleCountQty |
| CycleCountQty4 | WHSMobileAppStepCycleCountQty |
| Disposition | WHSMobileAppStepDisposition |
| DriverCheckInConfirmation | WHSMobileAppStepDriverCheckInConfirmation |
| DriverCheckInId | WHSMobileAppStepDriverCheckInId |
| DriverCheckOutConfirmation | WHSMobileAppStepDriverCheckOutConfirmation |
| DriverCheckOutId | WHSMobileAppStepDriverCheckOutId |
| ExpDate | WHSMobileAppStepExpDate |
| FromBatchDisposition | WHSMobileAppStepFromBatchDisposition |
| FromInventoryStatus | WHSMobileAppStepInventoryStatusFrom |
| FullQty | WHSMobileAppStepFullQty |
| InboundPut | WHSMobileAppStepInboundPut |
| InventBatchId | WHSMobileAppStepBatch |
| InventColorId | WHSMobileAppStepInventColorId |
| InventLocation | WHSMobileAppStepInventLocation |
| InventLocationId | WHSMobileAppStepWarehouse |
| InventSerialId | WHSMobileAppStepInventSerialId |
| InventSizeId | WHSMobileAppStepInventSizeId |
| InventStatusId | WHSMobileAppStepInventStatus |
| InventStyleId | WHSMobileAppStepInventStyleId |
| InventVersionId | WHSMobileAppStepInventVersionId |
| ItemId | WHSMobileAppStepItem |
| ITMContainerID | ITMMobileAppStepContainerId |
| ITMShipmentID | ITMMobileAppStepShipmentId |
| KanbanCardId | WHSMobileAppStepKanbanCard |
| KanbanCardToEmpty | WHSMobileAppStepKanbanCardToEmpty |
| KanbanOrCardId | WHSMobileAppStepKanbanCard |
| LicensePlateId | WHSMobileAppStepLicensePlate |
| LoadId | WHSMobileAppStepLoadId |
| LocationLicensePlatePosition | WHSMobileAppStepLocationLicensePlatePosition |
| LocOrLP | WHSMobileAppStepLocOrLP |
| LocOrLP_From | WHSMobileAppStepLocOrLPFrom |
| LocOrLP_To | WHSMobileAppStepLocOrLPTo |
| LocOrLPCheck | WHSMobileAppStepLocOrLPCheck |
| LocVerification | WHSMobileAppStepLocVerification |
| LPAdjustIn | WHSMobileAppStepLPAdjustIn |
| LPBreakChildLP | WHSMobileAppStepLPBreakChildLP |
| LPBreakParentLP | WHSMobileAppStepLPBreakParentLP |
| LPBuildChildLP | WHSMobileAppStepLPBuildChildLP |
| LPBuildParentLP | WHSMobileAppStepLPBuildParentLP |
| LPVerification | WHSMobileAppStepLPVerification |
| MergeContainerId | WHSMobileAppStepMergeContainerId |
| MixedLPLineNum | WHSMobileAppStepMixedLPLineNum |
| MobileDeviceQueueMessageCollectionIdentifierId | WHSMobileAppStepSelectOrder |
| MovementConfirmCancel | WHSMobileAppStepMovementConfirmCancel |
| NewCaptureWeight | WHSMobileAppStepCatchWeight |
| NewQty | WHSMobileAppStepNewQty |
| OutboundCatchWeightTag | WHSMobileAppStepCatchWeightTag |
| OutboundPut | WHSMobileAppStepOutboundPut |
| OutboundWeight | WHSMobileAppStepCatchWeight |
| OverridePutNewLocation | WHSMobileAppStepOverridePutNewLocation |
| PieceByPieceConfirmation | WHSMobileAppStepQtyVerification |
| POLineNum | WHSMobileAppStepPOLineNum |
| 発注書番号 | WHSMobileAppStepPONum |
| PositionFull | WHSMobileAppStepPositionFull |
| PositionFullQty | WHSMobileAppStepPositionFullQty |
| ポテンシー | WHSMobileAppStepPotency |
| PrinterName | WHSMobileAppStepPrinterName |
| ProdId | WHSMobileAppStepProdId |
| ProdLastPalletConfirmation | WHSMobileAppStepProdLastPalletConfirmation |
| ProductConfirmation | WHSMobileAppStepProductConfirmation |
| ProductionScrapConfirmation | WHSMobileAppStepProductionScrapConfirmation |
| プット | WHSMobileAppStepPut |
| PutawayClusterId | WHSMobileAppStepPutawayClusterId |
| 数量 | WHSMobileAppStepQty |
| QtyAdjust | WHSMobileAppStepQtyAdjust |
| QtyShort | WHSMobileAppStepQtyShort |
| QtyToConsume | WHSMobileAppStepQtyToConsume |
| QtyToPick | WHSMobileAppStepQtyToPick |
| QtyToPut | WHSMobileAppStepQtyToPut |
| QtyToScrap | WHSMobileAppStepQtyToScrap |
| QtyVerification | WHSMobileAppStepQtyVerification |
| QtyWithScanningLimit | WHSMobileAppStepQtyAdjust |
| ReasonString | WHSMobileAppStepReasonString |
| RecvLocationId | WHSMobileAppStepRecvLocationId |
| RemoveContainerId | WHSMobileAppStepRemoveContainerId |
| ReprintLabelConfirmation | WHSMobileAppStepReprintLabelConfirmation |
| RMANum | WHSMobileAppStepRMANum |
| ShortPickReason | WHSMobileAppStepShortPickReason |
| SortConOrLP | WHSMobileAppStepSortConOrLP |
| SortLicensePlateId | WHSMobileAppStepSortLicensePlateId |
| SortPositionId | WHSMobileAppStepSortPositionId |
| SortVerification | WHSMobileAppStepSortVerification |
| StartLocationId | WHSMobileAppStepStartLocationId |
| StartProdOrderConfirmation | WHSMobileAppStepStartProdOrderConfirmation |
| TargetLicensePlateId | WHSMobileAppStepTargetLicensePlateId |
| TOLineNum | WHSMobileAppStepTOLineNum |
| ToLocation | WHSMobileAppStepToLocation |
| TONum | WHSMobileAppStepTONum |
| ToWarehouse | WHSMobileAppStepWarehouseTo |
| TransportLoadId | WHSMobileAppStepTransportLoadId |
| WaveLabelId | WHSMobileAppStepWaveLabelId |
| WaveLblQty | WHSMobileAppStepWaveLblQty |
| 太さ | WHSMobileAppStepWeight |
| WeightToConsume | WHSMobileAppStepWeightToConsume |
| WHSAdjustmentType | WHSMobileAppStepWHSAdjustmentType |
| WHSReceivingException | WHSMobileAppStepWHSReceivingException |
| WHSWorkException | WHSMobileAppStepWHSWorkException |
| WHSWorkLicensePlateId | WHSMobileAppStepWorkLicensePlateId |
| WMSLocationId | WHSMobileAppStepLocation |
| WorkId | WHSMobileAppStepWorkId |
| WorkIdToCancel | WHSMobileAppStepWorkIdToCancel |
| WorkLPIdPutawayCluster | WHSMobileAppStepWorkLPIdPutawayCluster |
| WorkPoolId | WHSMobileAppStepWorkPoolId |
| ZoneId | WHSMobileAppStepZoneId |

### <a name="available-step-icons"></a><a name="step-icons"></a>使用可能なステップ アイコン

システムには、カスタム ステップにも使用できる標準ステップ アイコンのコレクションが含まれています。 現在、カスタム ステップ アイコンはアップロードできません。 したがって、常に標準ステップ アイコンのいずれかを選択する必要があります。

次の表に、現在使用可能なすべての標準ステップ アイコンとその名前を示します。

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="ステップ アイコンについて"><br>情報</td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="ライセンス プレートまたは品目ステップ アイコンの追加"><br>AddLpOrItem</td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="バッチ廃棄ステップ アイコン"><br>BatchDisposition</td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="通信事業者ステップ アイコン"><br>配送業者</td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="CW タグ ステップ アイコン"><br>CatchWeightTag</td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="CW タグの重量ステップ アイコン"><br>CatchWeightTagWeight</td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="チェック ディジット ステップ アイコン"><br>CheckDigit</td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="チェックインまたはアウト ID ステップ アイコン"><br>CheckInOutId</td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="子ライセンス プレート ステップ アイコン"><br>ChildLP</td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="クラスター ID ステップ アイコン"><br>ClusterId</td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="クラスター位置ステップ アイコン"><br>ClusterPosition</td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="コンフィギュレーション ID ステップ アイコン"><br>ConfigId</td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="構成済フィールド ステップ アイコン"><br>ConfiguredField</td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con または LP ステップ アイコン"><br>ConOrLP</td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="ライセンス プレート ID から連結ステップ アイコン"><br>ConsolidateFromLicensePlateID</td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="ライセンス プレート ID に連結ステップ アイコン"><br>ConsolidateToLicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="コンテナー タイプ ステップ アイコン"><br>ContainerType</td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="棚卸ステップ アイコン"><br>棚卸</td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="棚卸理由コード ステップ アイコン"><br>CountingReasonCode</td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="原産国コード ステップ アイコン"><br>CountryOfOrigin</td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="廃棄ステップ アイコン"><br>Disposition</td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="完了ステップ アイコン"><br>完了</td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="配送担当者のチェックイン確認ステップ アイコン"><br>DriverCheckInConfirmation</td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="配送担当者のチェックイン ID ステップ アイコン"><br>DriverCheckInId</td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="配送担当者のチェックアウト ID ステップ アイコン"><br>DriverCheckOutId</td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="有効期限ステップ アイコン"><br>ExpDate</td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="フィールド ステップ アイコン"><br>フィールド</td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="バッチ廃棄からステップ アイコン"><br>FromBatchDisposition</td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="在庫状態からステップ アイコン"><br>FromInventoryStatus</td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="ID 属性ステップ アイコン"><br>IdAttribute</td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="在庫バッチ ID ステップ アイコン"><br>InventBatchID</td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="在庫の色 ID ステップ アイコン"><br>InventColorID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="在庫場所ステップ アイコン"><br>InventLocation</td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="在庫のシリアル ID ステップ アイコン"><br>InventSerialID</td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="在庫のサイズ ID ステップ アイコン"><br>InventSizeID</td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="在庫の状態 ID ステップ アイコン"><br>InventStatusID</td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="在庫のスタイル ID ステップ アイコン"><br>InventStyleID</td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="在庫のバージョン ID ステップ アイコン"><br>InventVersionID</td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="品目 ID ステップ アイコン"><br>ItemID</td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM コンテナー ID ステップ アイコン"><br>ITMContainerID</td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM 出荷 ID ステップ アイコン"><br>ITMShipmentID</td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="かんばんカード ID ステップ アイコン"><br>KanbanCardID</td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="かんばんまたはカード ID ステップ アイコン"><br>KanbanOrCardID</td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="ライセンス プレート ID ステップ アイコン"><br>LicensePlateID</td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="貨物 ID ステップ アイコン"><br>LoadId</td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="場所ライセンス プレートの位置ステップ アイコン"><br>LocationLicensePlatePosition</td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="場所またはライセンス プレート ステップ アイコン"><br>LocOrLP</td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="場所またはライセンス プレート チェック ステップ アイコン"><br>LocOrLPCheck</td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="場所またはライセンス プレート元ステップ アイコン"><br>LocOrLPFrom</td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="場所またはライセンス プレート先ステップ アイコン"><br>LocOrLPTo</td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="ロング プロセス完了ステップ アイコン"><br>LongProcessCompleted</td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP ブレーク 親 LP ステップ アイコン"><br>LPBreakParentLP</td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="結合コンテナー ID ステップ アイコン"><br>MergeContainerId</td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="混合ライセンス プレートの行番号ステップ アイコン"><br>MixedLPLineNum</td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="出庫重量ステップ アイコン"><br>OutboundWeight</td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="所有者ステップ アイコン"><br>所有者</td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="親ライセンス プレート ステップ アイコン"><br>ParentLP</td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="確認ステップ アイコン"><br>PleaseConfirm</td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="発注書行番号ステップ アイコン"><br>POLineNum</td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="発注書番号ステップ アイコン"><br>発注書番号</td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="満杯のポジション ステップ アイコン"><br>PositionFull</td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="ポテンシー ステップ アイコン"><br>ポテンシー</td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="プリンター名ステップ アイコン"><br>PrinterName</td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="製品 ID ステップ アイコン"><br>ProdId</td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="製品の確認ステップ アイコン"><br>ProductConfirmation</td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="プット ステップ アイコン"><br>プット</td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="プットアウェイ クラスター ID ステップ アイコン"><br>PutawayClusterId</td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="数量ステップ アイコン"><br>数量</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="数量調整ステップ アイコン"><br>QtyAdjustIn</td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="数量不足ステップ アイコン"><br>QtyShort</td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="消費数量ステップ アイコン"><br>QtyToConsume</td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="プット数量ステップ アイコン"><br>QtyToPut</td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="廃棄数量ステップ アイコン"><br>QtyToScrap</td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="数量確定ステップ アイコン"><br>QuantityConfirmation</td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="完了ジョブとしてレポート ステップ アイコン"><br>RAFEndJob</td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="受取場所 ID ステップ アイコン"><br>RecvLocationID</td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="削除コンテナー ID ステップ アイコン"><br>RemoveContainerID</td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA 番号ステップ アイコン"><br>RMANum</td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="順序選択ステップ アイコン"><br>SelectOrder</td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="ショート・ピックの理由ステップ アイコン"><br>ShortPickReason</td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="並べ替え位置 ID ステップ アイコン"><br>SortPositionId</td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="ターゲット ライセンス プレート ID ステップ アイコン"><br>TargetLicensePlateId</td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="行番号へステップ アイコン"><br>ToLineNum</td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="移動先ステップ アイコン"><br>ToLocation</td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="番号へステップ アイコン"><br>ToNum</td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="移動先倉庫ステップ アイコン"><br>ToWarehouse</td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="輸送貨物 ID ステップ アイコン"><br>TransportLoadId</td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="仕入先バッチ ID ステップ アイコン"><br>VendBatchId</td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="ウェーブ ラベル ID ステップ アイコン"><br>WaveLabelId</td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="ウェーブ ラベル数量ステップ アイコン"><br>WaveLblQty</td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="重量ステップ アイコン"><br>重量</td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="消費重量ステップ アイコン"><br>WeightToConsume</td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WMS adjustment type step icon" title="WMS 調整タイプ ステップ アイコン"><br>WHSAdjustmentType</td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WMS receiving exception step icon" title="WMS 受領例外ステップ アイコン"><br>WHSReceivingException</td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS 場所 ID ステップ アイコン"><br>WMSLocationID</td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="作業 ID ステップ アイコン"><br>WorkId</td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="キャンセルする作業 ID ステップ アイコン"><br>WorkIdToCancel</td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="作業ライセンス プレート ID ステップ アイコン"><br>WorkLicensePlateId</td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="作業ライセンス プレート ID プットアウェイ クラスター ステップ アイコン"><br>WorkLPIDPutawayCluster</td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="作業プール ID ステップ アイコン"><br>WorkPoolID</td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="ゾーン ID ステップ アイコン"><br>ZoneID</td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a>例: カスタム フローへのステップ アイコンとタイトルの割り当て

この例では、カスタム タスク フローのステップ アイコンとタイトルの設定方法を説明します。 このシナリオは、次のブログ記事: [倉庫モバイル アプリのカスタマイズ](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app) で詳細に説明および検討するカスタム タスク フローの例に基づいて作成されています。 タスク フローは次のように機能します:

1. アプリは、作業者にコンテナー ID の入力を求めるページを表示します (例えば、バーコードをスキャンするなど)。
1. コンテナー ID が有効な場合、アプリは新しいページを開き、作業者に重量の入力を求めます。 (コンテナー ID が無効な場合、作業者は最初のページに戻ります。)
1. 作業者が有効な重量を入力すると、システムは重量を格納し、作業者を最初のページに戻します。

次の図は、このタスク フローを示します。

![タスク フロー図。](media/step-icons-example-task-flow.png "タスク フロー図")

### <a name="create-a-step-class-for-the-container-input-page"></a>コンテナー入力ページ用のステップ クラスの作成

コンテナー入力ページでは、作業者がコンテナー ID をスキャンまたは入力できます。

![コンテナー入力ページ。](media/step-icons-example-container-input.png "コンテナー入力ページ")

コンテナー入力ページでは、入力フィールドのコントロール名は `ContainerId` です。 このコントロール名は [ステップ ID の一覧](#step-ids-classes) にないため、このコントロール名に基づく既存のステップは見つかりません。 したがって、ステップを表すステップ クラスを作成する必要があります。 次に例を示します。

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

ステップ アイコンの識別子は `defaultStepIcon` クラス メンバーに保存され、ステップ タイトルは `defaultStepTitle` クラス メンバーに保存されます。

ステップ アイコンを割り当てるには、`defaultStepIcon` をこの記事で前述した [使用可能なステップ アイコン](#step-icons) セクションに一覧表示されているアイコン ID の 1 つに設定します。

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a>重量入力に標準またはカスタムのステップ アイコンとタイトルを使用する

重量入力ページでは、作業者が重量を入力できます。

![重量入力ページ。](media/step-icons-example-weight-input.png "重量入力ページ")

重量入力ページでは、入力フィールドのコントロール名は [ステップ ID の一覧](#step-ids-classes) にある `Weight` です。 したがって、`WHSMobileAppStepWeight` クラスで定義されているステップ アイコンとタイトルが適切であれば、このステップで何も変更する必要はありません。

ただし、このステップで別のアイコンまたはタイトルを使用する場合は、ビルダー クラスで `stepId()` メソッドまたは `stepInfo()` メソッドを上書きできます。 各タスク フローには、独自のステップ情報ビルダーがあります。

#### <a name="override-the-stepid-method"></a>stepId() メソッドの上書き

次の例は、`stepId()` メソッドを上書きしてビルダー クラスを変更する方法の 1 つです。

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

次に、`NewWeight` ステップのステップ クラスを作成します。 コードは、この記事の前半で示した `ContainerId` の例のコードと似ている必要があります。

#### <a name="override-the-stepinfo-method"></a>stepInfo() メソッドの上書き

次の例は、`stepInfo()` メソッドを上書きしてビルダー クラスを変更する方法の 1 つです。

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

次に、`WHSMobileAppStepInfo` オブジェクトを作成し、アイコンやタイトルを直接設定します。

## <a name="additional-resources"></a>追加リソース

- [倉庫管理モバイル アプリのインストールと接続](install-configure-warehouse-management-app.md)
- [モバイル デバイスのユーザー設定](mobile-device-user-settings.md)
