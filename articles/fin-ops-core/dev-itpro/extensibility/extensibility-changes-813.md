---
title: Dynamics 365 for Finance and Operations バージョン 8.1.3 の拡張機能の変更
description: これは、Dynamics 365 for Finance and Operations バージョン 8.1.3 に実装された拡張機能の一覧です。
author: FrankDahl
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-12-07
ms.dyn365.ops.version: App 8.1.3
ms.openlocfilehash: 8fbb458be59a5f546a6660299919f5c4deec9903
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409336"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-813"></a>Dynamics 365 for Finance and Operations バージョン 8.1.3 の拡張機能の変更

[!include [banner](../includes/banner.md)]


これは、Dynamics 365 for Finance and Operations バージョン 8.1.3 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

これらの列挙は、このアップデートで拡張可能になりました。

| 列挙型|
| --------------- |
|AttributeDataType|
|BankDocumentBookType|
|BudgetPlanHCMReportGroupOption|
|CommitmentType|
|CommitmentType|
|CustVendNegInstStatus|
|CzAdvanceInvoiceStatus|
|DateTransactionDuedate|
|LedgerAllocationMethod|
|LedgerCovDocumentType|
|MCRFraudType|
|PercentHours|
|PerDayWeekMthQtYr|
|PrepaymentHandlingLayout_W|
|ProdStatusAll|
|TaxDirection|
|TaxType_IT|
|WHSWaveTemplateType|

## <a name="sql-operations-made-extensible"></a>拡張可能になった SQL 操作

これらの SQL 操作は、このアップデートで拡張可能になりました。

| 操作|
| --------------- |
|InventTrans.deleteReturnTransOrigin|
|InventUpd_ChangeDimension.updateForceInventTrans|
|PriceDiscAdmCheckPost.updatePriceDiscTableRecords|
|ProdJournalCleanUp.deleteJournals|
|ProjBudgetManager.createBudgetCostForecast|
|ProjBudgetManager.createBudgetEmplForecast|
|ProjBudgetManager.createBudgetRevenueForecast|
|ProjBudgetManager.createBudgetSalesForecast|
|SubledgerJourFinalNetAmtEntryProvider.getFinalRelievingEntriesWithNetAmounts|
|SubledgerJourFinalRelieveEntryProvider.populateEntriesBySide|
|SubledgerJournalAccountEntryRelievingTmp.mergeJournalizationEntries|
|SubledgerJournalFinalReliever.findEntriesAlreadyRelieved|
|SubledgerJournalFinalReliever.findEntriesToRelieve|
|SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadInterCompanyNonOffsetSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadInterCompanyOffsetSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadRelievingSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadReversingSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadYearEndSubledgerJournalTmpDetail|
|SubledgerJournalizer.summarizeJourAccountEntryDetailForRound|

## <a name="metadata-changes"></a>メタデータの変更

これらのメタデータの変更は、このアップデートで行われました。

| 操作 |
| --------------- |
|Classes/CustVendSettle/classDeclaration.field モディファイアー|
|Classes/LedgerPostingGeneralJournalController/transferLines.HookableAttribute|
|Classes/VendPaymentJournalDP.none|
|EcoResProductAttributeTranslationEntity.IsPublic|
|EcoResProductBarcodeEntity.Property.IsPublic|
|Enum/RDeferralsCalculatePeriod.Country 地域コード|
|Enum/RDeferralsInitRetirementDate.Country 地域コード|
|Enum/RDeferralsInitWriteStartDate.Country 地域コード|
|Enum/RDeferralsInitWriteStartDate/EnumValue|
|Enum/RDeferralsInterval.Country 地域コード|
|Enum/RDeferralsManualCalcType.Country 地域コード|
|Enum/RDeferralsMethod.Country 地域コード|
|Enum/RDeferralsPostValue.Country 地域コード|
|Enum/RDeferralsStatus.Country 地域コード|
|Enum/RDeferralsTableGroupAllBook.Country 地域コード|
|Enum/RDeferralsTransType.Country 地域コード|
|Extended Data Types/AttributeValueFloat.No Of Decimals は拡張可能です|
|OnAccount および経費の明細行タイプのプロジェクトの請求書/提案明細行の説明を増加します。|
|InventValue レポートは、カスタムの分析コードをサポートするようになりました|
|Maps/AccountSumMap.Balance08,Balance08Cur,Balance09,Balance09Cur|
|Table/PurchTable.Visible = True|
|Table/VendUnrealizedRev/Field/ReversalDate.Allow edit.AllowEdit|
|Tables/DirPartyTable/Fields.AOS 承認|
|Tables/VendSettlement/Relations/VendTrans.RelationshipType|
|Tables/WHSDocumentRoutingLine/Indexes/DocumentRoutingTablePrinterNameIdx|

## <a name="refactored-methods"></a>リファクターされたメソッド

これらのメソッドは、拡張性をサポートするためにリファクターされています。

| リファクターされたメソッド                                                                             |
|------------------------------------------------------------------------------------------------|
|AssetJournal.populateLedgerJournalTrans|
|AssetPost.postToGeneralLedger|
|AssetProposalDepreciation.run|
|AssetTransfer.addLedgerVoucherTransObjects|
|AxSalesLine.setDefaultDimension|
|BankChequeCopy.fillTmpChequePrintout|
|BankChequeLayout.updateDesign|
|BankDepositSlip.modifyBankAccountTrans|
|BankJournalHeaderEntity.ValidateField|
|BankPositivePayExport.sendFileToUser|
|BankStatementValidate.validateDate|
|BankStmtISOAccountStatement.deleteStatement|
|BOM.defaultField|
|BOM.validateField|
|BOM.validateWrite|
|BomCalcItem.insertBOMCalcTable|
|BomCalcItem.insertBOMCalcTrans|
|BomCalcProd.calcCostSheet|
|BOMReportFinishMax.retrieveInventTable|
|BudgetCaculateBalance.getActualLedgerAmountsQuery|
|BudgetCaculateBalance.getOriginalBudgetQuery|
|BudgetCaculateBalance.getRevisedBudgetQuery|
|BudgetSourceCollectionIntegrator.newBudgetSourceCollectionIntegrator|
|BudgetSourceIntegrator.newBudgetSourceIntegrator|
|ChequeController.ClassDeclaration|
|ChequeController.init|
|ContactPersonApplicationSuiteEventHandlers.initializedFromCommonEventHandler|
|CustBillOfExchangePostRemit.postSettlingStep|
|CustDirectDebitMandate.checkBankIBAN|
|CustDueReportDetailDP.updateCustDueReportDetailTmp|
|CustPostInvoiceJob.custPostInvoiceUpdate|
|CustSettleJournalizingEntries.createGeneratedEntries|
|CustSettleJournalizingEntries.getInterestOriginatingEntries|
|CustSettleJournalizingEntries.getOriginatingEntries|
|CustTransDetails.new|
|CustTransListDP.insertCustTransListTmp|
|CustTransOpenCashFlow.generateCashFlow|
|CustVendCheque.output|
|CustVendCreatePaymJournal_Vend.shouldAddCustVendTransOpen|
|CustVendEditTaxBranchHelper_TH.init|
|CustVendExchAdjTrans.initLedgerVoucher|
|CustVendSettle.reverseTax|
|CustVendTransReorg.paymentSchedSplit|
|CustVendTransReorg.post|
|CustVendTransReorg.reorganize|
|CustVendVoucher.setTransactionTxt|
|CustWriteOff.createTaxJournalLines|
|DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation|
|DirPartyRoleIsExternallyMaintained.setFieldRestrictions|
|EcoResDocumentAttachmentEntity.insertDatasourceDocuRef|
|EcoResProductNumberBuilderVariant.getEnumeratorForEnabledOrderedProductDimensions|
|EFDocMsgFormat_XmlSubmit_BR.createXmlDocumentFromEFDocument|
|EFDocumentXpath_BR.Not 適用|
|ERclasses - クラス署名|
|FiscalDocParmDataCreatorInvTransfer_BR.initHeaderParmData|
|FiscalDocParmDataCreatorInvTransfer_BR.setinventTransferTableFiscalInfo|
|FiscalDocumentParmDataCreator_BR.initTaxTransParmDataFromTaxTrans|
|FiscalDocumentParmDataCreator_BR.setAccountingAmountOnFiscalDocumentLines|
|FiscalDocumentPost_BR.initFiscalDocument|
|FreeTextInvoiceDP.insertIntoFreeTextInvoiceHeaderFooterTmp|
|HcmWorkerTransition.createHcmEmployment|
|HrpExpireWorkerLimits.expireLimitRequest,expireApprovedLimit,getAuthorityBasis|
|InventMov_Sales.accountBalanceSheet|
|InventReleaseOrderPickingForm_Sales.bldInventReleaseOrderPickingTmp|
|InventTestAssociationTable.checkExecutionTime|
|InventTrans.insertReturnTransOrigin|
|InventTrans.updateMarkReqTransCov|
|InventTransferOrderCopying_BR.createTransferLines|
|InventTransferOrderCopying_BR.createTransferOrder|
|InventTransferUpdShip.updateInventTransferLine|
|InventUnusedDimCleanup.isCandidateInventDimIdTable|
|InventUpd_ChangeDimension.updateTransSwitchDim|
|InventUpd_ChildReference.updateLessReceipt|
|InventUpd_ChildReference.UpdateMoreReceipt|
|InventUpd_Financial.updateFinancialIssue|
|InventUpd_Financial.updateStdCostPrice|
|InventUpd_Picked.updatePickMore|
|InventUpd_Registered.updateRegisterLess|
|InventUpd_Registered.updateRegisterMore|
|InventUpd_Reservation.updateReserveLess|
|InventUpdate.initializeInventTransToIssueListFromDatabase|
|InventUpdate.initInventTransToReceiveList|
|JmgJobBundleProdFeedbackForm.getTmpJobBundleProdFeedback|
|JmgPaySpecificationDP.Class 宣言|
|JmgPostStandardSystem.getProjTransCostPrice|
|JmgPostStandardSystem.postIPCTime|
|JmgPostStandardSystem.postProjTime|
|JmgProfiles.bundleSlizeTime|
|JmgProfiles.insertTimeGapsPlannedAbs|
|JmgProfiles.sumPayEventsSec|
|JmgStampJournalTransfer.insertStampTrans|
|JmgTransferEvents.createPayEventsArray|
|JmgTransferEvents.insertEvents|
|JournalizingDefinitionManagerPurch.getDefaultJournalizingDefinition|
|LedgerAccrualTrans.post|
|LedgerAllocationBasisRules.getBasisAmount|
|LedgerJournalCheckPost.checkJournal|
|LedgerJournalCheckPost.postJournal|
|LedgerJournalCheckPost.postTransV2|
|LedgerJournalCheckPost.updateInterCompanyJournal|
|LedgerJournalTrans.markedForSettlementError|
|LedgerJournalTrans.validateWrite_Server|
|LedgerJournalTransProject.checkProjId|
|LedgerJournalTransUpdate.updateInterCompany|
|LedgerJournalTransUpdateBank.updateNow|
|LedgerJournalTransUpdateCust.updateNow|
|LedgerJournalTransUpdateLedger.createTaxLinkForTaxTransfer|
|LedgerJournalTransUpdateLedger.updateNow|
|LedgerJournalTransUpdateVend.updateNow|
|LedgerTransPerJournalDP.insertForLedgerBase|
|LedgerTransPerJournalDP.insertVoucherDetails|
|LedgerTransPerJournalDP.processReport|
|LedgerVoucher.check|
|LedgerVoucherGroup.end|
|LedgerVoucherObject.addBalanceAdjustments|
|LedgerVoucherObject.allocateTransaction|
|LedgerVoucherObject.post|
|LedgerVoucherObject.updateBalances|
|LedgerVoucherTransObject.check|
|Markup.copy|
|McrPriceHistoryLine_Sales.initAndInsertRebate|
|メソッド署名: 測定単位宣言を行う前にコンテキスト情報を追加する|
|PdsRebateFindAndCreate.findPdsRebateAgreementLineAndCreate|
|PdsRebateFindAndCreate.tamFindBillBackAgreementAndCreateClaim|
|PriceDisc.findDisc|
|PriceDisc.findDiscAgreement|
|PriceDisc.findItemPrice|
|PriceDisc.findPrice|
|PriceDisc.findPriceAgreement|
|PriceDiscAdmCheckPost.runFromContract|
|ProdJournalCheckPost.postProdJournalTableBOM|
|ProdJournalCheckPostProd.postTransLedger|
|ProdJournalCreateBom.createSingleLineProdBOM|
|ProdTableCleanUp.deleteProductions|
|ProdUpdCostEstimation.costEstimateItems|
|ProdUpdCostestimation.updateSubProdTable|
|ProdUpdReportFinished.updateBomConsumption|
|ProdUpdStartup.UpdateBomConsumption|
|ProjAdjustment.getNewTotalCostAmount|
|ProjAdjustment.setHourCostPrice|
|ProjAdjustmentSplit.createNewTrans|
|ProjAdjustmentSplit.initializeTmpProjAdjustmentCreate|
|ProjAdjustmentUpdate_Post.post|
|ProjAdjustmentUpdate_Post.postCost|
|ProjAdjustmentUpdate_Post.postItem|
|ProjBudget.queryProjBudgetLineCost / ProjBudgetLineCost(DataSource)|
|ProjBudget.queryProjBudgetLineCost / ProjBudgetLineRevenue(DataSource)|
|ProjBudgetManager.createBudgetFromForecastModel|
|ProjCategoryLookup.buildQueryTsTimesheetLine|
|ProjInvoiceChoose.main|
|ProjInvoiceJournalCreate.initJournalHeader|
|ProjInvoiceJournalPost.createProjInvoiceSalesLine|
|ProjInvoiceProposalInsertLines.doCost、doEmpl、doItem、doOnAccount、doRevenue、doSalesLine|
|ProjInvoiceProposalPeriodic.Validate|
|ProjJournalTrans.setHourCostPrice|
|ProjJournalTrans.setHourPrices|
|ProjJournalTrans.setHourSalesPrice|
|ProjPlanVersionsManager.CopyHierarchy|
|ProjPost.postCost|
|ProjPostCostProposalSale.projTransUpdate|
|ProjPostEmplProposalSale.projTransUpdate|
|ProjPostItemProposalSale.projTransUpdate|
|ProjPostRevenueProposalSale.projTransUpdate|
|ProjTable.createSalesTable_ItemReq|
|ProjTable.editSubProjects|
|psaContractLineInvoiceDP.insertTmpPSAContractLineInvoice|
|PsaGenerateQuotationLines.createSalesQuotationLines|
|PsaManageInvoiceDP.insertTmpPSAManageInvoice|
|PSAProjInvoiceDP.processLinesFromInvoiceJournal|
|PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax|
|PSAProjPostEmplIndirectProposal.indirectCreditAccountTurnover|
|PurchCreateFromSalesOrder.autoCreatePurchOrder|
|PurchCreateFromSalesOrder.checkLine|
|PurchCreateFromSalesOrder.main|
|PurchCreateFromSalesOrder.querySalesLine|
|PurchCreateFromSalesOrder.run|
|PurchFormletterParmDataInvoice.copyMarkupFromPurchOrder|
|PurchFormletterParmDataInvoice.createInvoiceHeaderFromTempTable|
|PurchFormletterParmDataInvoice.createLineAsset|
|PurchFormletterParmDataInvoice.selectChooseLines|
|PurchInvoiceJournalPost.postInventory|
|PurchLineType.initReleasedProductSpecificDefaulting|
|PurchOrderLineSourceDocumentLineItem.initMonetaryAmountValue|
|PurchReApprovalPolicyRule.evaluatePolicy|
|PurchRFQAcceptJournalPost.updateSourceTable|
|PurchRFQSendJournalCreate.createOrUpdateRFQLine|
|PurchTableForm.main|
|rDeferralsJournal.createTrans|
|rDeferralsProposalReceipt.createJournalLines|
|rDeferralsProposalRetirement.createJournalLines|
|rDeferralsProposalWritingOff.createJournalLines|
|rDeferralsTableMethodIterator.new|
|ReqDemPlanForecastAggregator.deaggregate|
|ReqDemPlanImportForecastService.insertDemandForecast|
|ReqIntercompanyDemand.initReqTransFromIntercompanyReqPO|
|ReqPO.Update|
|ReqTrans.updateBOMQty|
|ReqTransPoMarkSumUp.updateSumUp|
|RequisitionReleaseStrategy.runAutoPurchOrderGeneration|
|RetailTransactionSalesTransMark.findInventDimFromWorkingTable; など。添付ファイルを確認してください|
|RetailTransactionSalesTransMark.updateTransactionSalesLine_InventDimId|
|RetailTransactionServiceOrder.createOrUpdateRetailOrderLines|
|RetailTransactionServiceOrders.cancelCustomerOrder|
|RunBaseMultiParm.initFromForm|
|SalesCopying.callerSalesTable.returnItem|
|SalesFormletterParmDataInvoice.createBasedOnPackingSlip|
|SalesInvoiceController.initFormLetterReport|
|SalesInvoiceController.parmRunOnBlockMode_TH|
|SalesInvoiceController.PrintMgmtPrintSettingDetail|
|SalesInvoiceDP.addProductDimensionsToInventDim; tmpTaxWorkTrans;|
|SalesInvoiceDP.initInventDimData|
|SalesInvoiceDP.populateSalesInvoiceHeaderFooterTmp|
|SalesInvoiceDP.printBackorders|
|SalesInvoiceDPBase.createData|
|SalesInvoiceDPBase.init|
|SalesInvoiceJournalPost.postCustVend|
|SalesInvoiceJournalPost.postLine|
|SalesLineType.pmfValidateBatchId|
|SalesLineType_ReturnItem.validateField|
|SalesPackingSlipController.initFormLetterReport|
|SalesPackingSlipController.parmRunOnBlockMode_TH|
|SalesPackingSlipDP.checkPrintLineHeader|
|SalesPackingSlipDP.initializeInventDimReportSetup|
|SalesPackingSlipJournalPost.updateInventory|
|SalesParmTable.createPaymentSched|
|SalesPurchOperationTypeController_BR.getReferenceLookup|
|SalesQuotationDP.initializeInventDimReport|
|SalesQuotationProjLinkWizard.endUpdate|
|SalesQuotationTableType.disableFieldsIfCustomerAccountNotSpecified|
|SingleReturn.POSDeveloperSupport|
|SubledgerJournalizer.addRelievingAccountingDistributions|
|SubledgerJournalizer.fillPreviewTmpSummaryWithRounding|
|SubledgerJournalizer.loadaccountingDistributionTmp|
|SubledgerJournalizer.loadFinalizeSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadInterCompanyNonOffsetSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadInterCompanyOffsetSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadIntercompanySubledgerJournalTmpDetail|
|SubledgerJournalizer.loadRelievingSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadReversingSubledgerJournalTmpDetail|
|SubledgerJournalizer.loadStandardSubledgerLedgerJournalTmpDetail|
|SubledgerJournalizer.loadYearEndSubledgerJournalTmpDetail|
|SubledgerJournalizer.previewSummarizeJournalAccEntryDetail|
|SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding|
|SubledgerJournalizer.recordSubledgerJournalAccountEntries|
|SubledgerJournalizer.summarizeJournalAccountEntryDetail|
|TAMTradePromotion.ValidateFundCostLevel|
|taxBooksection.checkNumberSequenceSetup|
|TaxCalculationAdjustment.adjustBaseForTaxIncluded|
|TaxJournalSpec.parmTaxSpec|
|TaxProjInvoice.new|
|TaxReport770TransHandler_IT.transferTaxWithholdTrans|
|TaxReport770Validate_IT.validateVendors|
|TaxSplitPaymentPost_IT.creareReverseTaxTrans|
|TaxWithhold.postTaxWithhold|
|TaxWithholdSpecialDP.createTaxWithholdSpecialTmp|
|TmpProjAdjustmentCreate.createFromAdjustment|
|TmpProjAdjustmentCreate.fieldModifiedProjId|
|TmpProjAdjustmentCreate.setDimension|
|TmpProjAdjustmentCreate.setHourCostPrice|
|TransactionReversal_Asset.reversalBook|
|TransactionReversal_Cust.createAuxiliaryCustTrans|
|TransactionReversal_Ledger.createGeneralJournal|
|TrvExpTrans.setTaxGroup|
|TSTimesheetEntry.setFocusOnDayIndex|
|TsTimesheetFavorites.createTimesheetLines|
|TsTimesheetFavorites.validateWrite|
|TSTimesheetTable.checkHours|
|VendAccountStatementIntDP.insertVendAccountStatementIntTmpRil|
|VendOutPaymControlController.Insert|
|VendPaymentJournalDP.insertDataFromSpecTrans|
|VendRequestAddVendor.init|
|WhsContainerization.createNewContainer|
|WHSLoadLine.updateQtyLeftToLoad|
|WHSLoadTableAssignOriginInfo.assignFromFirstLoadLine|
|WHSLocationDirective.findPickPutLocation|
|WhsPostPackingSlip.alterLoadLine|
|WHSProdTable.pickBatchQtys|
|WhsWorkCreate.checkMaximums|
|WHSWorkCreateProdPut.insertProdParmforProdItem|
|WhsWorkExecuteDisplay.buildAboveLocationDimensions|
|WhsWorkExecuteDisplay.buildPick|
|WhsWorkExecuteDisplay.getNextFormState|
|WhsWorkExecuteDisplay.processWorkLine|
|WHSWorkExecuteDisplayCycleCount.buildCycleCount|
|WhsWorkExecuteDisplayCycleCount.buildFinish|
|WhsWorkExecuteDisplayPOItemReceiving.buildPOReceiving|
|WhsWorkExecuteDisplaySpotCycleCounting.displayForm|
|WhsWorkExecuteDisplaySystemGrouping.displayNextForm|
|WhsWorkExecuteDisplaySystemGrouping.getWorkIdFromFieldName|
|WhsWorkExecuteDisplayUserDirected.displayForm|
|WhsWorkExecuteDisplayUserGrouping.displayForm|
|WhsWorkExecuteDisplayValidateUserDirect.displayForm|
|WhsWorkExecuteDisplayValidateUserDirect.validateUserDirectWorkExists|
|WHSWorkTable.executeWorkLinesInit|
|WmsJournalCheckPostReception.returnOrderUpdate|
|WmsPickingList_OrderPickDP.initQueryWMSOrderTrans|
|WmsPickingList_OrderPickDP.insertIntoTempTable|
|WmsPickingList_OrderPickDP.orderQty|
|WmsPickingList_OrderPickDP.orderUnit|
|WmsPickingList_OrderPickDP.printDocumentHeader|
|WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate|

## <a name="other-changes"></a>その他の変更

次の追加の変更が、拡張機能に対して行われました。

- 計算済のエイジング バケットの数を増やすためにカスタマイズ機能をサポートする、更新されたエイジングおよび残高リスト クラスおよびフォーム。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]