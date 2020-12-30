---
title: 製品所有者
description: このトピックでは、製品情報の所有者に関する情報を提供します。 製品所有者は、特定の製品を担当するユーザーのグループです。 グループのメンバーだけが、これらの製品をリリースできます。 製品所有者は、承認ワークフローで使用することもできます。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4308020d66995d857e547be47216cb82caacf035
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432412"
---
# <a name="product-owners"></a><span data-ttu-id="b8883-106">製品所有者</span><span class="sxs-lookup"><span data-stu-id="b8883-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8883-107">製品所有者は、特定の製品を担当するユーザーのグループです。</span><span class="sxs-lookup"><span data-stu-id="b8883-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="b8883-108">製品所有者グループが製品に割り当てられている場合は、そのグループのメンバーだけが製品をリリースできます。</span><span class="sxs-lookup"><span data-stu-id="b8883-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="b8883-109">製品所有者は、エンジニアリング変更管理の承認ワークフローで使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b8883-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="b8883-110">製品所有者はグローバル設定です。</span><span class="sxs-lookup"><span data-stu-id="b8883-110">Product owners are global settings.</span></span> <span data-ttu-id="b8883-111">したがって、これらはすべての法人で使用できます。</span><span class="sxs-lookup"><span data-stu-id="b8883-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="b8883-112">製品所有者グループの作成</span><span class="sxs-lookup"><span data-stu-id="b8883-112">Create a product owner group</span></span>

<span data-ttu-id="b8883-113">製品所有者グループを作成し、そのグループにメンバーを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8883-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="b8883-114">**エンジニアリング変更管理 \> 設定 \> 製品所有者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8883-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="b8883-115">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8883-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="b8883-116">**製品所有者** フィールドに、製品グループの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8883-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="b8883-117">**名前** フィールドに、グループの簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="b8883-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="b8883-118">**メンバー** クイック タブで、グループのメンバーにする作業者を追加します。</span><span class="sxs-lookup"><span data-stu-id="b8883-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="b8883-119">製品に製品所有者を割り当てる</span><span class="sxs-lookup"><span data-stu-id="b8883-119">Assign a product owner to a product</span></span>

<span data-ttu-id="b8883-120">製品に製品所有者を割り当てるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8883-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="b8883-121">関連する製品または製品マスターの **製品の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b8883-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="b8883-122">**一般** クイック タブで、**製品の所有者** フィールドを関連する製品所有者グループの名前に設定します。</span><span class="sxs-lookup"><span data-stu-id="b8883-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="b8883-123">製品所有者が製品に割り当てられている間は、製品所有者グループのメンバーのみが **製品所有者の設定** を編集できます。</span><span class="sxs-lookup"><span data-stu-id="b8883-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="b8883-124">製品所有者は、**リリース済製品** ページでも表示できます。</span><span class="sxs-lookup"><span data-stu-id="b8883-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="b8883-125">製品の所有者と製品リリース</span><span class="sxs-lookup"><span data-stu-id="b8883-125">Product owners and product releases</span></span>

<span data-ttu-id="b8883-126">その製品の製品所有者グループのユーザーだけが、その製品をリリースできます。</span><span class="sxs-lookup"><span data-stu-id="b8883-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="b8883-127">ただし、製品が子品目である場合は例外があり、その親は親の所有者によってリリースされます。</span><span class="sxs-lookup"><span data-stu-id="b8883-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="b8883-128">つまり、製品が別の製品の BOM の一部である場合、システムは BOM の各品目の製品所有者を確認しません。</span><span class="sxs-lookup"><span data-stu-id="b8883-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="b8883-129">親品目の製品所有者のみがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="b8883-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="b8883-130">たとえば、製品 X は、*設計キャビネット* 製品所有者グループに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="b8883-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="b8883-131">また、製品 X は製品 Y の一部であり、*デザイン スピーカー* 製品所有者グループに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="b8883-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="b8883-132">*デザイン スピーカー* 製品所有者グループのユーザーが、製品 Y とその BOM をリリースした場合、製品 X は製品 Y と共にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="b8883-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="b8883-133">製品所有者と承認</span><span class="sxs-lookup"><span data-stu-id="b8883-133">Product owners and approvals</span></span>

<span data-ttu-id="b8883-134">製品所有者は、特定の技術上の変更によって製品にメリットが得られるかどうかを把握しているので、多くの場合、エンジニアリング変更管理で承認プロセスの一部としてそれらを含めることは理にかなっています。</span><span class="sxs-lookup"><span data-stu-id="b8883-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="b8883-135">この方法は、エンジニアリング変更管理に使用されるワークフローの参加者プロバイダーとして製品所有者を設定することによって実装できます。</span><span class="sxs-lookup"><span data-stu-id="b8883-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="b8883-136">次に、エンジニアリング変更要求とエンジニアリング変更命令に含まれる製品に基づいて、ワークフローに承認タスクが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b8883-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="b8883-137">詳細については、[エンジニアリング製品に対する変更の管理](engineering-change-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8883-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
