---
title: 既存のサイト ページの変更
description: このトピックでは、Microsoft Dynamics 365 Commerce で既存のサイト ページを変更する方法について説明します。
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 87c90ed6ee62a094fe44f549c827cf9de2bf5b2f
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270007"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="d03eb-103">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="d03eb-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d03eb-104">このトピックでは、Microsoft Dynamics 365 Commerce で既存のサイト ページを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d03eb-105">概要</span><span class="sxs-lookup"><span data-stu-id="d03eb-105">Overview</span></span>

<span data-ttu-id="d03eb-106">ページを変更する必要がある場合は、最初にページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="d03eb-107">ページが含まれているサイトに移動し、ページの一覧で目的のページを見つけます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="d03eb-108">ページが見つからない場合は、オーサリング ツールのリッチ検索機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="d03eb-109">正確なページ名を入力するか、最初のいくつかの文字を入力してから、アスタリスク (\*) を入力します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="d03eb-110">フィルタ処理されたページの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-110">A filtered list of pages appears.</span></span> <span data-ttu-id="d03eb-111">この一覧を使用して、目的のページを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="d03eb-112">正しいページが見つかったら、ページ名を選択し、ページ エディターでページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="d03eb-113">ページがページインスペクタに表示されている場合は、 **編集** を選択してページをチェックアウトしてから、ページエディタでページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="d03eb-114">この方法で、一度に複数のページをチェックアウトできます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="d03eb-115">ページ エディターでページを開いたら、そのページがチェック アウトされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03eb-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="d03eb-116">オーサリング ツールのコマンド バーは、動的で、コンテキストおよび状態に応じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="d03eb-117">したがって、そのページに対して現在実行できるアクションのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="d03eb-118">たとえば、ページがチェック アウトされていない場合、コマンド バーには **保存** と **編集の終了** ボタンが表示されません。</span><span class="sxs-lookup"><span data-stu-id="d03eb-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="d03eb-119">ページの状態は、ウィンドウの右側にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="d03eb-120">ページがまだチェック アウトされていない場合は、コマンド バーで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="d03eb-121">コマンド バーを変更して、ページの新しい状態を反映します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="d03eb-122">また、このページがユーザーに対してチェック アウトされたことを示す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="d03eb-123">次の手順では、実際の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="d03eb-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="d03eb-124">左のページ アウトライン ツリーを使用して、変更するモジュールを見つけて選択し、右のプロパティ ウィンドウで変更を行うことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="d03eb-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="d03eb-125">ただし、モデルまたはフラグメントを追加したり、削除したりすることが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d03eb-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="d03eb-126">フラグメントまたはモジュールを追加するには、ページ アウトライン ツリーを使用して、モジュールまたはフラグメントを追加するスロットを見つけ、省略記号ボタン (**...**) をそのスロットに対して行います。</span><span class="sxs-lookup"><span data-stu-id="d03eb-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="d03eb-127">モジュールまたはフラグメントを追加するコマンドを含むメニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="d03eb-128">モジュールまたはフラグメントを削除するには、ページ アウトライン ツリーで目的のモジュールまたはフラグメントを見つけて選択し、省略記号ボタンを選択してから、モジュールまたはフラグメントを削除するコマンドを選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="d03eb-129">また、直接選択することで、「What You See Is What You Get」 (WYSIWYG) に表示されているモジュールのプロパティを表示および編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="d03eb-130">変更が完了し、その効果に対するプレビューの完了後、コマンド バーの **編集の終了** を選択して、ページをチェック インする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d03eb-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="d03eb-131">直ちに変更を発行するには、コマンド バーの**発行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="d03eb-132">変更したページの最新のチェック イン バージョンが発行され、サイトを表示する外部ユーザーが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d03eb-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="d03eb-133">例: ホーム ページのビデオを変更</span><span class="sxs-lookup"><span data-stu-id="d03eb-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="d03eb-134">次の例は、ビデオ プレーヤー モジュールに表示されるビデオを変更することによって、ホーム ページを変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d03eb-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="d03eb-135">**サイト**で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d03eb-136">左のナビゲーション ウィンドウで、**ページ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="d03eb-137">ホーム ページを検索、選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="d03eb-138">コマンド バーで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="d03eb-139">ページ アウトラインで、**メイン**スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="d03eb-140">**メイン**スロットの下で、すべての流動的なコンテナー モジュールを展開します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="d03eb-141">ビデオ プレーヤー モジュールを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="d03eb-142">右のプロパティ ウィンドウで、**ビデオ**プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="d03eb-143">資産ピッカーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d03eb-143">The asset picker appears.</span></span>
1. <span data-ttu-id="d03eb-144">資産ピッカーで、使用可能なビデオ資産を選択するか、または**新しい資産を更新**を選び、新しいビデオ資産を更新します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="d03eb-145">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-145">Select **OK**.</span></span>
1. <span data-ttu-id="d03eb-146">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d03eb-147">**コメント**フィールドで、**ビデオを変更した**と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="d03eb-148">**プレビュー**を選択して、更新されたページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="d03eb-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="d03eb-149">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="d03eb-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="d03eb-150">**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d03eb-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d03eb-151">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d03eb-151">Additional resources</span></span>

[<span data-ttu-id="d03eb-152">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="d03eb-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d03eb-153">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="d03eb-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d03eb-154">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="d03eb-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d03eb-155">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="d03eb-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d03eb-156">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="d03eb-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d03eb-157">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="d03eb-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="d03eb-158">ページ コンテンツ アクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="d03eb-158">Verify page content accessibility</span></span>](verify-accessibility.md)
