---
title: "フィールドの説明を表示およびエクスポートする"
description: "この記事では、フィールドの説明を表示する方法と説明をエクスポートするフィールドの [説明] ページを使用する方法について説明します。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FieldDescriptions
audience: Application User, Developer, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1ee87dbe9dab089a893d9c69d2573a4c4b11b58
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="view-and-export-field-descriptions"></a><span data-ttu-id="c9f3c-103">フィールドの説明を表示およびエクスポートする</span><span class="sxs-lookup"><span data-stu-id="c9f3c-103">View and export field descriptions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f3c-104">この記事では、フィールドの説明を表示する方法と説明をエクスポートするフィールドの [説明] ページを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-104">This article describes how to view field descriptions and how to use the Field descriptions page to export descriptions.</span></span>

<span data-ttu-id="c9f3c-105">Microsoft Dynamics 365 for Finance and Operations には、いくつかのさらに複雑なフィールドについての説明があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-105">Microsoft Dynamics 365 for Finance and Operations has descriptions for some of the more complex fields.</span></span> <span data-ttu-id="c9f3c-106">フィールド上に置くと、これらの説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-106">These descriptions appear when you hover over a field.</span></span> <span data-ttu-id="c9f3c-107">**フィールドの説明** ページを使用すると、フィールドの説明を表示およびエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-107">You can also view and export descriptions on the **Field descriptions** page.</span></span> 

<span data-ttu-id="c9f3c-108">すべてのページにフィールドの説明があるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-108">Not all pages have field descriptions.</span></span> <span data-ttu-id="c9f3c-109">より複雑なフィールドだけに説明を提供し、フィールドの使用が明確な場合は提供しません。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-109">We want to provide descriptions only for the more complex fields, not where the use of the field is obvious.</span></span> <span data-ttu-id="c9f3c-110">したがって、一部のページは、任意のフィールドの説明がない、一部のページには説明がある、多くのパラメーターのページなど複雑なページには多くの説明があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-110">Therefore, some pages don't have any field descriptions, some pages have a few descriptions, and some of the more complex pages, such as many of the parameters pages, have many descriptions.</span></span> 

<span data-ttu-id="c9f3c-111">Finance and Operations の開発環境に対するアクセス権を持つ場合、新しいフィールドの説明を追加して既存の説明をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-111">If you have access to the Finance and Operations development environment, you can add new field descriptions and customize existing descriptions.</span></span> <span data-ttu-id="c9f3c-112">たとえば、フィールドの説明に会社固有の情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-112">For example, you can add company-specific information to a field description.</span></span> <span data-ttu-id="c9f3c-113">詳細については、「[のフィールド ヘルプのカスタマイズ](../../dev-itpro/user-interface/customize-field-help.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-113">For more information, see [Customize field help](../../dev-itpro/user-interface/customize-field-help.md).</span></span>

## <a name="see-field-descriptions-in-the-user-interface"></a><span data-ttu-id="c9f3c-114">ユーザー インターフェイスのフィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-114">See field descriptions in the user interface</span></span>
<span data-ttu-id="c9f3c-115">フィールドの上にマウス ポインターを移動するとフィールド名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-115">You can view field descriptions by hovering over a field.</span></span> <span data-ttu-id="c9f3c-116">説明がない場合、フィールドの上にマウス ポインターを移動するとフィールド名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-116">If no description is available, you see the field name when you hover over the field.</span></span> <span data-ttu-id="c9f3c-117">(注記: Dynamics AX 7.0 (2016 年 2 月) のフィールドの説明では、**フィールドの説明** ページでのみ表示できます。) 次の図は、**カウント中に品目をロック** フィールドの上に置くときに表示されるフィールドの説明を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-117">(Note: In Dynamics AX 7.0 (February 2016), field descriptions can be viewed only on the **Field descriptions** page.) The following illustration shows the field description that appears when you hover over the **Lock items during count** field.</span></span> 

<span data-ttu-id="c9f3c-118">[![フィールドの説明の例](./media/field-description.png)](./media/field-description.png)</span><span class="sxs-lookup"><span data-stu-id="c9f3c-118">[![Example of a field description](./media/field-description.png)](./media/field-description.png)</span></span>

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a><span data-ttu-id="c9f3c-119">フィールドの説明ページを使用して、フィールドのヘルプを表示しエクスポートする</span><span class="sxs-lookup"><span data-stu-id="c9f3c-119">Use the Field descriptions page to view and export field help</span></span>
<span data-ttu-id="c9f3c-120">**フィールドの説明** ページを使用すると、フィールドの説明を表示およびエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-120">The **Field descriptions** page lets you view and export field descriptions.</span></span> <span data-ttu-id="c9f3c-121">一度に 1 ページずつ、使用できる説明を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-121">You can see the descriptions that are available for one page at a time.</span></span>

### <a name="view-the-descriptions-for-a-page"></a><span data-ttu-id="c9f3c-122">ページの説明を表示する</span><span class="sxs-lookup"><span data-stu-id="c9f3c-122">View the descriptions for a page</span></span>

<span data-ttu-id="c9f3c-123">ページの説明を表示するには以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-123">To view the descriptions for a page, follow this step.</span></span>

-   <span data-ttu-id="c9f3c-124">**名前を選択** フィールドに、ページの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-124">In the **Select a page** field, type the name of the page.</span></span> <span data-ttu-id="c9f3c-125">または、矢印をクリックしてすべてのページのリストを開き、一覧を参照またはフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-125">Alternatively, click the arrow to open a list of all the pages, and then browse or filter the list.</span></span>

<span data-ttu-id="c9f3c-126">ユーザー インターフェイス (UI) に表示されるページ名 (たとえば、**Customers**)、またはページを右クリックすると使用できる、**CustTable**などのページのコード名 (AOT 名) を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-126">You can use either the name of the page that is shown in the user interface (UI) (for example, **Customers**) or the code name (AOT name) that's available when you right-click a page (for example, **CustTable**).</span></span> 

<span data-ttu-id="c9f3c-127">ページの一覧にフィルターを適用するさまざまな方法については、この記事の後半の「ページを検索」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-127">For information about the various ways to filter the list of pages, see the "Searching for a page" section later in this article.</span></span> 

<span data-ttu-id="c9f3c-128">**説明のないフィールドを含める** オプションを **はい** に設定する場合、ページにフィールドの説明がなくても、ページのすべてのフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-128">If you set the **Include fields without a description** option to **Yes**, all the fields on the page are shown, even if they don't have a field description.</span></span>

### <a name="export-the-descriptions-for-a-page"></a><span data-ttu-id="c9f3c-129">ページの説明のエクスポート</span><span class="sxs-lookup"><span data-stu-id="c9f3c-129">Export the descriptions for a page</span></span>

<span data-ttu-id="c9f3c-130">ページの説明をエクスポートするには以下を実行します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-130">To export the descriptions for a page, follow these steps.</span></span>

1.  <span data-ttu-id="c9f3c-131">**ページの選択** フィールドでページを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-131">In the **Select a page** field, select a page.</span></span>
2.  <span data-ttu-id="c9f3c-132">右上隅の **Microsoft Office で開く** ボタンをクリックしてから、**FieldDescriptionTmp** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-132">Click the **Open in Microsoft Office** button in the upper-right corner, and then click **FieldDescriptionTmp**.</span></span>

### <a name="searching-for-a-page"></a><span data-ttu-id="c9f3c-133">ページを検索する</span><span class="sxs-lookup"><span data-stu-id="c9f3c-133">Searching for a page</span></span>

<span data-ttu-id="c9f3c-134">**ページの選択** フィールドでページを検索するには、様々な方法があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-134">There are several ways to search for a page in the **Select a page** field.</span></span> <span data-ttu-id="c9f3c-135">多くの場合、**ページの選択** フィールド内の矢印をクリックしてドロップダウン リストを開き、ページのフィルター済みリストから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-135">In many cases, you must click the arrow in the **Select a page** field to open the drop-down list, and then select from a filtered list of pages.</span></span>

-   <span data-ttu-id="c9f3c-136">名前の一部を入力してから、ドロップダウン リストを開き、ページのフィルター処理されたリストから選択します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-136">Type part of the name, and then open the drop-down list to select from a filtered list of pages.</span></span>
-   <span data-ttu-id="c9f3c-137">ドロップダウン リストを開いて、一覧の上部にある **ページ名** のヘッダー、または **ページの AOT 名** のヘッダーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-137">Open the drop-down list, and then click either the **Page name** heading at the top of the list or the **Page AOT name** heading.</span></span> <span data-ttu-id="c9f3c-138">これにより、**次の値で始まるページ名** などの、高度なフィルター処理オプションを使用することができる、ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-138">A dialog box appears, where you can use advanced filtering options, such as **Page name begins with**.</span></span>
-   <span data-ttu-id="c9f3c-139">ページの完全な名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-139">Type the full name of the page.</span></span> <span data-ttu-id="c9f3c-140">このオプションを使用するときは、フィールドの説明が表示される場合であっても、ドロップダウン リストを開いてリスト内にある他のものを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-140">When you use this option, it's best to open the drop-down list and see what else is in the list, even if field descriptions are shown.</span></span>
    -   <span data-ttu-id="c9f3c-141">名前とに完全に一致するものが 1 つある場合、そのページのフィールドの説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-141">If there is a single exact match to the name, the field descriptions for that page are shown.</span></span>
    -   <span data-ttu-id="c9f3c-142">複数の一致がある場合は、説明は表示されません。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-142">If there is more than one exact match, no descriptions are shown.</span></span> <span data-ttu-id="c9f3c-143">ドロップダウン リストを開き、表示するページを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-143">You must open the drop-down list and select the page that you want.</span></span>
    -   <span data-ttu-id="c9f3c-144">入力した名前が別のページの名前の一部である場合は、ページの説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-144">If the name that you typed is part of the name of another page, you see the descriptions for your page.</span></span> <span data-ttu-id="c9f3c-145">ただし、ドロップダウン リストを開くと、その名前が含まれている追加のページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-145">However, if you open the drop-down list, you see additional pages that contain that name.</span></span>

<span data-ttu-id="c9f3c-146">例えば、[*<strong><em> ページの選択</em></strong>*] フィールドに <strong>棚卸</strong> と入力しても、説明は表示されません。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-146">For example, no descriptions are shown when you type <strong>Counting</strong> in the *<strong><em>Select a page</em></strong>* field.</span></span> <span data-ttu-id="c9f3c-147">ドロップダウン リストを開くと、<strong>Counting</strong> という名前の 2 つのページが表示され、"Counting" という語を含む複数のページも表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-147">You open the drop-down list, and see that there are two pages that have the name <strong>Counting</strong> and several pages that contain the word "Counting" in the name.</span></span> <span data-ttu-id="c9f3c-148">AOT 名 <strong>InventJournalCount</strong> を持つページを選択すると、そのページのフィールドの説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-148">If you select the page that has the AOT name <strong>InventJournalCount</strong>, the field descriptions are shown for that page.</span></span> <span data-ttu-id="c9f3c-149">ただし、ドロップダウン リストを再度開くと、リスト内に AOT ページ名の一部として "InventJournalCount" を含むすべてのページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-149">However, if you open the drop-down list again, you will see that the list now contains all pages that have "InventJournalCount" as part of their AOT name.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c9f3c-150">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="c9f3c-150">Troubleshooting</span></span>
<span data-ttu-id="c9f3c-151">このセクションには、フィールドの説明を使用するときに発生する可能性がある問題の、トラブルシューティングに役立つ情報が用意されています。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-151">This section provides information to help you troubleshoot issues that you might encounter when you use field descriptions.</span></span>

### <a name="i-cant-find-a-field-description"></a><span data-ttu-id="c9f3c-152">フィールドの説明が見つかりません</span><span class="sxs-lookup"><span data-stu-id="c9f3c-152">I can't find a field description</span></span>

<span data-ttu-id="c9f3c-153">さらに複雑なフィールドに説明を追加するプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-153">We’re in the process of adding descriptions for the more complex fields.</span></span> <span data-ttu-id="c9f3c-154">特定のフィールドでサポートが必要な場合は、このトピックにコメントを追加して、通知してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-154">If you require help for a particular field, let us know by adding a comment for this topic.</span></span>

### <a name="the-field-description-isnt-helpful"></a><span data-ttu-id="c9f3c-155">フィールドの説明が役に立ちません</span><span class="sxs-lookup"><span data-stu-id="c9f3c-155">The field description isn't helpful</span></span>

<span data-ttu-id="c9f3c-156">このトピックにコメントを追加して、通知してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-156">Let us know by adding a comment for this topic.</span></span> <span data-ttu-id="c9f3c-157">可能な場合は、必要な追加情報について説明してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-157">If you can, describe the additional information that you require.</span></span>

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a><span data-ttu-id="c9f3c-158">[フィールドの説明] ページのフィールドが表示されません。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-158">I can't find a field on the Field descriptions page</span></span>

<span data-ttu-id="c9f3c-159">ページのすべてのフィールドを表示するには、**説明のないフィールドを含める** オプションに **はい** を設定します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-159">To show all the fields on a page, set the **Include fields without a description** option to **Yes**.</span></span> <span data-ttu-id="c9f3c-160">**ページの選択** フィールドをクリックして、適切なページを選択していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-160">Click the **Select a page** field to verify that you've selected the correct page.</span></span> <span data-ttu-id="c9f3c-161">入力した名前が別のフィールド名の一部である場合は、長い名前を持つページが選択されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-161">If the name that you typed is part of another field name, you might have selected the page that has the longer name.</span></span>

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a><span data-ttu-id="c9f3c-162">[フィールドの説明] ページのページが表示されません。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-162">I can't find a page on the Field descriptions page</span></span>

<span data-ttu-id="c9f3c-163">ページを検索するさまざまな方法については、この記事の前半の「ページを検索」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-163">For information about the various way to find pages, see the "Searching for pages" section earlier in this article.</span></span> <span data-ttu-id="c9f3c-164">ページの正確な名前を入力した場合、同じ名前のページが複数ある場合、フィールドの説明が表示されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-164">If you've typed the exact name of the page, the field descriptions might not be shown if more than one page has the same name.</span></span> <span data-ttu-id="c9f3c-165">**ページの選択** フィールド内の矢印をクリックして、使用できるページのフィルター処理されたリストを開きます。</span><span class="sxs-lookup"><span data-stu-id="c9f3c-165">Click the arrow in the **Select a page** field to open a filtered list of the pages that are available.</span></span>

<a name="additional-resources"></a><span data-ttu-id="c9f3c-166">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="c9f3c-166">Additional resources</span></span>
--------

[<span data-ttu-id="c9f3c-167">フィールド ヘルプのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c9f3c-167">Customize field help</span></span>](../../dev-itpro/user-interface/customize-field-help.md)





