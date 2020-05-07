---
title: エンティティ依存関係チェーン (同期順序)
description: このトピックでは、初期データを作成するために従う必要がある同期の順序を指定します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 9ae14703941b97308bca5845eeac3eb9b181ae75
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275490"
---
# <a name="entity-dependency-chain-synchronization-order"></a>エンティティ依存関係チェーン (同期順序)

[!include [banner](../../includes/banner.md)]

このトピックでは、**初期同期** 機能で提供されるエンティティの依存関係を使用していない場合に、初期データを作成するために従う必要がある同期の順序を指定します。 **初期同期** を使用しない場合は、各エンティティ マップを個別に実行する必要があります。

## <a name="dynamics-365-supply-chain-management-entities"></a>Dynamics 365 Supply Chain Management エンティティ

Supply Chain Management の次に示すエンティティは有効化する順序でリストされています。

| 二重書き込みページのマッピング名 | Supply Chain Management のエンティティ メタデータ名 | Common Data Service のエンティティ メタデータ名 | 摘要 |
|---|---|---|---|
| 単位 ... uoms                                                                      | UnitOfMeasureEntity                                    | 単位                                          | |
| 単位換算 ... msdyn_unitofmeasureconversions                                 | UnitOfMeasureConversionEntity                          | msdyn_unitofmeasureconversion                | |
| すべての製品 ... msdyn_globalproducts                                               | EcoResEveryProductEntity                               | msdyn_globalproduct                          | |
| 製品分析コード グループ ... msdyn_productdimensiongroups                           | EcoResProductDimensionGroupEntity                      | msdyn_productdimensiongroup                  | |
| 保管分析コード グループ ... msdyn_productstoragedimensiongroups                    | EcoResStorageDimensionGroupEntity                      | msdyn_productstoragedimensiongroup           | |
| 追跡用分析コード グループ ... msdyn_producttrackingdimensiongroups                  | EcoResTrackingDimensionGroupEntity                     | msdyn_producttrackingdimensiongroup          | |
| 色 ... msdyn_productcolors                                                      | EcoResProductColorEntity                               | msdyn_productcolor                           | |
| サイズ ... msdyn_productsizes                                                        | EcoResProductSizeEntity                                | msdyn_productsize                            | |
| スタイル ... msdyn_productstyles                                                      | EcoResProductStyleEntity                               | msdyn_productstyle                           | |
| コンフィギュレーション ... msdyn_productconfigurations                                      | EcoResProductConfigurationEntity                       | msdyn_productconfiguration                   | |
| リリース済製品 V2 ... msdyn_sharedproductdetails                                 | EcoResReleasedProductV2Entity                          | msdyn_sharedproductdetail                    | |
| Common Data Service リリース済の特徴的製品 ... products                         | EcoResReleasedDistinctProductCommon Data ServiceEntity | 製品                                      | |
| 製品番号識別バーコード ... msdyn_productbarcodes                         | EcoResProductNumberIdentifiedBarcodeEntity             | msdyn_productbarcode                         | |
| 既定の注文設定 ... msdyn_productdefaultordersettings                        | InventProductDefaultOrderSettingsEntity                | msdyn_productdefaultordersetting             | |
| 製品の既定の注文設定 V2 ... msdyn_productspecificdefaultordersettings     | InventProductSpecificOrderSettingsV2Entity             | msdyn_productspecificdefaultordersetting     | |
| 製品固有の単位換算 ... msdyn_productspecificunitofmeasureconversions | EcoResProductSpecificUnitConversionEntity              | msdyn_productspecificunitofmeasureconversion | |
| サイト ... msdyn_operationalsites                                                    | InventOperationalSiteEntity                            | msdyn_operationalsite                        | |
| 倉庫 ... msdyn_warehouses                                                     | InventWarehouseEntity                                  | msdyn_warehouse                              | [注記 1](#scm-notes) を参照してください。 |
| 製品マスターの色 ... msdyn_sharedproductcolors                                 | EcoResProductMasterColorEntity                         | msdyn_sharedproductcolor                     | |
| 製品マスターのサイズ ... msdyn_sharedproductsizes                                   | EcoResProductMasterSizeEntity                          | msdyn_sharedproductsize                      | |
| 製品マスターのスタイル ... msdyn_sharedproductstyles                                 | EcoResProductMasterStyleEntity                         | msdyn_sharedproductstyle                     | |
| 製品マスターのコンフィギュレーション ... msdyn_sharedproductconfigurations                 | EcoResProductMasterConfigurationEntity                 | msdyn_sharedproductconfiguration             | |
| 製品カテゴリ ... msdyn_productcategories                                      | EcoResProductCategoryEntity                            | msdyn_productcategory                        | [注記 2](#scm-notes) を参照してください。 |
| 製品カテゴリの割り当て ... msdyn_productcategoryassignments                   | EcoResProductCategoryAssignmentEntity                  | msdyn_productcategoryassignment              | |
| 製品カテゴリ階層 ... msdyn_productcategoryhierarchies                   | EcoResProductCategoryHierarchyEntity                   | msdyn_productcategoryhierarchy               | |
| 製品カテゴリ階層ロール ... msdyn_productcategoryhierarchyroles            | EcoResProductCategoryHierarchyRoleEntity               | msdyn_productcategoryhierarchyrole           | |
| 通路 ... msdyn_warehouseaisles                                           | WMSWarehouseAisleEntity                                | msdyn_warehouseaisle                         | |
| 倉庫ゾーン ... msdyn_warehousezones                                            | WHSWarehouseZoneEntity                                 | msdyn_warehousezone                          | |
| 倉庫ゾーン グループ ... msdyn_warehousezonegroups                                 | WHSWarehouseZoneGroupEntity                            | msdyn_warehousezonegroup                     | |
| 倉庫の場所 ... msdyn_inventorylocations                                    | WMSWarehouseLocationEntity                             | msdyn_inventorylocation                      | [注記 3](#scm-notes) を参照してください。 |
| 倉庫作業ヘッダー ... msdyn_warehouseworkheaders                               | WHSWarehouseWorkHeaderEntity                           | msdyn_warehouseworkheader                    | |
| 倉庫の作業明細行 ... msdyn_warehouseworklines                                    | WHSWarehouseWorkLineEntity                             | msdyn_warehouseworklines                     | [注記 4](#scm-notes) を参照してください。 |
| 荷渡のモード ... msdyn_shipvias                                                | DlvDeliveryModeEntity                                  | msdyn_shipvias                               | |
| 配送条件 ... msdyn_termsofdeliveries                                       | DeliveryTermsEntity                                    | msdyn_termsofdelivery                        | |
| 販売注文元コード ... msdyn_salesorderorigins                                | SalesOrderOriginEntity                                 | msdyn_salesorderorigin                       | |
| Common Data Service 販売注文ヘッダー ... salesorders                             | SalesOrderHeaderCommon Data ServiceEntity              | salesorder                                   | |
| Common Data Service 販売注文明細行 ... salesorderdetails                         | SalesOrderLineCommon Data ServiceEntity                | 販売注文詳細                            | |
| Common Data Service 販売見積ヘッダー ... quotes                               | SalesQuotationHeaderCommon Data ServiceEntity          | 見積                                        | |
| Common Data Service 販売見積明細行 ... quotedetails                          | SalesQuotationLineCommon Data ServiceEntity            | QuoteDetails                                 | |
| 売上請求書ヘッダー V2 ... invoices                                               | SalesInvoiceHeaderV2Entity                             | 請求書                                      | |
| 売上請求書明細行 V2 ... invoicedetails                                           | SalesInvoiceLineV2Entity                               | invoicedetail                                | |

### <a name="mapping-specific-notes"></a><a id='scm-notes'></a>マッピング固有の注記

1. 自己依存関係により初回同期の実行が 2 回必要な場合があります。
2. 既定では親子関係により初期同期がオフになっています (「スマート」注文はプラットフォームで処理されません)。 このため既存の製品カテゴリを正しい順序 (最初にルート カテゴリ、次に子、次に子の子) で、手動で同期する必要があります (たとえばカテゴリ説明の更新)。 **製品情報管理 \> 設定 \> カテゴリと属性 \> カテゴリ階層** の順に移動します。 **カテゴリ階層** ページで各階層を選択して、そこにある製品カテゴリを確認できます。
3. 空の **ItemNumberInLocation** ルックアップ フィールドと、最初、2 番目、3 番目の追加の倉庫ゾーンのマッピングのため、初期同期が失敗します。 そのため現在こうしたマッピングは削除されます。
4. 空の **CaptureWeight** フィールドのマッピングのため、初期同期が失敗します。 そのため現在このマッピングは削除されます。

### <a name="setup-related-information"></a>設定に関する情報

+ Dynamics 365 のモデル駆動型アプリの **製品** エンティティでレコードを最初に作成する場合、そのレコードの状態は **ドラフト** です。 状態を **有効** に変更する場合は、モデル駆動型アプリから **設定 \> 管理 \> システム設定 \> 営業** に順に移動し、**有効な状態で製品を作成する** オプションを **はい** に設定します。
+ 二重書き込みを有効化する前に Dynamics 365 や Common Data Service のモデル駆動型アプリで **製品** エンティティにレコードを作成すると、こうしたレコードが **会社** を含むキー全体が Finance and Operations アプリのデータと一致する場合にのみ更新されます。
+ **製品** エンティティの同期は Finance and Operations アプリから Common Data Service への単方向のみです。 Dynamics 365 のモデル駆動型アプリで **製品** エンティティのマップされたフィールドを更新すると、Finance and Operations アプリから次の同期を行う際に更新が上書きされます。

### <a name="known-issues"></a>既知の問題

- Finance and Operations アプリで単位を削除する場合はエラーが発生します。 測定単位を Finance and Operations アプリから Common Data Service に同期すると、特定のクラスで最初の単位が基本単位として作成され、これは削除されません。

    **軽減策:** 最初に Common Data Service で単位を削除します。 その後、Finance and Operations アプリで削除できます。

- Common Data Service で運用サイトを削除するとエラーが発生します。 エラー メッセージの文言、「情報ログ: 警告: 基本住所を削除できません。警告: 次のデータ ソースの検証に失敗したためエンティティ レコードを削除できません: InventSiteLogisticsLocation (InventSiteLogisticsLocation)。」 このエラーの原因は Finance and Operations アプリのデータ エンティティの問題です。

    **軽減策:** このサイトを Finance and Operations アプリで削除できます。 その後、対応する二重書き込みマップが実行中の場合、このサイトは Common Data Service で削除されます。

## <a name="dynamics-365-finance-entities"></a>Dynamics 365 Finance エンティティ

次の Dynamics 365 Finance のエンティティは有効化すべき順序でリストされています。

| 二重書き込みページのマッピング名 | Finance のエンティティ メタデータ名 | Common Data Service のエンティティ メタデータ名 | 摘要 |
|---|---|---|---|
| 通貨 ... transactioncurrencies                                            | CurrencyEntity                              | 通貨                                   | |
| 為替レート タイプ ... msdyn_exchangeratetypes                                  | ExchangeRateTypeEntity                      | msdyn_exchangeratetype                     | |
| 為替レートの通貨ペア ... msdyn_currencyexchangeratepairs                 | ExchangeRateCurrencyPairEntity              | msdyn_currencyexchangeratepair             | |
| Common Data Service 為替レート ... msdyn_currencyexchangerates              | ExchangeRateCommon Data ServiceEntity       | msdyn_currencyexchangerate                 | [注記 1](#fin-notes) を参照してください。 |
| 会計カレンダー統合エンティティ ... msdyn_fiscalcalendars                    | FiscalCalendarEntity                        | msdyn_fiscalcalendar                       | |
| 会計カレンダー統合エンティティ ... msdyn_fiscalcalendaryears           | FiscalCalendarYearEntity                    | msdyn_fiscalcalendaryear                   | |
| 会計カレンダー期間 ... msdyn_fiscalcalendarperiods                          | FiscalPeriodEntity                          | msdyn_fiscalcalendarperiod                 | |
| 組織階層タイプ ... msdyn_internalorganizationhierarchytypes        | OMOrganizationHierarchyTypeEntity           | msdyn_internalorganizationhierarchytype    | [注記 1](#fin-notes) を参照してください。 |
| 組織階層の目的 ... msdyn_internalorganizationhierarchypurposes | OMOrganizationHierarchyPurposeEntity        | msdyn_internalorganizationhierarchypurpose | [注記 1](#fin-notes) を参照してください。 |
| 法人 ... msdyn_internalorganizations                                  | OMLegalEntity                               | msdyn_internalorganization                 | [注記 1](#fin-notes) を参照してください。 |
| 法人 ... cdm_companies                                                | OMLegalEntity                               | cdm_company                                | |
| 作業単位 ... msdyn_internalorganizations                                  | OMOperatingUnitEntity                       | msdyn_internalorganization                 | [注記 1](#fin-notes) を参照してください。 |
| 組織階層 - 公開 ... msdyn_internalorganizationhierarchies    | OMOrganizationHierarchyPublishedEntity      | msdyn_internalorganizationhierarchy        | [注記 1](#fin-notes) を参照してください。 |
| 名前の接辞 ... msdyn_nameaffixes                                              | DirNameAffixEntity                          | msdyn_nameaffix                            | |
| 支払期日 Common Data Service ... msdyn_paymentdays                          | PaymentDayCommon Data ServiceEntity         | msdyn_paymentday                           | |
| 支払期日明細行 Common Data Service V2 ... msdyn_paymentdaylines              | PaymentDayLineCommon Data ServiceV2Entity   | msdyn_paymentdayline                       | |
| 支払スケジュール ... msdyn_paymentschedules                                     | PaymentScheduleEntity                       | msdyn_paymentschedule                      | |
| 支払スケジュール明細行 ... msdyn_paymentschedulelines                           | PaymentScheduleLineEntity                   | msdyn_paymentscheduleline                  | |
| 支払条件 ... msdyn_paymentterms                                         | PaymentTermEntity                           | msdyn_paymentterm                          | |
| 顧客支払方法 ... msdyn_customerpaymentmethods                        | CustomerPaymentMethodEntity                 | msdyn_customerpaymentmethod                | |
| 仕入先支払方法 ... msdyn_vendorpaymentmethods                            | VendorPaymentMethodEntity                   | msdyn_vendorpaymentmethod                  | |
| 顧客グループ ... msdyn_customergroups                                        | CustCustomerGroupEntity                     | msdyn_customergroup                        | |
| 仕入先グループ ... msdyn_vendorgroups                                            | VendVendorGroupEntity                       | msdyn_vendorgroup                          | |
| 消費税グループ ... msdyn_taxgroups                                            | TaxGroupEntity                              | msdyn_taxgroup                             | |
| 品目消費税グループ ... msdyn_taxitemgroups                                   | TaxItemGroupEntity                          | msdyn_taxitemgroup                         | |
| 消費税元帳転記グループ V2 ... msdyn_taxpostinggroups                   | TaxPostingGroupEntityV2                     | msdyn_taxpostinggroup                      | |
| 消費税非課税コード エンティティ Common Data Service ... msdyn_taxexemptcodes       | TaxExemptCodeCommon Data ServiceEntity      | msdyn_taxexemptcode                        | |
| 消費税所轄官庁 ... msdyn_taxauthorities                                  | TaxAuthorityEntity                          | msdyn_taxauthority                         | |
| 消費税コード ... msdyn_taxcodes                                               | TaxCodeEntity                               | msdyn_taxcode                              | [注記 1](#fin-notes) を参照してください。 |
| 財務分析コード形式 ... msdyn_financialdimensionformats                  | DimensionIntegrationFormatEntity            | msdyn_financialdimensionformat             | |
| 財務分析コード ... msdyn_dimensionattributes                              | DimensionAttributeEntity                    | msdyn_dimensionattribute                   | |
| 源泉徴収税グループ ... msdyn_withholdingtaxgroups                           | TaxWithholdingGroupEntity                   | msdyn_withholdingtaxgroup                  | |
| 源泉徴収税コード ... msdyn_withholdingtaxcodes                             | TaxWithholdingTaxCodes                      | msdyn_withholdingtaxcode                   | |
| 勘定科目表 ... msdyn_chartofaccountses                                   | LedgerChartOfAccountsEntity                 | msdyn_chartofaccounts                      | |
| 元帳 ... msdyn_ledgers                                                        | LedgerEntity                                | msdyn_ledger                               | [注記 1](#fin-notes) を参照してください。 |
| 主勘定カテゴリ ... msdyn_mainaccountcategories                         | MainAccountCategoryEntity                   | msdyn_mainaccountcategory                  | |
| 主勘定 ... msdyn_mainaccounts                                             | MainAccountEntity                           | msdyn_mainaccount                          | |
| 顧客 V3 ... accounts                                                       | CustCustomerV3Entity                        | 勘定                                    | [注記 2](#fin-notes) を参照してください。 |
| 顧客 V3 ... contacts                                                       | CustCustomerV3Entity                        | 連絡                                    | [注記 3](#fin-notes) を参照してください。 |
| 仕入先 V2 ... msdyn_vendors                                                    | VendVendorV2Entity                          | msdyn_vendor                               | [注記 2](#fin-notes) を参照してください。 |
| Common Data Service 連絡先 V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | 連絡                                    | [注記 4](#fin-notes) を参照してください。 |
| Common Data Service 連絡先 V2 ... contacts                                    | smmContactPersonCommon Data ServiceV2Entity | 連絡                                    | [注記 5](#fin-notes) を参照してください。 |

### <a name="mapping-specific-notes"></a><a id='fin-notes'></a>マッピング固有の注記

1. Finance and Operations アプリから Common Data Service に一方向の同期を行います。
2. 自己依存関係により初回同期の実行が複数回必要な場合があります。 Common Data Service の **勘定** ページから勘定を作成する際は、必ず **顧客** を関係タイプとして選択してください。 初期同期中に **基本連絡先** フィールドで問題が発生した場合は、そのフィールドをマッピングから削除して初期同期を再度実行します。 初期同期が正常に完了したらマッピングを停止して **基本連絡先** フィールドを再度追加します。 次にマッピングを開始し、ここでは初期同期をスキップします。 **基本連絡先** フィールドの値は初期同期に含まれないので、値を手動で移行する必要があります。
3. **個人** タイプの顧客を作成する場合は、Common Data Service の **連絡先** ページで **販売可能** オプションを **はい** に設定してください。
4. このマッピングには顧客の連絡先をリンクするフィルターが両方向にあります。 マッピングの詳細を開いて **Sales.Contact** エンティティ名の横にあるフィルター ボタン (じょうごのアイコン) を選択し、ファイル条件に **msdyn_contactforvendor eq true and msdyn_sellable eq false** が含まれていることを確認します。
5. このマッピングには仕入先の連絡先をリンクするフィルターが両方向にあります。 マッピングの詳細を開いて **Sales.Contact** エンティティ名の横にあるフィルター ボタン (じょうごのアイコン) を選択し、フィルター条件に **msdyn_contactforvendor eq true and msdyn_sellable eq false** が含まれていることを確認します。 

## <a name="dynamics-365-human-resources-entities"></a>Dynamics 365 Human Resources エンティティ

次の Dynamics 365 Human Resources のエンティティは有効化すべき順序でリストされています。

| 二重書き込みページのマッピング名 | 人事管理のエンティティ メタデータ名 | Common Data Service のエンティティ メタデータ名 | 摘要 |
|---|---|---|---|
| cdm_jobfunction - ジョブ機能                                |                                   | cdm_jobfunction                  | |
| cdm_jobtypes - ジョブ タイプ                                      |                                   | cdm_jobtypes                     | |
| cdm_jobs - ジョブ                                               |                                   | cdm_jobs                         | |
| cdm_jobs - ジョブの詳細                                        |                                   | cdm_jobs                         | |
| cdm_positiontype - PositionType                               | HcmPositionTypeEntity             | cdm_positiontype                 | |
| cdm_jobpositions - 基本職位                              | HcmPositionBaseEntity             | cdm_jobposition                  | [注記 1](#hr-notes) を参照してください。 |
| cdm_jobposition - 職位の詳細                            | HcmPositionDetailEntity           | cdm_jobposition                  | [注記 1](#hr-notes) を参照してください。 |
| cdm_jobposition - 職位の期間                           | HcmPositionDurationEntity         | cdm_jobposition                  | [注記 1](#hr-notes) を参照してください。 |
| cdm_jobposition - 職位の階層                        | HcmPositionHierarchyEntity        | cdm_jobposition                  | [注記 1](#hr-notes) を参照してください。 |
| cdm_veteranstatus - 退役軍人状態                            |                                   | cdm_veteranstatus                | |
| cdm_ethnicorigin - 出身民族                              |                                   | cdm_ethnicorigin                 | |
| cdm_languagecode - 言語コード                              |                                   | cdm_languagecode                 | |
| cdm_worker - 作業者                                           | HcmWorkerEntity                   | cdm_worker                       | |
| cdm_employments - 雇用                                 |                                   | cdm_employments                  | |
| cdm_employments - 雇用詳細                           |                                   | cdm_employments                  | |
| cdm_positionworkerassignmentmaps - 職位作業者割り当て | HcmPositionWorkerAssignmentEntity | cdm_positionworkerassignmentmaps | [注記 2](#hr-notes) を参照してください。|

### <a name="mapping-specific-notes"></a><a id='hr-notes'></a>マッピング固有の注記

1. 1 つの Common Data Service エンティティを複数の Finance and Operations アプリ エンティティにマッピングしています。
2. このマッピングで自己参照が発生しています。

## <a name="asset-management-entities"></a>資産管理エンティティ

次の Dynamics 365 Supply Chain Management の資産管理エンティティは有効化すべき順序でリストされています。

| 二重書き込みページのマッピング名 | 資産管理のエンティティ メタデータ名 | Common Data Service のエンティティ メタデータ名 | 摘要 |
|---|---|---|---|
| FO.AssetManagementAssetLifecycleStates--Common Data Service.msdyn_assetlifecyclestates                           | 資産管理資産のライフサイクル状態               | msdyn_assetlifecyclestates               | |
| FO.AssetManagementAssetLifecycleModels--Common Data Service.msdyn_assetlifecyclemodels                           | 資産管理資産のライフサイクル モデル               | msdyn_assetlifecyclemodels               | |
| FO.AssetManagementFunctionalLocationLifecycleModels--Common Data Service.msdyn_functionallocationlifecyclemodels | 資産管理機能の場所のライフサイクル モデル | msdyn_functionallocationlifecyclemodels  | |
| FO.AssetManagementFunctionalLocationLifecycleStates--Common Data Service.msdyn_functionallocationlifecyclestates | 資産管理機能の場所のライフサイクル状態 | msdyn_functionallocationlifecyclestates  | |
| FO.AssetManagementAssetTypes--Common Data Service.msdyn_customerassetcategories                                  | 資産管理資産のタイプ                          | msdyn_customerassetcategories            | |
| FO.AssetManagementFunctionalLocationTypes--Common Data Service.msdyn_functionallocationtypes                     | 資産管理機能の場所のタイプ            | msdyn_functionallocationtypes            | |
| FO.AssetManagementFunctionalLocations--Common Data Service.msdyn_functionallocations                             | 資産管理機能の場所                 | msdyn_functionallocations                | [注記](#am-notes) を参照してください。 |
| FO.AssetManagementAssets--Common Data Service.msdyn_customerassets                                               | 資産管理資産                               | msdyn_customerassets                     | [注記](#am-notes) を参照してください。 |
| FO.AssetManagementManufacturers--Common Data Service.msdyn_manufacturers                                         | 資産管理メーカー                        | msdyn_manufacturers                      | |
| FO.AssetManagementModels--Common Data Service.msdyn_models                                                       | 資産管理モデル                               | msdyn_models                             | |
| FO.AssetManagementWarranty--Common Data Service.msdyn_warranties                                                 | 資産管理の保証                             | msdyn_warranties                         | |

### <a name="mapping-specific-notes"></a><a id='am-notes'></a>マッピング固有の注記

- 自己依存関係により初回同期の実行が複数回必要な場合があります。
