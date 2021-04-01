---
title: 実験のプレビューと発行
description: このトピックでは、Dynamics 365 Commerce から実験をプレビューおよび公開する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 7b35af35f5d0347192ed94bed51dfd2484cfa481
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238585"
---
# <a name="preview-and-publish-an-experiment"></a><span data-ttu-id="903f3-103">実験のプレビューと発行</span><span class="sxs-lookup"><span data-stu-id="903f3-103">Preview and publish an experiment</span></span>

<span data-ttu-id="903f3-104">このトピックでは、[実験を接続してバリエーションを編集](experimentation-connect-edit.md) した後、Dynamics 365 Commerce で実験をプレビューして公開する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="903f3-104">This topic describes how to preview and publish your experiment in Dynamics 365 Commerce after you've [connected your experiment and edited your variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="903f3-105">次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="903f3-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="903f3-106">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="903f3-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="903f3-107">[ ![実験ユーザー体験 - プレビューと公開](./media/experimentation_preview_publish.svg)](./media/experimentation_preview_publish.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="903f3-107">[ ![Experimentation user journey - Preview & Publish](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)</span></span>

## <a name="preview-your-experiment-variations"></a><span data-ttu-id="903f3-108">実験のバリエーションをプレビューする</span><span class="sxs-lookup"><span data-stu-id="903f3-108">Preview your experiment variations</span></span>
<span data-ttu-id="903f3-109">バリエーションをプレビューして、希望どおりに表示されるまで編集を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="903f3-109">You can preview your variations and continue editing them until they look the way you want them to.</span></span>

<span data-ttu-id="903f3-110">Commerce サイト ビルダーでの実験のバリエーションを確認するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="903f3-110">To preview your experiment variations in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="903f3-111">コマンド バーの下にあるバリエーションのドロップダウン メニューを使用して、プレビューするコンテンツを選択します。</span><span class="sxs-lookup"><span data-stu-id="903f3-111">From the variations drop-down menu below the command bar, select the content you want to preview.</span></span> 
1. <span data-ttu-id="903f3-112">コマンド バーで、**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="903f3-112">On the command bar, select **Preview**.</span></span> <span data-ttu-id="903f3-113">公開されたときのコンテンツがどのように表示されるかのプレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="903f3-113">A preview of what the content will look like when it's published is displayed.</span></span>
1. <span data-ttu-id="903f3-114">異なるバリエーションをプレビューするには、バリエーション ドロップダウン メニューからそのバリエーションを選択し、**プレビュー** をもう一度選択します。</span><span class="sxs-lookup"><span data-stu-id="903f3-114">To preview a different variation, select it from the variation drop-down menu and select **Preview** again.</span></span>

## <a name="publish-your-experiment"></a><span data-ttu-id="903f3-115">実験の公開</span><span class="sxs-lookup"><span data-stu-id="903f3-115">Publish your experiment</span></span>
<span data-ttu-id="903f3-116">公開グループを使用して実験の公開時期をスケジュールしておらず、すぐに公開する場合は、コマンド バーの **公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="903f3-116">If you aren't using a publish group to schedule when your experiment goes live and you want to publish immediately, select **Publish** in the command bar.</span></span> <span data-ttu-id="903f3-117">実験に属するすべてのバリエーションが公開されます。</span><span class="sxs-lookup"><span data-stu-id="903f3-117">All variations that belong to the experiment will be published.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="903f3-118">ページに未発行の URL がある場合は、最初に URL を公開する必要があります。そうしないと、Web サイトのユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="903f3-118">If the page has an unpublished URL, you must first publish the URL or it won't be visible to your website users.</span></span> <span data-ttu-id="903f3-119">詳細については、[ページの保存、プレビュー、および公開](save-preview-publish-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="903f3-119">For details, see [Save, preview, and publish a page](save-preview-publish-page.md).</span></span>
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a><span data-ttu-id="903f3-120">公開グループを使用して、実験がいつ公開されるかをスケジュールする</span><span class="sxs-lookup"><span data-stu-id="903f3-120">Use publish groups to schedule when your experiment goes live</span></span>
<span data-ttu-id="903f3-121">サイト ビルダーで作成したバリエーションは、発行グループを使用して、公開をスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="903f3-121">Variations created in site builder can be scheduled for publishing by using a publish group.</span></span> <span data-ttu-id="903f3-122">発行グループ内では、左側のナビゲーション ペインで **実験** を選択することにより、ページまたはフラグメントを試験に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="903f3-122">Within a publish group, you can connect a page or fragment to your experiment by selecting **Experiments** in the left navigation pane.</span></span> <span data-ttu-id="903f3-123">また、この処理は **ページ** や **フラグメント** を選択して、[実験を接続してバリエーションを編集する](experimentation-connect-edit.md)に記載の指示に従うことでも実施できます。</span><span class="sxs-lookup"><span data-stu-id="903f3-123">You can also do this by selecting **Pages** or **Fragments** and following the instructions in [Connect an experiment and edit variations](experimentation-connect-edit.md).</span></span> <span data-ttu-id="903f3-124">公開グループの詳細については、[公開グループの使用](publish-groups.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="903f3-124">For information about publish groups, see [Work with publish groups](publish-groups.md).</span></span>

<span data-ttu-id="903f3-125">実験で公開グループを使用する場合は、注意すべき重要な考慮事項がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="903f3-125">When using publish groups with experiments, there are some important considerations to be aware of.</span></span>
- <span data-ttu-id="903f3-126">実験が実行されているページまたはフラグメントを公開グループに追加すると、その実験は公開グループのページまたはフラグメントから実験が削除されます。</span><span class="sxs-lookup"><span data-stu-id="903f3-126">When you add a page or fragment that has an experiment running on it to a publish group, the experiment will be removed from the page or fragment in the publish group.</span></span>
- <span data-ttu-id="903f3-127">実際のサイトのページに関連付けられている実験は、公開グループ内のページでは使用できません。またその逆も同様です。</span><span class="sxs-lookup"><span data-stu-id="903f3-127">Experiments that are connected to pages in a live site aren't available to pages within publish groups and vice-versa.</span></span> <span data-ttu-id="903f3-128">同様に、実際のサイトでの実験が実行されているページは、公開グループの他の実験では使用できません。またその逆も同様です。</span><span class="sxs-lookup"><span data-stu-id="903f3-128">Similarly, pages that have experiments running on them in a live site aren't available to other experiments in publish groups and vice versa.</span></span>
- <span data-ttu-id="903f3-129">公開グループを公開またはスケジュールすると、公開グループに関連付けられている実験があるかどうかにかかわらず、公開グループのすべてのコンテンツが公開されます。</span><span class="sxs-lookup"><span data-stu-id="903f3-129">When you publish or schedule a publish group, all content in the publish group is published, regardless of whether there's an experiment associated with the publish group.</span></span>
- <span data-ttu-id="903f3-130">公開グループは、実際のサイトに公開された後も引き続き存続されるため、公開グループの実験も存続します。</span><span class="sxs-lookup"><span data-stu-id="903f3-130">Because a publish group continues to persist after it's been published to a live site, experiments in the publish group will also persist.</span></span> <span data-ttu-id="903f3-131">したがって、他の実験を同じページまたはフラグメントに関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="903f3-131">Therefore, you won't be able to associate other experiments with the same page or fragment.</span></span> <span data-ttu-id="903f3-132">この制限を回避するには、実験が存続している公開グループを削除します。</span><span class="sxs-lookup"><span data-stu-id="903f3-132">To avoid this limitation, delete any publish groups with persisting experiments.</span></span> <span data-ttu-id="903f3-133">同様に、公開グループにも存在する実際のサイトの実験を削除する場合は、最初に公開グループから実験を削除します。</span><span class="sxs-lookup"><span data-stu-id="903f3-133">Similarly, if you want to delete an experiment in a live site that also exists in a publish group, delete it from the publish group first.</span></span>

## <a name="previous-step"></a><span data-ttu-id="903f3-134">前のステップ</span><span class="sxs-lookup"><span data-stu-id="903f3-134">Previous step</span></span>
[<span data-ttu-id="903f3-135">実験を接続して編集する</span><span class="sxs-lookup"><span data-stu-id="903f3-135">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)

## <a name="next-step"></a><span data-ttu-id="903f3-136">次のステップ</span><span class="sxs-lookup"><span data-stu-id="903f3-136">Next step</span></span>
[<span data-ttu-id="903f3-137">実験の実行と監視</span><span class="sxs-lookup"><span data-stu-id="903f3-137">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]