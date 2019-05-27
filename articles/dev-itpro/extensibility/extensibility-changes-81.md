---
title: Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: App 8.1
ms.openlocfilehash: d252a5ec5feb258f9e013cc435a54bb2fc33941a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510973"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-81"></a>Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更

[!include [banner](../includes/banner.md)]

これは、Dynamics 365 for Finance and Operations バージョン 8.1 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="refactored-methods-to-support-extensibility"></a>拡張性をサポートするためにリファクターされたメソッド

これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。

| メソッド|
| --------------- |
|AssetPost.createTrueUpDepreciation|
|AssetPost.createTrueUpDepreciation|
|AssetPostDisposal.post|
|AssetPostDisposal.postVoucherTransactions|
|AssetPostDisposal.postVoucherTransactions|
|AssetTable.buildComposedOf|
|AssetTable.createStruct|
|AxInventDim_SalesLine.setInventSiteId|
|BankChequePrint.printDocument|
|BankCodaProcessing.custSettlement|
|BankDeposit.InitFromLedgerJournalTrans|
|BankExchAdj_RU.calcAndPostCurrency|
|BankExchAdj_RU.calcAndPostCurrency|
|BankExchAdj_RU.calcBalance|
|BankPrintTestCheque.printCheque|
|BankPrintTestCheque.printCheque|
|BankPrintTestCheque.printCheque|
|BankPrintTestCheque.printCheque|
|BlindCloseView.MPOS_ExtensibleViews|
|BudgetAnalysisInquiryHelper_PSN.insertTreeNodes|
|BudgetAnalysisInquiryHelper_PSN.insertTreeNodes|
|BudgetAnalysisInquiryProcessor_PSN.getBudgetAnalysisLedgerDimensions|
|CAMStatisticalEntryTransferJournalEntryDataMapper.newFromParameters|
|CaseUpdateStatus_Close.changeStatus|
|CashManagementView.NewExtension|
|ChequeController.init|
|ChequeDP.insertChequeTmp|
|クラス InventTransferEstimation.updateEstimatedPre|
|クラス Markup.insertReturnMarkupTrans|
|クラス MarkupTransInsert.insertForCodes|
|クラス PurchLineType.updateSalesLine|
|クラス PurchPackingSlipJournalPost.postInventory|
|クラス SalesQuantity_PackingSlip.calcQtyInvent|
|クラス SalesQuantity_PackingSlip.calcQtySales|
|Class/AssetPost.post|
|Class/FormLetterJournalPost.post|
|Class/PurchReqTableListPageInteraction.applyFilter|
|Class\PurchFormLetter_PackingSlip.checkFormLetterId|
|Class\PurchFormletterProvider.checkLines|
|Class\TaxCalculationAdjustment.calcManualInserted|
|CompanyInfoHelper.onValidateField|
|CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite|
|CustAccountStatementExtController.initAgingBalances|
|CustAccountStatementExtController.preprocessParty|
|CustAccountStatementExtController.processParty|
|CustAccountStatementExtController.processTrans|
|CustAccountStatementExtController.runPrintMgmt|
|CustCollectionLetterCreate.run|
|CustCollectionLetterPost.RUN|
|CustInterestAdjust.createCustInvoiceTable|
|CustInterestCreate.createJournal|
|CustInterestCreate.logDateRecordError|
|CustInterestCreate.newAccount|
|CustInterestCreate.resetCustInterest|
|CustInterestCreate.runOnce|
|CustInvoiceCalcTax_Invoice.updateTaxWriteCode|
|CustInvoiceLine.Insert|
|CustOutPaym.generatePaymentLines|
|CustQuotationJour.printJournal|
|CustTable.CanSubmitToWorkflow|
|CustTrans.documentDateModified|
|CustTrans.documentDateModified|
|CustTransSettlement.insertSettlementLines|
|CustVendCheque.createBankChequePaymentTrans|
|CustVendCheque.initTmpChequePrintout|
|CustVendCheque.output|
|CustVendChequeSlipTextCalculator.seebelow|
|CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen|
|CustVendPaymProposalTransferToJournal.transferProposal|
|CustVendPaymSched.construct|
|CustVendPaymSched.initCalcPaymSched|
|CustVendReversePosting.restoreCustVendTransOpen|
|CustVendVoucher.post|
|DataEntityView/SalesOrderLineEntity/Method/validateWrite|
|DataEntityView/SalesQuotationLineEntity/Method/validateWrite|
|EFDocEmailProcessor_BR.saveReceivedXmlData|
|EFDocMsgFormat_XmlBase_BR.createElementWithValue|
|メソッドに抽出: SalesParmTable.GetPaymentSched|
|フォーム InventJournalAsset\Methods\init|
|フォーム InventJournalCount\Methods\init|
|フォーム InventJournalMovement.init|
|フォーム TrvExpenses.confirmCategoryChange|
|Form\SalesEditLines.closeOk|
|FormletterJournalPost.newPostPurch|
|FreeTextInvoiceDP.Variable 宣言|
|HcmActionTypeSetup.lookupWorkflowTable|
|HcmPosition_HcmPositionDefaultDimension_formDatasource.selectionChanged|
|HcmPositionTransition:: createHcmPositionWorkerAssignment|
|HcmPositionWorkerAssignmentDialog:: createWorkerActionOk|
|HRMCompFixedPlanTable::enforcePayRateTolerance |
|InterCompanyPostPurch.construct|
|InterCompanyPostPurch.formLetterUpdate|
|InterCompanyPostSales.formLetterUpdate|
|InterCompanySyncPurchTableType.setSalesTableData|
|IntrastatCheck.Run|
|IntrastatTransfer.calcAmountsAndMarkups|
|IntrastatTransfer.calcValuesSign|
|IntrastatTransfer.distributeIntrastatAddValueLV|
|IntrastatTransfer.run|
|IntrastatTransferIT.calcCounty|
|IntrastatTransferIT.updateTransactionCurrencyAmount|
|InventAdj_Transact.run|
|InventCostPost.postInventCostTransVariance|
|InventMov_Purch.updateAutoLossProfit|
|InventMov_Purch.updateBuffer|
|InventMovement.checkUpdatePhysical|
|InventoryLookupMatrixView.ExtensibleViews|
|InventTable.pdsValidateBestBeforeDays|
|InventTransWMS_Register.updateInventFromMovementServer|
|InventUpd_ChildReference.updateLessIssue|
|InventUpd_ChildReference.updateLessReceipt|
|InventUpd_ChildReference.updateMoreIssue|
|InventUpd_ChildReference.updateMoreReceipt|
|InventUpd_Financial.newSalesInvoice|
|InventUpd_Physical.updatePhysicalIssue|
|InventUpd_Physical.updateTransPhysicalReturnedReceipt|
|InventUpd_Physical::newSalesPackingSlip|
|InventUpd_Reservation.updateNow|
|InventUpd_Reservation.updateReserveMore|
|InventUpdate.updateInventTransPosting|
|InventUpdate.writeInventTrans|
|InventUpdate.writeInventTrans|
|InventUpdateMarking.addMarking|
|InventUpdateMarking.removeMarking|
|InventUpdateReserveMore.createQueryRuns|
|JmgCalcApprovePickDialog.closeOk|
|JmgJobBundle.postTime|
|JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback|
|JournalStaticDataModel.initializeJournalTableFields|
|Ledger.populateTmpTable|
|Ledger::populateTmpTable|
|LedgerAccrualTrans_Calendar.allocate|
|LedgerAccrualTrans_Calendar.allocate|
|LedgerAccrualTrans_Fiscal.allocate|
|LedgerAccrualTrans_Fiscal.allocate|
|LedgerAutomaticTransactionAccountEntity|
|LedgerCreatePeriodBalances.createPeriodBalancesMainAccount|
|LedgerExchAdj.postAdjustment|
|LedgerExchAdj.run|
|LedgerFiscalJournalDP_IT.getDisplaySequenceNumber|
|LedgerJournalCheckPost.checkJournal|
|LedgerJournalCheckPost.postJournal|
|LedgerJournalCheckPost.runInternal|
|LedgerJournalEngine.accountModified|
|LedgerJournalEngine.calculateTaxForCompleteJournal|
|LedgerJournalEngine.findSettledAmount|
|LedgerJournalEngine.formSettlement|
|LedgerJournalEngine.newVoucher|
|LedgerJournalPeriodicCopy.journalTransCopy|
|LedgerJournalTrans.checkVATTransaction|
|LedgerJournalTrans.checkVatTransaction|
|LedgerJournalTrans.validateWrite_Server|
|LedgerJournalTrans_Project.checkCategoryId|
|LedgerJournalTransUpdateAsset|
|LedgerJournalTransUpdateLedger.updateNow|
|LedgerJournalTransVoucherTemplates.createVoucherTemplate|
|LedgerJournalTransVoucherTemplates.createVoucherTemplate|
|LedgerJournalTransVoucherTemplates.saveVoucherTemplate|
|LedgerJournalTransVoucherTemplates.saveVoucherTemplate|
|LedgerJournalTransVoucherTemplates.SaveVoucherTemplate、CreateVoucherTemplate|
|LedgerPostingGeneralJournalController.addLine|
|LedgerPostingGeneralJournalController.getLineValues|
|LedgerTransferOpening.getMainAccountStorageSegment|
|LedgerTransferOpening.processNewClosingRecordsForOpening|
|LedgerTransferOpening.processQueryForPublicSector|
|LedgerTransModule.tax|
|LedgerVoucherObject.allocateTransaction|
|LedgerVoucherObject.updateLedgerPostingJournal|
|LogisticsEntityLocationFormHandler.manageControls|
|LogisticsPostalAddressFormEventHandler.updatePrimaryControl|
|MainAccount.canSubmitToWorkflow|
|可能であれば変数宣言を最初の割り当てに移動|
|NewElement.NewMethod|
|OmOperatingUnit.getDimensionViewId|
|Originaldocuments.findFromCustTrans|
|Originaldocuments.findFromGeneralJournal|
|PaymSchedCalc.createCustVendTransaction|
|PaymSchedCalc.initFromPurchTotals|
|PaymSchedCalc.initFromSalesTotals|
|POSApidts.NewTrigger|
|PosAPidts.NewTrigger|
|PriceDiscAdmCheckPost.checkForOverlapsAndGaps|
|PriceDiscAdmCheckPost.runFromContract|
|PriceDiscTable.buildSearchFilter|
|PrintableReceipt|
|ProjAdjustmentUpdate.newPostAdjustment|
|ProjAdjustmentUpdate.projTrans|
|ProjAdjustmentUpdate.transEmplNew|
|ProjAdjustmentUpdate_Post.Post|
|ProjAdjustmentUpdate_Post.update|
|ProjBudgetManager.createBudgetRevenueForecast、createBudgetSalesForecast|
|ProjBudgetManager.insertProjBudgetLine|
|ProjBudgetManager.insertProjBudgetLine|
|ProjBudgetManager.updateProjBudgetLinesWithAmt|
|ProjCategory.categoryType2CategoryEmplOption|
|ProjCategory.categoryType2CategoryEmplOption|
|ProjCategory.categoryType2TransType|
|Projcategory.transType2CategoryType|
|Projcontrol.categoryType2CostType|
|Projcontrol.costType2CategoryType|
|ProjControlPosting.insertControlTrans、processSalesValue|
|ProjectSourceDocumentLineItemHelper.projOrigin および projTransType|
|ProjForecastListPageInteraction.runForcastFormBasedOnForecastUnion|
|ProjForecastReduce.newProjPost|
|ProjFormLetter メソッド main/mainOnServer|
|ProjInvoiceCancel.cancelProposal|
|ProjInvoiceChoose.run|
|ProjInvoiceJournalCreate.createJournalHeader|
|ProjInvoiceLines.run|
|ProjInvoiceProposalCreateLines.loadLastValue|
|ProjInvoiceProposalCreateLines.runItemQuery|
|ProjInvoiceProposalInsertLines.run|
|ProjInvoiceProposalInsertLines.setProjProposalJour|
|ProjInvoiceProposalInsertLines.setProjProposalJour|
|ProjInvoiceProposalInsertLines.setProjProposalTotals|
|ProjInvoiceTableCreate.initializeValues|
|Projparameters.defaultProjCategory|
|ProjPeriodPostingLedgerCost.updateTrans|
|ProjPost.newCheckTrans|
|Projpost.newCreateProjTransAndLedger|
|Projpost.newCreateProjTransAndLedgerAdj|
|Projpost.newTransAdjNegativeJournal|
|Projpost.postcost|
|ProjSalesItemReq.modified|
|ProjSplitBill.transType|
|ProjSplitBill.transType|
|ProjTable.generateNextSubProjectId|
|ProjTableCreate.canClose|
|ProjTableLookup.isJournal|
|ProjTableWizardCtrl.createProject|
|PsaProjAndContractInvoiceController.getReportTitle|
|PsaProjAndContractInvoiceController.getReportTitle|
|PsaProjAndContractInvoiceController.getReportTitle|
|PSAProjRetainerInvoicing.run|
|PsaQuotationsController.getReportTitle|
|PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState|
|PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState|
|PurchaseOrderResponseConsume.consumeChangesToPurchLineAndUpdateResponeLineConsumptionState|
|PurchAutoCreate_Sales.createPurchTable|
|PurchAutoCreate_Sales.setPurchTable|
|PurchCalcTax_Invoice.updateTaxWriteCode|
|PurchCopying.copyLine|
|PurchCreateFromSalesOrder.autoCreatePurchOrder|
|PurchFormletter_Invoice.newinvoice|
|PurchFormletter_Packingslip.runProjectPostings|
|PurchFormletterParmData.createParmLine|
|PurchFormletterParmData.newData|
|PurchFormLetterParmData.reSelectLines|
|PurchFormletterParmDataInvoice.chooseLinesNext|
|PurchFormletterParmDataInvoice.cleanupChooseLines|
|PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder|
|PurchFormletterParmDataInvoice.processAdditional|
|PurchFormletterProvider.checkLines|
|PurchInvoiceJournalCreate.checkInvoice|
|PurchInvoiceJournalPost.postInventory|
|PurchLine.delete|
|PurchLine.setProjSalesPrice|
|PurchLine.update|
|PurchLine.validateWrite_Server|
|PurchLineCopy.canClose|
|PurchLineType.syncSalesLine|
|PurchLineType.updateInventory|
|PurchLineType.updatePurchStatus|
|PurchLineType.validateDelete|
|PurchPackingSlipJournalPost.postInventory|
|PurchPackingSlipJournalPost.updateSalesLine|
|PurchPackingSlipJournalPost.updateSalesTable|
|PurchPackingSlipJournalPost.updateSourceLine|
|PurchQuantity_PackingSlip.calcQtyInvent|
|PurchQuantity_PackingSlip.calcQtyPurch|
|PurchReqAddItems.init|
|PurchReqTable.init|
|PurchReqWFExpendiParticipantProvider.resolve|
|PurchSelectLinesManager.mark|
|PurchTableForm.purchLine_WritePreSuper|
|PurchTableInteractionHelper.getDeliveryScheduleEnabled|
|PurchTableInteractionHelper.getHasMultipleDeliveries|
|PurchUpdateRemain.updateRemainPhysical|
|ReqCalc.insertItemInventSum|
|ReqTransPlanIdFilter.setPlanIdOnQueryRange|
|ReqTransPoMarkFirm.createPurchLine|
|ReqTransPoMarkFirm.createPurchTable|
|ReqTransPoMarkFirm.createPurchTable|
|ReqTransPoMarkFirm.dialog|
|RetailAssortmentLookupTask.CreateChannelGroups|
|RetailKitAssemblyOrder.createOrUpdateBOMJournal|
|RetailPackage.close|
|RetailProductPropertyManager.saveProductDimensions|
|RetailStatementPostChecker::checkStatement|
|ReturnTable.isDispositionCodeValid|
|RouteCopyToRoute|
|SalesCalcAvailableDlvDates.newCommonSalesDlvDateType|
|SalesCalcAvailableDlvDates.newCommonSalesDlvDateTypeByEntity|
|SalesCopying.copyLines|
|SalesEditLines.FormDesign/FormMenuFunctionButtonControl/ButtonPaymentSched/Method/clicked|
|SalesFormLetter.onCreatePaymSched|
|SalesFormLetterParmDataPackingSlip.selectChooseLines|
|SalesFormletterProvider.checkLines|
|SalesFormletterProvider.checkSalesLineChanged|
|SalesInvoiceController.initFormLetterReport|
|SalesInvoiceJournalPost.postInventory|
|SalesInvoiceJournalPostProj.updateInventory|
|SalesLine.createAlternativeItem|
|SalesLine.delete|
|SalesLine.returnLineUpdate|
|SalesLineCopy.canClose|
|SalesLineType.initFromCustInvoiceTrans|
|SalesOrderEntryStatistics.createOrderEntry|
|SalesOrderEntryStatistics.deleteOrderEntry|
|SalesPackingSlipDP.itemId|
|SalesPackingSlipJournalPost.postInventory|
|SalesParmLine.setQty|
|SalesQuantity_Invoice.calcQtyInvent|
|SalesQuantity_Invoice.calcQtySales|
|SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesLines|
|SalesQuotationEditLinesForm_Sales_Confir メソッド createSalesTable|
|SalesQuotationEditLinesForm_Sales_Confir.createSalesLine|
|SalesQuotationEditLinesForm_Sales_Confir.createSalesLines|
|SalesQuotationLine.createLine|
|SalesQuotationLine.createQuotationLineFromTemplate|
|SalesQuotationLine.createQuotationLineFromTemplate|
|SalesQuotationLine.createQuotationLineFromTemplate|
|SalesQuotationLine.delete|
|SalesQuotationLine.setCostSalesPrice|
|SalesQuotationLine.updateSalesQuotationTable|
|SalesQuotationListPageInteraction.initIsSalesQuotation|
|SalesQuotationListPageInteraction.setButtonFollowup|
|SalesQuotationListPageInteraction.setButtonQuotation|
|SalesQuotationTableForm_DlvSchedule.updateSalesQuotationLineTable|
|SalesQuotationTableType.validateDelete|
|SalesTable.update|
|SalesTableForm_DeliverySchedule.updateSalesLineTable|
|SalesTableForm_ProjectSalesItem.resetSalesLine|
|SalesTableInteractionHelper.isOpenOrderNotReturnNotProjectRelatedSalesLine|
|SalesTableInteractionHelper.notPartiallyPickedPackedOrInvoiced|
|SalesTableInteractionHelper.notReservedOrderedNorPhysical|
|SalesTableType.checkUpdate|
|SalesTableType.checkUpdate|
|SalesTableType.checkUpdate|
|SalesTaxDeclarationInformationReportService.processReport|
|SettlementPair_Vend.fetchPayment|
|smmActivityParentLinkTable.insert|
|smmBusRelTable.convert2Customer|
|smmBusRelTable.convert2Customer|
|SmmBusRelTable.convert2Vendor|
|SmmBusRelTable.convert2Vendor|
|smmBusRelTable.createConvertedBusRel|
|smmLeadTable.createBusRelRecord|
|SmmProjectCreate.createProjectGroup|
|SpecTransInsertSetManager.insertDatabase|
|SubledgerJournalizerProjectExtension.createProjectActualCostDetail、createProjectActualHeader|
|SubledgerJournalizerProjectExtension.getProjectActualMap|
|SuppItemSales.initSalesLine|
|テーブル PurchLine.insert|
|テーブル PurchLine.insert|
|テーブル PurchLine.update|
|テーブル PurchTable.update|
|テーブル PurchTable.update|
|テーブル SalesLine.insert|
|テーブル SalesLine.projIdModified|
|テーブル SalesLine.salesQtyModifiedInteraction|
|テーブル SalesLine.update|
|テーブル SalesQuotationLine.insert|
|テーブル SalesQuotationLine.update|
|テーブル SalesQuotationTable.update|
|テーブル SalesQuotationTable.update|
|テーブル SalesTable.update|
|テーブル SalesTable.update|
|Table\VendTable.name|
|Table\VendTable.updateOnHold|
|Tax.createOrphanLinkInsteadPost_RU|
|Tax.distributeTotalTax|
|Tax.distributeTotalTax|
|Tax.InsertIntersection|
|Tax.insertIntersection|
|Tax.post|
|Tax.Post|
|Tax.postCharge|
|Tax.postTaxProjInvoice_IN|
|Tax.postTaxPurchInvoice_IN|
|Tax.postTaxSalesInvoice_IN|
|Tax.saveAndPost|
|Tax.taxTotals|
|Tax.taxTotals|
|Tax.taxTotals|
|Tax.taxTotalsPosted|
|Tax.taxTotalsPosted|
|Tax.taxTotalsPosted|
|TaxBookSection.checkTaxBookSection|
|TaxCalculationAdjustment.calcManualInserted|
|TaxCalculationJournal.saveTaxTransfers|
|TaxFreeInvoice_Invoice.updateAndPost|
|TaxInvoiceSpec.parmTaxSpec|
|TaxListDP.insertTaxListTaxTmpData|
|TaxListDP.updateTaxListTaxTmpData|
|TaxMainAccDimensionListProvider.populateMainAccountDimensionList|
|TaxPost.postToLedger|
|TaxReportController_US.init|
|TaxReportInclAdjustmentDP.insertTaxReportInclAdjustmentTmp|
|TaxReportingDP.insertTaxReportingTmp|
|TaxReverse.adjustTaxTransDueToExchangeRateGainLoss|
|TaxReverse.postAccountingCurrency|
|TaxReverse.postAccountingCurrency|
|TaxReverse.postAccountingCurrency|
|TaxReverse.postCharge|
|TaxReverse.postGainLossInReportingCurrency|
|TaxSales.calc|
|TaxSales.calc|
|TaxSales.calcMarkup|
|TaxSales.configureTaxForSalesLine|
|TaxVoucherService.taxAmountForLedgerType|
|TmpCustVendTrans.CustTransBalanceCurrency|
|TmpProjAdjustment.adjustmentType2JournalType|
|TmpProjAdjustment.adjustmentType2TransType|
|TmpProjAdjustment.updateFundingLimits|
|TmpProjAdjustmentCreate.salesPrice|
|TrvExpenseLinesVisibilityController.isVisibilityResetRequired|
|TrvExpenses.updateFormVisibilityOnCategoryChange|
|TrvExpTrans.calcTaxAmount|
|TrvTaxExpense.calculateTax|
|TSTimesheetEntry.init、initFields、setHeaderObjects、validateWrit、lookup|
|UnitOfMeasureConverter.Convert|
|VendInvoicePaymentAuthorizationTask.postSavedInvoice|
|VendPackingSlipTrans.unpostedInvoicePurchQtyServer および VendPackingSlipTrans.unpostedInvoiceInventQtyServer|
|VendTable.checkVATNumUsed|
|VendTax1099Update.calcMiscChargeAmountTax|
|VendTrans.documentDateModified|
|VendTrans.documentDateModified|
|VendVoucher.createTransOpen|
|VendVoucher.createTransOpen|
|WHSContainerTable.closeContainer|
|WHSDocumentRouting.translate|
|WHSLoadLine.orderHeader|
|WHSLoadTable.validateInventTransTypeMatches|
|WHSLoadTableAssignOriginInfo.classDeclaration|
|WmsArrivalCreateJournal.createWMSJournalTransFromTmp|
|WMSOrderTrans.split|
|WmsOrderTransType_Output.updateReservations|
|WorkflowHierarchyProviderHelperEventHandler::getPersonnelNumberIdBySysDictTypeDelegate|
|WorkTimeTable.removeDisplayCache|
|WrkCtrResourceAbilityMapController.insertData|
|数量の拡張による小数点以下の精度の増加を有効にする|

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

これらの列挙は、このアップデートで拡張可能になりました。

| 列挙型|
| --------------- |
|AssetPostValue|
|AssetPropertyType|
|AssetStatus|
|CaseStatus|
|CommissionSalesRepCode|
|DirSubNameSequenceType|
|FreightSlipType|
|HRPLimitDocumentType|
|IntrastatPaymentMethod_IT|
|InventBlockingType|
|JmgPaySpecTypeEnumPick|
|KMQuestionAnswerInputType|
|LedgerJournalType|
|LogisticsAddrZipCodeImportCountryRegion|
|LogType|
|MarkupModuleType|
|MarkupModuleType|
|MCRBrokerValueType|
|PaymentType|
|PDSCalcElementTypeBase|
|PdsStatus|
|PdsVendorCheckItem|
|ProdStatus|
|ProjActiveAll|
|ProjAdjustmentType|
|ProjAllTrxType|
|ProjBudgetAction|
|ProjCostType|
|ProjForecastInvoiceFrequency|
|ProjLinePropertySearch|
|ProjSalesPriceMarkup|
|ProjSortValue|
|ProjTableEditSubProj|
|ReqCovType|
|ResCharacteristicSetEnum|
|SettlementType|
|smmShowTimeAs|
|SourceDocumentRelationType|
|TaxRegistrationTypesList|
|TaxReportLayout|
|TradeWorkflowState|
|WMSExpeditionStatus|


## <a name="extensible-sql-operations"></a>拡張可能な SQL 操作

これらの SQL 操作は、このアップデートで拡張可能になりました。

| 工程 |
| --------------- |
|CustInterestPost.postVoucherPerTransaction|
|InventMov_ProdLine_JournalBom.insertChildBuffer|
|InventUpdate.initInventTransToReceiveList|
|ProjAdjustmentUpdate_PostAsync.postAsync|
|ProjBudgetManager.createBudgetCostForecast|
|ProjBudgetManager.createBudgetEmplForecast|
|ProjBudgetManager.createBudgetRevenueForecast|
|ProjBudgetManager.createBudgetSalesForecast|


## <a name="metadata-changes"></a>メタデータの変更

これらのメタデータの変更は、このアップデートで行われました。

| 工程 |
| --------------- |
|/Data entities/ReqPlannedOrderEntity.Is Public|
|/DataTypes/Extended Data Types/AmountQty.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/AssetDepreciationAmountUnitReportingCurrency.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/BOMProductQuantity.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/CostPriceNonMonetary.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/CostQuantity.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/MCRRoyaltyValue.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/PdsRebateValue.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/PriceDiscAmount.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/PriceQty.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/PriceUnit.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/PriceUnit.Scale|
|/DataTypes/Extended Data Types/ProductQuantity.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/ProductQuantityHourValue.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/ProjName.Extends|
|/DataTypes/Extended Data Types/TAMRebateValue.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/UnitAmountCur.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/UnitAmountMST.NoOfDecimalsIsExtensible|
|/DataTypes/Extended Data Types/WeightBase.NoOfDecimalsIsExtensible|
|/Tables/LedgerJournalTrans_Project/Relations/LedgerJournalTrans.createNavigationPropertyMethod|
|/Tables/PriceDiscGroup.Cache Lookup|
|/Tables/VendInvoiceJour/Fields/DefaultDimension.Visible|
|/Tables/VendInvoiceTrans/Fields/DefaultDimension.Visible|
|/Tables/WMSAisle.Cache Lookup|
|/Tables/WorkCalendarTable.Create Rec Id Index|
|/Tables/WorkTimeLine.Cache Lookup|
|/Tables/WorkTimeTable.Cache Lookup|


## <a name="additional-extensibility-enhancements"></a>追加の拡張性強化

リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。

- バグ リクエスト: "CustCollectionLetterTrans -> CollectionLetterNum" 関係プロパティ
- 価格の拡張による小数点以下の精度の増加を有効にする
- 重量の拡張による小数点以下の精度の増加を有効にする
- マップ拡張: LogisticsEntityLocationMap
- OMOperatingUnit は、DimAttributeOMDepartment.Value のユーザー フレンドリおよび定義済の値を指定する必要がある
- InventPosting が LedgerDimension を検索する方法を再設計
- WhsWorkExecuteDisplayAdjustIn を ProcessGuide フレームワークにリファクター
- WHSWorkExecuteDisplayChangeWarehouse を ProcessGuide フレームワークにリファクター
- WhsWorkExecuteDisplayInquiryItem を ProcessGuide フレームワークにリファクター
- WhsWorkExecuteDisplayInquiryLocation を ProcessGuide フレームワークにリファクター
- WhsWorkExecuteDisplayInquiryLP を ProcessGuide フレームワークにリファクター
- whsWorkExecuteDisplayReprintLabel を ProcessGuide フレームワークにリファクター
- 小売チャネル: サポート BankDropOperationRequest

