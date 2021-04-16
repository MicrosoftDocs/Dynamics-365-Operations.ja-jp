---
title: タブ モジュール
description: このトピックでは、タブ モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c865d5e055e3fadf2dda225b49f13a163974768f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797458"
---
# <a name="tab-module"></a><span data-ttu-id="37a85-103">タブ モジュール</span><span class="sxs-lookup"><span data-stu-id="37a85-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37a85-104">このトピックでは、タブ モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="37a85-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="37a85-105">タブ モジュールは、サイト ページの情報をタブに編成する目的で使用するコンテナーと類似するモジュールです。</span><span class="sxs-lookup"><span data-stu-id="37a85-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="37a85-106">これらは、タブで情報を提示する必要のあるページで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="37a85-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="37a85-107">タブ モジュール内では、1つ以上のタブ項目のモジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="37a85-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="37a85-108">それぞれのタブ項目モジュールは、単一のタブを表します。各タブ項目モジュールでは、1つ以上のモジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="37a85-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="37a85-109">タブ項目モジュールに追加できるモジュールのタイプに制限はありません。</span><span class="sxs-lookup"><span data-stu-id="37a85-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="37a85-110">以下の図は、サイトのページにおけるタブ モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="37a85-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="37a85-111">この例では、選択された **配送** タブを使用します。</span><span class="sxs-lookup"><span data-stu-id="37a85-111">In this example, the **Shipping** tab selected.</span></span>

![タブ モジュールの例](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="37a85-113">タブ モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="37a85-113">Tab module properties</span></span>

| <span data-ttu-id="37a85-114">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="37a85-114">Property name</span></span> | <span data-ttu-id="37a85-115">値</span><span class="sxs-lookup"><span data-stu-id="37a85-115">Values</span></span> | <span data-ttu-id="37a85-116">説明</span><span class="sxs-lookup"><span data-stu-id="37a85-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="37a85-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="37a85-117">Heading</span></span> | <span data-ttu-id="37a85-118">テキスト</span><span class="sxs-lookup"><span data-stu-id="37a85-118">Text</span></span> | <span data-ttu-id="37a85-119">このプロパティは、タブ モジュールで使用するオプションのテキスト ヘッダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a85-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="37a85-120">有効なタブ インデックス</span><span class="sxs-lookup"><span data-stu-id="37a85-120">Active Tab Index</span></span> | <span data-ttu-id="37a85-121">番号</span><span class="sxs-lookup"><span data-stu-id="37a85-121">Number</span></span> | <span data-ttu-id="37a85-122">このプロパティは、ページが読み込まれた際に既定で有効となるタブを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a85-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="37a85-123">値が指定されていない場合は、最初のタブ項目が既定で有効となります。</span><span class="sxs-lookup"><span data-stu-id="37a85-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="37a85-124">タブ項目モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="37a85-124">Tab item module properties</span></span>

| <span data-ttu-id="37a85-125">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="37a85-125">Property name</span></span> | <span data-ttu-id="37a85-126">値</span><span class="sxs-lookup"><span data-stu-id="37a85-126">Values</span></span> | <span data-ttu-id="37a85-127">説明</span><span class="sxs-lookup"><span data-stu-id="37a85-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="37a85-128">タイトル</span><span class="sxs-lookup"><span data-stu-id="37a85-128">Title</span></span> | <span data-ttu-id="37a85-129">テキスト</span><span class="sxs-lookup"><span data-stu-id="37a85-129">Text</span></span> | <span data-ttu-id="37a85-130">このプロパティは、タブ項目モジュールで使用するタイトル テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="37a85-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="37a85-131">タブ モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="37a85-131">Add a tab module to a page</span></span>

<span data-ttu-id="37a85-132">ページにタブ モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="37a85-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="37a85-133">Fabrikam マーケティングにテンプレート (または制限のない任意のテンプレート) を使用して、**店舗のポリシー ページ** という名前の新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="37a85-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="37a85-134">**既定のページ** の **メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="37a85-135">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="37a85-136">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="37a85-137">**モジュールの追加** ダイアログ ボックスで、**タブ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="37a85-138">タブ モジュールのプロパティ ウィンドウで、鉛筆の記号の横にある **見出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="37a85-139">**見出しテキスト** 配下の、**見出し** ダイアログ ボックスに、見出しのテキスト (**ポリシ** ーなど) を入力します。</span><span class="sxs-lookup"><span data-stu-id="37a85-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="37a85-140">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-140">Then select **OK**.</span></span>
1. <span data-ttu-id="37a85-141">**タブ** スロットにて、省略ボタン (**...**) を選択し、続いて **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="37a85-142">**モジュールの追加** ダイアログ ボックスで、**タブ項目** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="37a85-143">**タイトル** 配下の、タブ項目モジュールのプロパティ ウィンドウで、にタイトル テキストを入力します (**配送** など ) 。</span><span class="sxs-lookup"><span data-stu-id="37a85-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="37a85-144">**タブ項目** スロットにて、省略ボタン (**...**) を選択し、続いて **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="37a85-145">**モジュールの追加** ダイアログ ボックスで、**テキスト ブロック** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="37a85-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="37a85-146">**リッチ テキスト** 配下の、テキスト ブロック モジュールのプロパティ ウィンドウに一段落分のテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="37a85-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="37a85-147">**タブ** スロットで、見出しを持つタブ項目モジュールをいくつか追加します。</span><span class="sxs-lookup"><span data-stu-id="37a85-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="37a85-148">各タブ項目モジュールで、コンテンツを含むテキスト ブロック モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="37a85-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="37a85-149">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="37a85-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="37a85-150">このページには、タブ項目モジュールを含むタブ モジュールに追加した内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="37a85-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="37a85-151">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="37a85-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37a85-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="37a85-152">Additional resources</span></span>

[<span data-ttu-id="37a85-153">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="37a85-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="37a85-154">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="37a85-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="37a85-155">アコーディオン モジュール</span><span class="sxs-lookup"><span data-stu-id="37a85-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="37a85-156">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="37a85-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]