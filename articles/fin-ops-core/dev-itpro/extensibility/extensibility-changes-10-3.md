---
title: Dynamics 365 for Finance and Operations バージョン 10.0.3 の拡張機能の変更
description: この記事では、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 に実装された拡張機能を一覧します。
author: FrankDahl
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-10
ms.dyn365.ops.version: App 10.0
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4d9c347e305221d917c6a0d93810d5c3c62f98b3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270915"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-version-1003"></a>Dynamics 365 for Finance and Operations バージョン 10.0.3 の拡張機能の変更

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.3 にて実装された拡張機能を記載しています。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="enumerations-made-extensible"></a>拡張可能になった列挙

今回のアップデートで実装された拡張を以下に記載します。

- LedgerJournalWFApprovalModule
- RetailReceiptTransaction

## <a name="sql-operations-made-extensible"></a>拡張可能になった SQL 操作

今回のアップデートでは、以下のSQL操作が拡張されました。

- 拡張可能マップパターンにむけた CustVendTrans の実装

## <a name="metadata-changes"></a>メタデータの変更

今回のアップデートで以下のメタデータが更新されました。

- CostSheetAmount.NoOfDecimalsIsExtensible
- SalesLinePercent.NoOfDecimalsIsExtensible

## <a name="refactored-methods"></a>リファクターされたメソッド

拡張性をサポートするために、以下のメソッドがリファクターされました。

- BankReconciliationDataInitializer.initDocumentOpenTmp
- BankReconciliationDataInitializer.initStatementOpenTmp
- Class\\BomCalcJob\_All.processSingleTask
- Class\\KanbanEventQuantityMap.newStandard
- Class\\MCRFullTextSearchRefresh.run
- Class\\PdsRebateAgreementValidate.validate
- Class\\PurchRFQFormLetter.main
- Class\\ReqTransPoMarkFirm.getPurchIdSingleThread
- Class\\TAMVendRebateCorrectClaims.correctClaims
- Class\\TAMVendRebateCorrectClaims.createClaimCorrection
- Class\\TAMVendRebateCorrectClaims.rebateAmountPerUnit
- Class\\WhsReleaseToWarehouseForm.buttonRelease\_clicked
- Classes\\LedgerAllocationRules.ValidateDimension
- Classes\\ProjJournalCheckPost.checkFeeJournalDimensions
- Commission\_Sales.run
- CreditcardPaymentCardTokenize.getFromDialog
- CustInPaymDialog.openDialog
- CustVendDisputeHelper.canDeleteDispute
- EcoResCategoryTreeDatasource.new
- EcoResProductRelationtable.validateWrite
- Form\\EcoResProductCreate.updateCallers
- Form\\InventOnhandReserve\\DataSource\\InventSum.reserveNow
- Form\\PdsRebateAgreement\\DataSource\\PdsRebateAgreement.executeQuery
- Form\\ProcCategoryHierarchyManagement\\FormDesign\\CategoryTreeGroup\\CategoryTreeCtrl.selection
- Form\\ReqSupplyDemandSchedule.updateDesign
- Form\\SalesTable\\DataSource\\MCRSalesLineDropShipment\\field\\DropShipment.modified
- Form\\SalesTable\\DataSource\\SalesTable.create
- FormletterService.removeProforma
- InventJournalTrans.validateWrite
- InventJournalTrans\_Tag.validateWrite
- InventMovement.addLedgerPhysicalAmount
- InventMovement.canAutoReserveQuantity
- InventTransSerialNumberCreate.checkFormat
- InventUpd\_Reservation.updateReserveLess
- LedgerJournalEngine.onSegmentChangedForPrimaryAccount
- LedgerJournalTransCustPaym.enableDisableMandate
- LedgerTransStatementDP.processOffsetAccountInStaging
- PdsBatchAttribReserveForm.checkReserveLine
- PriceDisc.findDiscAgreement
- PriceDiscAdmCheckPost.postJournal
- PriceDiscHeading.updateDiscQty
- PriceDiscHeading.updateMultiLineDiscTmp
- PriceDiscPolicyFindOrCreate.run
- ProjInvoiceControl.projInvoiceControl
- ProjPostCostJournal.new
- PurchLineType.validateWrite
- ReqTransFormExplosion.tmpReqExplosionOnhandBuildServer
- ReqTransPoMarkFirm.createPurchTable
- ReqTransPoMarkFirm.updatePurchBuyerGroup
- RequisitionPurchaseOrderGeneration.createPurchaseOrder
- RetailBarCodeManagement.CreateBarCodeNoDim
- RetailTransactionServiceOrders.createCustomerOrder
- RetailTransactionTransformer.readTransactionSalesTrans
- SalesLine.createLine
- SalesLine.initFromPriceDisc
- SalesLine.insert
- SalesLine.update
- SalesLine.validateDelete
- SalesLine.writeRetailSalesLine
- SalesTable.updateMultiLineDisc
- SmaServiceFunctionLine\_transfer.Run
- SmmOpportunityStatusUpdate.updateFromQuote
- Table\\MCRCustpaymTable.salesTableByPassCreditLimit, displayOrderID, getCurrency, and mcrCustPaym\\getCustomerPostingProfile
- Table\\ReqPO.findAnySalesLineForReqPO
- TaxUncommitted.createTaxUncommitted, added local method createTaxUncommittedFromTmpTaxWorkTrans
- TmpTaxReport\_IT.create
- TrvExpTrans.defaultTaxGroupFromWorker
- WHSBillOfLadingDP.insertWHSBillOfLadingTmp
- WHSControlItemId.populate
- WhsWarehouseRelease.creditLimitCheck
- WhsWorkCreate.addRangesToWorkTemplateQuery
- WHSWorkExecute.CreateTransferJournalLine
- WhsWorkTypePrintHandler.buildLabelAndConfirm

## <a name="other-extensibility-enhancements"></a>その他の拡張性の強化

- The PriceDiscHeading マップが拡張可能になりました。
- **小売チャンネル:** Shipped、PackingSlip、MarkAsPacked に対してプレトリガーが追加されました。
- **小売チャンネル:** キャンセル費用のダイアログボックスを無効化することができます。
- **小売チャンネル:** オーダー検索のダイアログボックスに、オーダー取消のデフォルト パラメータ値が拡張されました。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
