---
title: 分離型二重書き込みアプリケーション オーケストレーション ソリューションの適用
description: 二重書き込みアプリケーション オーケストレーション パッケージは、単一のパッケージではなく、小さいパッケージに分離されています。 この記事では、各パッケージに含まれるソリューションとマップ、および他のパッケージへの依存関係について説明します。
author: RamaKrishnamoorthy
ms.date: 04/25/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: separate-solution
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-11-29
ms.openlocfilehash: 7f2a9b9e52b80c0feae0ac0dcb1ddf0a5c0cd27c
ms.sourcegitcommit: 8aba7d2f45ef03a14f33f4b430ce92a11c876e2e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/16/2022
ms.locfileid: "9884119"
---
# <a name="separated-dual-write-application-orchestration-package"></a>分離型二重書き込みアプリケーション オーケストレーション ソリューションの適用

[!include [banner](../../includes/banner.md)]



以前は、二重書き込みアプリケーション オーケストレーション パッケージは、次のソリューションを含む 1 つのパッケージでした:

- Dynamics 365 Notes
- Dynamics 365 財務と運用共通アンカー
- Dynamics 365 財務と運用二重書き込みエンティティ マップ
- Dynamics 365 アセット マネジメント アプリ
- Dynamics 365 アセット マネジメント
- HCM 共通
- Dynamics 365 Supply Chain Extended
- Dynamics 365 Finance Extended
- Dynamics 365 財務と運用共通
- Dynamics 365 Company
- Currency Exchange Rates
- Field Service Common

このパッケージは 1 つのパッケージであったため顧客にとっては「オール・オア・ナッシング」の状態になっていました。 しかし、マイクロソフトでは現在、これらを小さなパッケージに分けています。 そのため、顧客は必要なソリューションのパッケージだけを選択することができます。 例えば、Microsoft Dynamics 365 Supply Chain Management のユーザーで、Dynamics 365 Human Resources、ノート、資産管理との連携を必要としない場合、それらのソリューションをインストールされるソリューションから除外することができます。 基本的なソリューション名、公開元、マップのバージョンは変わらないため、この変更による影響はありません。 既存のインストールをアップグレードする必要があります。

![区切られたパッケージ。](media/separated-package-1.png)

この記事では、各パッケージに含まれるソリューションとマップ、および他のパッケージへの依存関係について説明します。

## <a name="dual-write-application-core"></a>二重書き込みアプリケーション コア

二重書き込みアプリケーション コア パッケージは、ユーザーが Customer Engagement アプリを使用せずに二重書き込みをインストールして設定することができます。 次の 5 つのソリューションが含まれています。

| 固有の名前                           | 表示名                               |
|---------------------------------------|--------------------------------------------|
| Dynamics365Company                    | Dynamics 365 Company                       |
| Dynamics365FinanceAndOperationsCommon | Dynamics 365 Finance and Operations Common |
| CurrencyExchangeRates                 | Currency Exchange Rates                    |
| msdyn_DualWriteAppCoreMaps            | 二重書き込みアプリケーション コア エンティティのマップ   |
| msdyn_DualWriteAppCoreAnchor          | 二重書き込みアプリケーション コア アンカー        |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用アプリ     | Customer Engagement アプリ                    |
|---------------------------------|---------------------------------------------|
| 作業単位                  | msdyn_internalorganizations                 |
| 組織階層          | msdyn_internalorganizationhierarchies       |
| 法人                  | msdyn_internalorganizations                 |
| 法人                  | cdm_companies                               |
| 組織階層の目的 | msdyn_internalorganizationhierarchypurposes |
| 為替レートの通貨ペア     | msdyn_currencyexchangeratepairs             |
| 名前の接辞                    | msdyn_nameaffixes                           |
| 為替レート タイプ              | msdyn_exchangeratetypes                     |
| CDS 為替レート              | msdyn_currencyexchangerates                 |
| 組織階層タイプ     | msdyn_internalorganizationhierarchytypes    |
| 通貨                      | transactioncurrencies                       |
| Mixed Reality ガイド エンティティ     | msmrw_guides                                |

**依存関係情報**

二重書き込みアプリケーション コア パッケージは、他のパッケージに依存していません。

## <a name="dual-write-human-resources"></a>Dual-write Human Resources

Dual-write Human Resources パッケージには、人事データの同期に必要なソリューションとマップが含まれています。 次の 3 つのソリューションが含まれています。

| 固有の名前                | 表示名                             |
|----------------------------|------------------------------------------|
| HCMCommon                  | HCM 共通                               |
| msdyn_Dynamics365HCMMaps   | Dynamics 365 Human Resources エンティティ マップ |
| msdyn_Dynamics365HCMAnchor | Dynamics 365 Human Resourcesアンカー      |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用アプリ | Customer Engagement アプリ         |
|-----------------------------|----------------------------------|
| 出身民族              | cdm_ethnicorigins                |
| 報酬ジョブ機能   | cdm_jobfunctions                 |
| 職位 V2                | cdm_jobpositions                 |
| 職務                        | cdm_jobs                         |
| 報酬ジョブ タイプ       | cdm_jobtypes                     |
| 言語コード              | cdm_languages                    |
| 職位タイプ               | cdm_positiontypes                |
| 職位作業者割り当て | cdm_positionworkerassignmentmaps |
| 退役軍人ステータス              | cdm_veteranstatuses              |
| 作業者                      | cdm_workers                      |
| 会社ごとの雇用      | cdm_employments                  |

**依存関係情報**

Dual-write Human Resources パッケージは、デュアル書き込みアプリケーション コア パッケージによって異なります。 したがって、Dual-write Application Core パッケージをインストールしてから、Dual-write Human Resources パッケージをインストールする必要があります。

## <a name="dual-write-supply-chain"></a>Dual-write Supply Chain

Dual-write Supply Chainパッケージには、Supply Chain Management データを同期させるために必要なソリューションとマップが含まれています。 次の 3 つのソリューションが含まれています。

| 固有の名前                                | 表示名                                              |
|--------------------------------------------|-----------------------------------------------------------|
| Dynamics365SupplyChainExtended             | Dynamics 365 Supply Chain Extended                        |
| msdyn_Dynamics365SupplyChainExtendedMaps   | Dynamics 365 Supply Chain Management 拡張エンティティ マップ |
| msdyn_Dynamics365SupplyChainExtendedAnchor | Dynamics 365 Supply Chain Management 拡張アンカー      |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用アプリ                 | Customer Engagement アプリ                      |
|---------------------------------------------|-----------------------------------------------|
| 単位                                       | uoms                                          |
| CDS 販売注文ヘッダー                     | 販売注文                                   |
| CDS 販売注文明細行                       | 販売注文詳細                             |
| CDS 販売見積ヘッダー                  | 見積                                        |
| CDS 販売見積明細行                   | 見積詳細                                  |
| 特徴的製品をリリースした CDS              | 製品                                      |
| 倉庫ゾーン                             | msdyn_warehousezones                          |
| 倉庫ゾーン グループ                       | msdyn_warehousezonegroups                     |
| 倉庫作業明細行                        | msdyn_warehouseworklines                      |
| 倉庫作業ヘッダー                      | msdyn_warehouseworkheaders                    |
| 倉庫                                  | msdyn_warehouses                              |
| 通路                             | msdyn_warehouseaisles                         |
| 単位換算                            | msdyn_unitofmeasureconversions                |
| 配送条件                           | msdyn_termsofdeliveries                       |
| 荷渡方法                           | msdyn_shipvias                                |
| 製品マスターのスタイル                       | msdyn_sharedproductstyles                     |
| 売上請求書明細行 V2                      | invoicedetails                                |
| 売上請求書ヘッダー V2                    | 請求書                                      |
| 製品マスターのサイズ                        | msdyn_sharedproductsizes                      |
| リリース済製品 V2                        | msdyn_sharedproductdetails                    |
| 製品マスターのコンフィギュレーション               | msdyn_sharedproductconfigurations             |
| 製品マスターの色                       | msdyn_sharedproductcolors                     |
| 販売注文元コード                    | msdyn_salesorderorigins                       |
| 製品受領書ヘッダー                      | msdyn_purchaseorderreceipts                   |
| 製品受領書明細行                        | msdyn_purchaseorderreceiptproducts            |
| 発注書ヘッダー V2                   | msdyn_purchaseorders                          |
| ソフトウェアによって削除された CDS 発注書明細行のエンティティ | msdyn_purchaseorderproducts                   |
| CDS 購買注文明細行エンティティ              | msdyn_purchaseorderproducts                   |
| 追跡用分析コード グループ                   | msdyn_producttrackingdimensiongroups          |
| スタイル                                      | msdyn_productstyles                           |
| 保管分析コード グループ                    | msdyn_productstoragedimensiongroups           |
| 製品固有の単位換算           | msdyn_productspecificunitofmeasureconversions |
| 製品の既定の注文設定 V2           | msdyn_productspecificdefaultordersettings     |
| サイズ                                       | msdyn_productsizes                            |
| 製品分析コード グループ                    | msdyn_productdimensiongroups                  |
| 既定の注文設定                      | msdyn_productdefaultordersettings             |
| 構成                              | msdyn_productconfigurations                   |
| すべての製品                                | msdyn_globalproducts                          |
| カラー                                      | msdyn_productcolors                           |
| 製品カテゴリ階層ロール            | msdyn_productcategoryhierarchyroles           |
| 製品カテゴリ階層                | msdyn_productcategoryhierarchies              |
| 製品カテゴリの割り当て                | msdyn_productcategoryassignments              |
| 製品カテゴリ                          | msdyn_productcategories                       |
| 倉庫の場所                         | msdyn_inventorylocations                      |
| 以下の CDS 在庫                            | msdyn_inventoryonhandentries                  |
| 製品カテゴリ                          | msdyn_productcategories                       |
| 以下の CDS 在庫                            | msdyn_inventoryonhandrequests                 |
| バーコードを識別した製品番号           | msdyn_productbarcodes                         |
| ロイヤルティ カード                                | msdyn_loyaltycards                            |
| ロイヤルティ報酬ポイント                       | msdyn_loyaltyrewardpoints                     |
| 価格顧客グループ                       | msdyn_pricecustomergroups                     |
| サイト                                       | msdyn_operationalsites                        |
| CDS 販売見積明細行                   | 見積詳細                                  |
| CDS 販売注文明細行                       | 販売注文詳細                             |

**依存関係情報**

Dual-write Supply Chain パッケージは、次の 3 つのパッケージによって異なります。 したがって、このパッケージは、Dual-write Supply Chain パッケージをインストールする前にインストールしておく必要があります。

- 二重書き込みアプリケーション コア パッケージ
- 二重書き込み Finance パッケージ
- Dual-write Human Resources パッケージ
- Dynamics 365 HR の共通テーブル

## <a name="dual-write-finance"></a>Dual-write Finance

二重書き込み Finance パッケージには、Dynamics 365 Finance データの同期に必要なソリューションとマップが含まれています。 次の 4 つのソリューションが含まれています。

| 固有の名前                            | 表示名                               |
|----------------------------------------|-------------------------------------------|
| Dynamics365FinanceExtended             | Dynamics 365 Finance Extended             |
| msdyn_Dynamics365FinanceExtendedMaps   | Dynamics 365 Finance Extended エンティティ マップ |
| FieldServiceCommon                     | Field Service Common                      |
| msdyn_Dynamics365FinanceExtendedAnchor | Dynamics 365 Finance Extended アンカー      |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用アプリ             | Customer Engagement アプリ        |
|-----------------------------------------|---------------------------------|
| 源泉徴収税グループ                  | msdyn_withholdingtaxgroups      |
| CDS Contacts V2 (顧客)              | 連絡先                        |
| CDS Contacts V2 (仕入先)                | 連絡先                        |
| 顧客 V3                            | 連絡先                        |
| 源泉徴収税コード                   | msdyn_withholdingtaxcodes       |
| 仕入先 V2                              | msdyn_vendors                   |
| 仕入先支払方法                   | msdyn_vendorpaymentmethods      |
| 仕入先グループ                           | msdyn_vendorgroups              |
| 勘定科目表                       | msdyn_chartofaccountses         |
| 消費税元帳転記グループ V2      | msdyn_taxpostinggroups          |
| 品目消費税グループ                    | msdyn_taxitemgroups             |
| 消費税グループ                        | msdyn_taxgroups                 |
| 消費税非課税コード エンティティ CDS        | msdyn_taxexemptcodes            |
| 顧客グループ                         | msdyn_customergroups            |
| 顧客支払方法                 | msdyn_customerpaymentmethods    |
| 財務分析コード                    | msdyn_dimensionattributes       |
| 消費税所轄官庁                   | msdyn_taxauthorities            |
| 財務分析コード形式              | msdyn_financialdimensionformats |
| 会計カレンダー期間                  | msdyn_fiscalcalendarperiods     |
| 会計カレンダー統合エンティティ      | msdyn_fiscalcalendars           |
| 会計暦年統合エンティティ | msdyn_fiscalcalendaryears       |
| 支払条件                        | msdyn_paymentterms              |
| 支払スケジュール                        | msdyn_paymentschedules          |
| 支払スケジュール行                  | msdyn_paymentschedulelines      |
| 支払期日 CDS                        | msdyn_paymentdays               |
| 支払期日明細行 CDS V2                | msdyn_paymentdaylines           |
| 主勘定                            | msdyn_mainaccounts              |
| 主勘定カテゴリ                 | msdyn_mainaccountcategories     |
| 会計                                  | msdyn_ledgers                   |
| 顧客 V3                            | 勘定                        |

**依存関係情報**

Dual-write Finance パッケージは、デュアル書き込みアプリケーション コア パッケージによって異なります。 したがって、Dual-write Application Core パッケージをインストールしてから、Dual-write Finance パッケージをインストールする必要があります。

## <a name="dual-write-notes"></a>Dual-write Notes

Dual-write Notes パッケージには、メモや注釈データの同期に必要なソリューションとマップが含まれています。 次の 4 つのソリューションが含まれています。

| 固有の名前                  | 表示名                   |
|------------------------------|--------------------------------|
| Dynamics365Notes             | Dynamics 365 Notes             |
| Dynamics365NotesExtended     | Dynamics 365 notes 拡張版    |
| msdyn_Dynamics365NotesMaps   | Dynamics 365 notes エンティティ マップ |
| msdyn_Dynamics365NotesAnchor | Dynamics 365 notes アンカー      |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用                     | Customer Engagement |
|--------------------------------------------|---------------------|
| 販売注文のヘッダー ドキュメント添付    | 注釈         |
| 顧客の添付ファイル                       | 注釈         |
| 仕入先ドキュメントの添付ファイル                | 注釈         |
| 発注書のヘッダー ドキュメントの添付ファイル | 注釈         |

**依存関係情報**

Dual-write Notes パッケージは、次の 2 つのパッケージによって異なります。 したがって、このパッケージは、Dual-write Notes パッケージをインストールする前にインストールしておく必要があります。

- 二重書き込みアプリケーション コア パッケージ
- 二重書き込み Finance パッケージ

## <a name="dual-write-asset-management"></a>Dual-write アセット マネジメント

Dual-write アセット マネジメントパッケージには、Supply Chain Management の資産データや Dynamics 365 Field Service を同期させるために必要なソリューションとマップが含まれています。 次の 4 つのソリューションが含まれています。

| 固有の名前                          | 表示名                              |
|--------------------------------------|-------------------------------------------|
| Dynamics365AssetManagement           | Dynamics 365 アセット マネジメント             |
| Dynamics365AssetManagementApp        | Dynamics365 アセット マネジメント アプリ          |
| msdyn_DualWriteAssetManagementMaps   | Dynamics 365 アセット マネジメント エンティティ マップ |
| msdyn_DualWriteAssetManagementAnchor | Dynamics 365 アセット マネジメント アンカー      |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用アプリ                           | Customer Engagement アプリ                |
|-------------------------------------------------------|-----------------------------------------|
| 資産管理の保証                             | msdyn_warranties                        |
| 資産管理モデル                               | msdyn_models                            |
| 資産管理メーカー                        | msdyn_manufacturers                     |
| 資産管理機能の場所のタイプ            | msdyn_functionallocationtypes           |
| 資産管理機能の場所                 | msdyn_functionallocations               |
| 資産管理機能の場所のライフサイクル状態 | msdyn_functionallocationlifecyclestates |
| 資産管理機能の場所のライフサイクル モデル | msdyn_functionallocationlifecyclemodels |
| 資産管理資産                               | msdyn_customerassets                    |
| 資産管理資産のタイプ                          | msdyn_customerassetcategories           |
| 資産管理資産のライフサイクル状態               | msdyn_assetlifecyclestates              |
| 資産管理資産のライフサイクル モデル               | msdyn_assetlifecyclemodels              |

**依存関係情報**

Dual-write アセット マネジメント パッケージは、デュアル書き込みアプリケーション コア パッケージによって異なります。 したがって、Dual-write Application Core パッケージをインストールしてから、Dual-write アセット マネジメント パッケージをインストールする必要があります。

## <a name="packages-required-for-project-operations"></a>Project Operations に必要なパッケージ
Project Operations は、次のパッケージに依存します。 したがって、このパッケージは、Project Operations をインストールする前にインストールしておく必要があります。

- 二重書き込みアプリケーション コア パッケージ
- 二重書き込み Finance パッケージ
- Dual-write Supply Chain パッケージ
- Dual-write アセット マネジメント パッケージ
- Dual-write Human Resources パッケージ

## <a name="dual-write-party-and-global-address-book-solutions"></a>二重書き込み当事者およびグローバル アドレス帳ソリューション

二重書き込み当事者パッケージおよびグローバル アドレス帳パッケージには、当事者データとグローバル アドレス帳データを同期するために必要な次のソリューションとマップが含まれています。 

| 固有の名前                       | 表示名                            |
|-----------------------------------|-----------------------------------------|
| 関係者                             | 関係者                                   |
| Dynamics365GABExtended            | Dynamics 365 GAB 拡張版               |
| Dynamics365GABDualWriteEntityMaps | Dynamics 365 GAB 二重書き込みエンティティ マップ |
| Dynamics365GABParty_Anchor        | Dynamics 365 GAB と当事者              |

このパッケージでは、以下のマップが利用可能です。

| 財務と運用アプリ | Customer Engagement アプリ | 
|-----------------------------|--------------------------|
| CDS 関係者 | msdyn_parties | 
| CDS の配送先の場所 | msdyn_postaladdresscollections | 
| CDS 住所履歴 V2 | msdyn_postaladdresses | 
| CDS 関係者の配送先の場所 | msdyn_partypostaladdresses | 
| 関係者の連絡先 V3 | msdyn_partyelectronicaddresses | 
| 顧客 V3 | 勘定 | 
| 顧客 V3 | 連絡先 | 
| 仕入先 V2 | msdyn_vendors | 
| 連絡担当者の肩書き | msdyn_salescontactpersontitles | 
| 結句 | msdyn_complimentaryclosings | 
| あいさつ文 | msdyn_salutations | 
| 意思決定ロール | msdyn_decisionmakingroles | 
| 雇用職務権限 | msdyn_employmentjobfunctions | 
| ロイヤルティ レベル | msdyn_loyaltylevels | 
| 個人の特徴タイプ | msdyn_personalcharactertypes | 
| 連絡先 V2 | msdyn_contactforparties | 
| CDS 販売見積ヘッダー | 見積 | 
| CDS 販売注文ヘッダー | 販売注文 | 
| 売上請求書ヘッダー V2 | 請求書 | 
| CDS 住所ロール | msdyn_addressroles |

**依存関係情報**

二重書き込み当事者およびグローバル アドレス帳ソリューションは、次の 3 つのパッケージに依存します。 したがって、このパッケージは、二重書き込み当事者パッケージおよびグローバル アドレス帳ソリューション パッケージをインストールする前にインストールしておく必要があります。

- 二重書き込みアプリケーション コア パッケージ
- 二重書き込み Finance パッケージ
- Dual-write Supply Chain パッケージ

