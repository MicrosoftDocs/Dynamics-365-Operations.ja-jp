---
title: 作業指示書と固定資産
description: このトピックでは、資産管理における固定資産と作業指示書について説明します。
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 678bfae5d0b4ea469a91fc89306be40c39cb082d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223437"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="a2cba-103">作業指示書と固定資産</span><span class="sxs-lookup"><span data-stu-id="a2cba-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="a2cba-104">資産管理では、資産を固定資産に関連付けることができます。またこれらの資産の作業指示書を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2cba-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="a2cba-105">この機能を使用する場合、**プロジェクト管理および会計** モジュールと Microsoft Dynamics 365 for Finance and Operations の **固定資産** モジュールで、固定資産、関連する投資プロジェクトおよび投資プロジェクトに登録されている原価の概要を完全に取得できます。</span><span class="sxs-lookup"><span data-stu-id="a2cba-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="a2cba-106">**固定資産番号** フィールドは、作業指示書ジョブ プロジェクトでプロジェクト タイプとして **投資** が選択されている場合にのみ、作業指示書ジョブ プロジェクトに設定されます。</span><span class="sxs-lookup"><span data-stu-id="a2cba-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="a2cba-107">次の図は、**プロジェクト管理および会計** モジュールの投資プロジェクトと作業指示書ジョブ プロジェクトの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="a2cba-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![図 1](media/24-work-orders.png)

<span data-ttu-id="a2cba-109">次の手順では、資産、作業指示書、作業指示書プロジェクト、および固定資産関連について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="a2cba-110">固定資産に関連付ける資産を作成します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-110">You create an asset that you relate to a fixed asset.</span></span>

![図 2](media/25-work-orders.png)

2. <span data-ttu-id="a2cba-112">**作業指示書タイプ** ページ (**資産管理** > **設定** > **作業指示書** > **作業指示書タイプ**) で、作業指示書タイプを設定する場合は、投資を処理するための作業指示書タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="a2cba-113">[作業指示書タイプ](../setup-for-work-orders/work-order-types.md) も参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2cba-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![図 3](media/26-work-orders.png)

3. <span data-ttu-id="a2cba-115">**作業指示書プロジェクトの設定** ページ (**資産管理** > **設定** > **作業指示書** > **プロジェクト設定**) の **プロジェクト グループ** タブで作業指示書プロジェクト グループを設定する場合は、投資のために使用される作業指示書と **プロジェクト管理および会計** モジュールの **プロジェクト グループ** ページ (**プロジェクト管理および会計** > **設定** > **転記** > **プロジェクト グループ**) で投資のために作成されたプロジェクト グループの関係を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="a2cba-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![図 4](media/27-work-orders.png)

4. <span data-ttu-id="a2cba-117">固定資産に関連する作業指示書を作成する場合は、投資の処理に使用する **投資** などの作業指示書タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="a2cba-118">作業指示書が作成されると、関連する作業指示書タイプが **すべての作業指示書** ページで表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2cba-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![図 5](media/28-work-orders.png)

6. <span data-ttu-id="a2cba-120">作業指示書が作成されると、作業指示書に関連付けられたプロジェクトが、**プロジェクト管理および会計** モジュールの **すべてのプロジェクト** ページ (**プロジェクト管理および会計** > **プロジェクト** > **すべてのプロジェクト**) に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a2cba-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="a2cba-121">プロジェクトの関連情報を表示するには、**資産管理** モジュールの **すべての作業指示書** ページ (**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**) の詳細ビューの、**行の詳細** クイック タブの **一般** タブで、**プロジェクト ID** フィールドのリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![図 6](media/29-work-orders.png)

7. <span data-ttu-id="a2cba-123">固定資産に関連付けられているプロジェクトの概要を表示するには、**固定資産** > **固定資産** > **固定資産** を選択して、**固定資産番号** フィールドで、詳細ビューを開く固定資産のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="a2cba-124">ページの右側にある **関連情報** ウィンドウを展開し、**関連付けられたプロジェクト** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2cba-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]