---
title: Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 の拡張機能の変更
description: この記事は、Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 でリリースされた拡張機能を一覧表示します。
author: FrankDahl
ms.date: 06/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2018-06-30
ms.dyn365.ops.version: App 8.0.2
ms.openlocfilehash: f1e29f6209bc625337abb9820dd43f6c037cb26d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866915"
---
# <a name="extensibility-changes-in-dynamics-365-for-finance-and-operations-update-802"></a>Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 の拡張機能の変更

[!include [banner](../includes/banner.md)]

これは、Dynamics 365 for Finance and Operations 更新プログラム 8.0.2 に実装された拡張機能の一覧です。 拡張性をサポートする変更のスケジュールの詳細については、「[アプリケーション機能拡張計画](extensibility-roadmap.md)」を参照してください。

## <a name="refactored-methods-to-support-extensibility"></a>拡張性をサポートするためにリファクターされたメソッド

これらのメソッドはリファクターされ、コマンド チェーン、デリゲート、またはメンバーへのアクセスの提供によって、拡張性をサポートします。

| メソッド|
| --------------- |
|AccDistProcessorProjectExtension.allocateExistingDistribution|
|AccDistProcessorProjectExtension.createDistributionLists|
|AccDistProcessorProjectExtension.ledgerDimensionAllocationList|
|AgreementConfirmationDP.processReport|
|Bank_FR.checkControlText|
|Bank_IT.checkCIN|
|Bank_IT.checkRegistrationNum|
|CustVendCheque.initTmpChequePrintout|
|FBSpedFileCreator_Contabil_BR.createRecordI052|
|HierarchyTemplateCopying_proj.createFromHierarchySource|
|HierarchyTreeLookup.datasource smmActivities.init|
|InventDim.validateFieldCombination|
|InventTransWMS_Register|
|InventUpd_Financial.updateFinancialIssue|
|InventUpd_Registered|
|JmgPostStandardSystem.PostProjTime|
|MarkupAllocation.run|
|MarkupTrans。 MarkupTrans(datasource).active|
|PdsBatchAttribByItem.checkDuplicateAttributes|
|PdsBatchAttribByItem.validateFieldValue|
|PdsBatchAttribReserve.linkActive|
|PdsBatchAttributes.Datasource.PdsBatchAttributes.linkactive|
|ProjInvoiceProposalCreateLines.closeOK|
|ProjInvoiceProposalInsertLines.doCost|
|ProjInvoiceProposalInsertLines.doEmpl|
|ProjInvoiceProposalInsertLines.doItem|
|ProjInvoiceProposalInsertLines.doOnAccount|
|ProjPeriodPostingLedgerSales.enteItem|
|ProjPeriodPostingLedgerSales.enterCost|
|ProjPeriodPostingLedgerSales.enterEmpl|
|ProjPeriodPostingLedgerSales.enterRevenue|
|ProjPeriodPostingLedgerSales.run|
|ProjPlanVersionsManager.CopyHierarchy|
|ProjPlanVersionsManager::CopyHierarchy|
|ProjPlanVersionsManager::createDraftVersion|
|ProjPlanVersionsManager::createTemplateHierarchy|
|PurchAutoCreate_PurchReq.initializeAndCreatePurchLine|
|PurchOrderLineSourceDocumentLineItem.calculateSourceDocumentAmountMap|
|PurchRFQPriceDiscAdmCreate.createPriceDiscAdmTrans|
|SalesFormLetter.validate|
|SalesTable2LineUpdatePrompt.salesTableFieldModifiedHandler|
|SalesUpdateRemain.cancelOpenOrderLinesDeliveryRemainder|
|WHSShipmentTable.createShipmentNotes|
|WHSUnShipLoadLineTmpDataCreator.createTmpLoadLineInventoryFromContainerLines|

## <a name="additional-extensibility-enhancements"></a>追加の拡張性強化

リファクタされたメソッドに加えて、次の拡張性の強化が実行されました。

- 拡張子からマップのサポート: CustVendTrans
- 拡張子からマップのサポート: CustVendTransOpen
- SQL 明細書の機能拡張をサポート: PriceDiscAdmCheckPost.postJournal


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]