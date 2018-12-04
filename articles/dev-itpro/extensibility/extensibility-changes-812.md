---
title: "Dynamics 365 for Finance and Operations バージョン 8.1.2 の拡張機能の変更"
description: "このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.1.2 でリリースされた拡張機能を一覧表示します。"
author: FrankDahl
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: App 8.1.2
ms.translationtype: HT
ms.sourcegitcommit: d6c7c2af4dc6088d03a214ae2b289aaaa7244100
ms.openlocfilehash: 8f5bbf27fea600262a020a97f95b5b975a28393b
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2018

---

# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-812"></a>Dynamics 365 for Finance and Operations バージョン 8.1.2 の拡張機能の変更

[!include [banner](../includes/banner.md)]

[!include [preview-banner](../includes/preview-banner.md)]

これは、Dynamics 365 for Finance and Operations バージョン 8.1.2 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

これらの列挙は、このアップデートで拡張可能になりました。

| 列挙型|
| --------------- |
|DimensionHierarchyType|
|DirPartyType|
|DirPersonMaritalStatus|
|PrintPostCancel|
|INSAffiliate|
|LedgerJournalLinesDisplayOption|
|LedgerTransPerJournal|
|ProjDortValue|
|ProjPaymentStatus|
|RequisitionReleaseType|
|RetailPOSSeedDataType|
|SysDimension|
|TrvExpType|
|TSTimesheetEntryGridView|
|VendProspectiveVendorRegistrationWizardTab

## <a name="metadata-changes"></a>メタデータの変更

これらのメタデータの変更は、このアップデートで行われました。

| 工程 |
| --------------- |
|DataEntities/LedgerJournalNameEntity/Fields/DeleteLinesAfterPosting.Allow Edit|
|DataEntities/LedgerJournalNameEntity/Fields/DeleteLinesAfterPosting.AllowEditOnCreate|
|Forms/AssetProposalDepreciation/Design/Tab/ParametersTabPage/ParametersGroup/SummarizedDepreciationControl.Value|
|Data manipulation method not raising event: PriceDiscAdmDeleteTradeAgreements.run|
|Data Types/Base Enums/WHSReverseWorkMode.Label|
|DataEntity smmProspectEntity はパブリックではありません|
|DataEntityView/GeneralJournalAccountEntryEntity.PublicCollectionName、PublicEntityName および IsPublic|
|Enum/HcmPersonGender/EnumValue/NonSpecific.Label|
|LedgerJournalEngine.shouldOverwriteAmountWithSettledAmount|
|Query/LedgerDerivedFinHierarchy/EcoResCategoryHierarchyRole_1/Ranges/NamedCategoryHierarchyRole.Range/Value|
|Table/TSTimesheetLine/TableFieldEnum|
|Tables/InventTransPosting.DateVoucherTransIdx|
|プロジェクトの価格決定テーブル内の固有のインデックスを更新します|

## <a name="refactored-methods"></a>リファクターされたメソッド

これらのメソッドは、拡張性をサポートするためにリファクターされています。

| リファクターされたメソッド                                                                             |
|------------------------------------------------------------------------------------------------|
|AgreementConfirmationDP.getAgreementLine|
|AgreementConfirmationDP.getAgreementLineHistory|
|AssetBook.initDepreciationProfile|
|AssetPost.createTrueUpDepreciation|
|AssetPost.reduceLastDepreciation|
|Bank_CA.checkBankAccount|
|Bank_CA.checkBankRegNum|
|BankReconMatchingRuleAutoProcessor.doProcessMatchRule|
|BankReconMatchingRuleAutoProcessor.performMatchAction|
|BomCalcItem.calcCostSheet|
|ChequeCopy.printCheque|
|ChequeDP.fetch|
|Coupons.AddCouponTrigger|
|Cust.initLedgerVoucher|
|CustAgingReportDP.heading|
|CustBalanceList.constructAgingCalculation|
|CustCollectionLetterCreate.createJournal|
|CustCollectionLetterCreate.run|
|CustCollectionLetterPost.updateQuery|
|CustCollections.showAgingIndicator|
|CustCollectionsExcelStatement.setTransactionWorksheetHeader|
|CustDirectDebitMandate.lookupReference|
|CustDirectDebitMandate.validateMandate|
|CustDirectDebitMandate.validateMandate|
|CustFreeInvoiceCorrection.createAdjustingCorrectedInvoice|
|CustFreeInvoiceCorrection.createTaxes|
|CustFreeInvoiceCorrectionPost.postAdjustingInvoice|
|CustFreeInvoiceCorrectionPost.validate|
|CustinvoiceLine.insert|
|CustInvoicePrintJob.buildQueryForFreeText|
|CustInvoicePrintJob.processFreeText|
|CustOpenTrans.editMarkTrans|
|CustOpenTransReverse.markTrans|
|CustOverPaym.run|
|CustPackingSlipJour.printJournal|
|CustPaymEntry.hasMultipleOpenTransReferences|
|CustPaymEntry.isInvalidOpenTransReference|
|CustPostInvoice.allocateNumAndVoucher|
|CustPostInvoice.createJournalHeader|
|CustRecurrenceInvoicePostService.postRecurrenceInvoice|
|CustSettlementPriorityProcessing.initCustTransOpen|
|CustStatistics.TmpStatPer.linkActive|
|CustTable.createRecord|
|CustTable.CustTable_DS/fields/CustGroup/modified|
|CustVendCheque.checkDataOk|
|CustVendCheque.output|
|CustVendChequeSlipTextCalculator.getMaxSlipLines|
|CustVendChequeSlipTextCalculator.getUnprintableReportArea|
|CustVendCreatePaymJournal.runPaymentProposalGenerationProcess|
|CustVendCreatePaymJournal.runPaymentProposalGenerationProcess|
|CustVendOpenTransManager.createTaxWithholding|
|CustVendPaymProposal.addCustVendTransOpen|
|CustVendReversePosting.restoreCustVendTransOpen|
|CustWriteOff.calcSalesTaxOnOpenTrans|
|CustWriteOff.generateSummarizedTmpTaxTrans|
|DataEntityView/ExpenseJournalLineEntity.DataEntityView/ExpenseJournalLineEntity|
|DirPartyPostalAddressFormHandlerExt.onUpdateTransactionCaller_delegate|
|拡張可能クラス メソッド: PriceDisc.mcrPriceDiscTableFound|
|FBSpedFileCreator_Contabil_BR.createRecordI052|
|FiscalDocumentDate_BR.lastIssueDateForSeries|
|HrpSigningLimitPolicyUtil.createDefaultLimit|
|HrpSigningLimitPolicyUtil.insertJobOrCompensationRule|
|HrpSigningLimitPolicyUtil.private RefRecId checkLimitAgreementDetail(HRPTmpLimitAgreementRule _tmpLimitAgreementRule,HRPAuthorityBasis _authorityBasis)|
|HrpWorkerLimit.private recId getAuthBaseRecId(HRPAuthorityBasis _authBasis, RefRecId _positionId)|
|InterCompanySyncPurchTableType.setSalesTableData|
|InventCountCreate_Base.doCountingBasedOnCountCode|
|InventMov_Purch.updateAutoLossProfit|
|InventMov_Purch.updateLedgerFinancial|
|InventMovement.addLedgerPhysicalAmounts|
|InventMovement.addLedgerVoucherRevenueTransactionAmountsForFinancialUpdate|
|InventMovement.addLedgerVoucherRevenueTransactionAmountsForPhysicalUpdate|
|InventMovement.addLedgerVoucherTransactionAmountsForFinancialUpdate|
|InventMovement.addLedgerVoucherTransactionAmountsForPhysicalUpdate|
|InventMovement.checkUpdatePhysical|
|InventMovement.processLedgerPhysicalAmountList|
|InventMovement.setAutoReserving|
|InventMovement.setCostAmountPhysical|
|InventMovement.updateLedgerAdjust|
|InventMovement.updateLedgerFinancial|
|InventOnhandReserve.updateReserveLot|
|InventUpd_Estimated|
|InventUpd_Estimated.updateFieldsChange|
|JmgPayEventsExport_Std.run|
|JmgStampJournalTable.approve|
|JmgStampJournalTable.transfer|
|LedgerAccrualTrans.post|
|LedgerAllocationBasisRules.createGeneralJournalAccountEntrySumQuery|
|LedgerAllocationController.allocateAmounts|
|LedgerAllocationProcessRequest.allocate|
|LedgerJournalCheckPost.checkJournal|
|LedgerJournalCheckPost.postJournal|
|LedgerJournalDistribute.createNewJournal|
|LedgerJournalEngine.calculateTaxForCompleteJournal|
|LedgerJournalEngine.initValue|
|LedgerJournalTable.deleteAllLines|
|LedgerJournalTrans.deleteTaxUncommitted|
|LedgerJournalTransDaily.LedgerJournalTrans.AmountCurCredit.validate|
|LedgerJournalTransDaily.LedgerJournalTrans.AmountCurDebit.validate|
|LedgerJournalTransType.validateVoucher|
|LedgerJournalTransUpdate.updateIntercompany|
|LedgerJournalTransVendPaym./Forms/LedgerJournalTransVendPaym/Design/ActionPane(ActionPane)/ButtonGroup(ButtonGroup)/buttonCreatePayment(MenuFunctionButton)/Clicked|
|LedgerTransListReportHelper.buildFieldMap|
|LedgerTransPerJournalDP.insertForLedgerBase|
|LedgerVoucherObject.checkBalance|
|LedgerVoucherObject.checkBalanceRound|
|LogisticsLocationFormHandler.callerResearch|
|LoyaltyCardBlance.MPOS_ExtensibleViews|
|Macros.InventSumFields|
|MainAccount.DimensionAttributeValue_ds/dimensionAttributeValueIsSuspended|
|NumberSeqModuleProject.loadModule|
|PcSourceDocumentLineUtility.initialize|
|PdsRebateFindAndCreate.findPdsRebateAgreementAndCreateClaim + run|
|PriceDisc.findPriceAgreement|
|PriceDisc.FindPriceAgreement.mcrPriceDiscTablefound|
|PriceDiscResultFields.NA|
|ProdJournalBOM.insertJournalCreate|
|ProjAdjustment.splitLine|
|ProjAdjustmentSplit.calculateQty|
|ProjAdjustmentSplit.getNewTotalSaleAmount|
|ProjAdjustmentUpdate.newPostAdjustment|
|ProjAdjustmentUpdate.run|
|ProjAdjustmentUpdate.transCostNew / transEmplNew / transItemNew メソッド|
|ProjAdjustmentUpdate.transItemNew|
|ProjAdjustmentUpdate.updateAdjusted|
|ProjBudgetImport.SourceType - 変更済み|
|ProjBudgetRevision.updateGridHelper|
|ProjectPosting.getProjectLedgerDimension|
|ProjForecastEmpl.initValue|
|ProjFormletterParmData.updateQueryBuild|
|ProjGrant.canSubmitToWorkflow|
|ProjInvoiceChoose.doCost|
|ProjInvoiceChoose.doEmpl|
|ProjInvoiceChoose.doItem|
|ProjInvoiceChoose.doOnAccount|
|ProjInvoiceChoose.doRevenue|
|ProjInvoiceChoose.doSalesLine|
|ProjInvoiceChoose.psaAddEndDateToProposalJour|
|ProjInvoiceEditLines.Choose.clicked|
|ProjInvoiceEditLines.closeOk|
|ProjInvoiceProposalCreateLines.modifiedTransFilter|
|ProjInvoiceProposalCreateLines.run|
|ProjInvoiceProposalCreateLines.runSalesLineQuery|
|ProjInvoiceProposalInsertLines.doSalesLine|
|ProjInvoiceProposalInsertLines.setProjProposalJour|
|ProjInvoiceTable.createProposalJour|
|ProjLedgerUpdate.insert|
|ProjListTransDP.insertTmpTable|
|ProjPostItemPackingSlip .projTransCreate|
|ProjPostItemTransCost_Adj.projTransUpdate|
|ProjSplitBill.maxAllowedByLimits|
|ProjStatusTypeRule.enableRule|
|ProjTable.isCustomerTransferNeeded|
|ProjTableType.validateWrite|
|ProjValCheckTrans.validateMandatory|
|PsaProjAndContractInvoiceController.runPrintMgmt|
|PSAProjRetainerInvoicing.createTrans|
|PSAProjRetainerInvoicing.run|
|PurchAutoCreate_PurchReq.getPurchLineName|
|PurchAutoCreate_Sales.createLine|
|PurchCopying.updatePriceDiscLineChangePolicy|
|PurchCreateFromSalesOrder.run|
|PurchCreateOrder.PurchTable.write|
|PurchEditLines.Choose_Button.clicked|
|PurchEditLines.run|
|PurchFormLetter.prePromptInit|
|PurchFormLetter.reSelect|
|PurchFormLetter::main|
|PurchFormletterParmDataInvoice.reSelectLines|
|PurchInvoiceJournalCreate.allocateNumAndVoucher|
|PurchReqAddItem.N/A: 変数の変更 (メソッドではなく)|
|PurchRFQCaseTable.isCalledFromPurchRFQCTListPageProject|
|PurchTable.ConvertCurrencyCode|
|PurchTable.create|
|PurchTable.create (PurchTable データ ソース)|
|PurchTableType.validateDelete|
|ReqCalc.actionCalcItem|
|ReqCalc.covCalcDim|
|ReqCalc.covCodeQtyMinMax|
|ReqCalc.covCreatePlannedOrder|
|ReqCalc.covCreateSafetyInvent|
|ReqCalc.createSafetyInvent|
|ReqCalc.createSafetyInventKey|
|ReqCalc.deleteTransactionAndCoverage|
|ReqCalc.setParameters|
|ReqCalc.writeInventSum|
|ReqTransCache.listCovDimSorted|
|ReqTransPoMarkFirm.create|
|RequisitionPurchaseOrderGeneration.updateEmptyVendAccountsForManualCreation|
|RequisitionPurchaseOrderGeneration.validatePurchReqLine|
|RetailInternalOrganization.insert|
|RetailKitAssemblyOrder.createOrUpdateBOMJournal|
|RetailKitAssemblyOrder.createOrUpdateBOMJournalLine|
|RetailStatementPost.postRetailSpecific|
|RetailStoresToDeploy.setAllowEditTrue|
|RetailTransactionSalesTransMark.findInventDimIdFromWorkingTable|
|RetailTransactionSalesTransMark.populateTransactionSalesLineWorkingTable|
|RetailTransactionServiceOrders.cancelCustomerOrder|
|RetailTransactionServiceOrders.createCustomerOrder|
|RetailTransactionServiceOrders.createLedgerJournalTransForPayment|
|RetailTransactionServiceOrders.createRetailOrderPayment|
|RetailTransactionServiceOrders.invoiceSalesOrder|
|RetailTransactionServiceOrders.settleCustomerOrder|
|SalesCopying.canClose|
|SalesCreateOrder.updateDeliveryAddress|
|SalesFormLetter.main|
|SalesFormLetter.mainOnServer|
|SalesFormLetter.reSelect|
|SalesInvoiceJournalCreateBase.createJournalHeader|
|SalesInvoiceJournalPostBase.postLine|
|SalesInvoiceJournalPostBase.updateInventory|
|SalesLine.createLinesFromTmpFrmVirtual|
|SalesLine.runPriceDiscPolicyDialog|
|SalesLineType_ProjectSales.canBeInvoiced|
|SalesPurchLine.setPriceAgreement|
|SalesPurchLineInterface.setPriceAgreement|
|SalesPurchLineInterface.setPriceDisc|
|SalesQuotationEditLinesForm メソッド createParmLine|
|SalesQuotationListPageInteraction.linkActive|
|SalesQuotationProjLinkWizard.endUpdate|
|SalesQuotationTable.convertCurrencyCode|
|SalesQuotationTable.modified (SalesQuotationLine_ItemId フォーム コントロール)|
|SalesQuotationTableType.numberSeqFormHandlerQuotationId|
|SalesQuotationTransferToProject.createForecastOnAcc|
|SalesQuotationTransferToProject.createProject|
|SalesTable.convertCurrencyCode|
|SalesTable.modified|
|SalesTable.updateDeliveryAddress|
|SmaServiceFunctionLine.getFromDialog|
|smmBusRelTable.updateCustTable|
|smmBusRelTable.updateVendTable|
|SourceDocumentBalanceProvider.calculateEncumberedAmount|
|Table/MyAddressBook.xds|
|Table/TrvExpTrans.update|
|Tax.allocateInTaxWorkTrans|
|TaxCalculationJournal.saveTaxTransfer|
|TaxCashDisc.calcAndInsertTaxes|
|TaxData.find|
|TaxInventTransferInvoice_BR.post|
|TaxReversePrePayment.calcPostAndInsertTaxes|
|TaxReverseTax.insertTaxWorkTrans|
|TaxReverseTax.newTrans|
|TaxSettlement.retailCalcAndInsertTaxes|
|TaxWithHold.createTaxWithholdTrans|
|TaxWithhold.postTaxWithhold|
|TransactionReversal.updateTaxTrans|
|TransactionReversal_Vend.reversal|
|TransactionTxt.setKey1|
|TransactionTxt.setKey2|
|TransactionTxt.setKey3|
|TrvExpTrans.insertPerDiemDataLines|
|TrvPbsMainDataLines.clicked|
|TrvPostExpenseHeader.postCustVendTransactions|
|TSTimesheetTrans.getCostPrice|
|VendOutPaym_Cheque.generatePaymentLines|
|VendOutPaym_RBC.generatePaymentLines|
|VendOutPaymRecord_RBC_Credit.fillField03|
|VendOutPaymRecord_RBC_Credit.fillField07|
|WhsControlItemId.populate|
|WHSCycleCountCreatePlan.insertWorkLine|
|WHSLoadLineAllocationProcessor.validateBatchDisposition|
|WhsLoadLineUpdater.initLoadLine|
|WHSMobileAppServiceXMLTranslator.createXML|
|WHSPack.packFromScanningFields|
|WhsrfControlData.allowMixedBatch|
|WhsrfControlData.allowMixedItem|
|WHSRFControlData.processLegacyControl|
|WhsWorkExecuteDisplay.buildGetVendBatchDetails|
|WHSWorkExecuteDisplay.buildLPControlFromPass|
|WHSWorkExecuteDisplay.buildPORecTrackingDimensions|
|WHSWorkExecuteDisplay.buildRemainingReceiptQtyCurrentLPLabel|
|WHSWorkExecuteDisplay.buildTrackingDimensions|
|WHSWorkExecuteDisplay.processWorkLine|
|WHSWorkExecuteDisplay.setBatchDetails|
|WhsWorkExecuteDisplayClusterPicking.clusterCompleted|
|WhsWorkExecuteDisplayMenu.buildMenu|
|WHSWorkExecuteDisplayPOReceiving.displayForm|
|WHSWorkExecuteDisplayUserDirected.displayForm|
|WhsWorkExecuteDisplayWarehouseTransfer.displayForm|
|WrkCtrScheduler_Proj.insertOrder|


## <a name="other-changes"></a>その他の変更

次の表に、拡張機能に対して行われた追加の変更を一覧表示します。

| 計上額 |
| -------------|
- AppCommon に SysQueryUpdateRecordSet クラスを作成します。
- CW 品目の割合管理を有効にします。



