---
title: "データのインポート/エクスポート フレームワーク (DIXF) のエンティティ"
description: "このトピックでは、データのインポート/エクスポート フレームワーク、各エンティティが関連付けられているアプリケーション モジュール、および各エンティティのクラス、ステージング テーブル、およびターゲットテーブルを使用してインポートできるエンティティを一覧表示します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18011
ms.assetid: 46b9d56e-8692-45af-8e86-22ec0192444f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 950a4f0d5b4cabe07f143ee357506b3c615a7101
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="data-importexport-framework-dixf-entities"></a>データのインポート/エクスポート フレームワーク (DIXF) のエンティティ

[!include [banner](../../includes/banner.md)]

このトピックでは、データのインポート/エクスポート フレームワーク、各エンティティが関連付けられているアプリケーション モジュール、および各エンティティのクラス、ステージング テーブル、およびターゲットテーブルを使用してインポートできるエンティティを一覧表示します。

|                                                                             |                        |                                         |                                      |                                          |
|-----------------------------------------------------------------------------|------------------------|-----------------------------------------|--------------------------------------|------------------------------------------|
| **エンティティ (エンティティ タイプ)**                                                     | **アプリケーション モジュール** | **エンティティ クラス**                        | **ステージング テーブル**                    | **ターゲット テーブル**                         |
| 顧客 (マスター データ)                                                       | 顧客               | DMFCustomerEntityClass                  | DMFCustomerEntity                    | DMFCustomerTargetEntity                  |
| 顧客の住所 (マスター データ)                                               | 顧客               | DMFCustomerAddressEntityClass           | DMFCustomerAddressEntity             | DMFCustomerAddressTargetEntity           |
| 電子支払の送信ポート (システム構成)                | 顧客               | DMFCustVendAifPaymTableEntityClass      | DMFCustVendAifPaymTableEntity        | DMFCustVendAifPaymTableTargetEntity      |
| 監査ポリシー (ドキュメント)                                                     | Expense                | DMFSysPolicySourceDocuRuleEntityClass   | DMFSysPolicySourceDocumentRuleEntity | DMFSysPolicySourceDocuRuleTargetEntity   |
| クレジット カード コード (参照データ)                                           | Expense                | DMFTrvPBSCatCodesEntityClass            | DMFTrvPBSCatCodesEntity              | DMFTrvPBSCatCodesTargetEntity            |
| デリゲート (設定)                                                            | Expense                | DMFTrvAppEmplSubEntityClass             | DMFTrvAppEmplSubEntity               | DMFTrvAppEmplSubTargetEntity             |
| 経費カテゴリ (設定)                                                     | Expense                | DMFTrvCostTypeEntityClass               | DMFTrvCostTypeEntity                 | DMFTrvCostTypeTargetEntity               |
| 経費サブカテゴリ (設定)                                                  | Expense                | DMFTrvExpSubCategoryEntityClass         | DMFTrvExpSubCategoryEntity           | DMFTrvExpSubCategoryTargetEntity         |
| マイレージ レート層 (設定)                                                   | Expense                | DMFTrvCostTypeRatesEntityClass          | DMFTrvCostTypeRatesEntity            | DMFTrvCostTypeRatesTargetEntity          |
| 支払メソッド (参照データ)                                              | Expense                | DMFTrvPayMethodEntityClass              | DMFTrvPayMethodEntity                | DMFTrvPayMethodTargetEntity              |
| 有効な支払メソッド (参照データ)                                       | Expense                | DMFTrvValidatePaymentEntityClass        | DMFTrvValidatePaymentEntity          | DMFTrvValidatePaymentTargetEntity        |
| アセット (マスター データ)                                                          | 固定資産           | DMFAssetEntityClass                     | DMFAssetEntity                       | DMFAssetTargetEntity                     |
| 従業員 (マスター データ)                                                       | 人事管理        | DMFEmployeeEntityClass                  | DMFEmployeeEntity                    | DMFEmployeeTargetEntity                  |
| 従業員の住所 (マスター データ)                                               | 人事管理        | DMFEmployeeAddressEntityClass           | DMFEmployeeAddressEntity             | DMFEmployeeAddressTargetEntity           |
| ジョブの詳細 (マスター データ)                                                     | 人事管理        | DMFHcmJobDetailEntityClass              | DMFHcmJobDetailEntity                | DMFHcmJobDetailTargetEntity              |
| 組織階層 (ドキュメント)                                           | 人事管理        | DMFOMHierarchyEntityClass               | DMFOMHierarchyEntity                 | DMFOMHierarchyTargetEntity               |
| 従業員パラメーター (パラメーター)                                             | 人事管理        | DMFHRMParametersEntityClass             | DMFHRMParametersEntity               | DMFHRMParametersTargetEntity             |
| 位置 (マスター データ)                                                      | 人事管理        | DMFHcmPositionDetailEntityClass         | DMFHcmPositionDetailEntity           | DMFHcmPositionDetailTargetEntity         |
| 共有人事管理パラメーター (パラメーター)                                | 人事管理        | DMFHCmSharedParametersEntityClass       | DMFHCmSharedParametersEntity         | DMFHCmSharedParametersTargetEntity       |
| バーコード設定 (設定)                                                        | 棚卸資産              | DMFBarcodeSetupEntityClass              | DMFBarcodeSetupEntity                | DMFBarcodeSetupTargetEntity              |
| カテゴリ テーブル (設定)                                                       | 棚卸資産              | DMFCategoryTableEntityClass             | DMFCategoryTableEntity               | DMFCategoryTableTargetEntity             |
| 在庫仕訳帳 (仕訳帳)                                                  | 棚卸資産              | DMFInventJournalEntityClass             | DMFInventJournalEntity               | DMFInventJournalTargetEntity             |
| 項目 (マスター データ)                                                          | 棚卸資産              | DMFInventTableEntityClass               | DMFInventTableEntity                 | DMFInventTableTargetEntity               |
| 価格割引協定仕訳帳 (仕訳)                                   | 棚卸資産              | DMFPriceDiscAdmTransEntityClass         | DMFPriceDiscAdmTransEntity           | DMFPriceDiscAdmTransTargetEntity         |
| 製品 (マスター データ)                                                        | 棚卸資産              | DMFProductEntityClass                   | DMFProductEntity                     | DMFProductTargetEntity                   |
| 製品属性 (設定)                                                    | 棚卸資産              | DMFEcoResAttributeEntityClass           | DMFEcoResAttributeEntity             | DMFEcoResAttributeTargetEntity           |
| 製品属性タイプ (設定)                                               | 棚卸資産              | DMFEcoResAttributeTypeEntityClass       | DMFEcoResAttributeTypeEntity         | DMFEcoResAttributeTypeTargetEntity       |
| 製品カテゴリ階層 (設定)                                           | 棚卸資産              | DMFEcoResCategoryHierarchyEntityClass   | DMFEcoResCategoryHierarchyEntity     | DMFEcoResCategoryHierarchyTargetEntity   |
| 製品カテゴリ階層ロール (設定)                                      | 棚卸資産              | DMFEcoResCategoryHierarcRoleEntityClass | DMFEcoResCategoryHierarchyRoleEntity | DMFEcoResCategoryHierarcRoleTargetEntity |
| 製品マスター (マスター データ)                                                 | 棚卸資産              | DMFProductMasterEntityClass             | DMFProductMasterEntity               | DMFProductMasterTargetEntity             |
| 分析コード (参照データ)                                                   | Ledger                 | DMFDimensionEntityClass                 | DMFDimensionAttributeValueEntity     | DMFDimensionAttributeValueTargetEntity   |
| 分析コード セット (設定)                                                        | Ledger                 | DMFDimensionHierarchyEntityClass        | DMFDimensionHierarchyEntity          | DMFDimensionHierarchyTargetEntity        |
| 元帳パラメーター (パラメーター)                                                | Ledger                 | DMFLedgerParametersEntityClass          | DMFLedgerParametersEntity            | DMFLedgerParametersTargetEntity          |
| 主勘定 (マスター データ)                                                   | Ledger                 | DMFMainAccountEntityClass               | DMFMainAccountEntity                 | DMFMainAccountTargetEntity               |
| 開始残高 (仕訳帳)                                                    | Ledger                 | DMFLedgerBalanceEntityClass             | DMFLedgerJournalEntity               | DMFLedgerJournalTransEntity              |
| 作業単位 (マスター データ)                                                 | Ledger                 | DMFOMOperatingUnitEntityClass           | DMFOMOperatingUnitEntity             | DMFOMOperatingUnitTargetEntity           |
| 給与パラメーター (パラメーター)                                                | Payroll                | DMFPRLPayrollParametersEntityClass      | DMFPRLPayrollParametersEntity        | DMFPRLPayrollParametersTargetEntity      |
| BOM (部品表) (マスター データ)                                        | 実稼働             | DMFBOMEntityClass                       | DMFBOMEntity                         | DMFBOMTargetEntity                       |
| BOM バージョン (マスター データ)                                                    | 実稼働             | DMFBOMVersionEntityClass                | DMFBOMVersionEntity                  | DMFBOMVersionTargetEntity                |
| 工順 (マスター データ)                                                          | 実稼働             | DMFRouteEntityClass                     | DMFRouteEntity                       | DMFRouteTargetEntity                     |
| 工順工程 (マスター データ)                                               | 実稼働             | DMFRouteOperationEntityClass            | DMFRouteOperationEntity              | DMFRouteOperationTragetEntity            |
| 予算パラメーター (パラメーター)                                                | Project                | DMFBudgetParametersEntityClass          | DMFBudgetParametersEntity            | DMFBudgetParametersTargetEntity          |
| 予算登録エントリ (ドキュメント)                                          | Project                | DMFBudgetEntityClass                    | DMFBudgetTransactionLineEntity       | DMFBudgetTransactionTargetEntity         |
| 分割払 (ドキュメント)                                                       | Project                | DMFProjOnAccTransEntityClass            | DMFProjOnAccTransEntity              | DMFProjOnAccTransTargetEntity            |
| プロジェクト (マスター データ)                                                        | Project                | DMFProjTableEntityClass                 | DMFProjTableEntity                   | DMFProjTableTargetEntity                 |
| プロジェクト契約 (ドキュメント)                                                | Project                | DMFProjInvoiceTableEntityClass          | DMFProjInvoiceTableEntity            | DMFProjInvoiceTableTargetEntity          |
| プロジェクト仕訳帳 (仕訳)                                                    | Project                | DMFProjJournalTransEntityClass          | DMFProjJournalTransEntity            | DMFProjJournalTransTargetEntity          |
| 作業時間カレンダー (セットアップ)                                               | Project                | DMFWorkCalendarTableEntityClass         | DMFWorkCalendarTableEntity           | DMFWorkCalendarTableTargetEntity         |
| 作業時間 (セットアップ)                                                        | Project                | DMFWorkCalendarDateEntityClass          | DMFWorkCalendarDateEntity            | DMFWorkCalendarDateTargetEntity          |
| 作業時間の明細行 (セットアップ)                                                   | Project                | DMFWorkCalendarDateLineEntityClass      | DMFWorkCalendarDateLineEntity        | DMFWorkCalendarDateLineTargetEntity      |
| 発注書ヘッダー (ドキュメント)                                            | 発注書         | DMFPurchTableEntityClass                | DMFPurchTableEntity                  | DMFPurchTableTargetEntity                |
| 発注書明細行 (ドキュメント)                                              | 発注書         | DMFPurchLineEntityClass                 | DMFPurchLineEntity                   | DMFPurchLineTargetEntity                 |
| 連絡先のアドレス (マスター データ)                                                | 販売とマーケティング    | DMFContactPersonAddressEntityClass      | DMFContactPersonAddressEntity        | DMFContactPersonAddressTargetEntity      |
| 連絡担当者 (マスター データ)                                                 | 販売とマーケティング    | DMFContactPersonEntityClass             | DMFContactPersonEntity               | DMFContactPersonTargetEntity             |
| 販売注文ヘッダー (ドキュメント)                                               | 販売注文            | DMFSalesTableEntityClass                | DMFSalesTableEntity                  | DMFSalesTableTargetEntity                |
| 販売注文明細行 (ドキュメント)                                                 | 販売注文            | DMFSalesLineEntityClass                 | DMFSalesLineEntity                   | DMFSalesLineTargetEntity                 |
| 品目消費税グループ (設定)                                                 | 消費税              | DMFTaxItemGroupHeadingEntityClass       | DMFTaxItemGroupHeadingEntity         | DMFTaxItemGroupHeadingTargetEntity       |
| 品目消費税グループの設定 (設定)                                           | 消費税              | DMFTaxOnItemEntityClass                 | DMFTaxOnItemEntity                   | DMFTaxOnItemTargetEntity                 |
| 元帳転記グループ (設定)                                                | 消費税              | DMFTaxLedgerAccountGroupEntityClass     | DMFTaxLedgerAccountGroupEntity       | DMFTaxLedgerAccountGroupTargetEntity     |
| 消費税コード (設定)                                                      | 消費税              | DMFTaxTableEntityClass                  | DMFTaxTableEntity                    | DMFTaxTableTargetEntity                  |
| 消費税の詳細 (設定)                                                    | 消費税              | DMFTaxDataEntityClass                   | DMFTaxDataEntity                     | DMFTaxDataTargetEntity                   |
| 消費税グループ (設定)                                                      | 消費税              | DMFTaxGroupDataEntityClass              | DMFTaxGroupDataEntity                | DMFTaxGroupDataTargetEntity              |
| 消費税グループ ヘッダー (設定)                                               | 消費税              | DMFTaxGroupHeadingEntityClass           | DMFTaxGroupHeadingEntity             | DMFTaxGroupHeadingTargetEntity           |
| 消費税パラメーター (パラメーター)                                             | 消費税              | DMFTaxParametersEntityClass             | DMFTaxParametersEntity               | DMFTaxParametersTargetEntity             |
| 消費税期間 (設定)                                                     | 消費税              | DMFTaxPeriodHeadEntityClass             | DMFTaxPeriodHeadEntity               | DMFTaxPeriodHeadTargetEntity             |
| 税所轄官庁 (設定)                                                        | 消費税              | DMFTaxAuthorityAddressEntityClass       | DMFTaxAuthorityAddressEntity         | DMFTaxAuthorityAddressTargetEntity       |
| 有効なドキュメント テーブル (設定)                                               | System                 | DMFDocuTableEnabledEntityClass          | DMFDocuTableEnabledEntity            | DMFDocuTableEnabledTargetEntity          |
| 承認仕入先リスト (参照データ)                                        | System                 | DMFPdsApprovedVendorListEntityClass     | DMFPdsApprovedVendorListEntity       | DMFPdsApprovedVendorListTargetEntity     |
| 品揃えヘッダー (ドキュメント)                                                | System                 | DMFRetailAssortmentHeaderEntityClass    | DMFRetailAssortmentHeaderEntity      | DMFRetailAssortmentHeaderTargetEntity    |
| 品揃え明細行 (ドキュメント)                                                  | System                 | DMFRetailAssortmentLineEntityClass      | DMFRetailAssortmentLineEntity        | DMFRetailAssortmentLineTargetEntity      |
| 品揃え (ドキュメント)                                                      | System                 | DMFRetailAssortmentPublishEntityClass   | DMFRetailAssortmentPublishEntity     | DMFRetailAssortmentHeaderTargetEntity    |
| 銀行パラメーター (パラメーター)                                                  | System                 | DMFBankParametersEntityClass            | DMFBankParametersEntity              | DMFBankParametersTargetEntity            |
| バーコード (設定)                                                              | System                 | DMFProductBarcodeEntityClass            | DMFProductBarcodeEntity              | DMFProductBarcodeTargetEntity            |
| バッチ グループ (システム構成)                                          | System                 | DMFbatchGroupEntityClass                | DMFbatchGroupEntity                  | DMFbatchGroupTargetEntity                |
| ビジネス インテリジェンス レポート サーバー (システム構成)                  | System                 | DMFSRSServersEntityClass                | DMFSRSServersEntity                  | DMFSRSServersTargetEntity                |
| カードの設定 (設定)                                                           | System                 | DMFRetailStoreTenderTypeCardEntityClass | DMFRetailStoreTenderTypeCardEntity   | DMFRetailStoreTenderTypeCardTargetEntity |
| カードのタイプ (設定)                                                            | System                 | DMFRetailTenderTypeCardEntityClass      | DMFRetailTenderTypeCardEntity        | DMFRetailTenderTypeCardTargetEntity      |
| ケース ワークフロー (ドキュメント)                                                    | System                 | DMFWorkflowTableEntityClass             | DMFWorkflowTableEntity               | DMFWorkflowTableTargetEntity             |
| 現金貨幣単位 (設定)                                                   | System                 | DMFStoreCashDeclarationEntityClass      | DMFStoreCashDeclarationEntity        | DMFStoreCashDeclarationTargetEntity      |
| カテゴリ (設定)                                                             | System                 | DMFEcoResCategoryEntityClass            | DMFEcoResCategoryEntity              | DMFEcoResCategoryTargetEntity            |
| コンフィギュレーション (システム コンフィギュレーション)                                         | System                 | DMFBIConfigurationEntityClass           | DMFBIConfigurationEntity             | DMFBIConfigurationTargetEntity           |
| コンテンツ タイプ (設定)                                                        | System                 | DMFContentTypeEntityClass               | DMFContentTypeEntity                 | DMFContentTypeTargetEntity               |
| 原価計算パラメーター (パラメーター)                                        | System                 | DMFCOSParametersEntityClass             | DMFCOSParametersEntity               | DMFCOSParametersTargetEntity             |
| デリバリー モード (設定)                                                        | System                 | DMFDlvModeEntityClass                   | DMFDlvModeEntity                     | DMFDlvModeTargetEntity                   |
| ドキュメント データ ソース (設定)                                                | System                 | DMFDocuDataSourceEntityClass            | DMFDocuDataSourceEntity              | DMFDocuDataSourceTargetEntity            |
| ドキュメント管理パラメータ (パラメータ)                                   | System                 | DMFDocuParametersEntityClass            | DMFDocuParametersEntity              | DMFDocuParametersTargetEntity            |
| ドキュメント タイプ (設定)                                                       | System                 | DMFDocuTypeEntityClass                  | DMFDocuTypeEntity                    | DMFDocuTypeTargetEntity                  |
| 電子署名のパラメーター (パラメーター)                                  | System                 | DMFSIGParametersEntityClass             | DMFSIGParametersEntity               | DMFSIGParametersTargetEntity             |
| 電子メール パラメーター (システム コンフィギュレーション                                       | System                 | DMFSysEmailParametersEntityClass        | DMFSysEmailParametersEntity          | DMFSysEmailParametersTargetEntity        |
|  Microsoft Dynamics AX ドキュメント パラメーター (Parameter) のエンタープライズ ポータル | System                 | DMFEPDocuParametersEntityClass          | DMFEPDocuParametersEntity            | DMFEPDocuParametersTargetEntity          |
| 環境パラメーター (パラメーター)                                         | System                 | DMFEMSParameterEntityClass              | DMFEMSParameterEntity                | DMFEMSParameterTargetEntity              |
| 経費ポリシー (ドキュメント)                                                   | System                 | DMFTrvPolicyRuleEntityClass             | DMFTrvPolicyRuleEntity               | DMFTrvPolicyRuleTargetEntity             |
| 固定資産パラメーター (パラメーター)                                           | System                 | DMFAssetParametersClass                 | DMFAssetParametersEntity             | DMFAssetParametersTargetEntity           |
| コラボレーション ワークスペースの一般設定 (システム構成)         | System                 | DMFCollabSiteParametersEntityClass      | DMFCollabSiteParametersEntity        | DMFCollabSiteParametersTargetEntity      |
| ギフト カード (ドキュメント)                                                         | System                 | DMFRetailGiftCardEntityClass            | DMFRetailGiftCardEntity              | DMFRetailGiftCardTargetEntity            |
| グローバル アドレス帳パラメータ (パラメータ)                                   | System                 | DMFDirParametersEntityClass             | DMFDirParametersEntity               | DMFDirParametersTargetEntity             |
| ハードウェア プロファイル (マスター データ)                                              | System                 | DMFRetailHardwareProfileEntityClass     | DMFRetailHardwareProfileEntity       | DMFRetailHardwareProfileTargetEntity     |
| 受信ポート (システム構成)                                          | System                 | DMFAifInboundPortEntityClass            | DMFAifInboundPortEntity              | DMFAifInboundPorEntity                   |
| イントラスタット コード (セットアップ)                                                       | System                 | DMFIntrastatStateParametersEntityClass  | DMFIntrastatStateParametersEntity    | DMFIntrastatStateParametersTargetEntity  |
| 在庫パラメーター (パラメーター)                                             | System                 | DMFInventParametersEntityClass          | DMFInventParametersEntity            | DMFInventParametersTargetEntity          |
| リンクされた製品 (設定)                                                       | System                 | DMFRetailLinkedProductEntityClass       | DMFRetailLinkedProductEntity         | DMFRetailLinkedProductTargetEntity       |
| ルックアップ エントリ (設定)                                                         | System                 | DMFAifLookupEntryEntityClass            | DMFAifLookupEntryEntity              | DMFAifLookupEntryTargetEntity            |
| Microsoft Project Server アプリケーション (設定)                                | System                 | DMFProjServerSettingsEntityClass        | DMFProjServerSettingsEntity          | DMFProjServerSettingsEntity              |
| 組み合わせ割引ヘッダー (ドキュメント)                                    | System                 | DMFRetailMixAndMatchEntityClass         | DMFRetailMixAndMatchEntity           | DMFRetailMixAndMatchTargetEntity         |
| 組み合わせ割引明細行 (ドキュメント)                                      | System                 | DMFRetailMixAndMatchLineEntityClass     | DMFRetailMixAndMatchLineEntity       | DMFRetailMixAndMatchLineTargetEntity     |
| 番号順序コード (マスター データ)                                           | System                 | DMFNumberSequenceTableEntityClass       | DMFNumberSequenceTableEntity         | DMFNumberSequenceTableTargetEntity       |
| 操作 (参照データ)                                                  | System                 | DMFRouteOprTableEntityClass             | DMFRouteOprTableEntity               | DMFRouteOprTableTargetEntity             |
| 組織階層 (ドキュメント)                                         | System                 | DMFOrganizationHierarchyEntityClass     | DMFOrganizationHierarchyEntity       | DMFOrganizationHierarchyTargetEntity     |
| 送信ポート (システム構成)                                         | System                 | DMFAifOutboundPortEntityClass           | DMFAifoutboundPortEntity             | DMFAifoutboundPorEntity                  |
| 関係者のリレーションシップ (セットアップ)                                                  | System                 | DMFDirPartyRelationshipEntityClass      | DMFDirPartyRelationshipEntity        | DMFDirPartyRelationshipTargetEntity      |
| 格納する支払方法 (セットアップ)                                              | System                 | DMFRetailStoreTenderTypeEntityClass     | DMFRetailStoreTenderTypeEntity       | DMFRetailStoreTenderTypeTargetEntity     |
| 価格グループ (設定)                                                         | System                 | DMFPriceDiscGroupEntityClass            | DMFPriceDiscGroupEntity              | DMFPriceDiscGroupTargetEntity            |
| 製品カテゴリ (設定)                                                     | System                 | DMFProductCategoryEntityClass           | DMFProductCategoryEntity             | DMFProductCategoryTargetEntity           |
| 製品分析コード グループ (設定)                                              | System                 | DMFProductDimensionGroupEntityClass     | DMFProductDimensionGroupEntity       | DMFProductDimensionGroupTargetEntity     |
| 製品受領書 (設定)                                                      | System                 | DMFProductReceiptEntityClass            | DMFProductReceiptEntity              | DMFProductReceiptTargetEntity            |
| 生産パラメーター (パラメーター)                                            | System                 | DMFprodparametersEntityClass            | DMFprodparametersEntity              | DMFprodparametersTargetEntity            |
| 関連する製品 (参照データ)                                            | System                 | DMFProductRelationEntityClass           | DMFProductRelationEntity             | DMFProductRelationTargetEntity           |
| レポート配置設定 (システム構成)                            | System                 | DMFSRSReportDeploymentEntityClass       | DMFSRSReportDeploymentEntity         | DMFSRSReportDeploymentTargetEntity       |
| リソース パラメーター (パラメーター)                                              | System                 | DMFWrkCtrParametersEntityClass          | DMFWrkCtrParametersEntity            | DMFWrkCtrParametersTargetEntity          |
| リソース要件 (参照データ)                                       | System                 | DMFWrkCtrActivityRequirementEntityClass | DMFWrkCtrActivityRequirementEntity   | DMFWrkCtrActivityRequirementTargetEntity |
| 工順関係 (参照データ)                                              | System                 | DMFRouteRelationEntityClass             | DMFRouteRelationEntity               | DMFRouteRelationTargetEntity             |
| 販売とマーケティング パラメーター (パラメーター)                                   | System                 | DMFsmmParametersTableEntityClass        | DMFsmmParametersTableEntity          | DMFsmmParametersTableTargetEntity        |
| スケジューラ パラメーター (パラメーター)                                             | System                 | DMFRetailConnParametersEntityClass      | DMFRetailConnParametersEntity        | DMFRetailConnParametersTargetEntity      |
| サーバー構成 (システム コンフィギュレーション)                                  | System                 | DMFSysServerConfigEntityClass           | DMFSysServerConfigEntity             | DMFSysServerConfigTargetEntity           |
| サービス管理パラメーター (パラメーター)                                    | System                 | DMFsmaParametersEntityClass             | DMFsmaParametersEntity               | DMFsmaParametersTargetEntity             |
| 共有カテゴリ (設定)                                                      | System                 | DMFSharedCategoryEntityClass            | DMFSharedCategoryEntity              | DMFSharedCategoryTargetEntity            |
| ストア (設定)                                                                | System                 | DMFRetailStoreEntityClass               | DMFRetailStoreEntity                 | DMFRetailStoreTargetEntity               |
| サブスクリプション パラメーター (パラメーター)                                          | System                 | DMFSMAParametersSubscriptionClass       | DMFSMAParametersSubscriptionEntity   | DMFSMAParametersSubscriptionTargetEntity |
| 同期パラメーター (パラメーター)                                       | System                 | DMFSyncParametersEntityClass            | DMFSyncParametersEntity              | DMFSyncParametersTargetEntity            |
| システム パラメーター (システム コンフィギュレーション)                                     | System                 | DMFSystemParametersEntityClass          | DMFSystemParametersEntity            | DMFSystemParametersTargetEntity          |
| Terminals(Setup)                                                            | System                 | DMFRetailTerminalEntityClass            | DMFRetailTerminalEntity              | DMFRetailTerminalTargetEntity            |
| 期間 (設定)                                                         | System                 | DMFBITimePeriodsMDXEntityClass          | DMFBITimePeriodsMDXEntity            | DMFBITimePeriodsMDXTargetEntity          |
| 時刻トランザクション (設定)                                                    | System                 | DMFWorkTimeLineEntityClass              | DMFWorkTimeLineEntity                | DMFWorkTimeLineTargetEntity              |
| 振替明細行 (仕訳帳)                                                     | System                 | DMFTransferOrderLineEntityClass         | DMFTransferOrderLineEntity           | DMFTransferOrderLineTargetEntity         |
| 移動オーダーの受信 (ドキュメント)                                           | System                 | DMFTransferOrderReceiveEntityClass      | DMFTransferOrderReceiveEntity        | DMFTransferOrderShipReceiveTargetEntity  |
| 移動オーダー出荷 (ドキュメント)                                          | System                 | DMFTransferOrderShipmentEntityClass     | DMFTransferOrderShipmentEntity       | DMFTransferOrderShipReceiveTargetEntity  |
| 移動オーダー (仕訳帳)                                                    | System                 | DMFTransferOrderEntityClass             | DMFTransferOrderEntity               | DMFTransferOrderTargetEntity             |
| 旅費交通費パラメーター (パラメーター)                                    | System                 | DMFTrvParametersClass                   | DMFTrvParametersEntity               | DMFTrvParametersTargetEntity             |
| 単位 (参照データ)                                                       | System                 | DMFUnitOfMeasureEntityClass             | DMFUnitOfMeasureEntity               | DMFUnitOfMeasureTragetEntity             |
| ユーザー情報 (マスター データ)                                               | System                 | DMFUserEntityClass                      | DMFUserEntity                        | DMFUserTargetEntity                      |
| バリアント(設定)                                                              | System                 | DMFProductVariantEntityClass            | DMFProductVariantEntity              | DMFProductVariantTargetEntity            |
| 仕入先パラメーター (パラメーター)                                                | System                 | DMFVendparametersEntityClass            | DMFVendparametersEntity              | DMFVendparametersTargetEntity            |
| Websites(システム構成)                                              | System                 | DMFAifWebsitesEntityClass               | DMFAifWebsitesEntity                 | DMFAifWebsitesTargetEntity               |
| ワークフロー作業項目キュー (セットアップ)                                             | System                 | DMFWorkflowWorkItemQueueEntityClass     | DMFWorkflowWorkItemQueueEntity       | DMFWorkflowWorkItemQueueTargetEntity     |
| 作業時間テンプレート (マスター データ)                                         | System                 | DMFWorkTimeTableEntityClass             | DMFWorkTimeTableEntity               | DMFWorkTimeTableTargetEntity             |
| 仕入先 (マスター データ)                                                         | ベンダー                 | DMFVendorEntityClass                    | DMFVendorEntity                      | DMFVendorTargetEntity                    |
| 仕入先のアドレス (マスター データ)                                                 | ベンダー                 | DMFVendorAddressEntityClass             | DMFVendorAddressEntity               | DMFVendorAddressTargetEntity             |
| 仕入先グループ (参照データ)                                               | ベンダー                 | DMFVendGroupEntityClass                 | DMFVendGroupEntity                   | DMFVendGroupTargetEntity                 |
| 仕入先請求書ヘッダー (ドキュメント)                                            | ベンダー                 | DMFVendInvoiceInfoTableEntityClass      | DMFVendInvoiceInfoTableEntity        | DMFVendInvoiceInfoTableTargetEntity      |
| 仕入先請求明細行 (ドキュメント)                                              | ベンダー                 | DMFVendInvoiceInfoLineEntityClass       | DMFVendInvoiceInfoLineEntity         | DMFVendInvoiceInfoLineTargetEntity       |






