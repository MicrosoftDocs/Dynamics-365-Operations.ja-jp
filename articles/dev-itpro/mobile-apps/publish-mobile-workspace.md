---
title: "モバイル ワークスペースの公開"
description: "このトピックでは、システム管理者がモバイル ワークスペースを公開するために従わなければならない手順について説明します。 モバイル ワークスペースを公開して、ユーザーがモバイル アプリでアクセスできるようにする必要があります。"
author: sericks007
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysAppDesignerPane
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272873
ms.assetid: e9a3028b-3559-4314-afcc-ea0319cdd154
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 203741653d1be8da39787c9403f2b0d3fe079b25
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="publish-a-mobile-workspace"></a>モバイル ワークスペースの公開

[!include [banner](../includes/banner.md)]

このトピックでは、システム管理者がモバイル ワークスペースを公開するために従わなければならない手順について説明します。 モバイル ワークスペースを公開して、ユーザーが Dynamics 365 for Unified Operations のモバイル アプリでアクセスできるようにする必要があります。 

> [!NOTE]
> 以前のモバイル アプリの名前は、*Microsoft Dynamics 365 for Finance and Operations* でした。

## <a name="publish-a-mobile-workspace-by-using-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations のデータを使用してモバイル ワークスペースを公開

1. ブラウザーで、Microsoft Dynamics 365 for Finance and Operations を開始します。
2. **設定** > **モバイル アプリ**とクリックします。
3. 公開するモバイル ワークスペースを選択します。
4. **発行** をクリックします。

新しいワークスペースが発行された後、ユーザーはプルしてモバイル ワークスペースの一覧を更新する必要があります。 

[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="publish-a-mobile-workspace-by-using-microsoft-dynamics-365-for-operations-version-1611"></a>Microsoft Dynamics 365 for Operations バージョン 1611 を使用してモバイル ワークスペースを公開

### <a name="prerequisites"></a>前提条件

Microsoft Dynamics 365 for Operations バージョン 1611 に提供されているモバイル ワークスペースでは、KB (ホットフィックス) を実装する必要があります。 必要な KB の実装方法の詳細については、次のトピックを参照してください。

- [コスト管理モバイル ワークスペース](../../financials/cost-accounting/cost-controlling-mobile-workspace.md)
- [手持在庫モバイル ワークスペース](../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md)
- [販売注文モバイル ワークスペース](../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md)
- [仕入先コラボレーションのモバイル ワークスペース](../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md)
- [発注書承認モバイル ワークスペース](../../supply-chain/procurement/purchase-order-mobile-workspace.md)
- [プロジェクト時間入力モバイル ワークスペース](../../financials/project-management/project-time-entry-mobile-workspace.md)
- [経費管理モバイル ワークスペース](../../financials/expense-management/expense-management-mobile-workspace.md)

### <a name="publish-a-mobile-workspace"></a>モバイル ワークスペースの公開
1.  ブラウザーで、Microsoft Dynamics 365 for Finance and Operations を開始します。
2.  **システム パラメーター**ページの、**モバイル ワークスペースの管理**タブで、公開するワークスペースを選択します。
3.  **モバイル ワークスペースの公開**をクリックします。

新しいワークスペースが発行された後、ユーザーはプルしてモバイル ワークスペースの一覧を更新する必要があります。 

[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

