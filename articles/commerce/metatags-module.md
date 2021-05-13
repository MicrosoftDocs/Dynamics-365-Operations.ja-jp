---
title: メタタグ モジュール
description: このトピックでは、メタタグ モジュールと、それらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c75b69a3be938d84ee7dfd5bd9dff299131ae611
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853509"
---
# <a name="metatags-module"></a><span data-ttu-id="07d1d-103">メタタグ モジュール</span><span class="sxs-lookup"><span data-stu-id="07d1d-103">Metatags module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="07d1d-104">このトピックでは、メタタグ モジュールと、それらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-104">This topic covers metatags modules and describes how to add them to templates in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="07d1d-105">メタタグ モジュールは、サイト ページの検索エンジンの最適化 (SEO) ランキングの向上に役立つカスタム HTML メタ タグの入力をサポートします。</span><span class="sxs-lookup"><span data-stu-id="07d1d-105">The metatags module supports the entry of custom HTML meta tags that can help improve search engine optimization (SEO) rankings for site pages.</span></span>

<span data-ttu-id="07d1d-106">メタタグ モジュールは、テンプレートの **HTML ヘッド** スロットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="07d1d-106">The metatags module is added to a template's **HTML Head** slot.</span></span> <span data-ttu-id="07d1d-107">その後、テンプレートとテンプレートから派生したサイト ページの両方で構成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="07d1d-107">It's then available for configuration both in the template and on the site pages that are derived from the template.</span></span>

<span data-ttu-id="07d1d-108">1 つ以上の一般メタ タグをテンプレートに追加できます。</span><span class="sxs-lookup"><span data-stu-id="07d1d-108">One or more general meta tags can be added to a template.</span></span> <span data-ttu-id="07d1d-109">ただし、ページ固有のメタ タグは関連するサイト ページに追加される必要があります。</span><span class="sxs-lookup"><span data-stu-id="07d1d-109">However, page-specific meta tags should be added to the relevant site pages.</span></span> <span data-ttu-id="07d1d-110">ページ レベルのメタ タグは、テンプレート レベルのメタ タグを上書きします。</span><span class="sxs-lookup"><span data-stu-id="07d1d-110">Page-level meta tags overwrite template-level meta tags.</span></span> 

<span data-ttu-id="07d1d-111">次の図は、メタ タグモジュールがテンプレートの **HTML ヘッド** スロットに追加された例を示しています。</span><span class="sxs-lookup"><span data-stu-id="07d1d-111">The following illustration shows an example where a metatags module has been added to the **HTML Head** slot of a template.</span></span>

![テンプレートの HTML ヘッド スロットに含まれるメタタグ モジュール](media/metatags-module-1.png)

## <a name="metatags-module-properties"></a><span data-ttu-id="07d1d-113">メタタグ モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="07d1d-113">Metatags module properties</span></span>

| <span data-ttu-id="07d1d-114">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="07d1d-114">Property name</span></span> | <span data-ttu-id="07d1d-115">値</span><span class="sxs-lookup"><span data-stu-id="07d1d-115">Values</span></span> | <span data-ttu-id="07d1d-116">説明</span><span class="sxs-lookup"><span data-stu-id="07d1d-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="07d1d-117">メタ タグ</span><span class="sxs-lookup"><span data-stu-id="07d1d-117">Meta Tags</span></span> | <span data-ttu-id="07d1d-118">テキスト</span><span class="sxs-lookup"><span data-stu-id="07d1d-118">Text</span></span> | <span data-ttu-id="07d1d-119">1 つ以上のメタ タグをモジュールに追加できます。</span><span class="sxs-lookup"><span data-stu-id="07d1d-119">One or more meta tags can be added to the module.</span></span> |

## <a name="add-a-metatags-module-to-a-template"></a><span data-ttu-id="07d1d-120">テンプレートへのメタ タグ モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="07d1d-120">Add a metatags module to a template</span></span>

<span data-ttu-id="07d1d-121">テンプレートに メタタグ モジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="07d1d-121">To add a metatags module to a template, follow these steps.</span></span>

1. <span data-ttu-id="07d1d-122">サイトのコマース サイト ビルダで、**テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-122">In Commerce site builder for your site, select **Templates**.</span></span>
1. <span data-ttu-id="07d1d-123">テンプレートを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-123">Select a template, and then select **Edit**.</span></span>
1. <span data-ttu-id="07d1d-124">**HTML ヘッド** スロットで省略 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-124">In the **HTML Head** slot, select the ellipsis (**...**), and then select **Add module**.</span></span>

    ![新しいモジュールの追加](media/metatags-module-2.png)

1. <span data-ttu-id="07d1d-126">**モジュールの追加** ダイアログ ボックスで、**メタタグ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-126">In the **Add Module** dialog box, select the **Metatags** module, and then select **OK**.</span></span>

    ![メタタグ モジュールの追加](media/metatags-module-3.png)

1. <span data-ttu-id="07d1d-128">メタ タグを追加するには **メタタグ** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-128">To add meta tags, select the **Metatags** slot.</span></span> <span data-ttu-id="07d1d-129">次に、モジュールのプロパティ ウィンドウで、**メタ タグの追加** を選択して各メタ タグを追加します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-129">Then, in the module properties pane, select **Add Meta Tag** to add each meta tag.</span></span> <span data-ttu-id="07d1d-130">上矢印ボタンと下矢印ボタンを使用して、メタ タグの順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="07d1d-130">You can reorder the meta tags by using the up arrow and down arrow buttons.</span></span>
1. <span data-ttu-id="07d1d-131">テンプレートの編集が完了したら、**保存** を選択し、**編集の完了** を選択して、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="07d1d-131">When you've finished editing the template, select **Save**, select **Finish editing**, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="07d1d-132">テンプレートにメタ タグ モジュールを追加した後、ページ固有のメタ タグをテンプレートを使用するサイトページに追加できます。</span><span class="sxs-lookup"><span data-stu-id="07d1d-132">After the meta tags module is added to a template, page-specific meta tags can be added to the site pages that use the template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07d1d-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="07d1d-133">Additional resources</span></span>

[<span data-ttu-id="07d1d-134">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="07d1d-134">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="07d1d-135">既定のページ モジュール</span><span class="sxs-lookup"><span data-stu-id="07d1d-135">Default page module</span></span>](default-page-module.md)

[<span data-ttu-id="07d1d-136">ページ集計モジュール</span><span class="sxs-lookup"><span data-stu-id="07d1d-136">Page summary modules</span></span>](page-summary-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
