---
title: 作業指示書と固定資産
description: このトピックでは、資産管理における固定資産と作業指示書について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250832"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="ff60b-103">作業指示書と固定資産</span><span class="sxs-lookup"><span data-stu-id="ff60b-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="ff60b-104">資産管理では、資産を固定資産に関連付けることができます。またこれらの資産の作業指示書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="ff60b-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="ff60b-105">この機能を使用する場合、**プロジェクト管理および会計**モジュールと**固定資産**モジュールで、固定資産、関連する投資プロジェクトおよび投資プロジェクトに登録されている原価の概要を完全に取得できます。</span><span class="sxs-lookup"><span data-stu-id="ff60b-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="ff60b-106">**固定資産番号**フィールドは、作業指示書ジョブ プロジェクトでプロジェクト タイプとして "投資" タイプが選択されている場合にのみ、作業指示書ジョブ プロジェクトに入力されます。</span><span class="sxs-lookup"><span data-stu-id="ff60b-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![図 1](media/24-work-orders.png)

<span data-ttu-id="ff60b-108">次の手順では、資産、作業指示書、作業指示書プロジェクト、および固定資産関連について説明します。</span><span class="sxs-lookup"><span data-stu-id="ff60b-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="ff60b-109">下の図が示すように、固定資産に関連付ける資産を作成します。</span><span class="sxs-lookup"><span data-stu-id="ff60b-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![図 2](media/25-work-orders.png)

2. <span data-ttu-id="ff60b-111">作業指示書タイプ (**資産管理** > **設定** > **作業指示書** > **作業指示書タイプ**) を設定する場合は、投資を処理するための作業指示書タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="ff60b-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="ff60b-112">[作業指示書タイプ](../setup-for-work-orders/work-order-types.md) も参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff60b-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![図 3](media/26-work-orders.png)

3. <span data-ttu-id="ff60b-114">作業指示書プロジェクト グループ (**資産管理** > **設定** > **作業指示書** > **プロジェクト設定** > **プロジェクト グループ** リンク) を設定する場合は、投資のために使用される作業指示書と**プロジェクト管理および会計**モジュール (**プロジェクト管理および会計** > **設定** > **転記** > **プロジェクト グループ**)で投資のために作成されたプロジェクト グループの関係を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ff60b-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![図 4](media/27-work-orders.png)

4. <span data-ttu-id="ff60b-116">固定資産オブジェクトに関連する作業指示書を作成する場合は、投資の処理に使用する "投資" などの作業指示書タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff60b-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="ff60b-117">作業指示書が作成されると、関連する作業指示書タイプが**すべての作業指示書**で表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff60b-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![図 5](media/28-work-orders.png)

6. <span data-ttu-id="ff60b-119">作業指示書が作成されると、その作業指示書に関連付けられているプロジェクトが**プロジェクト管理および会計** > **すべてのプロジェクト**に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ff60b-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="ff60b-120">作業指示書で**プロジェクト ID** リンクをクリックすると、プロジェクト関連の情報を確認できます (**資産管理**の作業指示書の詳細ビュー > **明細行の詳細**クイックタブ > **一般** タブ > **プロジェクト ID** フィールド)。</span><span class="sxs-lookup"><span data-stu-id="ff60b-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![図 6](media/29-work-orders.png)

7. <span data-ttu-id="ff60b-122">**固定資産**では、固定資産に関連付けられているプロジェクトの概要を閲覧できます (**固定資産** > **固定資産** > **固定資産** > **固定資産番号**フィールドの固定資産をクリック > **関連情報**ウィンドウでコンテンツを表示 > **関連付けられたプロジェクト** セクション)。</span><span class="sxs-lookup"><span data-stu-id="ff60b-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

