---
title: 既存のサイト ページの変更
description: このトピックでは、Microsoft Dynamics 365 Commerce で既存のサイト ページを変更する方法について説明します。
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803732"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="cf4c0-103">既存のサイト ページの変更</span><span class="sxs-lookup"><span data-stu-id="cf4c0-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf4c0-104">このトピックでは、Microsoft Dynamics 365 Commerce で既存のサイト ページを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cf4c0-105">ページを変更する必要がある場合は、最初にページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="cf4c0-106">ページが含まれているサイトに移動し、ページの一覧で目的のページを見つけます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="cf4c0-107">ページが見つからない場合は、オーサリング ツールのリッチ検索機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="cf4c0-108">正確なページ名を入力するか、最初のいくつかの文字を入力してから、アスタリスク (\*) を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="cf4c0-109">フィルタ処理されたページの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-109">A filtered list of pages appears.</span></span> <span data-ttu-id="cf4c0-110">この一覧を使用して、目的のページを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="cf4c0-111">正しいページが見つかったら、ページ名を選択し、ページ エディターでページを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="cf4c0-112">ページがページインスペクタに表示されている場合は、 **編集** を選択してページをチェックアウトしてから、ページエディタでページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="cf4c0-113">この方法で、一度に複数のページをチェックアウトできます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="cf4c0-114">ページ エディターでページを開いたら、そのページがチェック アウトされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="cf4c0-115">オーサリング ツールのコマンド バーは、動的で、コンテキストおよび状態に応じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="cf4c0-116">したがって、そのページに対して現在実行できるアクションのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="cf4c0-117">たとえば、ページがチェック アウトされていない場合、コマンド バーには **保存** と **編集の終了** ボタンが表示されません。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="cf4c0-118">ページの状態は、ウィンドウの右側にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="cf4c0-119">ページがまだチェック アウトされていない場合は、コマンド バーで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="cf4c0-120">コマンド バーを変更して、ページの新しい状態を反映します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="cf4c0-121">また、このページがユーザーに対してチェック アウトされたことを示す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="cf4c0-122">次の手順では、実際の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="cf4c0-123">左のページ アウトライン ツリーを使用して、変更するモジュールを見つけて選択し、右のプロパティ ウィンドウで変更を行うことがよくあります。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="cf4c0-124">ただし、モデルまたはフラグメントを追加したり、削除したりすることが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="cf4c0-125">フラグメントまたはモジュールを追加するには、ページ アウトライン ツリーを使用して、モジュールまたはフラグメントを追加するスロットを見つけ、省略記号ボタン (**...**) をそのスロットに対して行います。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="cf4c0-126">モジュールまたはフラグメントを追加するコマンドを含むメニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="cf4c0-127">モジュールまたはフラグメントを削除するには、ページ アウトライン ツリーで目的のモジュールまたはフラグメントを見つけて選択し、省略記号ボタンを選択してから、モジュールまたはフラグメントを削除するコマンドを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="cf4c0-128">また、直接選択することで、ビジュアル ページ ビルダー プレビューに表示されているモジュールのプロパティを表示および編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="cf4c0-129">変更が完了し、その効果に対するプレビューの完了後、コマンド バーの **編集の終了** を選択して、ページをチェック インする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="cf4c0-130">直ちに変更を発行するには、コマンド バーの **発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="cf4c0-131">変更したページの最新のチェック イン バージョンが発行され、サイトを表示する外部ユーザーが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="cf4c0-132">例: ホーム ページのビデオを変更</span><span class="sxs-lookup"><span data-stu-id="cf4c0-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="cf4c0-133">次の例は、ビデオ プレーヤー モジュールに表示されるビデオを変更することによって、ホーム ページを変更する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="cf4c0-134">**サイト** で、**Fabrikam** (またはサイトの名前) を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="cf4c0-135">左のナビゲーション ウィンドウで、**ページ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="cf4c0-136">ホーム ページを検索、選択して、ページ エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="cf4c0-137">コマンド バーで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="cf4c0-138">ページ アウトラインで、**メイン** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="cf4c0-139">**メイン** スロットの下で、すべての流動的なコンテナー モジュールを展開します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="cf4c0-140">ビデオ プレーヤー モジュールを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="cf4c0-141">右のプロパティ ウィンドウで、**ビデオ** プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="cf4c0-142">資産ピッカーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-142">The asset picker appears.</span></span>
1. <span data-ttu-id="cf4c0-143">資産ピッカーで、使用可能なビデオ資産を選択するか、または **新しい資産を更新** を選び、新しいビデオ資産を更新します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="cf4c0-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-144">Select **OK**.</span></span>
1. <span data-ttu-id="cf4c0-145">**保存** を選択し、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="cf4c0-146">**コメント** フィールドで、**ビデオを変更した** と入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="cf4c0-147">**プレビュー** を選択して、更新されたページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="cf4c0-148">完了したら、プレビュー タブを閉じて、作成ツールに戻ります。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="cf4c0-149">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf4c0-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf4c0-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cf4c0-150">Additional resources</span></span>

[<span data-ttu-id="cf4c0-151">新しいサイト ページの追加</span><span class="sxs-lookup"><span data-stu-id="cf4c0-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cf4c0-152">ページ レイアウトの選択</span><span class="sxs-lookup"><span data-stu-id="cf4c0-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="cf4c0-153">SEO メタデータの管理</span><span class="sxs-lookup"><span data-stu-id="cf4c0-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="cf4c0-154">ページの保存、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="cf4c0-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="cf4c0-155">製品ページの拡充</span><span class="sxs-lookup"><span data-stu-id="cf4c0-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="cf4c0-156">カテゴリ ランディング ページの拡充</span><span class="sxs-lookup"><span data-stu-id="cf4c0-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="cf4c0-157">ページ コンテンツのアクセシビリティの検証</span><span class="sxs-lookup"><span data-stu-id="cf4c0-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="cf4c0-158">URL のパラメーターに基いて動的な電子商取引ページを作成する</span><span class="sxs-lookup"><span data-stu-id="cf4c0-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
