---
title: Dynamics 365 for Finance and Operations バージョン 8.1.1 の拡張機能の変更
description: この記事では、Dynamics 365 for Finance and Operations バージョン 8.1.1 に実装された拡張機能を一覧する
author: FrankDahl
ms.date: 11/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-10-010
ms.dyn365.ops.version: App 8.1.1
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: b3b2699c18ea1934f56ea4c9ac8be3f864952de3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270887"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-811"></a>Dynamics 365 for Finance and Operations バージョン 8.1.1 の拡張機能の変更

[!include [banner](../includes/banner.md)]


これは、Dynamics 365 for Finance and Operations バージョン 8.1.1 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

これらの列挙は、このアップデートで拡張可能になりました。

| 列挙型|
| --------------- |
|BankCodeType|
|CountryRegionType|
|MainAccountDimensionListProviderType|
|ProdSchedulingSortType|
|ProjAccountTypeSales|
|ProjBudgetBalancesGroupByOptions|
|ProjListStateType|
|ProjStatementType|
|SalesDeliveryDateControlType|

## <a name="refactored-methods"></a>リファクターされたメソッド

これらのメソッドは、拡張性をサポートするためにリファクターされています。

| リファクターされたメソッド                                                                             |
|------------------------------------------------------------------------------------------------|
|[拡張性] メソッド シグネチャの変更: WHSWorkExecuteDisplayListWork.displayListWorkStep      |
|[拡張性] WhsWorkExecuteDisplayAdjustOut の ProcessGuide フレームワークへのリファクター               |
| AssetJournal                                                                                   |
| AXSalesQuotationTable.setQuotationId                                                           |
| BankStatementBankAccountIdentify.searchBankAccountTable                                        |
| BankStatementValidate.doValidate                                                               |
| BankStatementValidate.validateDate                                                             |
| BankStatementValidate.validatePeriodGap                                                        |
| BankStatementValidate.validatePeriodOverlap                                                    |
| BOM.validateWrite                                                                              |
| BomCalcDialog.updateBomRoute                                                                   |
| BOMCalcItem.createBomCalcItemAndAddToListBom                                                   |
| BOMCalcTable.transferToSalesLine                                                               |
| BOMCalcTable.transferToSalesQuotationLine                                                      |
| BomConsistOf.init                                                                              |
| BomLevelCalc.loadDependencies                                                                  |
| BOMReportFinishMax.init                                                                        |
| BOMReportFinishMax.update                                                                      |
| BOMReportFinishMax.updateBOMId                                                                 |
| BudgetTransactionManager.checkBudgetTransactionNumberSequence                                  |
| Commission.run                                                                                 |
| Cust/VendTableChangeProposalApply.apply                                                        |
| CustAccountStatementExtController.runPrintMgmt                                                 |
| CustDebitCreditNoteDP.insertForQuantity                                                        |
| CustDebitCreditNoteDP.insertForValue                                                           |
| CustInterestJour.findCustUnPostedInterestNote                                                  |
| CustOpenTrans.editMarkTrans                                                                    |
| CustPackingSlipJour.PrintJounal                                                                |
| CustTable.openInvoiceBalanceMST                                                                |
| CustTable.openinvoiceBalanceMSTDoc                                                             |
| CustTable.openPaymentBalanceMST                                                                |
| CustTable.openPaymentBalanceMSTDoc                                                             |
| CustTable.openPaymentBalanceMSTDue                                                             |
| CustVendCreatePaymJournal_Vend.searchTransactions                                              |
| CustVendDisputeHelper.update                                                                   |
| CustVendPaymProposalTransferToJournal.ClassDeclaration                                         |
| CustVendPaymProposalTransferToJournal.updateSpecTransSet                                       |
| CustVendPaymProposalTransferToJournal.updateSpecTransSingle                                    |
| CustVendPrePaymentReversal.construct                                                           |
| CustVendSettle.settleForDifferentProfilesOrPrepayment                                          |
| CustVendSumForPaym.run                                                                         |
| CzCustPostAdvanceInvoice.run                                                                   |
| DirPartyFormHandler.manageFields                                                               |
| EcoResProductCreate.close                                                                      |
| EcoResProductCreate.templateRecords2Controls                                                   |
| EcoResProductDetailsExtended.InventTable.validateWrite                                         |
| EssPersonSigningLimits/FormDataSourceRoot/HRPLimitRequestApproved.executeQuery                 |
| FormletterJournalPost.postLineDiscount                                                         |
| FormLetterParmData.updateQueryDocumentRanges                                                   |
| FormletterService.run                                                                          |
| FormletterServiceBatchTaskManager.createFormletterParmDataTasks                                |
| FormletterServiceBatchTaskManager.createFormletterServiceTasks                                 |
| FormletterServiceMultithread.newFormletterServiceMultiThread                                   |
| FreeTextInvoiceController.preRunModifyContract                                                 |
| FreeTextInvoiceController.runPrintMgmt                                                         |
| GeneralLedgerExtension.validateReferenceNumber                                                 |
| InterCompanyPost.formLetterCollect                                                             |
| InterCompanyPost.formLetterCollect                                                             |
| InterCompanySyncPurchLineType.createOrUpdateSalesLine                                          |
| InterCompanySyncPurchLineType.synchronizeInTradeCompany                                        |
| InterCompanySyncSalesLineType.classDeclaration                                                 |
| IntrastatTransfer.updateQuery                                                                  |
| InventBatch.insert                                                                             |
| InventBatchConsuptionValidator.ValidateExpiryDate                                              |
| InventDimCtrl_Frm_OnHand.modifyQueryBasedOnDatasourceName                                      |
| InventItemBarcode.validateWrite                                                                |
| InventItemPrice.init                                                                           |
| InventItemPriceSim.moveSimulatedToCurrent                                                      |
| InventMov_Transfer.updateLedgerFinancial                                                       |
| InventMovement.costValueChanged                                                                |
| InventMovement.updateReservation                                                               |
| InventOnhandReserve.ReserveLine.clicked                                                        |
| InventQualityManagementCreate.createPerQualityAssociations                                     |
| InventQualityManagementCreate.createPerQualityAssociations                                     |
| InventQualityOrderValidate.main                                                                |
| InventShelfLifeCriteria.initFromMovement                                                       |
| InventSplitTrans.check                                                                         |
| InventTableModule.initFromInventItemPriceSim                                                   |
| InventTableModule.update                                                                       |
| InventTrans.setSumAmount                                                                       |
| InventTrans.updateSumUp                                                                        |
| InventTransferOrders.InventBatchId.validate                                                    |
| InventTransferupd.createInventTransferJourLine                                                 |
| InventTransferUpd.createInventTransferJourLine                                                 |
| InventTransPick.ctrlUpdate.clicked                                                             |
| InventTransPick.InventDim.InventBatchId.Validate                                               |
| InventTransPick.TmpInventDim.InventBatchId.validate                                            |
| InventTransRegister.InventDim.InventBatchId.validate                                           |
| InventTransRegister.TmpInventDim.InventBatchId.validate                                        |
| InventTransWMS_Register.updateInventFromMovementServer                                         |
| InventTransWMS_Register.updateInventFromMovementServer                                         |
| InventUpd_Arrived.updateArrivedMorer                                                           |
| InventUpd_FinancialLite.updateTrans                                                            |
| InventUpd_Physical.displayErrorsIfIssueQtyGreaterThanPhysical                                  |
| InventUpd_Physical.updateMovementBasedOnPhysicalQty                                            |
| InventUpd_Picked.updatePickLess                                                                |
| InventUpd_Reservation.updateReserveMore                                                        |
| InventUpd_WHSReservation.updateReserveMore                                                     |
| InventUpdate.updateDimReserveChange                                                            |
| InventValueReportInit.initInstrumentation                                                      |
| JmgJobBundle.loadActiveJobs()                                                                  |
| JmgJobBundle.private void loadActiveJobs                                                       |
| JmgJobBundleProjStartupForm.getTmpJobBundleProjStartup                                         |
| JmgJobBundleProjStartupForm.onClose                                                            |
| JmgJobBundleProjStartupForm.validateCategoryId                                                 |
| JmgPayAdjustment.insertAdjustment                                                              |
| JmgPieceRateCalc.calcPieceRate                                                                 |
| JmgPieceRateCalc.insertEvents                                                                  |
| JmgPostStandardSystem.createReportFinishedJournal                                              |
| JmgProfileSpec.promptForAbsence                                                                |
| JmgStampJournalTrans.insert                                                                    |
| JmgStampJournalTrans.update                                                                    |
| JmgTransaction_Proj.postChange                                                                 |
| JmgTransaction_Proj.postChange                                                                 |
| LedgerAllocationController.allocateAmounts                                                     |
| LedgerAllocationRequest.closeOk                                                                |
| LedgerAllocationRequest.run                                                                    |
| LedgerExchAdj.calculateAdjustments                                                             |
| LedgerExchAdj.constructTargetToSourceMap                                                       |
| LedgerJournalCheckPost.postJournal                                                             |
| LedgerJournalEngine.findSettledAmount                                                          |
| LedgerJournalTransUpdateVend.checkVoucher                                                      |
| LedgerParameters/FormDataSourceRoot/RDeferralsParameters.init                                  |
| LedgerPostingGeneralJournalController.getLineValues                                            |
| LedgerPostingGeneralJournalController.transferReferences                                       |
| LedgerVoucher.check                                                                            |
| LedgerVoucherTransObject.check                                                                 |
| LedgerVoucherTransObject.check                                                                 |
| MainAccount.init                                                                               |
| MainAccount.MainAccount_ds/write                                                               |
| MainAccount.MainAccountLegalEntity_DS/legalEntityIsSuspended                                   |
| MainAccountTemplate.rolldownChanges                                                            |
| Markup.resolveOrigQty                                                                          |
| MarkupAdjustment.run                                                                           |
| MarkupAllocation.calculateValueNow                                                             |
| MarkupAllocation_VendInvoiceTrans.dialog                                                       |
| MarkupCopy.copyFromPurchOrder                                                                  |
| MarkupTrans.checkKeep                                                                          |
| メソッド シグネチャの変更                                                                        |
| OMLegalEntity.init                                                                             |
| OMorganizationHierarchy.updatePreviewPane                                                      |
| PdsBatchAttribReserve.ReserveLine.clicked                                                      |
| PdsBatchAttributesInput.init                                                                   |
| PdsRebateFindAndCreate.private void calculateSums()                                            |
| PdsRebateFindAndCreate.protected void createZeroRebate(PdsRebateAgreement _pdsRebateAgreement) |
| PdsRebateFindAndCreate.resetTransSums                                                          |
| PdsResetDispositionStatus.main                                                                 |
| pdsResetShelfDates.init                                                                        |
| PdsResetDispositionStatus.run                                                                  |
| PdsUpdateExpDate.run                                                                           |
| PdsUpdateShelfAdvice.run                                                                       |
| PriceConvert_Currency.parmPrice                                                                |
| PriceDisc.calcPriceAmount                                                                      |
| PriceDisc.resetPrice                                                                           |
| PriceDiscLine.hasOnlyLineAmount                                                                |
| PriceDiscLine.lineAmountModified                                                               |
| ProdJournalCheckPostRoute.postTransLedger                                                      |
| ProdJournalCreateBOM.createSingleLineProdBOM                                                   |
| ProdUpdCostEstimation.createProdTable                                                          |
| ProdUpdCostEstimation.pmfCreateSubProdTable                                                    |
| ProdUpdReportFinished.updateBOMConsumption                                                     |
| ProdUpdStartUp.updateBOMConsumption                                                            |
| ProjBudgetTransactionManager.getTotalTransactionBudget                                         |
| ProjControlPosting.queryNext                                                                   |
| ProjFormLetter.run                                                                             |
| ProjGroupChange.run                                                                            |
| ProjInvoiceChooseNormal.doProposal                                                             |
| ProjInvoiceChooseNormal.initQuery                                                              |
| ProjInvoiceJournalCreate.exchRateSet                                                           |
| ProjInvoiceJournalPost.insertProforma                                                          |
| ProjInvoiceJournalPost.matchInvoicePackingSlip                                                 |
| ProjInvoiceJournalPost.postCustVend                                                            |
| ProjInvoiceProposalCreateLinesBase.doDeduction                                                 |
| ProjInvoiceProposalCreateLinesBase.doSalesLine                                                 |
| ProjInvoiceProposalInsertLines.doRevenue                                                       |
| ProjInvoiceSelect.queryBuild                                                                   |
| ProjInvoiceSelect.run                                                                          |
| ProjPost.newCreateProjTransItemCostAdjustNeg                                                   |
| ProjPost.postCost                                                                              |
| ProjPostCostTransCost_Adj.projTransUpdate                                                      |
| ProjPostCostTransSale_Adj.projTransUpdate                                                      |
| ProjPostEmplJournal.projTransCreate                                                            |
| ProjPostEmplTransCost_Adj.projTransUpdate                                                      |
| ProjPostEmplTransSale_Adj.projTransUpdate                                                      |
| ProjPostItemTransSale_Adj.projTransUpdate                                                      |
| ProjPostRevenueJournal.projTransCreate                                                         |
| ProjProposalJour.insert                                                                        |
| ProjSalesItemReq.clicked                                                                       |
| ProjSalesItemReq.run                                                                           |
| ProjStatusUpd.main                                                                             |
| ProjTable.checkAccount                                                                         |
| ProjTable.createSalesTable_ItemReq                                                             |
| ProjTable.initFromCustTable                                                                    |
| ProjTable.insert                                                                               |
| ProjTable.update                                                                               |
| ProjTable.numberSeqFormHandler                                                                 |
| ProjTable.validateWrite                                                                        |
| ProjTable/FormDataSourceRoot/ProjTable.createFindRanges                                        |
| ProjTableCreate.initValue()                                                                    |
| ProjTableWizard.editProject                                                                    |
| ProjTableWizardCtrl.createProject                                                              |
| ProjWorkBreakdownStructureV2.updateControls                                                    |
| PsaQuotationsController.quoteLanguageId                                                        |
| PurchAutoCreate method setPurchTable                                                           |
| PurchAutoCreate_PurchReq.create                                                                |
| PurchCreateFromSalesOrder.ChkIncluded_CheckBox.clicked                                         |
| PurchCreateFromSalesOrder.included                                                             |
| PurchCreateFromSalesOrder.initFields                                                           |
| PurchCreateFromSalesOrder.SalesLine_ds.checkAllowCreate                                        |
| PurchCreateFromSalesOrder.SalesLine_ds.included                                                |
| PurchCreateFromSalesOrder.SalesLine_ds.specifyMinMaxQty                                        |
| PurchCreateFromSalesOrder.SalesLine_ds.specifyPriceComponent                                   |
| PurchCreateFromSalesOrder.SalesLine_ds.specifyVendAccount                                      |
| PurchFinalizeServiceTask.checkAccountDate                                                      |
| PurchFormletterParmDataInvoice.createParmLine                                                  |
| PurchInvoiceJournalPost.lateMatchPackingSlip                                                   |
| PurchInvoiceJournalPost.postInventory                                                          |
| PurchInvoiceJournalPost.updateJournalTable                                                     |
| PurchInvoiceJournalPost.updateSourceLine                                                       |
| PurchInvoiceJournalPost.updateSourceLine                                                       |
| PurchLine.checkInvoiceConstraints                                                              |
| PurchLine.createFromTmpFrmVirtual                                                              |
| PurchLine.deleteSoft                                                                           |
| PurchLine.deleteSoftClearValues                                                                |
| PurchLine.initFromSalesLine                                                                    |
| PurchLine.itemName                                                                             |
| PurchLineBackOrder.project                                                                     |
| PurchLineType.statusChangeAllowed                                                              |
| PurchLineType.updateApprovedLine                                                               |
| PurchPurchOrderJournalCreate.initJournalHeader                                                 |
| PurchRFQLine.createPurchRFQReplyLine                                                           |
| PurchTable.delete                                                                              |
| PurchTable.delete                                                                              |
| PurchTable.getFinalDiscPriceDateDelegate                                                       |
| PurchTable.initFromVendTableIL                                                                 |
| PurchTable.modifiedFieldWithUserInput                                                          |
| PurchYearEndProcess.processPurchOrder                                                          |
| ReqCalc.allowBatch                                                                             |
| ReqCalc.checkInsertInventTransRecord                                                           |
| ReqCalc.covCreatePlannedOrder                                                                  |
| ReqCalc.pmfCoCovCreatePlannedOrder                                                             |
| ReqCalcScheduleItemTable.createLoopMapFromQuery                                                |
| ReqCalcScheduleItemTable.insertDataCompleteNetChange                                           |
| ReqItemJournalUpdate.updateLines                                                               |
| ReqItemJournalUpdate.validate                                                                  |
| ReqTransCache_Periodic.insertProcessItemsFromQuery                                             |
| ReqTransPOCreate.insertFromReqPo                                                               |
| ReqTransPoMarkChangeType.updateType                                                            |
| ReqTransPoMarkFirm.createInventTransfer                                                        |
| ReqTransPoMarkFirm.createInventTransferJournal                                                 |
| ReqTransPoMarkFirm.createProdBOM                                                               |
| ReqTransPoMarkFirm.createProdTable                                                             |
| ReqTransPoMarkFirm.initInventTransferLine                                                      |
| ReqTransPoMarkSumUp.updateSumUp                                                                |
| ReqTransUpdate.initShelfLifeRef                                                                |
| ReqTransUpdate.mustUpdateQty                                                                   |
| SalesAutoCreate.setSalesTable                                                                  |
| SalesCalcTax_Sales.calcTax                                                                     |
| SalesCopying.copyFromSourceTable                                                               |
| SalesCopying.init                                                                              |
| SalesCopying_CreditNote.updateInvoiceCreditCopy                                                |
| SalesCreateOrderFromCustomer.create                                                            |
| SalesEditLines/FormDataSourceRoot/CustAdvanceInvoiceTable/Method/init                          |
| SalesFormletterParmData.createParmLine                                                         |
| SalesFormletterParmData.initSalesParmUpdateFormletter                                          |
| SalesFormletterParmData.updateQueryBuild                                                       |
| SalesInvoiceController.preRunModifyContract                                                    |
| SalesInvoiceController.runPrintMgmt                                                            |
| SalesInvoiceDPBase.getMarkUpTaxCode                                                            |
| SalesInvoiceDPBase.initLocalizationData                                                        |
| SalesInvoiceJournalCreateBase.createJournalHeader                                              |
| SalesInvoiceJournalPostBase.createReportData                                                   |
| SalesInvoiceJournalPostBase.postLine                                                           |
| SalesInvoiceJournalPostBase.updateJournalLine                                                  |
| SalesInvoiceJournalPostBase.updateJournalTable                                                 |
| SalesJournalSelect_Invoice.closeOK                                                             |
| SalesLine.returnUpdateBasedOnDispcode                                                          |
| SalesLineCopyFromSource.updateSalesLine                                                        |
| SalesLineType.formProduction                                                                   |
| SalesLineType.initFromCustInvoiceTrans                                                         |
| SalesLineType.initFromSalesBasketLine                                                          |
| SalesLineType.initFromSalesLine                                                                |
| SalesLineType.InitFromSalesTable                                                               |
| SalesLineType.initReleasedProductSpecificDefaulting                                            |
| SalesLineType.initStorageDimensionsFromSalesTable                                              |
| SalesLineType.pmfValidateBatchId                                                               |
| SalesLineType.setSalesStatusNonInventoried                                                     |
| SalesLineType.validateWrite                                                                    |
| SalesLineType_Project.validateWrite                                                            |
| SalesPackingSlipJournalPost.createReportData                                                   |
| SalesPackingSlipJournalPost.PostInventory                                                      |
| SalesPackingSlipJournalPost.updateSourceLine                                                   |
| SalesPackingSlipJournalPostProj.writeProjTrans                                                 |
| SalesParmTable.createPaymentSched                                                              |
| SalesQuotationCopying.copyServer                                                               |
| SalesQuotationEditLinesForm.initializeAndRun                                                   |
| SalesQuotationEditLinesForm.initializeAndRun                                                   |
| SalesQuotationEditLinesForm_Proj_Confirm.queryBuildSalesQuotationTable                         |
| SalesQuotationEditLinesForm_Sales_Confir.numRefSalesId                                         |
| SalesQuotationJumpRef.main                                                                     |
| SalesQuotationLineCopyFromSource.updateAfterCopy                                               |
| SalesQuotationLineType.salesQtyAllowEdit                                                       |
| SalesQuotationLineType_Proj.initFromSalesQuotationLine                                         |
| SalesQuotationProjLinkWizard.endUpdate                                                         |
| SalesQuotationProjLinkWizard.linkQuotationToProject                                            |
| SalesQuotationProjLinkWizard.next                                                              |
| SalesQuotationTable.clicked                                                                    |
| SalesQuotationTable.initFromBusinessRelationTable                                              |
| SalesquotationTable.initFromCustTable                                                          |
| SalesQuotationTable.initFromSalesQuotationTable                                                |
| SalesQuotationTable.modifiedField                                                              |
| SalesQuotationTable.modifiedFieldDDC                                                           |
| SalesQuotationTable.validatewrite                                                              |
| SalesquotationTable.writeCreateQuotation                                                       |
| SalesQuotationUpdate.main                                                                      |
| SalesTable.clicked                                                                             |
| SalesTable.SalesTable_ds.Create                                                                |
| SalesTableForm.enableUpdateJournalButtonsMultipleOrders                                        |
| SalesTableType.modifiedField                                                                   |
| SalesTableType.modifiedField                                                                   |
| SalesTableType.validateDelete                                                                  |
| SalesTotals.showTax                                                                            |
| SalesTotals.showTaxLine                                                                        |
| SalesTotals_Sales.calculateFreeValue                                                           |
| SubledgerJournalAccountEntryTmpSummary.getCopy                                                 |
| SubledgerJournalEntryBalance.initBalances                                                      |
| SubledgerJournalizer.validateDebitCreditBalance                                                |
| SubledgerJournalizer.validateTransferEntriesBalance                                            |
| SubledgerJourPennyDiffRecognizer.recognizePennyDifference                                      |
| SubledgerJourSummaryRptCurRoundAdjRcgnzr.recognizeRoundingAdjustment                           |
| Table/ProjTable.isCustomerTransferNeeded                                                       |
| Table/PurchTable.checkUpdate                                                                   |
| Table/TrvExpTrans/Method/setDefaultProjectFromExpenseReport                                    |
| TaxCalculationAdjustment.adjustBaseForAllLines                                                 |
| TMSMiscellaneousCharge.ValidateChargeCode                                                      |
| TmsProcessXML_Base.readAppPurchLine                                                            |
| TmsProcessXML_Base.writeShipManualAccessorials                                                 |
| TransactionReversal_Asset.reversalBook                                                         |
| TransactionReversal_Ledger.createGeneralJournal                                                |
| TSTimesheetEntryQuery.initializeQuery                                                          |
| TsTimesheetsPost.postNoNeverLedgerTrx                                                          |
| VendDocumentLineType_Invoice.validateRow                                                       |
| VendOpenTransReverse.initFromCommon                                                            |
| VendorInvoiceLineSourceDocLineItem.hasMainAccDerivationInputChanged                            |
| VendPurchOrderJour.printJournal                                                                |
| VendReport_LedgerReconciliation.insertLedgerTransactions                                       |
| VendTable.createRecord                                                                         |
| WhsControlQty.process                                                                          |
| WhsDocumentRouting.getRoute                                                                    |
| WHSDocumentRouting.translate                                                                   |
| WHSLocationDirective.validateBatchMixingOnLocation                                             |
| WHSLocationDirective.validateMixingRulesAndStockingLimit                                       |
| WHSPostEngineBase.prodPickQty                                                                  |
| WHSProdTable.stopAndUnpick                                                                     |
| WHSReverseSalesWork.createWorkToMoveItemsBack                                                  |
| WHSRFControlData.populateData                                                                  |
| WhsrfControlData.processDataInternal                                                           |
| WHSRFControlData.processLegacyControl                                                          |
| WHSSplitWork                                                                                   |
| WHSWarehouseRelease.createLoadLines                                                            |
| WhsWaveFormActions.printPickList                                                               |
| WHSWaveTable.createWaveTableFromTemplate                                                       |
| WhsWorkCreateProdPut.createOrUpdateBatch                                                       |
| WhsWorkCreateReceiving.createBatch                                                             |
| WhsWorkExecute.createAndPostTransferJournal                                                    |
| WHSWorkExecute.CreateDimTrackingRecord                                                         |
| WHSWorkExecuteDisplay.getNextFormState                                                         |
| WHSWorkExecuteDisplay.processTrackingDimDetails                                                |
| WHSWorkExecuteDisplay.processTrackingDimDetails                                                |
| WhsWorkExecuteDisplayAdjustIn.displayForm                                                      |
| WhsWorkExecuteDisplayCycleCountGrouping.getCycleCountWorkId                                    |
| WHSWorkExecuteDisplayListWork.addWorkListFieldForWork                                          |
| WHSWorkExecuteDisplayListWork.buildTableContents                                               |
| WHSWorkExecuteDisplayListWork.getWorkQuery                                                     |
| WhsWorkExecuteDisplayLPReceiving.buildReceivingLPInfoFromASNItem                               |
| WhsWorkExecuteDisplayPOItemReceiving.buildPOReceiving                                          |
| WHSWorkExecuteDisplayPOReceiving.buildLicensePlateLabels                                       |
| WHSWorkExecuteDisplayReportAsFinishedBySerial.createPutWork                                    |
| WHSWorkInventTransReservationCollectionBuilder.canMoveReservationFromWorkLine                  |
| WHSWorkUser.changePassword                                                                     |
| WHSWorkUserAuthenticator.authenticate                                                          |
| WmsArrivalCreateJournal.createWMSJournalTransFromArrivalDetails                                |
| WmsJournalFormTrans.promptSplitReturnLine                                                      |
| WmsJournalTransSplit.serverRun                                                                 |
| WMSOrder.updateReservOrderedDim                                                                |
| WmsPickingRoute.finishMulti                                                                    |
| WrkCtrCapResHandler.new                                                                        |

## <a name="metadata-changes"></a>メタデータの変更

これらのメタデータの変更は、このアップデートで行われました。

| 工程 |
| --------------- |
|/Data Entities/PdsItemBatchAttributeEntity.IsPublic|
|/Forms/WHSMobileAppField/FormDesign/AppBar/CreateDefaultButtonGroup/CreateDefaultButton.NeededPermission|
|/Forms/WMSPickingRegistration/Design/Tab(Tab)/Details(TabPage)/HeaderDetails(Tab)/PickingLinesPage(TabPage)/PickLinesGrid(Grid)/InventoryDimensionsGrid(Group).DataGroup|
|/Table/FreeTextInvoiceLocalizationTmp.Visible|
|/Tables/MarkupAutoTable/Indexes/MarkupIdx.MarkupIdx|
|Data types/Extended data types/ItemVolume.NoOfDecimalsIsExtensible|
|DataEntityView/EcoResProductCategoryAssignmentEntity は OData が有効です|
|DataEntityView/EcoResProductEntity は OData が有効です|
|DataEntityView/EcoResReleasedProductEntity は OData が有効です|
|Enum/InvoiceReferenceNumberFormulaType_FI.Country 地域コード|
|Enum/InvoiceReferenceNumberFormulaType_FI/EnumValue|
|RouteOprTime.NoIfDecimalsExtensible|
|Table/HRPDefaultSigningLimitRuleCompensationTmp.String size|
|Table/PSAProjInvoiceTmp/Properties.Title1、Title2|
|Table/VendUnrealizedRev/Field/ReversalDate.Allow edit|

## <a name="additional-extensibility-enhancements"></a>追加の拡張性強化

リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。

- 分析コード ベースの割引
- アルゴリズムを検索する InventPosting を再設計します 




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
