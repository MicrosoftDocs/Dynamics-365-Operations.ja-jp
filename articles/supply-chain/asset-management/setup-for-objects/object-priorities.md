---
title: 資産サービス レベル
description: このトピックでは、資産管理の資産サービス レベルについて説明します。
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783412"
---
# <a name="asset-service-levels"></a><span data-ttu-id="bf1ae-103">資産サービス レベル</span><span class="sxs-lookup"><span data-stu-id="bf1ae-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="bf1ae-104">このトピックでは、資産管理の資産サービス レベルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="bf1ae-105">資産サービス レベルは資産に関連し、メンテナンス要求およびワーク オーダーに転送されます。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="bf1ae-106">これらは、ワーク オーダー スケジューリング中にワーク オーダーの優先順位を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="bf1ae-107">変更が必要な場合、資産サービス レベルを変更できます。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="bf1ae-108">ワーク オーダー スケジューリングの評価スコアの計算に関連する設定の詳細については、[資産管理パラメーター](../setup-for-objects/enterprise-asset-management-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="bf1ae-109">資産サービス レベルに対して、少なくとも 1 つの既定レコードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="bf1ae-110">この既定のレコードは、ワーク オーダー スケジューリング中に他の一致が見つからない場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="bf1ae-111">**例 1:** 他の一致が見つからない場合に使用される既定のサービス レベル。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="bf1ae-112">このレコードでは、サービス レベルのみを選択します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="bf1ae-113">**例 2:** ボルボ トラック エンジンのジョブ スケジュールに使用される高サービス レベル。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="bf1ae-114">このレコードでは、関連する資産タイプ (**トラック エンジン**など)、メーカー (**ボルボ**) 、およびサービス レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="bf1ae-115">資産サービス レベルの設定</span><span class="sxs-lookup"><span data-stu-id="bf1ae-115">Set up asset service levels</span></span>

1. <span data-ttu-id="bf1ae-116">**資産管理** \> **設定** \> **資産サービス レベル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="bf1ae-117">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="bf1ae-118">資産サービス レベルに必要な詳細レベルに応じて、**機能場所**、**資産タイプ**、**メーカー**、**モデル**、**資産**、**ワーク オーダー タイプ**、および**サービス レベル** フィールドで関連する選択を行います。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bf1ae-119">資産サービス レベルがメンテナンス要求およびワーク オーダーに使用される場合、資産管理はすべての資産サービス レベル レコードを調べて、一致の可能性をチェックします。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="bf1ae-120">常に最も限定的な組み合わせを最初にチェックします。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="bf1ae-121">つまり、資産管理は、まず**ワーク オーダー タイプ** フィールドの一致をチェックします。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="bf1ae-122">一致するものが見つからない場合は、**資産**フィールドなどの一致がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="bf1ae-123">**資産 サービス レベル**ページのレイアウトで分かるように、この動作は、最も限定的な組み合わせを見つけるために、資産管理が各レコードを右から左に一致をチェックすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="bf1ae-124">一致するものが見つからない場合は、これらのフィールドに選択がない既定のレコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="bf1ae-125">**サービス レベル**フィールドで、サービス レベル (優先順位) を示す番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="bf1ae-126">ワーク オーダーで既に使用した後に**資産サービス レベル**ページで資産 サービス レベル レコードを変更した場合、メンテナンス要求とワーク オーダーにあるサービス レベルは適宜更新されません。</span><span class="sxs-lookup"><span data-stu-id="bf1ae-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
