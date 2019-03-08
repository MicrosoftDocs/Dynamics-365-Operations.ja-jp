---
title: ワークスペースのフィルター処理およびコンフィギュレーション
description: この記事は、ワークスペースを構成してフィルター処理する方法の概要について説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace, HcmBenefitWorkspace, BudgetPlanningWorkspace, BusinessProcessGenericWorkspace, RetailCatalogManagementWorkspace, RetailCategoryAndProductWorkspace, RetailChannelManagementWorkspace, HcmCompensationWorkspace, CAMCostAccountingLedgerAdminWorkspace, CostAdminWorkspace, CostAnalysisWorkspace, CAMCostControlWorkspace, CustomerCollectionManagerWorkspace, CustomerInvoiceWorkspace, CustPaymentWorkspace, DataManagementWorkspace, DataValidationWorkspace, ERWorkspace, LedgerPeriodCloseProjectWorkspace, AssetWorkspace, GeneralJournalEntryWorkspace, VendVendorPortalInvoiceWorkspace, BudgetTrackingWorkspace, ReqCreatePlanWorkspace, BusinessProcessGenericOwnerWorkspace, SelfHealingWorkspace, WHSOutboundWorkMonitoringWorkspace, WHSWavePlanningWorkspace, PayrollWorkspace, HcmWorkforceWorkspace, RetailDiscountPricingWorkspace, EcoResProductDiscreteManufacturingWorkspace, KanbanPrepareProductForLeanWorkspace, EcoResProductProcessManufacturingWorkspace, EcoResProductVariantMaintainWorkspace, JmgShopSupervisorWorkspace, ProjProjectManagementWorkspace, VendVendorPortalWorkspace, PurchOrderMaintainWorkspace, PurchOrderProcessReceiptsWorkspace, HcmRecruitmentWorkspace, EcoResProductMaintainWorkspace, FMClerkWorkspace, OpResLifecycleManagementWorkspace, RetailITWorkspace, RetailChannelOperationsWorkspace, RetailStoreManagementWorkspace, SalesOrderProcessingWorkspace, SalesReturnWorkspace, SystemAdministrationWorkspaceForm, VendVendorRequestForQuotationsWorkspace, VendVendorProfileManagementWorkspace, VendInvoiceWorkspace, VendPaymentWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17491
ms.assetid: 541e6012-4680-4684-8494-e9b5ca4684ee
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77d30759d2a8ed85a28f8a29663057f20496f16d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "325690"
---
# <a name="configure-and-filter-workspaces"></a>ワークスペースのフィルター処理およびコンフィギュレーション

[!include [banner](../includes/banner.md)]

この記事は、ワークスペースを構成してフィルター処理する方法の概要について説明します。

## <a name="configuring-a-workspace"></a>ワークスペースのコンフィギュレーション

ワークスペース全体に適用される設定を変更することにより、ワークスペースの外観と動作を変更できます。 ワークスペースが構成できる場合、[アクション] ウィンドウには設定を変更するボタンがあり、これをクリックするように指示が表示されます。 たとえば次の図では、**自分のワークスペースのコンフィギュレーション**というボタンが表示されています。

[![ワークスペースの構成とフィルター](./media/configure-and-filter-workspaces.png)](./media/configure-and-filter-workspaces.png)

ボタンをクリックすると、ワークスペースの定義済設定を変更できるダイアログが表示されます。 このダイアログに表示される特定の設定は、各ワークスペースによって異なり、ワークスペースで使用できる特定のコントロールや業務データによっても異なります。

[![マイ ワークスペースの構成](./media/configure-my-workspace.png)](./media/configure-my-workspace.png)

## <a name="filtering-a-workspace"></a>ワークスペースのフィルタ処理

多くのワークスペースでは、表示される内容をフィルタ処理することができます。 使用できるコントロールにより、ワークスペースのすべて内容や、ワークスペースの特定のセクションにある内容をフィルタ処理できる場合があります。 ワークスペースのフィルターは、ルックアップ、コンボ ボックス、自由書式のテキスト フィールド、または他のコントロール タイプである場合があります。 ただし、次のセクションで説明するように、それぞれのフィルタのタイプは同じ効果があります。

### <a name="workspace-wide-filters"></a>ワークスペース全体のフィルター

ワークスペース全体のフィルターを使用すると、ワークスペース全体をフィルター処理できます。 ワークスペース全体のフィルターは、ワークスペースの左上隅にあります。 ドロップダウン リストで特定の値を選択すると、その選択内容に基づいてワークスペースのコンテンツがフィルター処理されます。

[![ワークスペース フィルター](./media/workspace-filter.png)](./media/workspace-filter.png)

クリックしてフィルターを開くと、複数のオプションが表示されます。

[![展開済ワークスペース フィルター](./media/workspace-filter-expanded.png)](./media/workspace-filter-expanded.png)

オプションに基づいワークスペースのてフィルターを適用するオプションを選択します。

### <a name="workspace-section-filters"></a>ワークスペース セクション フィルター

ワークスペースのそれぞれのセクションにフィルタが存在する場合は、各セクションを個別にフィルタ処理できます。 次の図では、フィルター (テキスト「フィルター」を含むフィールド) は自由書式のテキスト フィールドのフィルターの例です。

[![ワークスペース セクション フィルター](./media/workspace-section-filters.png)](./media/workspace-section-filters.png)

ワークスペース全体のフィルターと同じように、希望のフィルター値を選択または入力して、セクションのコンテンツを絞り込みます。
