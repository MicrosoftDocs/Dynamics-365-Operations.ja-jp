---
title: 組織階層の設定
description: このトピックでは、Microsoft Dynamics 365 Commerce での組織階層の設定方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800570"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="e65ed-103">組織階層の設定</span><span class="sxs-lookup"><span data-stu-id="e65ed-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e65ed-104">このトピックでは、Microsoft Dynamics 365 Commerce での組織階層の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e65ed-105">チャネルを作成する前に、組織階層が設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e65ed-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="e65ed-106">業務について、さまざまな観点から表示と報告を行う組織階層を使用できます。</span><span class="sxs-lookup"><span data-stu-id="e65ed-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="e65ed-107">たとえば、税金、法律、または法令についての報告に使用する 1 つの階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e65ed-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="e65ed-108">法的に必須でなくても、内部報告に使用する財務情報を報告する別の階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e65ed-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="e65ed-109">組織階層を作成する前に、組織を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e65ed-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="e65ed-110">詳細については、[法人の作成](channels-legal-entities.md) または [作業単位の作成](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e65ed-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="e65ed-111">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e65ed-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="e65ed-112">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="e65ed-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e65ed-113">組織階層の計画</span><span class="sxs-lookup"><span data-stu-id="e65ed-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e65ed-114">組織階層の作成</span><span class="sxs-lookup"><span data-stu-id="e65ed-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="e65ed-115">組織階層の作成</span><span class="sxs-lookup"><span data-stu-id="e65ed-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="e65ed-116">組織階層を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e65ed-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e65ed-117">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 組織階層** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="e65ed-118">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e65ed-119">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="e65ed-120">**目的** セクションで、**目的の割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="e65ed-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="e65ed-122">組織階層に割り当てる目的を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="e65ed-123">**割り当て済の階層** セクションで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="e65ed-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="e65ed-124">In the list, mark the selected row.</span></span> <span data-ttu-id="e65ed-125">作成した階層を検索します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="e65ed-126">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-126">Select **OK**.</span></span>

<span data-ttu-id="e65ed-127">次の図は、架空の「Adventure Works」店舗のセットのために作成された組織階層の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e65ed-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![組織階層の例](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="e65ed-129">階層への組織の追加</span><span class="sxs-lookup"><span data-stu-id="e65ed-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="e65ed-130">階層に組織を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e65ed-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e65ed-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="e65ed-132">階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="e65ed-133">アクション ウィンドウで、**表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="e65ed-134">必要に応じて組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="e65ed-135">組織を追加するには、**編集** を選択して、**挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e65ed-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="e65ed-136">変更が完了したら、ドラフトを保存して変更を公開できます。</span><span class="sxs-lookup"><span data-stu-id="e65ed-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="e65ed-137">次の図は、「モール」、「アウトレット」、「オンライン」、および「コール センター」チャネルの 4 つの原価部門が追加された階層ルートに追加された法人を示しています。</span><span class="sxs-lookup"><span data-stu-id="e65ed-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="e65ed-138">その後、さまざまな小売、コール センター、およびオンライン チャネルをそれぞれに追加できます。</span><span class="sxs-lookup"><span data-stu-id="e65ed-138">Various retail, call center and online channels can then be added to each.</span></span>

![階層デザイナーの例](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="e65ed-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e65ed-140">Additional resources</span></span>

[<span data-ttu-id="e65ed-141">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="e65ed-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e65ed-142">組織階層の計画</span><span class="sxs-lookup"><span data-stu-id="e65ed-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e65ed-143">法人の作成</span><span class="sxs-lookup"><span data-stu-id="e65ed-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="e65ed-144">作業単位の作成</span><span class="sxs-lookup"><span data-stu-id="e65ed-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e65ed-145">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="e65ed-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e65ed-146">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="e65ed-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
