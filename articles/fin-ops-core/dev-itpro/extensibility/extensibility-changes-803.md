---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
ms.date: 08/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-08-31
ms.dyn365.ops.version: App 8.0.3
ms.openlocfilehash: 5a5899bb7f0116b5307e759f785d40fd5132b9aa
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866264"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-803"></a>Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 の拡張機能の変更

[!include [banner](../includes/banner.md)]

これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.3 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="refactored-methods-to-support-extensibility"></a>拡張性をサポートするためにリファクターされたメソッド

これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。

| メソッド|
| --------------- |
|AccountingSourceExplorerProcessor.filterEntries|
|AgreementClassification.init|
|AgreementConfirm.createLineVolumeCommittmentHistory|
|AgreementConfirm.newAgreementConfirm|
|Agreementline.findLineForAutoMatch|
|Agreementline.getAgreementLinesForOrderLine|
|AgreementLine.getAgreementLinesForPurchReqLine|
|Agreementline.getAgreementLinesList|
|Bank_FR.checkControlText|
|Bank_IT.checkCIN|
|Bank_IT.checkRegistrationNum|
|BankAccountTrans.insert|
|BankAccountTrans.update|
|BankChequeCopy.fillTmpChequePrintout|
|BankChequePrint.printDocument|
|BankPaymAdviceReportGeneratorVend|
|BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc|
|BankReconciliationMatchRuleLine.getFieldsOfSysGenMatchRuleLineOfDoc|
|BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList|
|BankReconMatchingRuleAutoProcessor.getSearchedDocumentIdList|
|BankVoucher.createBankAccountTrans|
|BankVoucher.createBankAccountTrans|
|BomCopyToProd.copyTo|
|BudgetPlanLineFieldActiveViewMapping.getBudgetPlanLineFieldName|
|BudgetTransaction.openLinesInExcel|
|ChequeController.init|
|CustAccountStatementExt.main|
|CustAccountStatementExtController.includeOnStatement|
|CustAccountStatementExtController.insertCustAccountStatementExtTmp|
|CustAccountStatementExtController.setCommonData|
|CustAccountStatementExtController.tmpCustVendTrans|
|CustAccountStatementExtUIBuilder.build|
|CustAuditorDP.setCustAuditorTmp|
|CustCollectionJourDP.insertCustCollectionJourDP|
|CustCreditLimit.Balance|
|CustInterestNoteDp.processReport|
|CustInvoiceJour.printJournal|
|CustInvoiceTable.checkCreditLimit|
|CustPackingSlipJour.interCompanyUpdate|
|CustPaymEntry.updateConditionalControls|
|custPostInvoicejob.custPostInvoiceUpdate|
|CustTrans.reverseTransact|
|CustVendCheque.createBankChequePaymentTrans|
|CustVendCheque.createBankChequePaymentTrans|
|CustVendCheque.initTmpChequePrintout|
|CustVendCheque.output|
|CustVendCheque.output|
|CustVendChequeSlipTextCalculator.getChequeDocLength|
|CustVendSumForPaym.validateSEPATransaction|
|CustVendSumUpJournal.createTrans|
|CustVendVoucher.post|
|DimDerDistRuleProjectTimesheetsExt.populateDimAllocListIntercompany|
|DimDerJourRuleProjectTimesheetsExt.getDefaultDimensionAllocation|
|DirPartyVerification.selectionChanged|
|EcoResCategoryTreeDatasource.initializeAvailableCategoriesMap|
|EcoResProductCreate.writeMoreFields|
|EcoResProductDetailsExtended.initInventDimensionsMetadataEntries|
|ElectronicPaymentRemitExport_BR.construct|
|ForecastPuch|
|ForecastSales.accountConsumption|
|ForecastSales.accountDisc|
|ForecastSales.accountIssue|
|ForecastSales.accountSales|
|InventPosting.accountItemLedgerDimension|
|InventSupply.init|
|InventTrans.insertReturnTransOrigin|
|InventTransferParmLine - いくつかの方法|
|InventTransferUpd::updateLines|
|InventTransFormHelper.formQueryAddDynalink|
|InventTransWMS_Pick::updateInventServer|
|InventUpd_Physical::updatePhysicalReceiptTrans|
|InventUpdate.writeInventTrans|
|InventUpdate::createInventTransOriginAndReferences|
|InventValueReportPopulateItem::findReportLine|
|JmgRegistration.JmgJobTable|
|JournalizingDefinitionManager.newJournalizingDefinitionManagerPurch|
|JournalStatic.initializeDataModel|
|LedgerFinancialJournalReportDPBE.calcDebCredTotals|
|LedgerFinancialJournalReportDPBE.processReport|
|LedgerJournalDP.insertJournalTransForLedgerJournalTable|
|LedgerJournalDP.insertLedgerJournalTmp|
|LedgerJournalEngine.newJournalActive|
|LedgerJournalTrans checkAllowPosting|
|LedgerJournalTransUpdateBank.setBankVoucherSource|
|LedgerJournalTransUpdateBank.updateNow|
|LedgerJournalTransUpdateBankLC.addBankVoucher|
|LedgerPostingGeneralJournalController.transferLines|
|LedgerPurchaseJournalReportDPBE.insertIntoTempTable|
|LedgerSalesJournalReportDPBE.processReport|
|LedgerTransFurtherPosting.createLedgerJournalTransFromGenJour|
|LedgerTransVoucher.getSubledgerVoucherLinkDataSource|
|LedgerTransVoucher.getSubledgerVoucherLinkDataSource|
|LedgerTransVoucher.getVoucherDateRange|
|LedgerVoucherObject.updateLedgerPostingJournal|
|LedgerVoucherTransObject.checkRounding|
|Markup.insertMarkupTrans|
|MarkupTrans.MarkupTable.MarkupCode.Lookup|
|PaymSchedCalc::init*|
|PaymSchedCalc_Line::createTransaction|
|PdsApprovedVendorListCheck.newBasedOnTableType|
|PmfFormulaCoBy.run|
|PmfFormulaCoBy.ValidateField|
|PmfProdCoBy.ValidateField|
|PmfProdCoBy.ValidateWrite|
|PriceDiscAdmSearch|
|PriceDiscPolicyDialog.runPolicyDialog|
|ProdBOM.checkIsItemsReleased|
|ProdBOM::update|
|ProdJournalProd.Insert|
|ProdPurch.createPurchTable|
|ProdUpdHistoricalCost_Process.checkValidCoBy|
|ProdUpdReportFinished::updateBOMConsumption|
|ProdUpdStartUp,getListOfBOMJournals|
|ProdUpdStatusDecrease_StartUp.reverseBOMStartUp|
|ProjBudgetParticipantProvider.resolveByProject|
|ProjBudgetParticipantProvider.resolveByProjectHierarchy|
|ProjBudgetParticipantProvider.resolveByRootProject|
|ProjCaseActivitiesHandler.smmActivities_onValidatedDelete|
|ProjControlPeriod.forecast|
|ProjControlPeriod.forecast|
|ProjControlPeriodCostGroup.totalBudgetMinusActual|
|ProjControlPeriodCostGroup.totalBudgetMinusActual|
|ProjectPosting.costLedgerDimension.|
|ProjectPosting.getProjectLedgerDimension.|
|ProjForecastEmpl.initValue|
|ProjForecastReduceHour.constructQuery|
|ProjFundingSource.setInvoiceLocation|
|ProjGroup.initFromProjType|
|ProjIntercompanyCustomerInvoiceCreator.createInvoiceLine|
|ProjIntercompanyTransactionSelection.runQuery|
|ProjIntercompanyTransQuery.buildExpenseQuery|
|ProjIntercompanyTransQuery.buildHoursQuery|
|ProjIntercompanyTransQuery.buildVendorInvoiceLinesQuery|
|ProjInventJournalTransMapForm.checkActivity||
|projInvoiceChooose.setProposalJour|
|ProjInvoiceChoose.doRevenue|
|ProjInvoiceChoose.updateInvoiceTotal|
|ProjInvoiceProposalCreateLines.isRevenueTrans|
|ProjInvoiceProposalCreateLinesBase.createProposalTrans|
|ProjInvoiceProposalCreateLinesBase.doOnAccount|
|ProjInvoiceTable|
|ProjLedger.classdeclaration|
|ProjPostItemJournal.projTransCreate|
|ProjProjectsListPage.CtrlStages|
|ProjProjectsListPageInteraction.enableButton|
|ProjProjectsListPageInteraction.showButton|
|ProjStatusUpd.main|
|ProjStatusUpd.new|
|ProjTable - ProjTable datasource.write|
|ProjTable.clicked|
|ProjTable.editSubProj|
|ProjTable.editSubProj|
|ProjTableCreate.close|
|ProjTableCreate.run|
|ProjTableCreate.write|
|ProjTableCreate.write|
|ProjTableLookup.ProjProjectLookup.init|
|PSAProjInvoiceDP.insertPSAProjInvoiceHeaderTmp|
|PSAProjInvoiceTaxTmp.insertPSAProjInvoiceTmpForTax|
|PsaProjProposalSelection|
|PurchAgreementAutoCreate::construct|
|PurchAutoCreate.setPurchTable|
|PurchAutoCreate_PurchReq.initializeAndCreatePurchLine|
|PurchAutoCreate_PurchReq.initializeAndCreatePurchLine|
|PurchAutoCreate_ReleaseFromAgreement.updateFinDimFromAgreemHeader|
|PurchCreateFromSalesOrder.shouldCreatePurchOrder|
|PurchFormLetter::main|
|PurchFormLetter::main|
|PurchFormletterParmDataPackingSlip::reSelectLines|
|PurchFormletterParmDataPackingSlip::selectChooseLines|
|PurchFormletterParmDataPurchOrder::selectChooseLines|
|PurchInvoiceJournalPost.checkBeforePostingLine |
|PurchInvoiceJournalPost.updateSourceLine |
|Purchline.createline|
|PurchOrderLineBudgetControlPolicy.canCheckBudget|
|PurchReceiptsListDP.setPurchReceiptsListDetailsTmp|
|PurchReceiptsListDP.setPurchReceiptsListHeaderTmp|
|PurchRFQAcceptJournalPost.updatePurchReq|
|ReqCalc.covCalcDim|
|ReqTrans.createTransferDemand|
|ReqTransPoMarkFirm.createProdRoute|
|RetailPeriodicDiscount.ClassDeclaration|
|RetailTransactionServiceOrders.cancelCustomerOrder|
|Return.ReturnDispositionCodeId::validate|
|SalesAutoCreate::construct|
|SalesFormLetter.mainOnServer|
|SalesFormLetter.mainOnServer|
|SalesFormLetter::main|
|SalesFormletterParmDataConfirm::selectChooseLines|
|SalesFormletterParmDataInvoice::mayJournalTransBePosted|
|SalesFormletterParmDataInvoice::selectChooseLines|
|SalesFormLetterParmDataPackingSlip::selectChooseLines|
|SalesInvoiceDP.insertIntoSalesInvoiceTmp,insertIntoSalesInvoiceHeaderFooterTmp|
|SalesInvoiceJournalCreate.createJournalLine|
|SalesLine.CheckItemId|
|SalesLine.ValidateWrite_Server|
|SalesLine::calcLineAvailQty|
|SalesLine::createFromTmpFrmVirtualIL|
|SalesLineType.SalesLineType|
|SalesPackingSlipDP.setSalesPackingSlipDetailsTmp|
|SalesPackingSlipDP.setSalesPackingSlipHeaderTmp|
|SalesPackingSlipDP.setSysDocuBrandDetailsRegular|
|SalesPackingSlipDP.setSysDocuBrandDetailsRegular|
|SalesPackingSlipJournalPost.updateInventory|
|SalesQuotationLineType_Proj.validateProjTransTypeItem|
|SalesQuotationProjTable データ ソース SalesQuotationline|
|SalesQuotationTableForm.createABSFromTemplate|
|SalesTable.setLocation|
|SalesTable2LineUpdate.update|
|SalesTable2LineUpdate.update|
|SalesTable2LineUpdatePrompt.initpriceDiscUpdateTriggers|
|smmActivitiesEventHandler|
|SuppitemTable Table Cache Lookup プロパティ|
|テーブル PurchPrepayTable.updateAdvanceApplicationRemaining|
|TransactionReversal_Cust.reversal|
|TransactionReversal_Cust.reversal|
|TransactionReversal_Vend.reversal|
|TransactionReversal_Vend.reversal|
|TransactionReversal_Vend.reversal|
|TsTimesheetAddFavorites.addToFavorites|
|TsTimesheetCreate.createTimesheetLine|
|TSTimesheetEntry.initFields|
|TSTimesheetFavorites.createTimesheetLines|
|TSTimesheetLine.setCategoryIdFromActivity|
|VendInvoiceDocumentDP.insertVendInvoiceDocumentTmp|
|WHSLoadLine.validateStatus|
|WHSLoadLineAllocationProcessor.allocateLoadLine|
|WHSPostEngine.validateAnyDimAboveLocationMissing|
|WhsWarehouseRelease.createShipmentsForAllSalesOrders|
|WhsWarehouseRelease.createShipmentsForTransferOrders|
|WhsWorkCreateLP.createTempTable|
|WHSWorkCreateProdPut.createTempTable|
|WHSWorkExecuteDisplay.buildNextDimensionCaptureControl|
|WHSWorkLine::cancelLine|
|WmsArrivalCreateJournal::createWMSJournalTransFromTmp|
|WmsArrivalOverviewGeneration::updateOverviewInformation|
|WmsJournalCheckPostReception::initJournal|
|WMSOrderTrans::adjustQtyWMSOrderTrans|
|WMSOrderTrans::createNewWMSOrderTrans|
|WMSOrderTrans::insertOrUpdate|
|WMSOrderTrans::updateWMSOrderTrans|
|WmsPickingList_OrderPickDP.insertIntoTempTable,setWMSPickingList_OrderPickTmpTemplate|
|WmsPickingList_OrderPickDP.setWMSPickingList_OrderPickTmpTemplate|
|WrkCtrlScheduler_Proj.loadJob|
|WrkCtrScheduler_Prod.saveOperation|
|WrkCtrScheduler_Prod.saveOrder|

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

これらの列挙は、このアップデートで拡張可能になりました。

| 列挙型|
| --------------- |
|BankReconMatchRuleLineSysGeneratedType|
|BankReconMatchRuleLineSysGeneratedType|
|BankReconMatchRuleLineSysGeneratedType|
|ItemNumAlternative|
|JmgRegistrationErrorMode|
|MCRCustSearchType|
|ModuleSalesPurch|
|ModuleSalesPurch|
|ProjStatusRule|
|PurchRFQUpdateType|
|TAMVendRebateItemCode|
|TMSLoadBuildSupplyDemandType|


## <a name="additional-extensibility-enhancements"></a>追加の拡張性強化

リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。

- EcoResProductSearchName の EDT の文字列のサイズを増加
- AssetLedgerAccounts の CacheLookup プロパティを NotInTTS に変更します。
- TaxOnItem、TaxJurisdiction、TaxGroupData、TaxData、およびAssetLedgerAcounts で CacheLookup プロパティを検出に変更します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]