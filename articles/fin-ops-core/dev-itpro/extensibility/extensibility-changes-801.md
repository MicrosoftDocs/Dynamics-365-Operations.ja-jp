---
title: Finance and Operations 更新プログラム 8.0.1 の拡張機能の変更
description: このトピックは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.1 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
ms.date: 05/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: App 8.0.1
ms.openlocfilehash: 0ef8f5c686425dac8ed88caab3568cde58cc917b
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866268"
---
# <a name="extensibility-changes-in-finance-and-operations-update-801"></a>Finance and Operations 更新プログラム 8.0.1 の拡張機能の変更

[!include [banner](../includes/banner.md)]

これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.1 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="refactored-methods-to-support-extensibility"></a>拡張性をサポートするためにリファクターされたメソッド

これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。

| 方法|
| --------------- |
|クラス ProjControlPeriod::PeriodInsert|
|クラス ProjInvoiceChoose::doSalesLine|
|クラス CustInvoiceJour::printFreeTextJournal|
|クラス ProjCostControl.createEmptyTransactionType|
|クラス ProjEstimate::autoGenerateEstimateLinesFromTask|
|クラス ProjEstimateDataContract.updateEstimates|
|クラス ProjForecastBudget.Run|
|クラス ProjHierarchyProvider.preDeleteHierarchy|
|クラス ProjPlanVersionsManager::CopyTasks|
|クラス ProjPlanVersionsManager.createDraftFromPublishedVersion|
|クラス ProjPlanVersionsManager.PublishQuotationSubHierarchy|
|クラス ProjPlanVersionsManager.CreateDraftVersion|
|クラス ProjTask.addTask|
|クラス ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup|
|クラス VendOpenTrans.editMarkTrans|
|クラス CustVendReversePosting.reverseTaxWithholdTrans|
|クラス CustVendSettle.postPennyDiff|
|クラス CustVendSettle.processStillOpenTransactions|
|クラス InventTransferOrderOverviewDP.insertTmp|
|クラス LedgerJournalTransCost.LedgerJournalTrans.Create|
|クラス ProjAdjustmentSelect.dialog|
|クラス ProjEstimate.syncEstimateLinesFromTask|
|クラス ProjEstimateDataContract.UpdateEstimates|
|クラス ProjForecastTransferFromWbs.transferToForecast|
|クラス ProjWizardActivityCtrl.insertDBOnServer|
|クラス ProjTaskEstimatesSynchronizer.calcTotalEstimateLineHours|
|クラス ProjTaskEstimatesSynchronizer.countNumberOfHourEstimateLines|
|クラス ProjTaskEstimatesSynchronizer.syncExistingHourEstimatesWithTask|
|クラス ProjTaskEstimatesSynchronizer.syncHourEstimatesWithTaskEffort|
|クラス ProjWbsCostPlanningServerActions.executeDataRetrievalAction|
|クラス ProjWbsCostPlanningServerActions.getProjectCategoryTypes|
|クラス ProjWbsSchedulePlanningServerActions.executeAction|
|クラス ProjWbsSchedulePlanningServerActions.executeDataRetrievalAction|
|クラス ProjStatisticCalc.validate|
|クラス WHSInventReserve.insert|
|クラス WHSInventReserveDelta.insert|
|クラス ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup|
|クラス ProjJournalTransEmpl - Datasource: ProjJournalTrans.Validate|
|クラス LedgerJournalEngine.initTaxItemGroup|
|クラス LedgerJournalEngine.initValue|
|クラス ProjJournalTrans.mergeResourceDimensionDefault|
|クラス ProjTask.setTaskinfo|
|クラス ProjJournalName.standardJournalName|
|フォーム ProjInvoiceProposalCreateLines.performTransTypeSelectionCtrlLookup|

## <a name="other-extensibility-enhancements"></a>その他の拡張性の強化

リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。

- 小数点以下の変数番号のサポート - InventTestLowerLimit
- 小数点以下の変数番号のサポート - InventTestLowerTolerance
- 小数点以下の変数番号のサポート - InventTestStandardValue 
- 小数点以下の変数番号のサポート - InventTestUpperLimit
- 小数点以下の変数番号のサポート - InventTestUpperTolerance
- トランザクションの取消でスキップ確認をサポートします。
- PSAProjQuotationApproval ワークフローの拡張機能の有効化


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]