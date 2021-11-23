---
title: Dynamics 365 for Finance and Operations バージョン 10.0.2 の拡張機能の変更
description: これのトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 に実装された拡張機能を一覧します。
author: FrankDahl
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-10
ms.dyn365.ops.version: App 10.0
ms.openlocfilehash: b1829498cec0c0a78289438b919e0a4bbaa634cf
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781895"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-1002"></a>Dynamics 365 for Finance and Operations バージョン 10.0.2 の拡張機能の変更

[!include [banner](../includes/banner.md)]

これのトピックでは、 Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.2 にて実装された拡張機能を記載しています。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

今回のアップデートで実装された拡張を以下に記載します。

- MarkupModuleType
- MCRCustPaymType
- PaymSchedBy

## <a name="sql-operations-made-extensible"></a>拡張可能になった SQL 操作

今回のアップデートでは、以下のSQL操作が拡張されました。

- JmgPayAdjustment.payAdjustLoop
- ProjPosting.ExtensionHash.New field
- WmsArrivalOverviewGeneration.buildPurch
- WmsArrivalOverviewGeneration.buildTransferOrder

## <a name="metadata-changes"></a>メタデータの変更

今回のアップデートで以下のメタデータが更新されました。

- CostSheetPercent.NoOfDecimalsIsExtensible
- WHSCycleCountingWarehouseWorkLineEntity.IsPublic

## <a name="refactored-methods"></a>リファクターされたメソッド

拡張性をサポートするために、以下のメソッドがリファクターされました。

- /Forms/ProjJournalTable/datasource/ProjJournalTable.initValue
- /Forms/PurchReqTable.instantiatePurchReqTableForm
- /Forms/PurchReqTable/DataSource/PurchReqTable.init
- /Forms/SalesQuotationProjLinkWizard/Controls/ProjInvoiceId.lookup
- /Tables/SalesTable.lastQuotation
- AccPolicyProductReceipt.isAccountingRequiredForSourceDocLine
- AssetFixedAssetEntity.overrideDataSource
- AssetProposalDepreciation.run
- AssetTableMethod.init
- BankAccountReconcile.validate
- Class\\BomCalcCost.calcCostModel
- Class\\MCRLoadContinuityCustInfo.insertLineData
- Class\\McrPriceHistoryUpdate.insertNewlyFoundReferences
- Class\\McrPriceHistoryUpdate.update
- Class\\McrPriceHistoryUpdate.updatePriceHistoryLineReferences
- Class\\ProjCopyItemEstimates.copyToItemRequirment
- Class\\PurchAutoCreate\_RFQ.createPurchOrderRFQLineReference
- Class\\ReqEventProcessDeleteUnusedKanban.deleteUnusedKanban
- Class\\ReqEventProcessDeleteUnusedKanban.run
- Class\\ReqTransUpdate.updateLogAddQty
- Class\\SalesCancelOrder.run
- Class\\SalesCreateOrderFromCustomer.main
- Class\\TAMVendRebateCorrectClaims.rebateAlreadyGiven
- Class\\tamVendRebateTableStatusType\_Approved.runPayment
- Class\\TamVendRebateTableStatusType\_Calculated.inserted
- Class\\TamVendRebateTableStatusType\_Calculated.runPayment
- Classes\\TaxWithhold.createAllTaxWithholdTrans
- Classes\\TaxWithhold.isCalculateTaxWithholdingNeeded\_TH
- Classes\\TaxWithhold.postTaxWithhold
- Classes\\TaxWithhold.totalInvoiceLineAmountSettled\_TH
- CustDirectDebitMandate.setDefaultMandate
- CustDueReportDetailDP.class declaration
- CustDueReportDetailDP.insertCustDueReportDetailTmp
- CustQuotationConfirmJour.printJournal
- CustVendCreatePaymJournal.pack
- CustVendCreatePaymJournal.parmHasBatchBeenSplit
- CustVendEditTaxBranch\_TH.init
- CustVendSumForPaym.run
- CustVendTransSettlement.post
- DimDerDistRuleSalesComplInvoice\_BR.createDimAllocForProjRevenue
- EcoResProductCreateExtended.SetAllowEditField
- EcoResProductVariantEntity.findDataSource
- FBSpedFileCreator\_Fiscal\_BR.createRecordC195
- Form\\ProdTableCreate.canContinueWithEmptyDim
- Form\\PurchCreateFromSalesOrder\\DataSource\\SalesLine.included
- Form\\PurchCreateFromSalesOrder\\DataSource\\SalesLine.specifyVendAccount
- Forms\\TaxWithholdTable.init
- FreeTextInvoiceDP.setSysDocuBrandDetails
- InventItemOrderSetupMap.checkNotStopped
- InventNonConformanceTable.InventNonConformanceTable.Create
- InventUpd\_Estimated.updateAutoDimBatchId
- InventUpdateReserveMore.InventUpdateReserveMore
- InventValueReportPopulateItem.updateReportLinePL
- JmgCalcApproveDateView.viewDate member
- JmgCalcApproveWeekView.viewDate member
- JmgPayAdjustment.payAdjustLoop
- LedgerJournalPeriodicCopy.journalTransCopy
- LedgerTransStatementDP.populateTempTableLedgerInStaging
- MCRCustpaym.validateWrite
- MCRFullTextSearch.buildSearchText
- MCRFullTextSearch.truncate
- MCRHoldCodeTrans.insert
- MCRHoldCodeTrans.setOrderStoppedFlag
- MCRHoldCodeTrans.unreserve
- McrPriceHistoryForm.calcPotential
- McrPriceHistoryForm.insertPotentialTradeAgreements
- PaymTerm.validateWrite
- PdsRebateAgreement.checkLineBreaks
- PdsRebateAgreement.groupChangeCheckValid
- PdsRebateAgreement.lineAmountHasGapOrOverlap
- PdsRebateAgreement.lineQuantityHasGapOrOverlap
- PdsRebateAgreementLine.selectRebateAgreementLineMax
- PriceDisc.mcrCalcPostageDisc
- PriceDiscLinePolicyRule.retrieveSystemPolicyFieldList
- ProdUpdCostEstimation.updateSubPurchLine
- ProjBudgetManager.createBudgetLineDetail
- ProjBudgetManager.getQuery
- ProjForecastCost.validateWrite
- ProjForecastEmpl.validateWrite
- ProjForecastRevenue.validateWrite
- ProjLedgerUpdate.insert
- ProjPlanVersionsManager.importHierarchy
- ProjPlanVersionsManager.importProjPlanVersionRecords
- ProjPost.PostCost
- ProjPost.PostCost
- ProjWorkBreakdownStructureHelper.addQuotationRelatedRecordsForTask
- ProjWorkBreakdownStructureHelper.Addtask
- ProjWorkBreakdownStructureHelper.Addtask
- ProjWorkBreakdownStructureHelper.Addtask
- ProjWorkBreakdownStructureV2FormHelper.IndentTaskV2
- ProjWorkBreakdownStructureV2FormHelper.MoveTasks
- PurchFormletterParmDataInvoice.createParmLinesAndTable
- PurchLine.delete
- PurchLine.distributionUpdateNeeded
- PurchLine.initFromPriceDisc
- PurchLine.insert
- PurchLine.update
- PurchLineType.statusChangeAllowed
- ReqEventProcessKanban.newStandard
- ReqTransNeutralTracker.trackReqTrans
- ReqTransPoMarkFirm.create
- 小売チャンネル: CartWorkflowHelper.AllowAggregation
- RetailEcoResProductReleaseManager\_Extension.setAndSaveRetailProductProperties
- RetailMassUpdateUploadDBManager.insertIntoProductProperty
- RetailPeriodicDiscount.validatePriceGroup
- RetailTransactionServiceCustomer.newCustomer
- RetailTransactionTransformer.ReadDiscountLines
- SalesInvoiceDP.setSysDocuBrandDetails
- SalesInvoiceJournalPost.run
- SalesInvoiceJournalPostBase.run
- SalesLine.CheckItemId
- Table\\InventTable.purchPriceAgreement
- Tables\\TaxWithholdTrans.copyTaxWithholdTrans, initFromTaxWithholdTable, insert, validateWrite, amountTotalWHT, existPeriod\_TH
- TAMVendRebatePaymentPost.main
- TAMVendRebateTableProcess.runProcess
- TrvPostExpenseHeader.postCustVendTransactions
- TrvPostExpenseHeader.postCustVendTransactions
- WhsControlLicensePlateId.process
- WhsLicensePlateLabelBuild.insertSingleLabelMenuItem
- WhsLicensePlateLabelBuild.insertSingleLabelPrintLine
- WhsrfControlData.processLegacyControl
- WhsWorkCreateProdPut.createReportFinishedParameters
- WhsWorkCreateProdPut.insertProdParmforCoByProduct
- WhsWorkCreateProdPut.insertProdParmForProdItem
- WhsWorkCreateProdPut.setAcceptError
- WHSWorkCreateReplenishment.checkExistingReplenWork
- WhsWorkExecuteDisplay.buildPick
- whsWorkExecuteDisplayInquiryLocation.buildLocationInquiry
- WmsArrivalOverviewGeneration.buildInventTransId
- WmsOrderTransType\_OutputDontPostTransfer.decreaseQty
- WmsOrderTransType\_OutputDontPostTransfer.increaseQtyOverdelivery

## <a name="other-extensibility-enhancements"></a>その他の拡張性の強化

- Classes\\BankPositivePayExport の accessmodifier が private から protected に変更されました。
- InventItemOrderSetupMap が拡張可能になりました。
- **小売チャンネル:** RetailTransactionViewのカスタムカラム。
- **小売チャンネル:** :サインイン要求の無効化ができます。
- **小売チャンネル:** 出荷ビュー拡張コントローラクラス。
- **小売チャンネル:** AddressAddEditView の [App Bar] ボタンの実装。
- **小売チャンネル:** ダイアログボックスで銀行預金額キーの無効化に対応。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]