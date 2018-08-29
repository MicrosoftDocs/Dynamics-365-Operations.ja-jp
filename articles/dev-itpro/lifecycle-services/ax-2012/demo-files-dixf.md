---
title: "データ インポート/エクスポート フレームワーク (DIFX) のデモ ファイル"
description: "このトピックでは、データ インポート/エクスポート フレームワーク (DIXF)のデモ ファイルとそれに対応するエンティティの一覧を示します。"
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 29921
ms.assetid: 70033f55-eddd-4e5a-8f91-5e8670d104c5
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 2cdebfe3c9ec8ce44d845f6c5bcdeed733a3aacd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="demo-files-for-the-data-importexport-framework-dixf"></a>データ インポート/エクスポート フレームワーク (DIFX) のデモ ファイル

[!include [banner](../../includes/banner.md)]

デモ ファイルは、Microsoft Dynamics AX 2012 の Contoso デモデータと共に使用できます。 具体的には、ファイルは CEU Contoso Entertainment Systems (West) 会社と組み合わせて使用するためのものです。

## <a name="source-data-format-settings-for-demo-files"></a>デモ ファイルのソース データ形式設定
次のテーブルに、ソース データ形式に入力する必要のあるコンフィギュレーション設定を示します。

| 設定                         | 先頭値                                             |
|---------------------------------|---------------------------------------------------|
| **ファイル形式**                 | 区切り                                         |
| **先頭行のヘッダー**            | 選択済                                          |
| **行区切り**               | {CR}{LF}                                          |
| **列区切り**            | コンマ {,}                                         |
| **テキスト修飾子**              | "                                                 |
| **コード ページ**                   | 1252 西ヨーロッパ (Windows)                   |
| **Unicode**                     | 未選択                                      |
| **言語ロケール**             | ja                                             |
| **分析コード**              | CostCenter、Department、または ExpensePurpose を選択します。 |
| **勘定科目表の区切り記号** | -                                                 |



## <a name="file-list"></a>ファイル リスト
次のテーブルに、各エンティティに関連付けられているデモ ファイルを示します。

**名前**

**Dynamics AX バージョン**

**デモ ファイル**

AIF

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         AifInboundPortEntity ·         AifLookupEntryEntity ·         AifOutboundPortEntity ·         AIfWebSitesEntity ·         CustVendAIFPaymTableEntity

資産

Dynamics AX 2012

·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier

Microsoft Dynamics AX 2012 Feature Pack 

·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier

Microsoft Dynamics AX 2012 (InformationSource)

·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL ·         AssetParametersEntity

属性タイプ

Dynamics AX 2012

·         AttributeTypesEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         AttributeTypesEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         AttributeTypesEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         AttributeTypesEntity\_Basic

属性

Dynamics AX 2012

·         AttributeEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         AttributeEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         AttributeEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         AttributeEntity\_Basic

監査ポリシー

Dynamics AX 2012

·         AuditPolicyEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         AuditPolicyEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         AuditPolicyEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         AuditPolicyEntity\_Basic

銀行パラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         BankParametersEnitty

BarcodeSetup

Dynamics AX 2012

·         BarCodeSetupEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail

Microsoft Dynamics AX 2012 (InformationSource)

·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

バッチ グループ

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         BatchGroupEntity

BOM

Dynamics AX 2012

·         BOMEntity\_Basic ·         BOMEntity\_Enum

Microsoft Dynamics AX 2012 Feature Pack 

·         BOMEntity\_Basic ·         BOMEntity\_Enum

Microsoft Dynamics AX 2012 (InformationSource)

·         BOMEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         BOMEntity ·         BOMEntity\_Basic

BOMVersion

Dynamics AX 2012

·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum

Microsoft Dynamics AX 2012 Feature Pack 

·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum

Microsoft Dynamics AX 2012 (InformationSource)

·         BOMVersionEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         BOMVersionEntity ·         BOMVersionEntity\_Basic

予算

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         BudgetParametersEntity ·         BudgetTransactionLineEntity

ビジネス インテリジェンス

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         BIConfigruationEntity ·         BITimePeriodsMDXEntity

ケースのワークフロー

Dynamics AX 2012

·         CaseWorkFlowEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         CaseWorkFlowEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         CaseWorkFlowEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         CaseWorkFlowEntity\_Basic

カテゴリ階層

Dynamics AX 2012

·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic  

Microsoft Dynamics AX 2012 Feature Pack 

·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         EcoResAttributeEntity ·         EcoResAttributeTypeEntity ·         EcoResCategoryHierarchyEntity ·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity ·         EcoResCategoryHierarchyRoleEntity\_Basic

カテゴリ テーブル

Dynamics AX 2012

·         CategoryTableEntity\_Project

Microsoft Dynamics AX 2012 Feature Pack 

·         CategoryTableEntity\_Project

Microsoft Dynamics AX 2012 (InformationSource)

·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         CategoryTableEntity ·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH

勘定構造のコンフィギュレーション

Dynamics AX 2012

·         DimensionHierarchyEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         DimensionHierarchyEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         DimensionHierarchyEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         DimensionHierarchyEntity ·         DimensionHierarchyEntity\_Basic

  ContactPerson

Dynamics AX 2012

·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         ContactPersonAddressEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU

ContactPersonAddress

Dynamics AX 2012

·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues

Microsoft Dynamics AX 2012 Feature Pack 

·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues

Microsoft Dynamics AX 2012 (InformationSource)

·         ContactPersonAddressEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU

原価会計パラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         COSParametersEntity

  顧客

Dynamics AX 2012

·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums

Microsoft Dynamics AX 2012 Feature Pack 

·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums

Microsoft Dynamics AX 2012 (InformationSource)

·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU

顧客の住所

Dynamics AX 2012

·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues

Microsoft Dynamics AX 2012 Feature Pack 

·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues

Microsoft Dynamics AX 2012 (InformationSource)

·         CustomerAddressEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         CustomerAddressEntity ·         CustomerAddressEntity\_Basic

部門

Dynamics AX 2012

·         DepartmentEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         DepartmentEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         DepartmentEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         DepartmentEntity\_Basic

  分析コード

Dynamics AX 2012

·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum

Microsoft Dynamics AX 2012 Feature Pack 

·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum

Microsoft Dynamics AX 2012 (InformationSource)

·         DimensionsEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         DimensionAttributeValueEntity ·         DimensionsEntity\_Basic

  DocuType

Dynamics AX 2012

·         DocuTypeEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         DocuTypeEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         DocuTypeEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         DocuTypeEntity ·         DocuTypeEntity\_Basic ·         DocuTableEnabledEntity

  ドキュメント管理

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         CollabSiteParametersEntity ·         ContentTypeEntity

電子署名

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SIGParametersEntity

従業員

Dynamics AX 2012

·         EmployeeEntity\_Address ·         EmployeeEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         EmployeeEntity\_Address ·         EmployeeEntityBasic

Microsoft Dynamics AX 2012 (InformationSource)

·         EmployeeEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         EmployeeEntity ·         EmployeeEntity\_Basic

従業員の住所

Dynamics AX 2012

·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues

Microsoft Dynamics AX 2012 Feature Pack 

·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues

Microsoft Dynamics AX 2012 (InformationSource)

·         EmployeeAddressEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         EmployeeAddressEntity ·         EmployeeAddressEntity\_Basic

エンタープライズ ポータル

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         EPDocuParametersEntity

  環境的持続可能なパラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         EMSParameterEntity

経費精算書パラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvParametersEntity

経費精算書の委任

Dynamics AX 2012

·         TrvAppEmplSubEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvAppEmplSubEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvApEmplSubEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvAppEmplSubEntity\_Basic

経費精算書のコスト

Dynamics AX 2012

·         TrvCostTypeEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvCostTypeEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvCostTypeEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvCostTypeEntity\_Basic

経費精算書カテゴリ

Dynamics AX 2012

·         TrvExpSubCateogoryEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvExpSubCategoryEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvExpSubCategoryEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvExpSubCategoryEntity\_Basic

経費精算書の支払方法

Dynamics AX 2012

·         TrvPayMethodEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvPayMethodEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvPayMethodEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvPayMethodEntity\_Basic

経費精算書カテゴリのコード マッピング

Dynamics AX 2012

·         TrvPBSCatCodesEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvPBSCatCodesEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvPBSCatCodeEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvPBSCatCodesEntity\_Basic

経費精算書ポリシー

Dynamics AX 2012

·         TrvPolicyEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvPolicyEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvPolicyEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvPolicyEntity\_Basic

経費精算書の検証方法

Dynamics AX 2012

·         TrvValidatePaymentEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvValidatePaymentEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvValidatePaymentEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvValidatePaymentEntity\_Basic

対外貿易

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         InstrastatStatParametersEntity

グローバル アドレス帳パラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         DirParametersEntity

人事管理

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         HRMParametersEntity

棚卸資産

Dynamics AX 2012

·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration

Microsoft Dynamics AX 2012 Feature Pack 

·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration

Microsoft Dynamics AX 2012 (InformationSource)

·         InventJournalEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         InventJournalEntity ·         InventJournalEntity\_RU ·         InventParametersEntity ·         InventTableEntity

在庫在庫の計量単位

Dynamics AX 2012

·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum

Microsoft Dynamics AX 2012 Feature Pack 

·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum

Microsoft Dynamics AX 2012 (InformationSource)

·         UnitOfMeasureEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         UnitOfMeasureEntity ·         UnitOfMeasureEntity\_Basic

職務

Dynamics AX 2012

·         HcmJobDetailsEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         HcmJobDetailsEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         HcmJobDetailsEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         HcmJobDetailEntity ·         HcmJobDetailsEntity\_Basic ·         HcmPositionDetailEntity ·         HcmSharedParametersEntity

  Ledger

Dynamics AX 2012

·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal

Microsoft Dynamics AX 2012 Feature Pack 

·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal

Microsoft Dynamics AX 2012 (InformationSource)

·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU ·         LedgerParametersEntity

主勘定

Dynamics AX 2012

·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements

Microsoft Dynamics AX 2012 Feature Pack 

·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements

Microsoft Dynamics AX 2012 (InformationSource)

·         MainAccountEntity\_BR ·         MainAccountEntity\_ES

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         MainAccountEntity ·         MainAccountEntity\_BR ·         MainAccountEntity\_ES

マイレージ レート層

Dynamics AX 2012

·         TrvCostTypeRatesEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TrvCostTypeRatesEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TrvCostTypeRatesEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TrvCostTypeRatesEntity ·         TrvCostTypeRatesEntity\_Basic

整理番号

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         NumberSequenceTableEntity

Office アドイン

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         DocuDataSourceEntity

Operations リソース

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         WrkCtrParametersEntity

組織

Dynamics AX 2012

·         OrganizationHierarchyEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         OrganizationHierarchyEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         OrganizationHierarchyEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         OMHierarchyEntity ·         OMOperatingUnitEntity ·         OrganizationHierarchyEntity ·         OrganizationHierarchyEntity\_Basic

Outlook

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SmmParametersTableEntity ·         SysEmailParametersEntity

Payroll

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         PRLPayrollParametersEntity

ポリシー

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SysPolicySourceDocumentRuleEntity

職位

Dynamics AX 2012

·         PositionsEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         PostionsEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         PositionsEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         PositionsEntity\_Basic

PriceDiscount

Dynamics AX 2012

·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal

Microsoft Dynamics AX 2012 Feature Pack 

·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal

Microsoft Dynamics AX 2012 (InformationSource)

·         PriceDiscountEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         PriceDiscAdmTransEntity ·         PriceDiscountEntity\_RU

品目

Dynamics AX 2012

·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchaseSalesInvent

Microsoft Dynamics AX 2012 Feature Pack 

·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchSalesInvent

Microsoft Dynamics AX 2012 (InformationSource)

·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         ProdParametersEntity ·         ProductEntity ·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU ·         ProductMasterEntity

Project

Dynamics AX 2012

·         ProjectEtnity\_Basic ·         ProjectEntity\_Enum

Microsoft Dynamics AX 2012 Feature Pack 

·         ProjectEntity\_Basic ·         ProjectEntity\_Enum

Microsoft Dynamics AX 2012 (InformationSource)

·         ProjectEntity\_PSA

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         ProjectEntity\_PSA ·         ProjInvoiceTableEntity ·         ProjJournalTransEntity ·         ProjOnAccTransEntity ·         ProjServerSettingsEntity ·         ProjTableEntitySyncParametersEntity

ProjectHourJournal

Dynamics AX 2012

·         ProjectHourJournalEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         ProjectHourJournalEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         ProjectHourEntity\_PSA

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         ProjectHourEntity\_PSA

PurchLine

Dynamics AX 2012

·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2

Microsoft Dynamics AX 2012 Feature Pack 

·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2

Microsoft Dynamics AX 2012 (InformationSource)

·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT

PurchTable

Dynamics AX 2012

·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2

Microsoft Dynamics AX 2012 Feature Pack 

·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2

Microsoft Dynamics AX 2012 (InformationSource)

·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         PurchTableEntity ·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL

工順

Dynamics AX 2012

·         RouteEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         RouteEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         RouteEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         RouteEntity ·         RouteEntity\_Basic

工順工程

Dynamics AX 2012

·         RouteOperationsEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         RouteOperationsEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         RouteOperationsEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         RouteOperationsEntity ·         RouteOperationsEntity\_Basic

SalesLine

Dynamics AX 2012

·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader

Microsoft Dynamics AX 2012 Feature Pack 

·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader

Microsoft Dynamics AX 2012 (InformationSource)

·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SalesLineEntity ·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT

SalesTable

Dynamics AX 2012

·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1

Microsoft Dynamics AX 2012 Feature Pack 

·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1

Microsoft Dynamics AX 2012 (InformationSource)

·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SalesTableEntity ·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL

サービス管理

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SmaParametersEntity

サーバー コンフィギュレーション

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SysServerConfigEntity

共有カテゴリ

Dynamics AX 2012

·         SharedCategoryEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         SharedCaegoryEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         SharedCategoryEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SharedCategoryEntity ·         SharedCategoryEntity\_Basic

サーバー構成 SQL Server Reporting Services

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SRSReportDeploymentEntity ·         SRSServersEntity

定期売買パラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SubscriptionParametersEntity

システム パラメーター

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         SystemParametersEntity

TaxAuthorityAddress

Dynamics AX 2012

·         TaxAuthrorityAddressEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxAuthorityAddressEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxAuthorityAddressEntity\_BR ·         TaxAuthorityAddressEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxAuthorityAddressEntity ·         TaxAuthroityAddressEntity\_RU

TaxData

Dynamics AX 2012

·         TaxDataEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxDataEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxDataEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxDataEntity ·         TaxDataEntity\_Basic

TaxGroupData

Dynamics AX 2012

·         TaxGroupDataEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxGroupDataEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxGroupDataEntity\_BR

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxGroupDataEntity ·         TaxGroupDataEntity\_BR

TaxGroupHeading

Dynamics AX 2012

·         TaxGroupHeadingEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxGroupHeadingEntity\_\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxGroupHeadingEntity\_W

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxGroupHeadingEntity ·         TaxGroupHeadingEntity\_W

TaxItemGroupHeading

Dynamics AX 2012

·         TaxItemGroupHeadingEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxItemGroupHeadingEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxItemGroupHeadingEntity ·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN

TaxLedgerAccountGroup  

Dynamics AX 2012

·         TaxLedgerAccountGroupEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxLedgerAccountGroupEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxLedgerAccountGroupEntity ·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU

TaxOnItem

Dynamics AX 2012

·         TaxOnItemEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxOnItemEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxOnItemEntity ·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN

TaxParameters

Dynamics AX 2012

·         TaxParametersEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxParametersEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxParametersEntity ·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU

TaxPeriodHead

Dynamics AX 2012

·         TaxPeriodHeadEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxPeriodHeadEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxPeriodHeadEntity\_HU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxPeriodHeadEntity ·         TaxPeriodHead\_HU

TaxTable  

Dynamics AX 2012

·         TaxTableEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         TaxTableEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         TaxTableEntity ·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH

仕入先グループ

Dynamics AX 2012

·         VendGroupEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         VendGroupEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendGroupEntity ·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL

ベンダー

Dynamics AX 2012

·         VendorEntity\_Address ·         VendorEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         VendorEntity\_Address ·         VendorEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendorEntity ·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU

仕入先の住所

Dynamics AX 2012

·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MultipeAddressValues

Microsoft Dynamics AX 2012 Feature Pack 

·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MulitipleAddressValues

Microsoft Dynamics AX 2012 (InformationSource)

·         VendorAddressEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendorAddressEntity ·         VendorAddressEntity\_Basic

仕入先請求書ヘッダー  

Dynamics AX 2012

·         VendInvoiceInfoTableEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         VendInvoiceInfoTableEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         VendInvoiceInfoTableEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendInvoiceInfoTableEntity\_Basic

仕入先請求明細行    

Dynamics AX 2012

·         VendInvoiceInfoLineEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         VendInvoiceInfoLineEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         VendInvoiceInfoLineEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendInvoiceInfoLineEntity\_Basci

仕入先請求書テーブル

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendInvoiceInfoTableEntity ·         VendInvoiceInfoTableEntity\_Basic

仕入先請求書パラメーター  

Dynamics AX 2012

Microsoft Dynamics AX 2012 Feature Pack 

Microsoft Dynamics AX 2012 (InformationSource)

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         VendParametersEntity

作業カレンダー

Dynamics AX 2012

·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic

ワークフロー    

Dynamics AX 2012

·         WorkflowWorkItemQueueEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         WorkflowWorkItemQueueEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         WorkflowWorkItemQueueEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         WorkflowTableEntity ·         WorkflowWorkItemQueueEntity ·         WorkflowWorkItemQueueEntity\_basic

WorkTimeLine

Dynamics AX 2012

·         WorkTimeLineEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         WorkTimeLineEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         WorkTimeLineEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         WorkTimeLineEntity\_Basic

WorkTimeTable      

Dynamics AX 2012

·         WorkTimeTableEntity\_Basic

Microsoft Dynamics AX 2012 Feature Pack 

·         WorkTimeTableEntity\_Basic

Microsoft Dynamics AX 2012 (InformationSource)

·         WorkTimeTableEntity\_Basic

Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7

·         WorkTimeTableEntity\_Basic



## <a name="xml-demo-files"></a>XML デモ ファイル
次のファイルは、Microsoft Dynamics AX 2012 R2 および AX 2012 R3 の累積的な更新プログラム 7 と共に出荷されるデータ インポート/エクスポート フレームワークのバージョンで使用できます。

|                                   |                                   |
|-----------------------------------|-----------------------------------|
| AifInboundPortEntity              | ProjInvoiceTableEntity            |
| AifLookupEntryEntity              | ProjJournalTransEntity            |
| AifOutboundPortEntity             | ProjOnAccTransEntity              |
| AIfWebSitesEntity                 | ProjServerSettingsEntity          |
| AssetEntity                       | ProjTableEntity                   |
| AssetParametersEntity             | PurchLineEntity                   |
| BankParametersEntity              | PurchTableEntity                  |
| BarCodeSetupEntity                | RouteEntity                       |
| BatchGroupEntity                  | RouteOperationsEntity             |
| BIConfigurationEntity             | SalesLineEntity                   |
| BITimePeriodsMDXEntity            | SalesTableEntity                  |
| BOMEntity                         | SharedCategoryEntity              |
| BOMVersionEntity                  | SIGParametersEntity               |
| BudgetParametersEntity            | SmaParametersEntity               |
| BudgetTransactionLineEntity       | SmmParametersTableEntity          |
| CategoryTableEntity               | SRSReportDeploymentEntity         |
| CollabSiteParametersEntity        | SRSServersEntity                  |
| ContactPersonAddressEntity        | SubscriptionParametersEntity      |
| ContactPersonEntity               | SyncParametersEntity              |
| ContentTypeEntity                 | SysEmailParametersEntity          |
| COSParametersEntity               | SysPolicySourceDocumentRuleEntity |
| CustomerAddressEntity             | SysServerConfigEntity             |
| CustomerEntity                    | SystemParametersEntity            |
| CustVendAIFPaymTableEntity        | TaxAuthorityAddressEntity         |
| DimensionAttributeValueEntity     | TaxDataEntity                     |
| DimensionHierarchyEntity          | TaxGroupDataEntity                |
| DirParametersEntity               | TaxGroupHeadingEntity             |
| DocuDataSourceEntity              | TaxItemGroupHeadingEntity         |
| DocuTableEnabledEntity            | TaxLedgerAccountGroupEntity       |
| DocuTypeEntity                    | TaxOnItemEntity                   |
| EcoResAttributeEntity             | TaxParametersEntity               |
| EcoResAttributeTypeEntity         | TaxPeriodHeadEntity               |
| EcoResCategoryHierarchyEntity     | TaxTableEntity                    |
| EcoResCategoryHierarchyRoleEntity | TrvAppEmplSubEntity               |
| EmployeeAddressEntity             | TrvCostTypeEntity                 |
| EmployeeEntity                    | TrvCostTypeRatesEntity            |
| EMSParameterEntity                | TrvExpSubCategoryEntity           |
| EPDocuParametersEntity            | TrvParametersEntity               |
| HcmJobDetailEntity                | TrvPayMethodEntity                |
| HcmPositionDetailEntity           | TrvPBSCatCodesEntity              |
| HcmSharedParametersEntity         | TrvPolicyEntity                   |
| HRMParametersEntity               | TrvValidatePaymentEntity          |
| IntrastatStateParametersEntity    | UnitOfMeasureEntity               |
| InventJournalEntity               | VendGroupEntity                   |
| InventParametersEntity            | VendInvoiceInfoLineEntity         |
| InventTableEntity                 | VendInvoiceInfoTableEntity        |
| LedgerJournalEntity               | VendorAddressEntity               |
| LedgerParametersEntity            | VendorEntity                      |
| MainAccountEntity                 | VendParametersEntity              |
| OMHierarchyEntity                 | WorkCalendarDateEntity            |
| OMOperatingUnitEntity             | WorkCalendarDateLineEntity        |
| OrganizationHierarchyEntity       | WorkCalendarTableEntity           |
| PriceDiscAdmTransEntity           | WorkflowTableEntity               |
| PRLPayrollParametersEntity        | WorkflowWorkItemQueueEntity       |
| ProdParametersEntity              | WorkTimeLineEntity                |
| ProductEntity                     | WorkTimeTableEntity               |
| ProductMasterEntity               | WrkCtrParametersEntity            |






