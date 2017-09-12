--- 
title: "売上税の割り当ておよび上書き"
description: "この手順では、小売チャンネルに売上税グループを割り当てる方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b3f13738044c81d32098072f26f204a4acb2d08d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="6cb5b-103">売上税の割り当ておよび上書き</span><span class="sxs-lookup"><span data-stu-id="6cb5b-103">Sales tax assignment and overrides</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cb5b-104">この手順では、小売チャンネルに売上税グループを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="6cb5b-105">また、新しい売上税の上書きを作成して、既存の売上税の上書きグループに割り当てる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="6cb5b-106">この手順では</span><span class="sxs-lookup"><span data-stu-id="6cb5b-106">This procedure</span></span>

<span data-ttu-id="6cb5b-107">デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6cb5b-108">[小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="6cb5b-109">リストで、[小売チャンネル ID] リンクの「ヒューストン」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="6cb5b-110">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-110">Click Edit.</span></span>
    * <span data-ttu-id="6cb5b-111">[売上税グループ] フィールドには、現在の会社における売上税グループのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="6cb5b-112">現在割り当てられているグループは、「テキサス州」の一般的な売上税グループです。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="6cb5b-113">また、「ワシントン州」と「ワシントン州キング郡」の売上税グループもあります。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="6cb5b-114">売上税グループに複数の自治体に該当する税を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="6cb5b-115">[売上税の上書き] フィールドによって、売上税の上書きグループをチャンネルにマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="6cb5b-116">売上税の上書きグループを使用して、複数の店舗で有効な売上税の上書きをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="6cb5b-117">売上税の上書きを一つずつ手動で割り当てるのではなく、グループを作成し、チャンネルに直接割り当てることで時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="6cb5b-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-118">Click Save.</span></span>
5. <span data-ttu-id="6cb5b-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-119">Close the page.</span></span>
6. <span data-ttu-id="6cb5b-120">[小売りとコマース] > [チャンネル設定] > [売上税] > [売上税の上書き] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="6cb5b-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-121">Click New.</span></span>
8. <span data-ttu-id="6cb5b-122">[売上税の上書き] フィールドで、新しい上書きの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="6cb5b-123">[説明] フィールドに、上書きの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="6cb5b-124">ステータスを「有効化」に設定します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="6cb5b-125">[上書き] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="6cb5b-126">[タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="6cb5b-127">品目売上税グループは、グループに属する特定の品目に対して税を上書きするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="6cb5b-128">たとえば、食品は一般的に耐久財と異なる税金が課され、独自の売上税グループがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="6cb5b-129">売上税グループは、特定のチャンネルに該当する税グループです。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="6cb5b-130">たとえば、チャンネルで小売販売と企業間の両方で販売する場合、異なる品目売上税グループを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="6cb5b-131">すべての該当する税は、売上税グループにマップされます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="6cb5b-132">ここでは、「上書き元税」と「上書き先税」、または「上書き元税グループ」と「上書き先税グループ」を選択して売上税の上書きを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="6cb5b-133">[ソース] フィールドは上書きする税または税グループを示します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="6cb5b-134">品目売上税グループによる上書きは、売上税グループによる上書きとは異なるオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="6cb5b-135">売上税の上書きは、すべてのトランザクションまたはトランザクションの特定明細行の税を上書きするように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="6cb5b-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-136">Click Save.</span></span>
14. <span data-ttu-id="6cb5b-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-137">Close the page.</span></span>
15. <span data-ttu-id="6cb5b-138">[小売りとコマース] > [チャンネル設定] > [売上税] > [売上税の上書きグループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="6cb5b-139">この手順では、ヒューストン チャンネルに割り当てられた売上税の上書きグループに、新しく作成された売上税の上書きを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="6cb5b-140">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-140">Click Edit.</span></span>
17. <span data-ttu-id="6cb5b-141">[設定] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="6cb5b-142">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-142">Click Add.</span></span>
19. <span data-ttu-id="6cb5b-143">[売上税の上書き] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6cb5b-144">リストから以前に作成した売上税の上書きを選択します。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="6cb5b-145">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="6cb5b-146">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6cb5b-146">Click Save.</span></span>


