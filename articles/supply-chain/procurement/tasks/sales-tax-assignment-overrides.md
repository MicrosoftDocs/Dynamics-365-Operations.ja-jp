---
title: 売上税の割り当ておよび上書き
description: この手順では、コマース チャネルに売上税グループを割り当てる方法を示します。
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40723d35c1914f6cec6aa361a6c38100d1667cb6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003630"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="d3dba-103">消費税の割り当ておよび上書き</span><span class="sxs-lookup"><span data-stu-id="d3dba-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3dba-104">この手順では、コマース チャネルに売上税グループを割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="d3dba-105">また、新しい売上税の上書きを作成して、既存の売上税の上書きグループに割り当てる処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="d3dba-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d3dba-107">Retail および Commerce > チャネル > 店舗 > すべての店舗の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="d3dba-108">リストで、チャンネル ID リンクの "ヒューストン" をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="d3dba-109">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-109">Click Edit.</span></span>
    * <span data-ttu-id="d3dba-110">[売上税グループ] フィールドには、現在の会社における売上税グループのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3dba-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="d3dba-111">現在割り当てられているグループは、「テキサス州」の一般的な売上税グループです。</span><span class="sxs-lookup"><span data-stu-id="d3dba-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="d3dba-112">また、「ワシントン州」と「ワシントン州キング郡」の売上税グループもあります。</span><span class="sxs-lookup"><span data-stu-id="d3dba-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="d3dba-113">売上税グループに複数の自治体に該当する税を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="d3dba-114">[売上税の上書き] フィールドによって、売上税の上書きグループをチャンネルにマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="d3dba-115">売上税の上書きグループを使用して、複数の店舗で有効な売上税の上書きをグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="d3dba-116">売上税の上書きを一つずつ手動で割り当てるのではなく、グループを作成し、チャンネルに直接割り当てることで時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="d3dba-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-117">Click Save.</span></span>
5. <span data-ttu-id="d3dba-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-118">Close the page.</span></span>
6. <span data-ttu-id="d3dba-119">Retail とコマース > チャンネル設定 > 売上税 > 売上税の上書きの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="d3dba-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-120">Click New.</span></span>
8. <span data-ttu-id="d3dba-121">[売上税の上書き] フィールドで、新しい上書きの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="d3dba-122">[説明] フィールドに、上書きの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="d3dba-123">ステータスを「有効化」に設定します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="d3dba-124">[上書き] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="d3dba-125">[タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="d3dba-126">品目売上税グループは、グループに属する特定の品目に対して税を上書きするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="d3dba-127">たとえば、食品は一般的に耐久財と異なる税金が課され、独自の売上税グループがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3dba-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="d3dba-128">売上税グループは、特定のチャンネルに該当する税グループです。</span><span class="sxs-lookup"><span data-stu-id="d3dba-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="d3dba-129">たとえば、チャンネルで小売販売と企業間の両方で販売する場合、異なる品目売上税グループを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3dba-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="d3dba-130">すべての該当する税は、売上税グループにマップされます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="d3dba-131">ここでは、「上書き元税」と「上書き先税」、または「上書き元税グループ」と「上書き先税グループ」を選択して売上税の上書きを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="d3dba-132">[ソース] フィールドは上書きする税または税グループを示します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="d3dba-133">品目売上税グループによる上書きは、売上税グループによる上書きとは異なるオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="d3dba-134">売上税の上書きは、すべてのトランザクションまたはトランザクションの特定明細行の税を上書きするように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="d3dba-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-135">Click Save.</span></span>
14. <span data-ttu-id="d3dba-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-136">Close the page.</span></span>
15. <span data-ttu-id="d3dba-137">Retail とコマース > チャネル設定 > 売上税 > 売上税の上書きグループの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="d3dba-138">この手順では、ヒューストン チャンネルに割り当てられた売上税の上書きグループに、新しく作成された売上税の上書きを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="d3dba-139">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-139">Click Edit.</span></span>
17. <span data-ttu-id="d3dba-140">[設定] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="d3dba-141">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-141">Click Add.</span></span>
19. <span data-ttu-id="d3dba-142">[売上税の上書き] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d3dba-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="d3dba-143">リストから以前に作成した売上税の上書きを選択します。</span><span class="sxs-lookup"><span data-stu-id="d3dba-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="d3dba-144">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="d3dba-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3dba-145">Click Save.</span></span>

