---
title: Dynamics 365 for Finance and Operations バージョン 10.0.1 の拡張機能の変更
description: この記事では、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 に実装された拡張機能を一覧します。
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
ms.openlocfilehash: 6ddf5cd066f16c20fc9dad1edb8b13f8f4af76ce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866933"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-1001"></a>Dynamics 365 for Finance and Operations バージョン 10.0.1 の拡張機能の変更

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 にて実装された拡張機能を記載しています。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

今回のアップデートで実装された拡張を以下に記載します。

- ACOCostStatus\_BR
- ACOCostType\_BR
- ACOJournalType\_BR
- BankModuloCheck\_NO
- InventTransferOrderType\_BR
- ProdJourType
- ProjTransStatus
- RetailLabelTypeBase
- RetailLedgerBank
- RetailTenderFunction
- SalesPurchTrntype\_BR
- SMAGetPriceFrom
- SMASubscriptionIndexChange

## <a name="sql-operations-made-extensible"></a>拡張可能になった SQL 操作

今回のアップデートでは、以下のSQL操作が拡張されました。

- InventSumDelta.findInventSumDeltaInventSumFieldsAll.
- LedgerFiscalJournal は、QueryObject を使用するように変更されました。
- TaxTransDP.

## <a name="metadata-changes"></a>メタデータの変更

今回のアップデートで以下のメタデータが更新されました。

- Data Entities/WMSItemArrivalJournalLineEntity.IsPublic, PublicCollectionName, PublicEntityName
- DataEntities/LedgerJournalNameEntity/Fields/voucherSeriesCode 作成時に編集することが可能となりました。
- DataEntities/LedgerJournalNameEntity/Fields/VoucherSeriesCompanyId.AllowEdit.
- Enums\\SalesStatus::Backorder, Delivered.Label.
- Types/WeightBase.Scale におけるデータの拡張。
- InventTransferOrders は、フォームコントロールグループをグリッドに追加しました。

## <a name="refactored-methods"></a>リファクターされたメソッド

拡張性をサポートするために、以下のメソッドがリファクターされました。

- AssetProposalDepreciation.run
- BankStatementValidate.validateDate
- Class\\BankDocumentBankAccountTrans.loadSourceBuffer
- Class\\BankReconMatchingRuleAutoProcessor.doProcessMatchRule
- Class\\ProjJournalTransMapForm.initFromProjTable
- Class\\RetailEodStatementPaymentJournal.createPaymentJournalLine
- Class\\RetailKitAssemblyOrder.CreateOrUpdateBOMJournal
- Class\\RetailTransactionServiceOrders.createOrUpdateRetailOrderLines
- Class\\SalesInvoiceController.initReportName\_IN
- Class\\SalesInvoiceJournalPost.endUpdate
- Class\\WrkCtrScheduler.loadRoute
- CreditCard.mcrInitFromCustPaymTable
- CreditcardProcess.mcrDoCapture
- CreditCardProcess.mcrDoRefund
- CreditCardProviderProcess.Submit
- CustCollectionLetterCreate.skipCustomer
- CustVendCheque.output
- CustVendSumForPaym.run
- EFDOCDanfe\_BR.additionalInformationPageBreak
- EfDocDANFEDP\_BR.additionalInformationBox
- ERDocuManagement.insertFile
- ERFileDestinationAttachment.saveFile
- ERFileDestinationBrowser.saveFile
- Form\\BankReconciliationWorksheet.Init
- FreeTextInvoiceController.initReportName\_IN
- HcmWorkerTransition.createHcmWorker
- InventCostClosingCancel\_Init.createTasks
- InventDimCtrl\_Frm\_OnHand.initFromCaller
- InventMov\_Jour\_BOM.journalPostTrans
- InventProcessGuideDisplayLicensePlateDetailsPageBuilder.generateItemInfoForLicensePlate
- InventProcessGuideDisplayLocationDetailsPageBuilder.generateItemInfoForLocation
- InventStockCardDP.createInventStockCardTmpLineDetail
- InventTable.checkProjCategoryId
- InventUpd\_WHSReservation.updateReserveMore
- JmgCalcApproveWeekView.initializeData
- LedgerConsolidate.Run and getSelectedDimensionAttributes
- LedgerFiscalJournalDP\_IT.addStarsToTmpTable
- LedgerFiscalJournalDP\_IT.insertLedgerFiscalJournalTmp\_IT
- LedgerFiscalJournalDP\_IT.insertLedgerFiscalJournalTmp\_IT
- LedgerFiscalJournalDP\_IT.processReport
- LedgerJournalTrans.checkAllowEditWhenCheckPrinted
- LedgerJournalTransUpdateVend.pdateNow
- LedgerVoucherTransList.First
- LedgerVoucherTransList.next
- MCRFullTextIndexField.tableIdFromEnum
- MCRFullTextIndexField.viewFromTable
- MCRInventSearch.searchProduct
- McrPriceHistoryLine\_Purch.initAndInsertRebate
- PartyProvider.operatingUnitTypeToName
- PdsRebateAgreementValidate.construct
- POS\_IssueLoyaltyCardView.NA
- PriceDiscAdmCheckPostPriceDiscTableUpdater.formattedQueryValue
- PriceDiscAdmTrans.checkItemRelation
- ProjBudgetManager.deleteProjBudgetLinesWhenZeroAmount
- ProjBudgetManager.updateProjBudgetLinesWithAmt
- ProjHourCostPrice.psaFindCostPrice
- ProjInvoiceProposalListPageInteraction.initializeQuery
- ProjPostEmplProposalSale.new
- ProjPostRevenueProposalSale.new
- ProjTable.initProjectFromCustomerAndInvoice
- ProjTransferPrice.findByContractResourceCategory, findTransferPrice, find
- ProjValElementServer.addProjToResource
- ProjValElementServer.deleteProjFromResource
- PurchPackingSlipJournalPost.postMarkupOnTrans
- PurchReqLine.setProjSalesPrice
- PurchRFQSendJournalCreate.createOrUpdateRFQLine
- ReqCalc.covCalcDim
- ReqCalc.covCalcDim
- ReqCalc.covCalcDim
- RequisitionPurchaseOrderGeneration.create
- RequisitionPurchaseOrderGeneration.create
- Commerce runtime (CRT) のRetail extension point は ValidateCartLineQuantityAndPriceSymbol メソッドを無効にします。
- RetailCatalogProductAttributeFormHelper.addProductAttributeControls
- RetailCreateSpecificLabel.makeLabel
- RetailEodStatementCustomerOrderInvoiceController.run
- RetailEodStatementPaymentJournal.ledgerBank2LedgerJournalACType
- RetailEodStatementPaymentJournal.postPaymentJournalForOthers, postPaymentJournalForSales, createTenderedPaymentLines, createPaymentJournalLine
- RetailEodTransactionTransformer.ReadTransactionHeader
- RetailEodTransactionTransformer.setExtensionProperty
- RetailEventNotificationAction.packingSlipCompletion
- RetailMediaAssociationHelper.associateProduct
- RetailProductPropertyManager.validateWriteOnInventModelGroupItem
- RetailSMBSeedGenerator.AccountReceivable
- RetailStatementPost.createPaymentLedgerTrans
- RetailTransactionSalesTransMark.MarkTransactions
- RetailTransactionServiceOrder.settleCustomerOrder
- RetailTransactionServiceOrders.cancelCustomerOrder
- RetailTransactionServiceOrders.createCustomerOrder
- RetailTransactionServiceOrders.createLedgerJournalForStore
- RetailTransactionServiceOrders.createOrUpdateRetailOrderHeader
- RetailTransactionServiceOrders.createOrUpdateRetailOrderLines
- RetailTransactionServiceTransactions.fillPaymentTransDetails
- RetailTransactionServiceTransactions.fillRetailTransactionDetails
- RetailTransactionServiceTransactions.fillSalesTransDetails
- RetailTransactionServiceTransactions.getJournalListQuery
- SalesCreateOrder.updateDeliveryAddress
- SubledgerJournalizer.loadAccountingdistributionTmp
- SubledgerJournalizer.recordSubledgerJourAccEntriesForRounding
- SubledgerJournalizer.recordSubledgerJournalAccountEntries
- Table\\MCRContinuityScheduleLine.UpdateOtherLines
- Tax1099SummaryHelper.populateTaxSummaryFromVendSettlementTax
- TrvCreditCardTransactionEntity.validateWrite
- TrvExpenses.initializePersonalAmount
- TrvExpenses.updateFormVisibilityOnCategoryChange
- TrvExpenses.updateItemizationControls
- TrvExpTrans.copyValueToChildLines
- TrvExpTrans.defaultTaxGroupFromWorker
- TrvExpTrans.modifiedField
- TsTimesheetSignOffDP.insertTmpTSTimesheetSignOff
- WHSBillOfLadingDataUtil.populateCarrierInformation
- WHSBillOfLadingDataUtil.populateCustomerOrderInfo
- WHSLoadPlanningWorkbenchServerForm.addLoadLinesToLoad
- WHSLocationDirective.getValidSellableDaysQty
- WHSMobileAppAttachedImageDetails.getImageTypeFromSymbol
- WhsPostPackingSlip.updatePurchaseLoadLines
- WhsPostPackingSlip.updatePurchParmLineQuantityData
- WhsWarehouseRelease.main
- WhsWorkManualComplete.executeWorkLines
- WhsWorkManualComplete.performValidation
- WorkTimeCheckClassWorkCalendarDateLineTableWorkTimeLineTable class, validateWrite()
- WorkTimeLine.createWorkTimeCheck

## <a name="other-extensibility-enhancements"></a>その他の拡張性の強化

- **小売チャンネル:** OrderFulfillmentViewにおける機能拡張、 [すべて選択] と [すべてクリア] が利用可能となります。
- **小売チャンネル** : トランザクションアプリケーションプログラミングインターフェイス (API) から行IDごとに、戻り行をカートに表示します。
- **小売チャンネル** : OrderFulfillmentViewにてラインアイテムの場所を表示することができます。
- **小売チャンネル:** OrderFulfillmentView に ICustomListColumn が追加され、詳細情報を参照できるようになります。
- Retail ステートメントのポスティングメソッドは、RetailTransactionAggregationFieldListテーブルを使用して、別の集計ビューを追加します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]