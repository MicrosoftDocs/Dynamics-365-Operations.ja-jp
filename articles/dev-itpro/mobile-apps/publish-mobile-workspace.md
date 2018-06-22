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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c3bf003d945cbe54d45e5ace122e9d142d6c763
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="publish-a-mobile-workspace"></a><span data-ttu-id="69a2f-104">モバイル ワークスペースの公開</span><span class="sxs-lookup"><span data-stu-id="69a2f-104">Publish a mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69a2f-105">このトピックでは、システム管理者がモバイル ワークスペースを公開するために従わなければならない手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="69a2f-105">This topic describes the steps that system administrators must follow to publish a mobile workspace.</span></span> <span data-ttu-id="69a2f-106">モバイル ワークスペースを公開して、ユーザーが Dynamics 365 for Unified Operations のモバイル アプリでアクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="69a2f-106">A mobile workspace must be published so that users can access it in the Dynamics 365 for Unified Operations mobile app.</span></span> 

> [!NOTE]
> <span data-ttu-id="69a2f-107">以前のモバイル アプリの名前は、*Microsoft Dynamics 365 for Finance and Operations* でした。</span><span class="sxs-lookup"><span data-stu-id="69a2f-107">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

## <a name="publish-a-mobile-workspace-by-using-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="69a2f-108">Microsoft Dynamics 365 for Finance and Operations のデータを使用してモバイル ワークスペースを公開</span><span class="sxs-lookup"><span data-stu-id="69a2f-108">Publish a mobile workspace by using Microsoft Dynamics 365 for Finance and Operations</span></span>

1. <span data-ttu-id="69a2f-109">ブラウザーで、Microsoft Dynamics 365 for Finance and Operations を開始します。</span><span class="sxs-lookup"><span data-stu-id="69a2f-109">In your browser, start Microsoft Dynamics 365 for Finance and Operations.</span></span>
2. <span data-ttu-id="69a2f-110">**設定** > **モバイル アプリ**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="69a2f-110">Click **Settings** > **Mobile app**.</span></span>
3. <span data-ttu-id="69a2f-111">公開するモバイル ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="69a2f-111">Select the mobile workspace to publish.</span></span>
4. <span data-ttu-id="69a2f-112">**発行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69a2f-112">Click **Publish**.</span></span>

<span data-ttu-id="69a2f-113">新しいワークスペースが発行された後、ユーザーはプルしてモバイル ワークスペースの一覧を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69a2f-113">After a new workspace is published, users must pull to refresh the list of mobile workspaces.</span></span> 

<span data-ttu-id="69a2f-114">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="69a2f-114">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="publish-a-mobile-workspace-by-using-microsoft-dynamics-365-for-operations-version-1611"></a><span data-ttu-id="69a2f-115">Microsoft Dynamics 365 for Operations バージョン 1611 を使用してモバイル ワークスペースを公開</span><span class="sxs-lookup"><span data-stu-id="69a2f-115">Publish a mobile workspace by using Microsoft Dynamics 365 for Operations version 1611</span></span>

### <a name="prerequisites"></a><span data-ttu-id="69a2f-116">前提条件</span><span class="sxs-lookup"><span data-stu-id="69a2f-116">Prerequisites</span></span>

<span data-ttu-id="69a2f-117">Microsoft Dynamics 365 for Operations バージョン 1611 に提供されているモバイル ワークスペースでは、KB (ホットフィックス) を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69a2f-117">The mobile workspaces that are provided for Microsoft Dynamics 365 for Operations version 1611 require that KBs (hotfixes) be implemented.</span></span> <span data-ttu-id="69a2f-118">必要な KB の実装方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="69a2f-118">For more information about how to implement the required KBs, see the following topics:</span></span>

- [<span data-ttu-id="69a2f-119">コスト管理モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-119">Cost controlling mobile workspace</span></span>](../../financials/cost-accounting/cost-controlling-mobile-workspace.md)
- [<span data-ttu-id="69a2f-120">手持在庫モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-120">Inventory on-hand mobile workspace</span></span>](../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md)
- [<span data-ttu-id="69a2f-121">販売注文モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-121">Sales orders mobile workspace</span></span>](../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md)
- [<span data-ttu-id="69a2f-122">仕入先コラボレーションのモバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-122">Vendor collaboration mobile workspace</span></span>](../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md)
- [<span data-ttu-id="69a2f-123">発注書承認モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-123">Purchase order approval mobile workspace</span></span>](../../supply-chain/procurement/purchase-order-mobile-workspace.md)
- [<span data-ttu-id="69a2f-124">プロジェクト時間入力モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-124">Project time entry mobile workspace</span></span>](../../financials/project-management/project-time-entry-mobile-workspace.md)
- [<span data-ttu-id="69a2f-125">経費管理モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="69a2f-125">Expense management mobile workspace</span></span>](../../financials/expense-management/expense-management-mobile-workspace.md)

### <a name="publish-a-mobile-workspace"></a><span data-ttu-id="69a2f-126">モバイル ワークスペースの公開</span><span class="sxs-lookup"><span data-stu-id="69a2f-126">Publish a mobile workspace</span></span>
1.  <span data-ttu-id="69a2f-127">ブラウザーで、Microsoft Dynamics 365 for Finance and Operations を開始します。</span><span class="sxs-lookup"><span data-stu-id="69a2f-127">In your browser, start Microsoft Dynamics 365 for Finance and Operations.</span></span>
2.  <span data-ttu-id="69a2f-128">**システム パラメーター**ページの、**モバイル ワークスペースの管理**タブで、公開するワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="69a2f-128">On the **System parameters** page, on the **Manage mobile workspaces** tab, select the workspace to publish.</span></span>
3.  <span data-ttu-id="69a2f-129">**モバイル ワークスペースの公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="69a2f-129">Click **Publish mobile workspace**.</span></span>

<span data-ttu-id="69a2f-130">新しいワークスペースが発行された後、ユーザーはプルしてモバイル ワークスペースの一覧を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="69a2f-130">After a new workspace is published, users must pull to refresh the list of mobile workspaces.</span></span> 

<span data-ttu-id="69a2f-131">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="69a2f-131">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>
