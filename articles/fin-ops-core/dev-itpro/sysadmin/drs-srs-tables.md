---
title: 重複レコード データ共有でサポートされるテーブル
description: この記事では、重複レコード データ共有でサポートされるテーブルについて説明します。 これは、展開において、参照およびグループ データを会社間で共有するためのメカニズムです。
author: RamaKrishnamoorthy
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: Platform update 1
ms.custom: 89071
ms.assetid: 0bbe7453-624f-4551-a1d0-842484067311
ms.search.form: SysDataSharingConfiguration
ms.openlocfilehash: 0d160ddc29e1c6227e93b3f7ed864ebcbdf2420d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272542"
---
# <a name="tables-supported-for-duplicate-record-data-sharing"></a>重複レコード データ共有でサポートされるテーブル
この記事では、重複レコード データ共有でサポートされるテーブルについて説明します。 重複レコード データ共有は、展開において、参照およびグループ データを会社間で共有するためのメカニズムです。 重複レコード データ共有ポリシーにテーブルを追加できる可能性がありますが、次の表に一覧表示されていないテーブルは正式にサポートされていません。

**Dynamics 365 Finance**

| **テーブル オブジェクト名**        | **テーブルの説明 (ラベル)**   |
|------------------------------|---------------------------------|
| AssetCondition               | 固定資産の状況           |
| BankCentralBankPurpose       | 支払目的コード           |
| BankChequeLayout             | レイアウトの確認                    |
| BankGroup                    | 銀行グループ                     |
| BankParameters               | 銀行パラメーター                 |
| BankTransType                | 銀行トランザクション タイプ           |
| CompanyNAFCode               | NAF コード                       |
| CredManAccountStatusTable    | 勘定状態                |
| CredManCollectionsGroupTable | 督促グループ               |
| CredManGroup                 | 与信管理グループ        |
| CredManReasonTable           | 理由テーブル                    |
| CustBankAccount              | 顧客の銀行口座          |
| CustCollectionLetterTable    | 督促状の設定         |
| CustDefaultLocation          | 顧客の既定の場所      |
| CustGroup                    | 顧客グループ                 |
| CustLedger                   | 顧客転記プロファイル       |
| CustPaymModeTable            | 支払方法 – 顧客  |
| CustStaticsGroup             | 統計グループ                |
| CustTable                    | 顧客                       |
| CustTradingPartnerCode       | 取引相手コード            |
| CustVendItemGroup            | 外部品目説明グループ |
| LedgerJournalName            | 仕訳帳名                 |
| LineOfBusiness               | 業種                |
| PaymDay                      | 支払期日                    |
| PaymDayLine                  | 支払期日明細行               |
| PaymSched                    | 支払スケジュール                |
| PaymSchedLine                | 支払スケジュール行          |
| PaymTerm                     | 支払条件                |
| ReasonTable                  | 理由                         |
| Tax1099Fields                | 1099 フィールド                     |
| VendExceptionGroup           | 仕入先例外グループ         |
| VendLedger                   | 仕入先転記プロファイル          |
| VendPriceToleranceGroup      | 仕入先価格許容範囲グループ   |

**税**

| **テーブル オブジェクト名**           | **テーブルの説明 (ラベル)** |
|---------------------------------|-------------------------------|
| TaxAuthorityAddress             | 所轄官庁                     |
| TaxAuthorityAddressRegistration | 所轄官庁登録番号 |
| TaxGroupHeading                 | 消費税グループの説明   |
| TaxItemGroupHeading             | 品目消費税グループ          |
| TaxParameters                   | 消費税パラメーター          |
| TaxPeriodHead                   | 消費税の期間の説明  |

**Dynamics 365 Supply Chain Management**

| **テーブル オブジェクト名**                        | **テーブルの説明 (ラベル)**                          |
|----------------------------------------------|--------------------------------------------------------|
| BarcodeSetup                                 | バーコード設定                                          |
| BOMCalcGroup                                 | 計算グループ                                     |
| BOMCostGroup                                 | 原価グループ                                             |
| CommissionCustomerGroup                      | コミッション顧客グループ                              |
| CommissionSalesGroup                         | コミッション売上グループ                                 |
| CommissionItemGroup                          | コミッション品目グループ                                  |
| CommissionSalesRep                           | コミッション販売担当者                                  |
| CustClassificationGroup                      | 顧客分類グループ                         |
| DlvMode                                      | 配送方法                                       |
| DlvReason                                    | 配送の理由                                     |
| DlvTerm                                      | 配送条件                                      |
| ForecastItemAllocation                       | 品目配賦キー                                   |
| InventBuyerGroup                             | 購入担当グループ                                           |
| InventCountingReasonCodePolicy               | 棚卸理由コード ポリシー                          |
| InventFiscalLIFOGroup                        | 会計年度 LIFO レポート グループ                            |
| InventItemGroup                              | 品目グループ                                            |
| InventItemPriceToleranceGroup                | 価格許容範囲品目グループ                            |
| InventJournalName                            | 在庫仕訳帳の名前                                |
| InventLocationInventCountingReasonCodePolicy | 倉庫に対する在庫棚卸理由コード ポリシー    |
| InventModelGroup                             | 品目モデル グループ                                      |
| InventNumGroup                               | 番号グループ                                          |
| InventOrderEntryDeadlineGroup                | 注文入力期限グループ                            |
| InventPackagingGroup                         | 梱包グループ                                         |
| InventProblemType                            | 問題タイプ                                          |
| InventProblemTypeSetup                       | 問題/不適合タイプの検証               |
| KittingGroupTable                            | キット グループ                                             |
| MarkupGroup                                  | 諸費用グループ                                         |
| PdsBatchAttrib                               | バッチ属性 (複数)                                       |
| PdsBatchAttribByAttribGroup                  | グループ属性                                       |
| PdsBatchAttribEnumValues                     | 属性列挙値                             |
| PdsBatchAttribGroup                          | バッチ属性グループ                                 |
| PdsCustRebateGroup                           | 顧客リベート グループ (複数)                                 |
| PdsDispositionMaster                         | バッチ状態マスター                               |
| PdsFreightGroup                              | 運賃配賦グループ                               |
| PdsItemRebateGroup                           | 品目リベート グループ                                      |
| PdsRebateProgramTMATable                     | TMA グループ                                             |
| PersonTitleTable                             | タイトル/職業                                     |
| PlSADRateGroup                               | 関税率グループ                                      |
| PriceDiscGroup                               | 価格グループ                                           |
| PriceDiscSmartRoundingGroup                  | 丸めバージョン                                       |
| PriceDiscSmartRoundingGroupCurrency          | 丸めバージョン番号                               |
| PriceDiscSmartRoundingRule                   | 端数処理ルール                                         |
| ProdGroup                                    | 生産グループ                                      |
| ProdPool                                     | 生産管理グループ                                       |
| PurchPool                                    | 購買管理グループ                                         |
| ReasonTable                                  | 理由                                                |
| ReqGroup                                     | 品目補充グループ                                   |
| ReqReduceKey                                 | 下方修正キー                                         |
| ReqReduceLine                                | 下方修正明細行                                        |
| ReqSitePolicy                                | マスター プラン サイト ポリシー                          |
| RetailBarcodeMaskCharacter                   | バーコード マスク文字                               |
| RetailBarcodeMaskSegment                     | バーコード マスク区分                                  |
| RetailBarcodeMaskTable                       | バーコード マスク                                          |
| RetailInventoryLevelProfile                  | 在庫レベルのプロファイル                                |
| RetailInventoryLevelProfileProcessingRange   | 在庫レベルの処理範囲                       |
| RetailInventoryLevelProfileRange             | 在庫レベルの範囲                                  |
| RetailPricingPriorityTable                   | 価格決定優先順位                                       |
| RetailSeasonTable                            | 時期                                                 |
| RevRecRevenueSchedule                        | 売上スケジュール                                      |
| RevRecRevenueScheduleDetail                  | 収益スケジュールの詳細                               |
| RouteCostCategory                            | 原価カテゴリ                                        |
| SalesOrigin                                  | 発注元コード                                     |
| SalesPool                                    | 注文管理グループ                                            |
| smmBusRelChainGroup                          | 会社グループ                                         |
| smmBusRelDefaultLocation                     | 見込顧客の既定の場所                             |
| smmBusRelSalesDistrictGroup                  | 販売地域                                        |
| smmBusRelSectorTable                         | 見込顧客部門テーブル                                  |
| smmBusRelSegmentGroup                        | 区分テーブル                                          |
| smmBusRelStatusGroup                         | ステータス テーブル                                           |
| smmBusRelSubSegmentGroup                     | 小区分テーブル                                       |
| smmBusRelTable                               | 見込顧客                                              |
| smmBusRelTypeGroup                           | タイプ テーブル                                             |
| smmBusSectorGroup                            | 業種テーブル                          |
| smmCharacterGroup                            | 連絡先の特徴                                     |
| smmContactGreetingsGroup                     | 結句                                    |
| smmContactInterest                           | 連絡先の関心事項                                      |
| smmContactIntroGroup                         | あいさつテキスト                                       |
| smmConvertedBusRel                           | 変換済見込顧客                                    |
| smmDecisionGroup                             | 意思決定テーブル                                         |
| smmFunctionGroup                             | 関数                                               |
| smmInterestGroup                             | 関心事項                                              |
| smmLeadPriorityTable                         | 潜在顧客の優先順位                                          |
| smmLeadRatingTable                           | 潜在顧客の評価                                            |
| smmLeadTable                                 | 潜在顧客                                                  |
| smmLeadTypeTable                             | 潜在顧客タイプ                                              |
| smmLoyaltyGroup                              | ロイヤルティ                                              |
| smmOpportunityTable                          | 営業案件                                          |
| smmQuotationProbabilityGroup                 | 受注の確度                                  |
| smmQuotationPrognosisGroup                   | 妥当性判断診断                                    |
| smmQuotationReasonGroup                      | 見積理由                                       |
| smmSalesUnit                                 | 販売管理単位                                 |
| smmSalesUnitMembers                          | 販売単位のメンバー                                     |
| smmSourceTypeOptions                         | ソース タイプ オプション                                     |
| smmSourceTypeTable                           | ソース タイプ                                            |
| SuppItemGroup                                | 提供品グループ                              |
| TAMItemVendRebateGroup                       | 品目リベート グループ (複数)                                     |
| TAMVendRebateGroup                           | 仕入先リベート グループ                                    |
| TMSBillingGroup                              | 請求グループ                                          |
| TMSBreakDetail                               | 分割の詳細                                           |
| TMSBreakMaster                               | ブレーク マスター                                           |
| TMSDlvTerm                                   | 輸送管理に関連する配送条件 |
| TMSNumberSequence                            | 番号順序                                       |
| TMSRateBase                                  | レート基準                                              |
| TMSRateBaseAssignment                        | レート基準の割り当て                                   |
| TMSRateBaseDetail                            | レート基準の詳細                                       |
| TMSRateBaseType                              | レート基準タイプ                                        |
| TMSRateBaseTypeField                         | "レート基準タイプ" フィールド                                   |
| TMSRateEngine                                | レート エンジン                                            |
| TMSRateMaster                                | レート マスター                                            |
| TMSTransitTimeDetail                         | 輸送時間の詳細                                    |
| TMSTransitTimeEngine                         | 輸送時間エンジン                                    |
| TMSTransitTimeField                          | 輸送時間フィールド                                     |
| TMSZoneEngine                                | ゾーン エンジン                                            |
| VendGroup                                    | 仕入先グループ                                          |
| WHSClusterProfile                            | クラスター プロファイル                                       |
| WHSClusterSort                               | クラスターの並べ替え                                        |
| WHSContainerAttributes                       | コンテナー属性                                   |
| WHSContainerGroup                            | コンテナー グループ                                       |
| WHSContainerGroupLine                        | コンテナー グループの詳細                                 |
| WHSDocumentRoutingLayout                     | ドキュメント回覧レイアウト                               |
| WHSFilterParm                                | 必要なフィルター                                       |
| WHSFilters                                   | 製品フィルター                                        |
| WHSLoadTemplate                              | 積荷テンプレート                                         |
| WHSLocationFormat                            | 場所形式                                       |
| WHSLocationFormatLine                        | 場所形式の詳細                                 |
| WHSLocationType                              | 在庫場所タイプ                                         |
| WHSLocDirHint                                | ディレクティブ コード                                        |
| WHSMovementType                              | 移動タイプ                                         |
| WHSPackageClass                              | 梱包クラス                                        |
| WHSPackSizeCategory                          | 梱包サイズ カテゴリ                                   |
| WHSPhysDimGroupTable                         | グループ別の現物分析コード                            |
| WHSRequestType                               | 要求タイプ:                                          |
| WHSUOMSeqGroupLine                           | 単位順序グループの詳細                             |
| WHSUOMSeqGroupTable                          | 単位順序グループ                                   |
| WHSWaveAttributes                            | ウェーブ属性                                        |
| WHSWaveLabelType                             | ウェーブ ラベルのタイプ                                        |
| WHSWorkClassTable                            | 作業クラス                                           |
| WHSWorkClassValidLocType                     | 有効なプット場所のタイプ                               |
| WHSWorkPool                                  | 作業プール                                             |
| WHSZone                                      | 倉庫ゾーン                                        |
| WHSZoneGroup                                 | 倉庫ゾーン グループ                                  |
| WorkCalendarDate                             | 作業時間                                          |
| WorkCalendarDateLine                         | 作業時間                                           |
| WorkCalendarTable                            | カレンダー                                               |
| WrkCtrProperty                               | プロパティ                                             |
| WrkCtrPropertyLine                           | プロパティ                                               |

**Dynamics 365 Project Operations**

| **テーブル オブジェクト名** | **テーブルの説明 (ラベル)** |
|-----------------------|-------------------------------|
| CategoryTable         | カテゴリ テーブル                |
| ProjLineProperty      | 明細行プロパティ                 |

**顧客および仕入先のマスター共有機能が有効になっている場合の追加のテーブル**

| **テーブル オブジェクト名**              | **テーブルの説明 (ラベル)**             | 
|------------------------------------|-------------------------------------------|
| BankConstantSymbol                 | 銀行の固定記号                     |
| BankCustPaymIdTable                | 支払 ID                                | 
| BankTransactionTypeGroupHeader     | 銀行トランザクション グループ                   |
| ContactPerson                      | 連絡先                                  |
| CreditCardCust                     | 顧客のクレジット カード                      |
| CustFineSetup_BR                   | ファイン コード                                |
| CustInterestSetup_BR               | 利息コード                            |
| CustomChequeLayout_BR              | 小切手のカスタム レイアウト                       |
| CustomsTariffCodeTable_IN          | 関税率コード                      |
| ExciseTariffCodes_IN               | 物品税税率コード                       |
| LvPaymTransCodes                   | 支払トランザクション コード                  |
| PaymentFormatCodeSets_W            | 支払フォーマット コード セット                  |
| RetailCustTable                    | 顧客 (小売)                        |
| RetailVendTable                    | 製品インポート仕入先の設定               |
| SalesTaxFormTypes_IN               | インドの売上税のフォーム タイプ                |
| smmResponsibilitiesEmpTable        | 職責の割り当て                |
| StatRepInterval                    | 統計                                |
| StatRepIntervalLine                | エイジング期間                             |
| TaxBranch                          | 納税支店                                |
| TaxComponentTable_IN               | 税コンポーネント (複数)                            |
| TaxInformationCustTable_IN         | 顧客の税情報               |
| TaxInformationVendTable_IN         | 仕入先の税情報                 |
| TaxLedgerAccountGroup_IN           | 税の元帳転記グループ                  |
| TaxVatNumTable                     | 課税控除番号テーブル                   |
| TaxWithholdComponentGroupTable_IN  | 源泉徴収税コンポーネント グループ          |
| TaxWithholdComponentTable_IN       | 源泉徴収税グループ コンポーネント                |
| TaxWithholdTable                   | 源泉徴収税コード                     |
| VendBankAccount                    | 仕入先の銀行口座                      |
| VendContractZakat_SA               | 契約社員                                |
| VendDefaultAccounts                | 仕入先の既定の勘定科目       |
| VendDefaultLocation                | 仕入先の既定の場所                   |
| VendFineSetup_BR                   | ファイン コード                                |
| VendInfoZakat_SA                   | 仕入先                                   | 
| VendInterestSetup_BR               | 利息コード                            |
| VendStateTaxID                     | 仕入先の州税 ID                      |
| VendTable                          | 仕入先                                   |

**使用可能な重複レコード データ共有のテンプレート**
<table>
<thead>
<tr class="header">
<th>LCS でのパッケージ名</th>
<th>データ共有ポリシー</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>テンプレートを共有する財務データ</td>
<td><ul>
<li>銀行パラメーター</li>
<li>仕訳元帳の名前</li>
<li>支払期日</li>
<li>支払スケジュール</li>
<li>支払条件</li>
<li>非課税コード</li>
</ul></td>
</tr>
<tr class="even">
<td>サプライ チェーン データ共有テンプレート</td>
<td><ul>
<li>バーコード パラメーター</li>
<li>バーコード設定</li>
<li>購入担当グループ</li>
<li>諸掛グループ</li>
<li>コミッション</li>
<li>出荷先コード</li>
<li>不適合タイプ</li>
<li>注文入力期限グループ</li>
<li>発注元コード</li>
<li>注文管理グループ</li>
<li>生産グループ</li>
<li>生産管理グループ</li>
<li>配送の理由</li>
<li>提供品グループ</li>
<li>配送条件</li>
<li>作業時間カレンダー</li>
</ul></td>
</tr>
</tbody>
</table>


## <a name="download-a-cross-company-data-sharing-template-from-lcs"></a>会社間データ 供給テンプレートを LCS からダウンロード
Lifecycle Services (LCS) から会社間データ共有のテンプレートをダウンロードするには、以下の手順を実行します。 
1.  LCS にサインインします。
2.  ホーム ページで、共有アセット ライブラリを選択します。
3.  資産タイプ リストで、データ パッケージを選択します。
4.  使用可能なデータ パッケージ ファイルのいずれかを選択してダウンロードします。
テンプレートの使用方法の詳細については、 [会社間で財務データの共有を構成する](../data-entities/tasks/configure-financial-cross-company-data-sharing.md) を参照してください。

## <a name="tables-supported-for-master-company-data-sharing"></a>マスター会社のデータ共有でサポートされているテーブル
マスター会社データ共有ポリシーにテーブルを追加できる可能性がありますが、次の表に一覧表示されていないテーブルは正式にサポートされていません。

**Dynamics 365 Finance**

| **テーブル オブジェクト名**          | **テーブルの説明 (ラベル)**   |
|--------------------------------|---------------------------------|
| AssetCondition                 | 固定資産の状況           |
| BankCentralBankPurpose         | 支払目的コード           |
| BankChequeLayout               | レイアウトの確認                    |
| BankGroup                      | 銀行グループ                     |
| BankParameters                 | 銀行パラメーター                 |
| BankTransType                  | 銀行トランザクション タイプ           |
| BankTransactionTypeGroupHeader | 銀行トランザクション グループ         |
| CompanyNAFCode                 | NAF コード                       |
| CreditCardCust                 | 顧客のクレジット カード            |
| CreditCardProcessors           | 支払サービス                |
| CreditCardTypeCurrency         | クレジット カードのタイプの通貨       |
| CreditCardTypeSetup            | クレジット カードのタイプの設定          |
| CredManAccountStatusTable      | 勘定状態                |
| CredManCollectionsGroupTable   | 督促グループ               |
| CredManGroup                   | 与信管理グループ        |
| CredManReasonTable             | 理由テーブル                    |
| CustBankAccount                | 顧客の銀行口座          |
| CustCollectionLetterTable      | 督促状の設定         |
| CustDefaultLocation            | 顧客の既定の場所      |
| CustGroup                      | 顧客グループ                 |
| CustLedger                     | 顧客転記プロファイル       |
| CustPaymModeTable              | 支払方法 – 顧客  |
| CustStaticsGroup               | 統計グループ                |
| CustTable                      | 顧客                       |
| CustTradingPartnerCode         | 取引相手コード            |
| CustVendItemGroup              | 外部品目説明グループ |
| LedgerJournalName              | 仕訳帳名                 |
| LineOfBusiness                 | 業種                |
| PaymDay                        | 支払期日                    |
| PaymDayLine                    | 支払期日明細行               |
| PaymSched                      | 支払スケジュール                |
| PaymSchedLine                  | 支払スケジュール行          |
| PaymTerm                       | 支払条件                |
| ReasonTable                    | 理由                         |
| ReasonTableRef                 | 理由の参照               |
| StatRepInterval                | 統計                      |
| StatRepIntervalLine            | エイジング期間                   |
| Tax1099Fields                  | 1099 フィールド                     |
| VendExceptionGroup             | 仕入先例外グループ         |
| VendLedger                     | 仕入先転記プロファイル          |
| VendPriceToleranceGroup        | 仕入先価格許容範囲グループ   |
| VendStateTaxID                 | 仕入先の州税 ID            |

**税**

| **テーブル オブジェクト名**           | **テーブルの説明 (ラベル)** |
|---------------------------------|-------------------------------|
| TaxAuthorityAddress             | 所轄官庁                     |
| TaxAuthorityAddressRegistration | 所轄官庁登録番号 |
| TaxGroupHeading                 | 消費税グループの説明   |
| TaxItemGroupHeading             | 品目消費税グループ          |
| TaxParameters                   | 消費税パラメーター          |
| TaxPeriodHead                   | 消費税の期間の説明  |

**Dynamics 365 Supply Chain Management**

| **テーブル名**                       | **テーブルの説明 (ラベル)**              |
|--------------------------------------|--------------------------------------------|
| BarcodeSetup                         | バーコード設定                              |
| ContactPerson                        | 連絡先                                   |
| CustClassificationGroup              | 顧客分類グループ             |
| DlvMode                              | 配送方法                           |
| DlvReason                            | 配送の理由                         |
| DlvTerm                              | 配送条件                          |
| InventProblemType                    | 問題タイプ                              |
| InventProblemTypeSetup               | 問題/ 不適合タイプの検証  |
| PriceDiscGroup                       | 価格グループ                               |
| PriceDiscSmartRoundingGroup          | 丸めバージョン                           |
| PriceDiscSmartRoundingGroupCurrency  | 丸めバージョン番号                   |
| PriceDiscSmartRoundingRule           | 端数処理ルール                             |
| smmBusRelDefaultLocation             | 見込顧客の既定の場所                 |
| smmBusRelSectorTable                 | 見込顧客部門テーブル                      |
| smmBusRelTable                       | 見込顧客                                  |
| smmLeadTable                         | 潜在顧客                                      |
| smmOpportunityTable                  | 営業案件                              |
| smmQuotationPrognosisGroup           | 妥当性判断診断                        |
| smmQuotationReasonGroup              | 見積理由                           |
| smmResponsibilitiesEmplTable         | 職責の割り当て                 |
| smmSalesUnit                         | 販売管理単位                     |
| smmSalesUnitMembers                  | 販売単位のメンバー                         |
| smmSourceTypeOptions                 | ソース タイプ オプション                         |
| smmSourceTypeTable                   | ソース タイプ                                |
| TAMVendRebateGroup                   | 仕入先リベート グループ                        |
| WorkCalendarDate                     | 作業時間                              |
| WorkCalendarDateLine                 | 作業時間                               |
| WorkCalendarTable                    | カレンダー                                   |
| WrkCtrPropertyLine                   | プロパティ                                   |

製品の会社間データ共有機能 (プライベート プレビュー) が有効になっている場合の、Supply Chain Management の追加テーブル。

>[!NOTE]
> 次のテーブルはマスター会社のデータ共有ポリシーに追加できますが、現在プライベート プレビューにある「製品の会社間データ共有」機能が有効になっている場合のみサポートされます。

| **テーブル名**                            | **テーブルの説明 (ラベル)**                  |
|-------------------------------------------|------------------------------------------------|
| InventStdCostConv                         | 標準原価換算                       |
| InventStdCostConvItem                     | 標準原価換算品目                 |
| 在庫テーブル                               | 品目                                          |
| InventTableInventCountingReasonCodePolicy | 品目に対する在庫棚卸理由コード ポリシー |
| InventTableModule                         | 在庫モジュール パラメーター                    |
| KittingInventTable                        | キット構造の管理                           |
| MCRInventTable                            | 在庫テーブル小売情報             |
| PdsBatchAttribByItem                      | 製品固有                               |
| RetailInventTable                         | 品目表                                     |
| TMSInventEnabled                          | 輸送品目番号                     |
| WarrantyInventTable                       | 保証品目                                 |
| WHSInventEnabled                          | 在庫管理品目の一覧             |
| WHSInventTable                            | 在庫品番号                          |
| WHSPhysDimUOM                             | 単位別の現物分析コード                     |

**Dynamcis 365 Project Operations**

| **テーブル オブジェクト名** | **テーブルの説明 (ラベル)** |
|-----------------------|-------------------------------|
| CategoryTable         | カテゴリ テーブル                |
| ProjLineProperty      | 明細行プロパティ                 |
