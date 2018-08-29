---
title: "Finance and Operations バージョン 8.0 の拡張機能の変更"
description: "これは、Dynamics 365 for Finance and Operations バージョン 8.0 に実装された拡張機能の一覧です。"
author: FrankDahl
manager: AnnBe
ms.date: 04/13/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-04-04
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 7719338e572a56cc6acf40f95d97655779fe8017
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="extensibility-changes-in-the-finance-and-operations-version-80"></a>Finance and Operations バージョン 8.0 の拡張機能の変更

[!include[banner](../includes/banner.md)]

## <a name="hard-sealed-application-models"></a>ハード シールされたアプリケーション モデル

Dynamics 365 for Finance and Operations バージョン 8.0 では、Microsoft のアプリケーション モデルはすべてハード シールされています。 これらのモデルのオーバーレイ コードは、現在コンパイル エラーを発生します。 カスタマイズ モデルは拡張機能によってのみサポートされます。 拡張機能によってこれらのモデルをカスタマイズできない場合は、標準のアプリケーションを変更して拡張機能を有効にするよう、Microsoft に要求する必要があります。

次の表に、今回のリリースで現在ハード シールされているモデルの一覧が含まれています。

| モジュール | モデル         |
| --------------- |-------------|
|ApplicationCommon | ApplicationCommon |
|ApplicationSuite | Electronic Reporting Application Suite Integration |
|ApplicationSuite | Foundation Upgrade |
|ApplicationSuite | Foundation |
|ApplicationSuite | SCMControls |
|ApplicationSuite | Tax Books Application Suite Integration |
|ApplicationSuite | Tax Engine Application Suite Integration |
|CaseManagement | CaseManagement |
|Currency | Currency |
|DataImpExpApplication | DataImpExpApplication |
|DataUpgrade | DataUpgrade |
|Directory | Directory |
|Directory | SecurityReports |
|GeneralLedger | GeneralLedger |
|Ledger | Ledger |
|PersonnelManagement | PersonnelManagement |
|ProcessGuide | ProcessGuide |
|Retail | Retail |
|SourceDocumentation | SourceDocumentation |
|SourceDocumentationTypes | SourceDocumentationTypes |
|Subledger | Subledger |
|Tax | Tax |

## <a name="enumerations-that-have-been-made-extensible"></a>拡張可能になった列挙

列挙の拡張をサポートするために以下の変更が行われました。
- 標準アプリケーションの多くの列挙が拡張可能になりました。 列挙を拡張可能にするには、列挙に関する 2 つのプロパティを設定します。 **IsExtensible** プロパティは **はい** に、**UseEnumValue** プロパティは **いいえ** に設定されます。 
- 一部の列挙型は状態を表します。 拡張機能によって列挙値の追加を可能にする新しいファサード メソッドが追加されました。 列挙型を拡張する方法については、「[列挙値の追加](add-enum-value.md)」を参照してください。
- 拡張機能をサポートするために、列挙を使用する一部のアプリケーション コードが変更されました。 一般的な変更の内容は以下の通りです。
    + ポストイベント サブスクリプションを許可するための、switch の default ケースの **throw** 例外ステートメントの削除。
    + 拡張機能の **SysExtension** サポートの追加。
    + 明示的なデリゲートの追加。

| 列挙型|
| --------------- |
|BOMConsumpType|
|BOMFormula|
|BOMType|
|ChequeFormType|
|CostGroupType|
|CustAccountStatement|
|CustMandateScheme|
|CustVendDisputeStatus|
|DispositionAction|
|ItemCalcType|
|KMCollectionAnswerStatus|
|KanbanEventType|
|LedgerAccrualPeriod|
|LogisticsAddressElement|
|LogisticsLocationEntityType|
|NoneBeginTransEnd|
|PSAInvoiceFormats|
|PdsCumulationPeriod|
|PdsRebateProgramType|
|PdsRebateTransaction|
|PdsUnitType|
|PriceDiscSystemSource|
|ProdFlushingPrincipBOM|
|ProdFlushingPrincipItem|
|ProdReservation|
|ProjAccountTypeCost|
|ProjAccountTypeSales|
|ProjAccountType|
|ProjJournalType|
|RevenueContributionMargin|
|SMATransactionType|
|SysPolicyRuleEnum|
|SysPolicyRuleTypeEnum|
|SysPolicyTypeEnum|
|TAMRebateAmtType|
|TAMVendRebateStatus|
|TMSRecordType|
|Voided|
|WMSJointShippingType|
|WMSReferenceType|

## <a name="data-manipulation-methods-that-do-not-raise-dataevents-or-missing-insert-update-delete-pre--and-post-data-events"></a>DataEvents または欠落している insert、update、delete プリおよびポストデータ イベントを生成しないデータ操作メソッド

一般なプラクティスとして、テーブルのデータ メソッドを使用して、アプリケーションの拡張に使用できるイベントを発生させます。 コード ベースは、必ずしもこのプラクティスに従っていませんでした。 たとえば、**doInsert**、**doUpdate**、および **doDelete** データ メソッドと特定のテーブルの実装では、データ メソッドで **super()** の呼び出しは行われませんでした。

タイプ クラスの **insert**、**update**、および **delete** メソッドはリファクターされました。 データ メソッドで **super()** が確実に呼び出されるように変更が行われました。 これらの変更により、これらのメソッドへの拡張機能の追加が可能になり、その結果、プリイベントとポストイベントが拡張機能で使用できるようになりました。 次の表に、**insert**、**update**、および **delete** イベントが拡張機能に対して有効になったテーブルを表示します。

| タイプ、名前、データ ソース、およびメソッド |
| ----------------------|
|フォーム ProjTableCreate.ProjTable.write|
|フォーム ReturnTable.ReturnTable.leaveRecord|
|フォーム SalesQuotationProjTable.SalesQuotationTable.leaveRecord|
|フォーム SalesQuotationTable.SalesQuotationTable.leaveRecord|
|フォーム SalesTable.SalesTable.leaveRecord|

## <a name="refactored-methods-to-support-extensibility"></a>拡張性をサポートするためにリファクターされたメソッド

これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。

| タイプ、名前、およびメソッド |
| ----------------------|
|クラス AgreementConfirm_Sales.startConfirm|
|クラス AssetChangeGroup.updateAssetGroupInfo|
|クラス AssetPost.createAssetTransForPost|
|クラス AssetSplit.getUpdatedSplitValueModel|
|クラス AssetTableMethod.init|
|クラス AssetTableMethod_SL.calc|
|クラス AxSalesLine|
|クラス BankPaymCancel.serverRun|
|クラス BomSearch.New|
|クラス BomSearch_BOMCopyType.New|
|クラス Commission.run|
|クラス CostSheetPanel.build|
|クラス CreateInvoiceJournalPost.createFixedAsset|
|クラス CustAccountStatementIntDP.printingAmountMST|
|クラス CustCreditLimit.balanceEstimate|
|クラス CustCreditLimit.calculateBalance|
|クラス CustCreditLimit_SalesTable.New|
|クラス CustInterestCreate|
|クラス CustVoucher.post|
|クラス DimensionDerivationRule.buildDimensionCombination|
|クラス EcoResProductInformation.main|
|クラス EcoResProductReleaseManager.setAndSaveRetailProductProperties|
|クラス EcoResProductValidator.isEssentialFieldValuesSet|
|クラス FormLetterServiceController.newFromContract|
|クラス FormletterJournalPost.postLineDiscount|
|クラス Graphics_WrkCtrCapBooking.insertLoad|
|クラス Graphics_WrkCtrCapBooking.loadGroupReservations|
|クラス Graphics_WrkCtrCapBooking.loadNumReservations|
|クラス InterCompanyPostPurch.construct|
|クラス InterCompanySyncPurchLineType|
|クラス InterCompanySyncPurchTableType.setSalesTableData|
|クラス InterCompanySyncPurchTableType|
|クラス InventAgeDimDP.createOrMergeInventAgeDimTmp|
|クラス InventAgeDimDP.insertOrMergeInventAgeDimTmp|
|クラス InventAgingCmdAggregateSelected.execute|
|クラス InventCostItemDim.initInventSettlement|
|クラス InventCostReport.newInventCostReport_CostBaseType|
|クラス InventCountCreateItems.run|
|クラス InventDimCtrl_Frm.clearInvisibleRanges|
|クラス InventItemPriceActivationTaskActivateSim.activateOneInventItemPriceSim|
|クラス InventItemPriceSim.moveSimulatedToCurrent|
|クラス InventLedgerPostingDefinitionEntityHelper.inventAccountTypeX2InventAccountType|
|クラス InventMov_SalesQuotation.isQuotationQtyEditable|
|クラス InventProductDimensionLookup.dimEDT2FieldId|
|クラス InventProductDimension|
|クラス InventQualityManagementBlock.actOnAssociations|
|クラス InventQualityManagementCreate.createOnRegistration|
|クラス InventQualityManagementCreate.createQualityOrder|
|クラス InventQualityManagementCreate.generateQualityOrders|
|クラス InventQualityManagementCreateInvent.generateQualityOrdersWithDiscrimination|
|クラス InventQualityMgmtCreateNonInvent.generateQualityOrdersWithDiscrimination|
|クラス InventQualityOrderReopen.main|
|クラス InventQualityOrderReopen.run|
|クラス InventQualityOrderValidate.main|
|クラス InventQualityOrderValidate.run|
|クラス InventQualityReferenceTypeSales.isEligibleForQualityManagement|
|クラス InventQualityReferenceTypeSales.supportsInventoryBlocking|
|クラス InventQualitymanagementCreate.createPerQualityAssociations|
|クラス InventSumReCalcItem.updateActualInventSum|
|クラス InventTestAssociationTable.checkAccountRelation|
|クラス InventTestAssociationTable.initRecord|
|クラス InventTrackingDimTracingCriteria.initFromArgs|
|クラス InventTransLine.insert|
|クラス InventTransferMulti.run|
|クラス InventTransferMultiReceive::main|
|クラス InventTransferMultiShip.buildParmFromWMSShipment|
|クラス InventTransferMultiShip.runUpdate|
|クラス InventTransferOrderOverviewDP.insertTmpTable|
|クラス InventTransferUpdShip.updateInventTransferLine|
|クラス InventUpd_Physical.updatePhysicalIssue|
|クラス InventUpd_Physical.updatePhysicalReturnedReceipt|
|クラス InventUpd_Picked.updatePickInventTrans|
|クラス InventUpd_Reservation.whsUpdateReserveMore|
|クラス InventUpdate.raiseOnHandChangingOnPhysicalStatusUpd|
|クラス InventUpdate.updateDimReservePhysical|
|クラス InventUpdate.updateTransDimTransferReceipt|
|クラス InventUpdate.writeInventTransAutoDim|
|クラス InventValueReportDP.processInventValueReportTmpLine|
|クラス InventoryMainAccDimensionListProvider.populateMainAccountDimensionList|
|クラス LedgerBalanceQueryGeneralJournal.addToBalanceTotals|
|クラス LedgerBalanceQueryGeneralJournal.createQuery|
|クラス LedgerJournalCheckPost.checkJournal|
|クラス LedgerJournalCheckPost.postJournal|
|クラス LedgerJournalDP.insertJournalTransForLedgerJournalTable|
|クラス LedgerJournalDP.insertLedgerJournalTmp|
|クラス LedgerJournalGetTrans.createLedgerJournalTrans|
|クラス LedgerVoucherObject.addTrans|
|クラス LedgerVoucherTransObject.check|
|クラス LogisticsLocationSelectForm.construct|
|クラス LogisticsLocationSelectForm.main|
|クラス LogisticsPostalAddressFormHandlerExt.onNewParameters_delegate|
|クラス MCRItemListGeneration.generateItemListLines|
|クラス MCRItemListGeneration.generateItemListLines|
|クラス MCRMarginAlert.skipMarginCalc|
|クラス Markup.mcrDeleteNonUser|
|クラス MarkupAllocationSelectionManager.setQueryRanges|
|クラス PSAProjInvoiceDP.insertPSAProjInvoiceTmp|
|クラス PSAProjInvoiceDP.insertProformaPSAProjInvoiceTmp |
|クラス PdsApprovedVendorListCheck.newBasedOnTableType|
|クラス PlanActivityTimeCalculation.calculatePlanActivityTime|
|クラス PordJournalCreateBOM.createLinesProdBOM|
|クラス PriceDisc.accountRelation|
|クラス PriceDisc.findDiscAgreement|
|クラス PriceDisc.findDisc|
|クラス PriceDisc.findPriceAgreement|
|クラス PriceTypeConverter.priceTypeToPriceGroupType|
|クラス PrintMgmtReportFormatSubscriber.add|
|クラス PrintMgmtReportFormatSubscriber.populate|
|クラス ProdBOM.prodFlushingPrincipItem2BOM|
|クラス ProdJournalCreateBOM.createLinesInventTrans|
|クラス ProdJournalCreateBOM.createLinesInventTrans|
|クラス ProdJournalCreateBOM.createLinesProdBOM|
|クラス ProdJournalCreateBOM.dialog|
|クラス ProdJournalCreateBOM.validate|
|クラス ProdJournalFormTransBOM.setupCWFormControl|
|クラス ProdPickListController.prePromptModifyContract|
|クラス ProdPicklistDP.insertValues|
|クラス ProdStatusType_Released.checkPostJournal|
|クラス ProdTableListPageInteraction.getEnabledControls|
|クラス ProdUpdReportFinished.updateBomConsumption|
|クラス ProdUpdReportFinished.updateRouteConsumption|
|クラス ProdUpdSplit.createSplitToProduction|
|クラス ProdUpdStartUp.getListOfBOMJournals|
|クラス ProdUpdStartUp.updateBOMConsmption|
|クラス ProjInvoiceDP.insertIntoProjInvoiceTmp|
|クラス ProjInvoiceProposalInsertLines.run|
|クラス ProjInvoiceProposalInsertLines::run()|
|クラス ProjPlanVersionsManager|
|クラス ProjPostItemJournal::projTransCreate|
|クラス ProjProposalTotals.calc|
|クラス PsaProjInvoiceDP::insertProformaPSAProjInvoiceTmp|
|クラス PsacustomerRetention.createFeeTransactionForProposal|
|クラス PurchAgreementGenerateReleaseOrder.check|
|クラス PurchAgreementGenerateReleaseOrder.validatePurchLinesWithPurchQty|
|クラス PurchAutoCreate.construct|
|クラス PurchAutoCreate.construct|
|クラス PurchAutoCreate_RFQ.construct|
|クラス PurchAutoCreate_SalesProjectItemReq.createLine|
|クラス PurchAutoCreate_SalesProjectItemReq.createPurchLine|
|クラス PurchCancel.parmPurchTable|
|クラス PurchCancel.run|
|クラス PurchCopying.deleteLines|
|クラス PurchCreateFromSalesOrder|
|クラス PurchFormLetterParmData.createParmLine|
|クラス PurchFormLetterParmDataInvoice.createParmLineAndSubLines|
|クラス PurchFormletterParmData.reSelectLines|
|クラス PurchFormletterParmDataApproveJournal.updateQueryBuild|
|クラス PurchFormletterParmDataInvoice|
|クラス PurchInvoiceCreate.createJournalLine|
|クラス PurchInvoiceJournalCreate.checkInvoicePolicies|
|クラス PurchInvoiceJournalCreate.checkMatching|
|クラス PurchInvoiceJournalPost.createFixedAsset|
|クラス PurchInvoiceJournalPost.lateMatchPackingSlip|
|クラス PurchLineType.validateWrite|
|クラス PurchLineVersioningFieldSet.isChangeConfirmationRequired|
|クラス PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap|
|クラス PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap|
|クラス PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap|
|クラス PurchPackingSlipDP.createProductReceiptLines|
|クラス PurchPackingSlipJournalPost.selectFormletterJournalTrans|
|クラス PurchRFQCaseAutoCreate.newAutoCreate|
|クラス PurchReApprovalPolicyRuleFieldList.addTable2Hierarchy|
|クラス PurchReApprovalPolicyRuleFieldList.addTable2Hierarchy|
|クラス PurchSelectLinesManager.passSets|
|クラス PurchTableInteraction.enableHeaderPurchase|
|クラス PurchTableInteractionHelper.getJournalEnquiryButtons|
|クラス PurchTableInteractionHelper.getUpdateJournalButtons|
|クラス PurchaseOrderResponseConsume.checkIfPurchLinesRequireUpdate|
|クラス PurchaseOrderResponseConsume.checkIfResponseLineCannotBeConsumedAndUpdateConsumptionState|
|クラス PurchaseOrderResponseConsume.consumeFirstPurchaseOrderResponeLineAndInitiateArchivingOnPurchLine|
|クラス PurchaseOrderResponseConsume.consumeRemainingPurchaseOrderResponseLines|
|クラス PurchaseOrderResponseConsumeLine.checkIfSelectedPurchLinesRequireUpdate|
|クラス ReqCalc.covCodeQty|
|クラス ReqCalc.insertItemInventSum|
|クラス ReqCalc.insertItemInventTrans|
|クラス ReqTransFormPo.validateFromInventLocationId|
|クラス ReqTransPoMarkChangeToRFQ.DialogPostRun|
|クラス ReqTransPoMarkFirm.createPurchLine|
|クラス ReqTransPoMarkFirm.setPurchTable|
|クラス RetailAssortmentLookupTask.explodeAssortments|
|クラス RetailCreateLinesFromProductsToAdd.createPeriodicDiscount|
|クラス RetailCreateLinesFromProductsToAdd.loadLines|
|クラス RetailPackagePurchManagement.createLines|
|クラス RetailProductPropertyManager.saveInventTableAndRelated|
|クラス RetailProductPropertyManager.validateWriteOnInventTable|
|クラス RetailSalesOrderCalculator.saveSalesOrder|
|クラス RetailSalesOrderCalculator.setPriceOnCurrentLine|
|クラス RetailSalesQuotationCalculator.saveSalesQuote|
|クラス RetailSalesQuotationCalculator.setPricesOnCurrentLine|
|クラス ReturnTableInteraction.enableControl|
|クラス RouteCopyToRoute.insertRouteOpr|
|クラス SMAServiceFunctionLine_Transfer.checkJournalType|
|クラス SMAServiceFunctionLine_Transfer.postJournalType|
|クラス SMAServiceFunctionLine_Transfer.sumjournals|
|クラス SMAServiceOrderCreate.createServiceOrderLine|
|クラス SalesAutoCreate_ReleaseFromAgreement.createSalesTable|
|クラス SalesCancelOrder.run|
|クラス SalesCopying.copy|
|クラス SalesCreateOrderFromCutomer.main|
|クラス SalesFormLetter.mainOnServer|
|クラス SalesFormLetterParmData.createParmLine|
|クラス SalesFormLetterReport.construct|
|クラス SalesFormletterParmData.reSelectLines|
|クラス SalesFormletterParmDataInvoice.reSelectInit|
|クラス SalesInvoiceDP.invoiceTxt|
|クラス SalesInvoiceDP.itemId|
|クラス SalesLineCopyFromSource.updateCopiedLine|
|クラス SalesLineType.setReservation|
|クラス SalesLineType.setSalesStatus|
|クラス SalesLineType.syncPurchLine|
|クラス SalesPackingSlipDP.createSalesPackingSlipLines|
|クラス SalesPackingSlipJournalPost.addToInventReportDimHistory|
|クラス SalesPurchLineInterface.setPriceAgreement|
|クラス SalesQuotationCopying.copyHeader|
|クラス SalesQuotationEditLinesForm_Sales_Confir.createSalesTable|
|クラス SalesQuotationEditLinesForm|
|クラス SalesQuotationLineType_Sales.validateWrite|
|クラス SalesTableListPageInteraction.setButtonInterCompany|
|クラス SalesTableType.checkUpdate|
|クラス SalesTableType.interCompanyMirror|
|クラス SmmCampaignQueries|
|クラス SmmLeadUpdate|
|クラス SmmOpportunityLink|
|クラス SmmUpdateBusRel.updateFromCustTableSFA2|
|クラス TradeCurrencyConversionPrompt.construct|
|クラス TradeLineRenumbering.renumber|
|クラス TradeTotals.calc|
|クラス VendDocumentLineInterface.setPurchaseQty|
|クラス VendInvoicePolicyValidation.policyViolationMessage|
|クラス VendProvisionalBalanceDP.processReport|
|クラス WHSPool.pickFromWorkCenter|
|クラス WHSShipConfirm.createUOMStructure|
|クラス WHSWorkExecute.pickLicensePlateHandledByLP|
|クラス WhsInventOnHandReserve.changeReservation|
|クラス WhsInventOnHandReserve.setMovement|
|クラス WhsPackForm.buttonPack_clicked|
|クラス WhsPostEngineBase.createLoadFromShipment|
|クラス WhsShipConfirm.createInventTransferParmLineTMS|
|クラス WhsShipConfirm.createInventTransferParmLine|
|クラス WhsWorkExecute|
|クラス WmsBillOfLadingDP::insertIntoTempTable|
|クラス WmsOrderTransType_OutputDontPostTransfer.updateParentMovement|
|クラス WrkCtrCapResHandler.hasNewCapacityReservation|
|クラス WrkCtrCapResHandler.loadCapacityReservations|
|クラス WrkCtrReservedSum.calcReservationSumGroupId|
|クラス WrkCtrReservedSum.calcReservationSumGroupId|
|クラス WrkCtrReservedSum.calcReservationSumWrkCtrId|
|クラス WrkCtrReservedSum.calcReservationSumWrkCtrId|
|クラス WrkCtrScheduler_Prod.saveOperation|
|クラス createParmLinesFromTransferLinesOnLoad|
|クラス smmCampaignQueries.lookupClass|
|エンティティ EcoResProductDimensionGroupEntity.dataSourceDimensionFieldId|
|エンティティ InventProductDefaultOrderSettingsEntity.insertEntityDataSource|
|エンティティ InventProductSiteSpecificOrderSettingsEntity.insertEntityDataSource|
|エンティティ PSAActualEntity.createQuery_LaborConsumptionQty|
|エンティティ PSAActualEntity.createQuery_LaborConsumption|
|エンティティ PSAActualEntity.createQuery_PlLaborCost|
|エンティティ PSAActualEntity.createQuery_PlLaborQty|
|エンティティ PSAForecastEntity.createQuery_LaborConsumptionForecastQty|
|エンティティ PSAForecastEntity.createQuery_LaborConsumptionForecast|
|エンティティ PSAForecastEntity.createQuery_PlLaborForecastCost|
|エンティティ PSAForecastEntity.createQuery_PlLaborForecastQty|
|フォーム BOMCalcDialog.updateDesign|
|フォーム EcoResProductCreate.releaseProductToCompany|
|フォーム InventItemOrderSetup.InventItemSetupSupplyType.editOrderType|
|フォーム InventLocationIdLookup.InventDim_DS.init|
|フォーム InventLocationIdLookup.InventLocation_DS.init|
|フォーム InventNonConformanceTable.init|
|フォーム InventNonConformanceTableCreate.InventNonConformanceTable.write|
|フォーム InventQualityOrderTableCreate.allowEdit|
|フォーム InventQualityOrderTableCreate.refreshCaller|
|フォーム InventTestAssociationTable.initRecord|
|フォーム InventTransPick\TmpInventTransWMS.validateWrite|
|フォーム LedgerTransVoucher.updateQueryForProject|
|フォーム MarkupAllocation.init|
|フォーム MarkupAllocation_VendInvoiceTrans|
|フォーム PdsBatchAttributes.PdsBatchAttributes.linkActive|
|フォーム PriceDiscAdmTable.init|
|フォーム PriceDiscTable.appendInventCriteria|
|フォーム PriceDiscTable.buildOrderLineFilter|
|フォーム PriceDiscTable.buildSearchFilter|
|フォーム PriceDiscTable.isLineFilterEnabled|
|フォーム PriceDiscTable.retrieveRelationType|
|フォーム ProdParmStartUp.ProdParmStartUp.active|
|フォーム ProjCreditNoteSelect.editMark|
|フォーム ProjTableCreate.ProjTable.write|
|フォーム PurchCreateFromSalesOrder.initFields|
|フォーム PurchUpdateRemain.closeOk|
|フォーム ReqTransPoMarkFirm.init|
|フォーム RetailAddItems.closeOk|
|フォーム RetailColorGroupTable.RetailColorGroupTrans.recordHasChanges|
|フォーム RouteLookupOprNum.init|
|フォーム VendEditInvoice.invoiceAccountModified|
|フォーム VendEditInvoice.run|
|フォーム VendOpenTrans.editMarkTrans|
|フォーム WrkCtrCapResGraphDialog.setParm|
|マップ BomCalcTransMap.displayUnitId|
|テーブル AssetTable.lookupAccountNum|
|テーブル AssetTrans|
|テーブル CaseDetailBase.validateWrite|
|テーブル EcoResProductMasterConfiguration.existWithSameConfigUnit|
|テーブル FormletterJournalTrans.getLinePrefix|
|テーブル InventItemPriceSim.autoSalesPrice|
|テーブル InventQualityOrderLine.adjustInt|
|テーブル InventQualityOrderTable.createInventQualityOrderLines|
|テーブル InventQualityOrderTable.initFromReference|
|テーブル InventQualityOrderTable.initQtyFromAssocation|
|テーブル InventTestAssocationTable.checkAccountRelation|
|テーブル InventTestAssocationTable.validateWrite|
|テーブル InventTrans.insertReturnTransOrigin|
|テーブル InventTransOrigin.createOrigin|
|テーブル InventTransferParmLine.createPickLines|
|テーブル InventTransferParmLine.createReceiveLines|
|テーブル InventTransferParmLine.createShipLines|
|テーブル JmgStampjournalTrans|
|テーブル JmgTermReg.createJournalSignIn|
|テーブル JmgTermReg.update|
|テーブル LedgerJournalTrans.delete|
|テーブル LedgerJournalTrans.validateWrite_Server|
|テーブル PriceDiscAdm.getEntityAutoReportFieldGroupName|
|テーブル PriceDiscAdm.getEntityJournalNumberFieldName|
|テーブル PriceDiscAdmTrans.CheckAccountRelation|
|テーブル PriceDiscAdmTrans.checkItemRelation|
|テーブル PurchLine.setPriceDisc|
|テーブル RouteVersion.selectRouteVersion|
|テーブル SalesLine.checkItemId|
|テーブル SalesLine.getSourcingFields|
|テーブル SalesLine.setPriceAgreement|
|テーブル SalesLine.setPriceDisc|
|テーブル SalesLine.setSourcingFields|
|テーブル SalesQuotationLine.IsCategoryBased|
|テーブル SalesQuotationLine.mcrCreateFromTmpFrmVirtualFromContract|
|テーブル SalesQuotationLine.setPriceAgreement|
|テーブル SalesQuotationLine.setPriceDisc|
|テーブル Salesline.splitReturnLine|
|テーブル SuppItemCreate.createLine|
|テーブル TmpInventTransMark.packTmpMark|
|テーブル VendInvoiceMatchingLine.initFromPurchLine|
|テーブル VendTable.updateOnHold|
|テーブル WHSInvent.checkNonPhysicalDims|
|テーブル WHSShipmentTable.consolidateShipments|
|テーブル WHSShipmentTable.transferShipment|
|テーブル WHSTmpPackingLine.addTmpPackLine|
|テーブル salesLine.initFromProjTable|
|テーブル smmBusRelTable.updateReferences|
|テーブル smmLeadTable|
|テーブル smmOpportunityTable|


## <a name="maps-enabled-for-extensibility"></a>拡張性に対して使用可能なマップ

拡張機能によるフィールドとメソッドの追加を可能にするマップ実装に対して、新しいパターンが導入されました。 これの実行方法の詳細は、インターフェイスとして使用されるマップが含まれるドキュメントとバージョン管理実装のためのドキュメントの両方にあります。

次の表に、拡張性を有効にするために変更が適用されたマップとその関連テーブルを一覧表示します。

| マップ |
| -------------------|
|CustVendSettlement|
|JmgStampTransMap|
|PriceDiscResultFields|
|SalesPurchLine|

## <a name="inventory-dimensions"></a>在庫分析コード

今回のリリースでは、拡張機能による複数のシナリオのサポートをすべて対象とする在庫分析コードの追加のために、新しいモデルにマイナーな改良を加えました。 

| 変更 |
| -------------|
|BOM 階層はコンフィギュレーション分析コードとのみ連携します|
|フォーム BOMDesigner は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム EcoResProductSearchLookup は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム FactureJournal_RU は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム InventDimParmFixed.InventDimensionXXFlag.Style は正しくありません|
|フォーム InventItemOrderSetup は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム InventTransferParmPick は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム InventTransferReleaseOrderPicking は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム KanbanCreateScheduled は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム KanbanJobPickingListPart は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム KanbanRules は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム LeanPeggingTree は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム MCRItemDisplay は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム MCRPriceDiscGroupItem は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PlanActivityServiceWizard は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム ProdBOMVendor は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム PurchAgreementGenerateReleaseOrder は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム PurchAgreementHistory は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchComplementaryInvoice は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchRFQCompareLineDimensions は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchTable.TrackingDimesions のスペルが正しくありません|
|フォーム PurchVendorPortalAllResponse は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchVendorPortalConfirmedOrders は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchVendorPortalOriginalOrder は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchVendorPortalRequests は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム PurchVendorPortalResponses は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム ReqDemPlanEasyItemAllocator は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム ReqOutboundIntercompanyDemand は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム ReqSupplyDemandScheduleFilters は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム RetailVariantLookup は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム RouteVersionFeasibility は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム SMAAgreementTable は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム SalesAgreementGenerateReleaseOrder は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム SalesAgreementHistory は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム SalesComplementaryInvoice は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム SalesLineDeliveryDetails は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム SalesQuotationProjTable は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム SalesQuotationTable は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム SalesTable は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム TAMFundManagement は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム TAMTradePromotions は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム VendEditInvoice は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム VendJournalMatch_PackingSlip は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム WHSLoadPlanningWorkBench は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム WHSLoadPlanningWorkbench は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム WHSLoadTable は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム WHSLoadTable は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム WHSProdWaveTableManageBOMPool は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム WHSWorkTable は、分析コードの表示にフィールド グループを使用する必要があります |
|フォーム WMSOrderTransUnPick は、分析コードの表示にフィールド グループを使用する必要があります|
|フォーム WMSPickingRegistration は、分析コードの表示にフィールド グループを使用する必要があります |
|レポート InventAging は追加の分析コードをサポートしません|
|テーブル EcoResProductVariantStaging.StagingIdx は、追加の分析コード フィールドを必要とします|

## <a name="other-changes"></a>その他の変更

次の表に、拡張機能に対して行われた追加の変更を一覧表示します。

| 変更 |
| -------------|
|フィルター インターフェイスの追加: form InventQualityOrderTable|
|住所管理: 新しい住所フィールドの追加|
|AxMaps - TradePostalAddress - partyTable|
|銀行トランザクション コメント - BankReconciliationDataInitializer|
|取消ログ要件 - 販売配送残量の更新|
|購買要求明細行から購買明細行にグループ分けするメカニズムの拡張|
|購買要求明細行から購買明細行に分割するメカニズムの拡張|
|在庫品目要求と共に複数の資金調達ソースを許可|
|為替レート プロバイダー フレームワークの実装|
|すべての使用で PriceDiscPartyCodeType を拡張可能にする|
|すべての使用で PriceDiscProductCodeType を拡張可能にする|
|テーブル RetailChannelTable には ReplacementKey がありません|
|テーブル RetailSeasonTable CreateRecIdIndex True|
|インデックスの変更: テーブル InventTestAssociationTable|
|パブリックに切り替えられたエンティティ UnitOfMeasureEntity|
|パブリックに切り替えられたエンティティ UnitOfMeasureTranslationEntity|

