---
title: アコーディオン モジュール
description: このトピックでは、アコーディオン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページへの追加方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417257"
---
# <a name="accordion-module"></a><span data-ttu-id="e439d-103">アコーディオン モジュール</span><span class="sxs-lookup"><span data-stu-id="e439d-103">Accordion module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e439d-104">このトピックでは、アコーディオン モジュールと、Microsoft Dynamics 365 Commerce のサイト ページへの追加方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e439d-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e439d-105">概要</span><span class="sxs-lookup"><span data-stu-id="e439d-105">Overview</span></span>

<span data-ttu-id="e439d-106">アコーディオン モジュールは、コンテナと類似するモジュールで、折りたたみ可能な引き出しのような機能を提供することにより、ページ上の情報またはモジュールを整理する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="e439d-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="e439d-107">アコーディオン モジュールは、任意のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="e439d-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="e439d-108">アコーディオン モジュール内では、1つ以上のアコーディオン項目のモジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e439d-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="e439d-109">各アコーディオン項目モジュールは、折りたたみ可能なドロワーを表しています。</span><span class="sxs-lookup"><span data-stu-id="e439d-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="e439d-110">アコーディオン モジュール内では、1つ以上のアコーディオン項目のモジュールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e439d-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="e439d-111">アコーディオン項目のモジュールに追加できるモジュールのタイプに制限はありません。</span><span class="sxs-lookup"><span data-stu-id="e439d-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="e439d-112">次の図は、ストアのよく寄せられる質問 (FAQ) ページで情報を整理する目的で使用するアコーディオン モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="e439d-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![アコーディオン モジュールの例](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="e439d-114">アコーディオン モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="e439d-114">Accordion module properties</span></span>

| <span data-ttu-id="e439d-115">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e439d-115">Property name</span></span> | <span data-ttu-id="e439d-116">値</span><span class="sxs-lookup"><span data-stu-id="e439d-116">Values</span></span> | <span data-ttu-id="e439d-117">説明</span><span class="sxs-lookup"><span data-stu-id="e439d-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e439d-118">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e439d-118">Heading</span></span> | <span data-ttu-id="e439d-119">テキスト</span><span class="sxs-lookup"><span data-stu-id="e439d-119">Text</span></span> | <span data-ttu-id="e439d-120">このプロパティは、アコーディオン モジュールで使用するオプションのテキスト ヘッダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="e439d-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="e439d-121">すべて展開</span><span class="sxs-lookup"><span data-stu-id="e439d-121">Expand All</span></span> | <span data-ttu-id="e439d-122">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e439d-122">**True** or **False**</span></span> | <span data-ttu-id="e439d-123">この値が **True** に設定されている場合は 、展開/折りたたみ機能が有効になり、アコーディオン モジュール内のすべての項目を展開して折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="e439d-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="e439d-124">やり取りのスタイル</span><span class="sxs-lookup"><span data-stu-id="e439d-124">Interaction Style</span></span> | <span data-ttu-id="e439d-125">**単独**または **単一の項目のみを展開する**</span><span class="sxs-lookup"><span data-stu-id="e439d-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="e439d-126">このプロパティでは、アコーディオン項目の操作スタイルを定義します。</span><span class="sxs-lookup"><span data-stu-id="e439d-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="e439d-127">この値が **単独** に設定されている場合は 、各アコーディオン項目を個別に展開したり折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="e439d-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="e439d-128">この値が**単一の項目のみを展開する**ように設定されている場合は、一度に1つの項目のみを展開できます。</span><span class="sxs-lookup"><span data-stu-id="e439d-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="e439d-129">項目が展開されると、それまで展開されていた項目が折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="e439d-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="e439d-130">アコーディオン項目モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="e439d-130">Accordion item module properties</span></span>

| <span data-ttu-id="e439d-131">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e439d-131">Property name</span></span> | <span data-ttu-id="e439d-132">値</span><span class="sxs-lookup"><span data-stu-id="e439d-132">Values</span></span> | <span data-ttu-id="e439d-133">説明</span><span class="sxs-lookup"><span data-stu-id="e439d-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e439d-134">タイトル</span><span class="sxs-lookup"><span data-stu-id="e439d-134">Title</span></span> | <span data-ttu-id="e439d-135">テキスト</span><span class="sxs-lookup"><span data-stu-id="e439d-135">Text</span></span> | <span data-ttu-id="e439d-136">このプロパティは、アコーディオン項目モジュールで使用するタイトル テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="e439d-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="e439d-137">タイトル領域を選択することで、セクションを展開したり折りたたむことができます。</span><span class="sxs-lookup"><span data-stu-id="e439d-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="e439d-138">既定で展開する</span><span class="sxs-lookup"><span data-stu-id="e439d-138">Expand by default</span></span> | <span data-ttu-id="e439d-139">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e439d-139">**True** or **False**</span></span> | <span data-ttu-id="e439d-140">この値が **True** に設定されている場合、既定の状態として、ページの読み込み時にアコーディオン項目が展開されます。</span><span class="sxs-lookup"><span data-stu-id="e439d-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="e439d-141">アコーディオン モジュールを FAQ ページに追加する</span><span class="sxs-lookup"><span data-stu-id="e439d-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="e439d-142">FAQ ページにアコーディオン モジュールを追加して、サイト ビルダーにそのプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e439d-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e439d-143">**ページ** に移動し、Fabrikam マーケティングにテンプレート (または制限のない任意のテンプレート) を使用して、**店舗の FAQ**という名前の新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="e439d-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="e439d-144">**既定のページ**の**メイン** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e439d-145">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e439d-146">**コンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e439d-147">**モジュールの追加** ダイアログ ボックスで、**アコーディオン** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e439d-148">アコーディオン モジュールのプロパティ ウィンドウで、鉛筆の記号の横にある **見出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="e439d-149">**見出し** ダイアログ ボックスの **見出しテキスト** ボックスに、**よく寄せられる質問**を入力します。</span><span class="sxs-lookup"><span data-stu-id="e439d-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="e439d-150">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-150">Then select **OK**.</span></span>
1. <span data-ttu-id="e439d-151">アコーディオン モジュールのプロパティ ウィンドウで、**すべてを展開する** チェック ボックスをオンにし、**相互作用スタイル** フィールドで **単独** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="e439d-152">**アコーディオン** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e439d-153">**モジュールの追加** ダイアログ ボックスで、**アコーディオン項目** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e439d-154">アコーディオン項目モジュールのプロパティ ウィンドウで、**タイトル**にタイトル テキストを入力します (**返品の仕組み**など ) 。</span><span class="sxs-lookup"><span data-stu-id="e439d-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="e439d-155">**アコーディオン項目**スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e439d-156">**モジュールの追加** ダイアログ ボックスで、**テキスト ブロック** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e439d-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e439d-157">テキスト ブロックモジュールのプロパティ ウィンドウで、一段落分のテキストを入力します (たとえば、**コールセンターを使用して、返品を処理する必要があります。返品については、1-800 ~ FABRIKAMに問い合わせてください。製品には、30日間の返品ポリシーが含まれています。返品は、この時間枠内で開始する必要があります**)。</span><span class="sxs-lookup"><span data-stu-id="e439d-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="e439d-158">**アコーディオン**スロットで 、アコーディオン項目のモジュールをいくつか追加します。</span><span class="sxs-lookup"><span data-stu-id="e439d-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="e439d-159">各アコーディオン項目モジュールで、コンテンツを含むテキスト ブロック モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e439d-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="e439d-160">**保存** を選択し、 続いて**プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="e439d-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="e439d-161">このページには、追加したコンテンツを含むアコーディオン モジュールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e439d-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="e439d-162">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="e439d-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e439d-163">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e439d-163">Additional resources</span></span>

[<span data-ttu-id="e439d-164">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="e439d-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e439d-165">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="e439d-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e439d-166">タブ モジュール</span><span class="sxs-lookup"><span data-stu-id="e439d-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="e439d-167">テキスト ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="e439d-167">Text block module</span></span>](add-content-rich-block.md)
