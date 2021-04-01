---
title: 公開グループの作業
description: このトピックでは、Microsoft Dynamics 365 Commerce の公開グループ機能について説明します。
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b623573f598f6b21291cafe95fa04e6777cffe11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244842"
---
# <a name="work-with-publish-groups"></a><span data-ttu-id="34f4f-103">公開グループの作業</span><span class="sxs-lookup"><span data-stu-id="34f4f-103">Work with publish groups</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="34f4f-104">このトピックでは、Microsoft Dynamics 365 Commerce の公開グループ機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-104">This topic describes the publish groups feature in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34f4f-105">概要</span><span class="sxs-lookup"><span data-stu-id="34f4f-105">Overview</span></span>

<span data-ttu-id="34f4f-106">E コマース Web サイトは年間を通して常に新しいコンテンツで更新されています。</span><span class="sxs-lookup"><span data-stu-id="34f4f-106">E-commerce websites are constantly updated with new content throughout the year.</span></span> <span data-ttu-id="34f4f-107">更新は多くの場合、休日、季節的なマーケティング キャンペーン、またはプロモーション開始などの、忙しい E コマース イベントに関連するバッチで公開されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-107">Updates are often published in batches around busy e-commerce events such as holidays, seasonal marketing campaigns, or promotional launches.</span></span> <span data-ttu-id="34f4f-108">これらの更新は多くの場合、Web サイト コンテンツ (例えばページ、画像、フラグメント、テンプレート) のグループを単一のアクションで同時にステージング、検証、および発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-108">These updates often require that groups of website content (for examples, pages, images, fragments, and templates) be staged, validated, and published concurrently in a single action.</span></span>

<span data-ttu-id="34f4f-109">項目を一緒に公開する論理セットに項目をグループ化するこの機能は、各セットには独自のライフサイクルがあり、サイト作成者にとって多くの利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-109">The ability to group items into logical sets that publish items together, where each set has its own lifecycle, provides many advantages to site authors.</span></span> <span data-ttu-id="34f4f-110">コマースでは、これらの論理セットは公開グループと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-110">In Commerce, these logical sets are known as publish groups.</span></span> <span data-ttu-id="34f4f-111">サイト作成者はこれにより、更新のセットを独自のコンフィギュレーション可能、テスト可能、および公開可能なエンティティとして追跡できます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-111">They let site authors track sets of updates as their own configurable, testable, and publishable entities.</span></span>

<span data-ttu-id="34f4f-112">作成者は、実際のサイトまたはその他の自己完結型の公開グループに影響を与えずに、段階的な公開グループ内の更新をプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-112">Authors can preview updates in a staged publish group without affecting the live site or other self-contained publish groups.</span></span> <span data-ttu-id="34f4f-113">その後、作成者は公開アクションをスケジュールして、公開グループ内のすべての項目を実際のサイトに同時に公開することができます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-113">Authors can then schedule the publish action to simultaneously publish all the items in the publish group to the live site.</span></span> <span data-ttu-id="34f4f-114">公開用の更新のグループ化、プレビュー、およびスケジュールする機能は、イベント ベースのサイト更新マイルストーンに関連するかなりの年間収益を生み出す多くのエンタープライズ レベルの会社にとって重要です。</span><span class="sxs-lookup"><span data-stu-id="34f4f-114">The ability to group, preview, and schedule updates for publishing is important for many enterprise-level companies that generate considerable annual revenue around event-based site update milestones.</span></span>

<span data-ttu-id="34f4f-115">会社は、スムーズに実行されない低速または無効化したコンテンツのロールアウトによる費用を負担する場合があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-115">Companies can incur costs from slow or invalidated content rollouts that don't go smoothly.</span></span> <span data-ttu-id="34f4f-116">公開グループは、起動が組織され、検証され、さらに時間どおりに公開されることを保証します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-116">Publish groups help guarantee that launches are organized, validated, and published on time.</span></span> <span data-ttu-id="34f4f-117">大規模であろうと小規模であろうと、公開グループでは、作成者が実行中のサイト更新タスクを組織および簡素化するのに役立つ貴重なツールセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-117">Whether they are large or small, publish groups provide a valuable toolset that helps authors organize and simplify ongoing site update tasks.</span></span>

## <a name="when-to-use-publish-groups"></a><span data-ttu-id="34f4f-118">公開グループを使用する場合</span><span class="sxs-lookup"><span data-stu-id="34f4f-118">When to use publish groups</span></span>

<span data-ttu-id="34f4f-119">複数のドキュメントをまとめて準備し公開する必要がある場合は、公開グループを使用できます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-119">You can use publish groups whenever you must stage and publish multiple documents together.</span></span> <span data-ttu-id="34f4f-120">たとえば、Web サイトが季節ごとにコンテンツを更新する場合、これらの季節的なマーケティング活動用の公開グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-120">For example, if your website updates content every season, you can create publish groups for these seasonal marketing motions.</span></span> <span data-ttu-id="34f4f-121">"秋の更新" 公開グループには、新しい季節の画像、季節的なマーケティング メッセージを含むフラグメント、季節的な製品コレクションを含むページ、またはその他の季節に応じた Web サイト更新が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-121">Your "Autumn Seasonal Update" publish group might contain new seasonal images, fragments that have seasonal marketing messages, pages that include seasonal product collections, or other seasonal website updates.</span></span>

<span data-ttu-id="34f4f-122">公開グループの利点は、複数の更新を同時に準備できるという点です。</span><span class="sxs-lookup"><span data-stu-id="34f4f-122">An advantage of publish groups is that you can stage multiple updates in parallel.</span></span> <span data-ttu-id="34f4f-123">たとえば、"秋の更新" 公開グループの更新後すぐに、特定の週末休暇のコンテンツ更新がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-123">For example, soon after the update for the "Autumn Seasonal Update" publish group, there might be a content update for a specific holiday weekend.</span></span> <span data-ttu-id="34f4f-124">この場合、"秋の更新" 公開グループ用のコンテンツを準備すると同時に、次に続く "秋の休日更新" 公開グループ用のコンテンツを準備できます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-124">In this case, you can stage content for the "Autumn Seasonal Update" publish group at the same time that you stage content for a subsequent "Autumn Holiday Update" publish group.</span></span> <span data-ttu-id="34f4f-125">各公開グループには一意のページ、画像、フラグメント、テンプレートなどのセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-125">Each publish group contains its own unique set of pages, images, fragments, templates, and so on.</span></span> <span data-ttu-id="34f4f-126">これら 2 つの公開グループを個別にしかも同時実行タイムラインで準備、プレビュー、および検証できます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-126">You can stage, preview, and validate these two publish groups independently but on a concurrent timeline.</span></span> <span data-ttu-id="34f4f-127">これにより、各公開グループをサイトで特定の日時に稼動するようにスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-127">Each publish group can then be scheduled to go live on your site at specific dates and times.</span></span>

## <a name="turn-on-the-publish-groups-feature"></a><span data-ttu-id="34f4f-128">公開グループ機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="34f4f-128">Turn on the publish groups feature</span></span>

<span data-ttu-id="34f4f-129">公開グループ機能はオプションであり、サイトに対して有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-129">The publish groups feature is optional and must be turned for your site.</span></span>

<span data-ttu-id="34f4f-130">コマース作成ツールで、サイトの公開グループ機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-130">To turn on the publish groups feature for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="34f4f-131">左のナビゲーション ウィンドウで、**サイト設定** を選択して展開します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-131">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="34f4f-132">**サイト設定** で、**機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-132">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="34f4f-133">**公開グループ** オプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-133">Set the **Publish groups** option to **On**.</span></span>

## <a name="create-a-publish-group"></a><span data-ttu-id="34f4f-134">公開グループの作成</span><span class="sxs-lookup"><span data-stu-id="34f4f-134">Create a publish group</span></span>

<span data-ttu-id="34f4f-135">コマース作成ツールで、サイトの公開グループを作成にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-135">To create a publish group for your site in the Commerce authoring tools, follow these steps.</span></span>

1. <span data-ttu-id="34f4f-136">左のナビゲーション ウィンドウで、**公開グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-136">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="34f4f-137">上部コマンド バーで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-137">In the top command bar, select **New**.</span></span>
1. <span data-ttu-id="34f4f-138">**公開グループの作成** ダイアログ ボックスの、**公開グループ名** に、内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-138">In the **Create Publish Group** dialog box, under **Publish Group Name**, enter a descriptive name.</span></span> <span data-ttu-id="34f4f-139">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-139">Then select **OK**.</span></span>

## <a name="set-the-publish-group-authoring-context"></a><span data-ttu-id="34f4f-140">公開グループ作成コンテキストの設定</span><span class="sxs-lookup"><span data-stu-id="34f4f-140">Set the publish group authoring context</span></span>

<span data-ttu-id="34f4f-141">コマースでは、既定の作成コンテキストが実際のサイト コンテキストになります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-141">In Commerce, the default authoring context is the live site context.</span></span> <span data-ttu-id="34f4f-142">実際のサイト作成コンテキストは、公開グループを使用せずに直接 Web サイトを表示したり変更したりできる既定のビューです。</span><span class="sxs-lookup"><span data-stu-id="34f4f-142">The live site authoring context is the default view where you can view and make changes directly to your website without using a publish group.</span></span> <span data-ttu-id="34f4f-143">サイトの公開されたバージョンに対する最新の直接更新を表します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-143">It represents the latest direct updates to the published version of your site.</span></span> <span data-ttu-id="34f4f-144">左のナビゲーション ウィンドウの **公開グループ** の下にあるコンテキスト コントロールに **実際のサイト** の名前が表示されている場合、実際のサイトの作成コンテキストで作業していることになります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-144">If the context control under **Publish Groups** in the left navigation pane shows the name **Live site**, you're working in the live site authoring context.</span></span> <span data-ttu-id="34f4f-145">**実際のサイト** は、コンテキスト コントロールの既定の名前です。</span><span class="sxs-lookup"><span data-stu-id="34f4f-145">**Live site** is the default name of the context control.</span></span> <span data-ttu-id="34f4f-146">それ以外の場合、コンテキスト コントロールには公開グループの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-146">Otherwise, the context control shows the name of a publish group.</span></span>

<span data-ttu-id="34f4f-147">公開グループを使用するには、その公開グループの作成コンテキストに切り替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-147">To work in a publish group, you must switch to the publish group authoring context for it.</span></span> <span data-ttu-id="34f4f-148">公開グループ コンテキストを設定するには、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-148">To set the publish group context, follow one of these steps.</span></span>

- <span data-ttu-id="34f4f-149">左のナビゲーション ウィンドウで、**公開グループ** の真下にあるコンテキスト コントロールを選択し、表示されるオプションのリストで公開グループの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-149">In the left navigation pane, select the context control directly under **Publish Groups**, and then select the name of the publish group in the list of options that appears.</span></span> <span data-ttu-id="34f4f-150">コンテキスト コントロールが名前変更され、公開グループの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-150">The context control is renamed and shows the name of the publish group.</span></span>
- <span data-ttu-id="34f4f-151">左のナビゲーション ウィンドウで、**公開グループ** を選択し、**公開グループ** の下で、公開グループの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-151">In the left navigation pane, select **Publish Groups**, and then, under **Publish Groups**, select the name of the publish group.</span></span> <span data-ttu-id="34f4f-152">コンテキスト コントロールが名前変更され、公開グループの名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-152">The context control is renamed and shows the name of the publish group.</span></span>

<span data-ttu-id="34f4f-153">公開グループ作成コンテキストを設定した後、サイト コンテンツをプレビューおよび編集するときに、その公開グループ コンテキストで作業を行います。</span><span class="sxs-lookup"><span data-stu-id="34f4f-153">After you set your publish group authoring context, you're working in that publish group context when you preview and edit site content.</span></span>

<span data-ttu-id="34f4f-154">既定の実際のサイト作成コンテキストに戻るには、コンテキスト コントロールを選択し、**実際のサイト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-154">To return to the default live site authoring context, select the context control, and then select **Live site**.</span></span>

## <a name="add-pages-or-other-items-to-a-publish-group"></a><span data-ttu-id="34f4f-155">公開グループへのページまたはその他の項目の追加</span><span class="sxs-lookup"><span data-stu-id="34f4f-155">Add pages or other items to a publish group</span></span>

<span data-ttu-id="34f4f-156">公開グループ作成コンテキストを選択し、左のナビゲーション ウィンドウのコンテキスト コントロールでその名前を表示された後、既定の実際のサイト コンテキストで実行するのと同じようにコンテンツを作成できます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-156">After you've selected a publish group authoring context, and the context control in the left navigation pane shows its name, you can create content just as you do in the default live site context.</span></span> <span data-ttu-id="34f4f-157">他の公開グループから、または実際のサイト コンテキストからの既存のページや他の項目を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-157">You can also add existing pages or other items from other publish groups, or from the live site context.</span></span>

<span data-ttu-id="34f4f-158">既存のページを公開グループにコピーするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-158">To copy existing pages to a publish group, follow these steps.</span></span>

1. <span data-ttu-id="34f4f-159">コピー元の作成コンテキストを選択し、左のナビゲーション ウィンドウで、**ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-159">Select the authoring context to copy from, and then, in the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="34f4f-160">公開グループに追加するページを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-160">Select the page to add to a publish group.</span></span>
1. <span data-ttu-id="34f4f-161">コマンド バーで、**公開グループにコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-161">In the command bar, select **Copy to Publish group**.</span></span>
1. <span data-ttu-id="34f4f-162">**公開グループの選択** ダイアログ ボックスで、ページの追加先となる公開グループを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-162">In the **Select a Publish Group** dialog box, select the publish group to add the page to, and then select **OK**.</span></span>

<span data-ttu-id="34f4f-163">同じ基本手順を使用して、カスタマイズされた製品ページ、URL、テンプレート、レイアウト、フラグメント、およびメディア ライブラリ資産を作成したり、またはこれらのタイプの既存の項目を公開グループに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-163">You can use the same basic steps to create customized product pages, URLs, templates, layouts, fragments, and media library assets, or to add existing items of these types to a publish group.</span></span>

## <a name="validate-a-publish-group"></a><span data-ttu-id="34f4f-164">公開グループの検証</span><span class="sxs-lookup"><span data-stu-id="34f4f-164">Validate a publish group</span></span>

<span data-ttu-id="34f4f-165">公開グループ コンテンツの依存関係がすべて満たされ、およびすべての検証に合格していることを確認するには、検証を実行して、公開アクションをスケジュールする前に解決する必要のある任意の問題を特定します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-165">To make sure that all dependencies in publish group content are satisfied, and that all validations are passed, you can run validation to identify any issues that must be addressed before you schedule a publish action.</span></span>

<span data-ttu-id="34f4f-166">スケジュールする前に公開グループを検証するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-166">To validate your publish group before you schedule it, follow these steps.</span></span>

1. <span data-ttu-id="34f4f-167">左のナビゲーション ウィンドウで、**公開グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-167">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="34f4f-168">検証する公開グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-168">Select the publish group to validate.</span></span>
1. <span data-ttu-id="34f4f-169">コマンド バーで、**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-169">In the command bar, select **Validate**.</span></span>

<span data-ttu-id="34f4f-170">検証は、公開グループのすべてのコンテンツ上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-170">Validation is run on all content in the publish group.</span></span> <span data-ttu-id="34f4f-171">公開アクションの成功を妨げる任意の問題は、右上に表示される通知ボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-171">Any issues that will prevent a successful publish action are shown in a notification box that appears in the upper right.</span></span>

> [!NOTE]
> <span data-ttu-id="34f4f-172">検証は、公開グループがスケジュールされると常に自動で実行されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-172">Validation is always run automatically when a publish group is scheduled.</span></span> <span data-ttu-id="34f4f-173">ただし、コマンド バーの **検証** ボタンを使用すると、公開グループを稼働するようスケジュールする前に、修正の必要な問題を特定しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-173">However, the **Validate** button in the command bar is useful because it helps identify issues that you must fix before you try to schedule a publish group to go live.</span></span>

## <a name="schedule-a-publish-group-to-go-live"></a><span data-ttu-id="34f4f-174">公開グループを稼働するようスケジュールする</span><span class="sxs-lookup"><span data-stu-id="34f4f-174">Schedule a publish group to go live</span></span>

<span data-ttu-id="34f4f-175">公開グループをサイトで稼働するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-175">To schedule a publish group to go live on your site, follow these steps.</span></span>

1. <span data-ttu-id="34f4f-176">左のナビゲーション ウィンドウで、**公開グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-176">In the left navigation pane, select **Publish Groups**.</span></span>
1. <span data-ttu-id="34f4f-177">**公開グループ** で、スケジュールする公開グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-177">Under **Publish Groups**, select the publish group to schedule.</span></span>
1. <span data-ttu-id="34f4f-178">コマンド バーで、**スケジュールの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-178">In the command bar, select **Edit Schedule**.</span></span> <span data-ttu-id="34f4f-179">**スケジュールの編集** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-179">The **Edit Schedule** dialog box appears.</span></span>
1. <span data-ttu-id="34f4f-180">公開グループを稼働する必要がある日時を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-180">Select the date and time when your publish group should go live, and then select **OK**.</span></span>

<span data-ttu-id="34f4f-181">公開グループのスケジュールを取り消すには、同じ手順を実行しますが、**スケジュールの編集** ダイアログ ボックスで **公開グループのスケジュール取消** を選択します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-181">To unschedule a publish group, follow the same steps, but select **Unschedule publish group** in the **Edit Schedule** dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="34f4f-182">非常に大きな公開グループは、スケジュールされた時間に達したときに発行されるまでに 1 〜 2 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-182">Very large publish groups might take up to a minute or two to be published when their scheduled time arrives.</span></span> <span data-ttu-id="34f4f-183">公開アクションは瞬時に行われず、より小さい公開グループの方が先に公開されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="34f4f-183">Be aware that a publish action isn't instantaneous, and that smaller publish groups will be published faster.</span></span>

## <a name="publish-groups-faq"></a><span data-ttu-id="34f4f-184">公開グループに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="34f4f-184">Publish groups FAQ</span></span>

<span data-ttu-id="34f4f-185">**公開グループにはいくつの項目を含めることができますか ?**</span><span class="sxs-lookup"><span data-stu-id="34f4f-185">**How many items can be in a publish group?**</span></span>

<span data-ttu-id="34f4f-186">現時点では、公開グループごとに 2000 項目までという制限があります。</span><span class="sxs-lookup"><span data-stu-id="34f4f-186">Currently, there is a limit of 2,000 items per publish group.</span></span> <span data-ttu-id="34f4f-187">非常に大きな公開グループは、スケジュールされた時間に達したときに発行されるまでに数分かかる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="34f4f-187">Be aware that very large publish groups might take several minutes to be published when their scheduled time arrives.</span></span>

<span data-ttu-id="34f4f-188">**公開グループとは、ソフトウェア開発用語でいうコード "分岐" のようですか ?**</span><span class="sxs-lookup"><span data-stu-id="34f4f-188">**Are publish groups like code "branches" in software development terminology?**</span></span>

<span data-ttu-id="34f4f-189">はいとも、いいえとも言えます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-189">Yes and no.</span></span> <span data-ttu-id="34f4f-190">公開グループは、サイトの分岐されたバージョンと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-190">Publish groups can be thought of as forked versions of your site.</span></span> <span data-ttu-id="34f4f-191">そのように、分岐のような機能を果たします。</span><span class="sxs-lookup"><span data-stu-id="34f4f-191">In that way, they do act like branches.</span></span> <span data-ttu-id="34f4f-192">ただし、個々の項目のレベルでのマージの概念はありません。</span><span class="sxs-lookup"><span data-stu-id="34f4f-192">However, there is no concept of a merge at the level of individual items.</span></span> <span data-ttu-id="34f4f-193">最後に公開される項目は以前に存在したものだけを上書きし、最新の公開アクションは以前の公開アクションよりも常に優先されます。</span><span class="sxs-lookup"><span data-stu-id="34f4f-193">The item that is published last just overwrites what previously existed, and the most recent publish action always supersedes previous publish actions.</span></span>

<span data-ttu-id="34f4f-194">**2 つの公開グループを同時に稼働するようスケジュールできますか ?**</span><span class="sxs-lookup"><span data-stu-id="34f4f-194">**Can I schedule two publish groups to go live at the same time?**</span></span>

<span data-ttu-id="34f4f-195">一連番号</span><span class="sxs-lookup"><span data-stu-id="34f4f-195">No.</span></span> <span data-ttu-id="34f4f-196">パフォーマンスと競合の理由から、予定スケジュールされた公開グループを少なくとも 5 分間隔ずらすようシステムが作動します。</span><span class="sxs-lookup"><span data-stu-id="34f4f-196">For performance and conflict reasons, the system will force you to stagger scheduled publish groups at least five minutes apart.</span></span>

<span data-ttu-id="34f4f-197">**公開グループを使用して、割引や製品更新などのオムニチャネル バック オフィス項目をスケジュールできますか ?**</span><span class="sxs-lookup"><span data-stu-id="34f4f-197">**Can I use publish groups to schedule omnichannel back-office items, such as discounts and product updates?**</span></span>

<span data-ttu-id="34f4f-198">現時点では、公開グループ機能は Web サイトのコンテンツのみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="34f4f-198">Currently, the publish groups feature supports only website content.</span></span> <span data-ttu-id="34f4f-199">ただし、Microsoft は、バック オフィス マーチャンダイジング シナリオとの統合が、オムニチャネル キャンペーン開始の調整と自動化にとって価値があることを認識しています。</span><span class="sxs-lookup"><span data-stu-id="34f4f-199">However, Microsoft is aware that integration with back-office merchandising scenarios could be valuable for the coordination and automation of omnichannel campaign launches.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34f4f-200">追加リソース</span><span class="sxs-lookup"><span data-stu-id="34f4f-200">Additional resources</span></span>

[<span data-ttu-id="34f4f-201">コンテンツを追加する方法</span><span class="sxs-lookup"><span data-stu-id="34f4f-201">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="34f4f-202">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="34f4f-202">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="34f4f-203">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="34f4f-203">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="34f4f-204">クロスチャネル共有の有効化と使用</span><span class="sxs-lookup"><span data-stu-id="34f4f-204">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="34f4f-205">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="34f4f-205">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="34f4f-206">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="34f4f-206">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="34f4f-207">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="34f4f-207">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="34f4f-208">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="34f4f-208">Customize site navigation</span></span>](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]