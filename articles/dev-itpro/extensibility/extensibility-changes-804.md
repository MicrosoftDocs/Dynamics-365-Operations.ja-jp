---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
manager: AnnBe
ms.date: 08/27/2018
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
ms.search.validFrom: 2018-08-31
ms.dyn365.ops.version: App 8.0.4
ms.openlocfilehash: 906fac352834648508e8bb3fc2b7b076cca7c4b8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550891"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-804"></a>Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 の拡張機能の変更

[!include [banner](../includes/banner.md)]

これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.4 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="refactored-methods-to-support-extensibility"></a>拡張性をサポートするためにリファクターされたメソッド

これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。

| メソッド|
| --------------- |
|AgreementHeader.getModuleType|
|AssetSplit.construct|
|BankDepositSlipController.main|
|BankPositivePayExport.sendFileToUser|
|CaseDetailForm.getRecordsFromDataSource|
|CostSheetDesigner.DataSource:CostSheetCalculationFactor.validateWrite|
|CostSheetNodeCalculation.validate|
|CostSheetNodeCalculationRate.calcLowestLevel|
|CostSheetNodeCalculationSurcharge.equal|
|CustAccountStatementExtController.processParty|
|CustAccountStatementExtDP.insertNewRecords|
|CustAccountStatementExtDP.setSysDocuBrandDetails|
|CustBillOfExchangePost.postNextStep|
|CustBillOfExchangePostProtestHonored.postNextStep|
|CustCollectionJourController.runPrintMgmt|
|CustCollectionLetterCreate.createJournal|
|CustCollectionLetterCreate.run|
|CustCollectionLetterNote.CustCollectionLetterJour.active|
|CustCollectionLetterPost.processRow|
|CustCollectionLetterPost.validateCollectionLetter|
|CustFreeInvoiceCorrection.createInvoiceLines|
|CustInterestPost.main|
|CustInterestPost.validateInterestTrans|
|CustInvoiceJour.printJournal|
|CustInvoiceTable.calcDue|
|CustOpenBalanceCurrency.Data Sources – VendTrans – init|
|CustOpenTrans.editMarkTrans|
|CustPackingSlipJourFormHelper.areCancelCorrectButtonsEnabled|
|CustPaymEntry.editIsMarkedForSettlement|
|CustPostInvoice.main|
|CustPostInvoice.run|
|CustPostInvoice.validate|
|CustPostInvoiceJob.custPostInvoiceUpdate|
|CustPostInvoiceJob.initializeCustPostProcess|
|CustPostInvoiceJob.main|
|CustPostInvoiceJob.processCustPostInvoiceUpdate|
|CustProvisionalBalanceDP.calculateAmounts|
|CustProvisionalBalanceDP.insertCustProvisionalBalanceTmp|
|CustProvisionalBalanceDP.populateCustProvisionalBalanceTmpProcessing|
|CustProvisionalBalanceDP.processReport|
|CustProvisionalBalanceDP.translateMainAccountNamesOnCustProvisionalBalanceTmpProcessing|
|CustQuotationJournal.launchReport|
|CustSettlementPriorityProcessing .createTempData|
|CustSettlementPriorityProcessing .setPaymentAmount|
|CustSettlementPriorityProcessing .updatePartialTrans|
|CustSettlementPriorityProcessing.classDeclaration|
|CustSettlementPriorityProcessing.constructCustOpenTrans|
|CustSettlementPriorityProcessing.constructCustPaymEntry|
|CustSettlementPriorityProcessing.constructOffsetVoucherCust|
|CustSettlementPriorityProcessing.getBillingPriorities|
|CustSettlementPriorityProcessing.getSettlementQuery|
|CustSettlementPriorityProcessing.initCustTransOpen|
|CustSettlementPriorityProcessing.insertAllLinesAccrossInvoices|
|CustSettlementPriorityProcessing.markTransactions|
|CustSettlementPriorityProcessing.markTransByCreditNoteOnBillingClasses|
|CustSettlementPriorityProcessing.validateMarkedTransactionOpenTrans|
|CustStatisticsUS - メソッド calcStatistics|
|CustTable.validateCNPJCPF_BR|
|CustTrans.checkReversal|
|CustVendCheque.processChequeNum|
|CustVendCreatePaymJournal_Vend.searchTransactions|
|CustVendExchAdjPostingEngine.addExchangeAdjustment|
|CustVendFindSettlements.getTmpTrans|
|CustVendPaymProposalTransferToJournal.transferProposalLineToJournal|
|CustVendSettle.createSummaryAccountReliefTransactions|
|CustVendSettle.mustOffsetOriginalSummaryDistributions|
|CustVendSettle.postingProfileSettle_CreateDistributions|
|CustVendSettle.settleNow|
|CustVendTransDistributionController.getDistributionFactorsForPostingTypes|
|CustVendTransExchAdjDistController.getDistributionFactorsForPostingTypes|
|CustVendTransSettle.post|
|CustVendVoucher.initLedgerPosting|
|CustWriteOff.createInterestWriteOffJournalForInterestTrans|
|DataFileImportExportUtils.readStreamWriterAndWriteToStreamWriter|
|EcoResProductCreate.initDefaultControlValues|
|EcoResProductReleaseManager.releaseToLegalEntity|
|ExchangeRateImportOperation.saveRates|
|FormletterJournalCreate.newPurchJournalCreate|
|FulfillmentLineView.NewExtension|
|InterCompanyPost.formLetterCollect|
|InventCostIndirectFinancial.remainingQty|
|InventCostItemDim.load|
|InventCostJournalIndirectCost > addTrans|
|InventCostTrans.setRefTypeFromInventTransType|
|InventDimCtrl_Rep_Sales.initDimParmFormletter|
|InventDimCtrl_Rep_Sales.mustShowField|
|InventDimCtrl_Rep_Sales.reportStrItemId|
|InventDistinctProductOrderDefaultingController.construct|
|InventItemLocationCountingStatus.updateStopCountingJournal|
|InventItemPriceActivationJob.activateCostSheetCalculationFactor|
|InventJournalCheckPost_Movement.postTransLedgerMovement|
|InventJournalFormTrans_Movement.initReleasedProductSpecificDefaulting|
|InventoryMainAccDimensionListProvider.ledgerPostingType2InventAccountType|
|InventQualityOrderTable.setTestResult|
|InventSerial.init|
|InventSumPhysicalSpec.setValueQty|
|InventTable.insertInventItemOrderSetup|
|InventTrans.updateSumUp|
|InventTransferLine.updates|
|InventTransferUpd.beginLedger|
|InventTransIdSum.update|
|InventUpd_Estimated.updateFieldsChange|
|InventUpd_Financial.updateFinancialIssue|
|InventUpd_Financial.updateNow|
|InventUpd_Physical.updatePhysicalReturnedReceipt|
|InventUpd_Registered.pickReleatedIssueTransMore|
|InventUpd_Reservation.updateReserveMore|
|InventUpdateMarking.updateReservations|
|JmgAbsenceCalendar|
|JmgMESSwitchCode.init|
|LedgerExchAdj.postAdjustment|
|LedgerExchAdj.run|
|LedgerJournalEngine.initTaxGroup|
|LedgerJournalEngine_CustBillSettle.initCustOffsetAccount|
|LedgerJournalTransCustPaym.LedgerJournalTrans.CustVendBankAccountId.jumpRef|
|LedgerJournalTransUpdateCust|
|LedgerJournalTransUpdateLedger.updateNow|
|LogisticsPostalAddress.whsAddressFormatValidation|
|LogisticsPostalAddressFormEventHandler.updatePrimaryControl|
|Markup.calc|
|MCRCustPaym.ValidateWrite|
|McrCustPaymTotals_Sales.allPaymentsSubmitted|
|OffsetVoucher.updateNow|
|PmfCoByProdCalcTrans.updateRealCalcIndirect|
|PmfCoByProdCalcTrans.updateRealCalcIndirect|
|POSAPIdts.New トリガー|
|PriceDiscAdmCheckPost.checkForOverlapsAndGaps|
|PriceDiscAdmTrans.canEditPriceDiscValueField|
|ProcCategoryHierarchyManagement.init|
|ProdCalcTrans > メソッド updateRealCalcIndirect|
|ProdIndirectTrans > メソッド type2ItemCalcType|
|ProdJournalCheckPostProd.postTransLedger|
|ProdTableForm.handleProdTableCreatePreSuper|
|ProdUpdReportFinished.updateBOMConsumption|
|ProdUpdReportFinished.updateBOMConsumption|
|ProjAdjustmentUpdate.deleteJournal|
|ProjFundingLimitTrackingManager.updateUsingSourceDocument|
|ProjInvoiceProposalInsertLines.run|
|ProjInvoiceTableCreate.canClose|
|ProjInvoiceTableCreate.initializeValues|
|ProjPlanVersionsManager.createTemplateHierarchy|
|ProjPostCostJournal.projTransCreate|
|ProjSalesItemReq.SalesLine.linkActive|
|ProjTableType_TimeMaterial.validateWrite|
|PurchAgreement.applyQueryRanges|
|PurchApproveJournalPost.postPurgeLedgerAccount|
|PurchaseOrderResponseService.shouldPurchaseOrderBeAutoConfirmed|
|PurchAutoCreate_PurchReq.initializeAndCreatePurchLine|
|PurchAutoCreate_PurchReq.initializeAndCreatePurchLine|
|PurchAutoCreate_Sales.createLine|
|PurchCalcTax.construct|
|PurchCancel.run|
|PurchCreateFromOrder.insertMinMaxQty|
|PurchCreateFromSalesOrder.insertIntoTmpPurchLinePrice|
|PurchCreateFromSalesOrder.refreshCallerDataSource|
|PurchCreateFromSalesOrder.Salesline.specifyMinMaxQty|
|PurchCreateFromSalesOrder.SalesLine.specifyVendAccount|
|PurchCreateFromSalesOrder.validateSalesLine|
|PurchEditLines.canClose|
|PurchEditLinesForm.construct|
|PurchFormLetter.construct|
|PurchFormLetterContract.newFromPackedVersion|
|PurchFormletterParmDataInvoice.selectFromJournalLines|
|PurchFormLetterProvider.checkPurchLineChanged|
|PurchInvoiceJournalPost.updateSourceLine|
|PurchLine.checkInvoiceConstraints|
|PurchLine.ledgerDimensionItem|
|PurchLine.ledgerDimensionReceipt|
|Purchline.unLinkAgreementLinePrompt|
|PurchLine.validateField|
|PurchLine::setProjSalesPrice|
|PurchPrepayTable.updateAdvanceApplicationRemaining|
|PurchPurchOrderJournalPost.updateSourceTable|
|PurchReqCreate.init|
|PurchReqLine.setDefaultDimension|
|PurchReqLine.validateWrite|
|PurchReqTable.init|
|PurchReqTableForm.new|
|PurchRFQCaseTable.init|
|PurchTable.jumpRefIntercompanySalesOrder|
|PurchTableForm_DeliverySchedule.updatePurchLineTable|
|PurchTableInteraction.enableHeaderReceive|
|PurchTableType.validateDelete|
|PurchTableUpdateFromPurchReqLineMap.update|
|ReqTransPoMarkFirm.setPurchBuyerGroupId & updatePurchBuyerGroup|
|RetailGroupMemberLineHelper.internalCreateOrUpdateOrRemoveRetailGroupMemberLine|
|RetailLabelDP.insertTmpTable|
|SalesCalcAvailableDlvDates.mainOnServer|
|SalesConfirmJournalPost.updateSourceTable|
|SalesCopying.editCopy|
|SalesCopying.editMarkAll|
|SalesCopying.initReturnOrderFromCustomer|
|SalesCreateQuotation.canClose|
|SalesDropShipmentCancel.removeMarking|
|SalesEditLines.canClose|
|SalesFormletterParmData.reArrangeLines|
|SalesFormletterParmData.reArrangeSplit|
|SalesFormletterParmData.reArrangeSplit|
|SalesFormLetterProvider.checkJournal|
|SalesInvoiceDP.insertGiroInformation|
|SalesInvoiceJournalCreate.checkDocumentData_PL|
|SalesInvoiceJournalPostBase.postLine|
|SalesLine.resetInvent|
|SalesLineType.initDimensionsSpecificDefaulting|
|SalesLineType.initReleasedProductSpecificDefaulting|
|SalesPackingSlipDP.setSalesPackingSlipDetailsTmp|
|SalesPackingSlipJournalCreate.updateJournalLine|
|SalesPackingSlipJournalCreate.updateJournalLine|
|SalesPackingSlipJournalPost.insertBackorderLine|
|SalesPackingSlipJournalPost.interCompanyPost|
|SalesPackingSlipJournalPost.updateJournalLine|
|SalesPurchSummaryModel_Account.createNewJournal|
|SalesQuotationCalcTax_Sales.construct|
|SalesQuotationEditLinesForm.postUpdate|
|SalesQuotationLineType.initFromProjTable|
|SalesQuotationLineType.initReleasedProductSpecificDefaulting|
|SalesQuotationTable.modifiedField|
|SalesQuotationTableForm.createFromTemplate|
|SalesQuotationUpdate_Cancelled.run|
|SalesQuotationUpdate_Lost.run|
|SalesTable.initFromCustTableMandatoryFields|
|SalesTable.jumpRefIntercompanyPurchaseOrder|
|SalesTable.setShipCarrierFromLogisticsLocation|
|SalesTable.update|
|SalesTableForm.interCompanyAutoCreateOrders|
|SettlementPair.createSettlementForDebitOrCreditTrans|
|SmaServiceFunctionLine_Transfer.createJournalLine|
|SmaServiceFunctionLine_Transfer.postJournalTransType|
|SmaServiceOrderCreate.createServiceOrderLine|
|SmaSubscriptionGenerator::postTrans|
|smmBusRelTable.relation2Vendor|
|smmBusRelTable.updateQuotations|
|SmmCampaignBroadcast::validate|
|SmmOpportunityStatusUpdate.updateOpportunity|
|smmOpportunityTable\Methods\openQuotation|
|SmmProjectCreate.createSingleProject|
|SmmProjectCreate.createSingleProject|
|SmmUpdateBusRel.updateFromVendTableSFA2|
|SubledgerJournalTransferController.run|
|SuppItem.calcSuppItem|
|SuppItem::newSuppItem|
|SuppItemCreate::newSuppItemCreate|
|Tax.post|
|Tax.saveAndPost|
|TaxFreeInvoice_Invoice.updateAndPost|
|TaxPost.moveTaxLineToNewOwner|
|TaxPost.saveAndPostFromTmpTaxWorkTrans|
|TaxPost.saveAndPostFromTmpTaxWorkTrans|
|TaxVoucherService.postTaxOnErrorAccount|
|TradePackingSlipJourChain.createRelationship|
|TradeTotals.calc|
|TradeTotals.updateOrderBalances|
|VendAccountStatementIntDP.processReport|
|VendEditInvoice\DataSource\VendInvoiceInfoTable\Methods\write|
|VendInvoiceMatching.initExpectedValues|
|VendInvoiceWFParticipantProviderExpend.resolve|
|VendOpenTrans.editMarkTrans|
|VendorInvoiceLineSourceDocLineItem.calculateSourceDocumentAmountMap|
|VendPaymentJournalDP.insertDataFromLedgerJournalTrans|
|VendPaymentJournalDP.insertDataFromSpecTrans|
|VendPromissoryNotePost.postNextStep|
|VendProvisionalBalanceDP.calculateAmounts|
|VendProvisionalBalanceDP.insertVendProvisionalBalanceTmp|
|VendProvisionalBalanceDP.processReport|
|VendTransListDP.ProcessReport|
|VendVoucher.createInvoiceJournal|
|WHSDocumentRouting.printDocument|
|WhsLoadLineInventTransValidator.checkLoadLineInventTransConsistencyOnInventoryUpdate|
|WHSLoadLineUpdater.initAndInsertLoadLine|
|WhsShipConfirm.createASNItems|
|WhsWarehouseRelease.createLoadLines|
|WHSWorkExecute.executeShortPick|
|WHSWorkExecuteDisplayLPReceiving.displayForm|
|WHSWorkExecuteDisplayLPReceiving.displayNextForm|
|WHSWorkExecuteDisplayMovementByTemplate.displayForm|
|WhsWorkExecuteForm.createLabel|
|WmsJournalCheckPostReception.postTrans|
|WmsOnlineCountingServer.getMovement|
|WmsOnlineCountingServer.handleLine|
|WmsOrderCreate.updateCreatewmsOrder|
|WrkCtrResourceAbilityMapController.loadData|

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

これらの列挙は、このアップデートで拡張可能になりました。

| 列挙型|
| --------------- |
|ABCModel|
|AccountOrder|
|AmountUnit|
|CostCalculationRateSubtype|
|CurrencyGainLossAccountType|
|CustInterestCodeSource|
|CustPaymentType|
|DirViewLocationNodeType|
|InterestCalcAccountChoice|
|InventTransPostingType|
|MCRCustSearchType|
|PaymentStub|
|PaymentStubInclAll|
|ProjCompletePrincip|
|ProjMatchingPrincip|
|RetailPOSSeedDataType|
|SalesQuotationStatus|
|TMSApptStatus|
|TMSCommunicationType|

## <a name="additional-extensibility-enhancements"></a>追加の拡張性強化

リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。

- CustVendSettle: 変数をプライベートではなく保護に設定します。
- イベントを引き起こさないデータ操作メソッド: WHSLocationDirective.loopLocDirLines。
- イベントを引き起こさないデータ操作メソッド: WhsWorkCreate.createTempLine。
- マップ拡張: LogisticsPostalAddressMap。
- マップ拡張: PurchReqLineMap。
- メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Is Public = Yes。
- メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Collection Name = ProjWBSActivityEstimates。
- メタデータの変更: DataEntityView/ProjWBSActivityEstimatesEntity.Public Entity Name = ProjWBSActivityEstimates
- メタデータの変更: /Data Model/Data Entities/EcoResProductAttributeValueEntity.IsPublic = Yes。
- メタデータの変更: Form/WHSLoadPlanningListPage/FormDesign/FormDesign/FormActionPaneTabControl/ActionPaneTabShipReceive.Needed permission。
- メタデータの変更: WHSContainerLine, Relations WHSLoadLine & WHSShipmentTable.On Delete。
- メタデータの変更: WHSContainerTable, Relation WHSShipmentTable.On Delete。
- プロジェクトの価格決定: 新しい価格決定検索メソッドの完全な取得。
