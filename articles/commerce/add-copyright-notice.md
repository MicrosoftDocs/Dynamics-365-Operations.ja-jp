---
title: 著作権に関する注意事項の追加
description: このトピックでは、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696948"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="7c4da-103">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="7c4da-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7c4da-104">このトピックでは、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7c4da-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="7c4da-105">Prerequisites</span></span>

<span data-ttu-id="7c4da-106">サイトに著作権に関する注意事項を追加する前に、次の項目が必要です。</span><span class="sxs-lookup"><span data-stu-id="7c4da-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="7c4da-107">共有フッター フラグメントを含むテンプレート。</span><span class="sxs-lookup"><span data-stu-id="7c4da-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="7c4da-108">そのテンプレートを使用するページ。</span><span class="sxs-lookup"><span data-stu-id="7c4da-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="7c4da-109">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="7c4da-109">Add a copyright notice</span></span>

<span data-ttu-id="7c4da-110">特定のテンプレートを使用する各ページの下に著作権に関する注意事項を追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="7c4da-111">**フラグメント**に移動し、**新しいページ フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="7c4da-112">ダイアログ ボックスで、**フッター** モジュールを選択し、フラグメントに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="7c4da-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="7c4da-113">たとえば、**フッター 著作権** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="7c4da-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-114">Select **OK**.</span></span>
1. <span data-ttu-id="7c4da-115">ナビゲーション ウィンドウで、**フッター**の横にある省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c4da-116">ダイアログ ボックスで、**フッター カテゴリ**を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="7c4da-117">ナビゲーション ウィンドウで、**フッター カテゴリ**の横にある省略記号ボタンを選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c4da-118">ダイアログ ボックスで、**コンテンツ リッチ ブロック項目**を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="7c4da-119">ナビゲーション ウィンドウで、**コンテンツ リッチ ブロック項目**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="7c4da-120">右側のプロパティ ウィンドウの、**段落**フィールドで、著作権に関するメッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="7c4da-121">たとえば、**(C) Fabrikam 2019** と入力します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="7c4da-122">**保存**を選択し、**チェックイン**を選択してから、**公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="7c4da-123">**テンプレート**に移動し、テンプレートを選択してから、**チェックアウト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="7c4da-124">**ページ アウトライン**で、**本文**を展開してから、**既定のページ**を展開します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="7c4da-125">**フッター スロット**の横にある省略記号ボタンを選択し、**フラグメントの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="7c4da-126">前に作成したフラグメントを選択し、**選択**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="7c4da-127">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="7c4da-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="7c4da-128">著作権に関する注意事項を含むフッターは、選択したテンプレートを使用するすべてのページの下部に自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7c4da-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c4da-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7c4da-129">Additional resources</span></span>

[<span data-ttu-id="7c4da-130">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="7c4da-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="7c4da-131">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="7c4da-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="7c4da-132">お気に入りの追加</span><span class="sxs-lookup"><span data-stu-id="7c4da-132">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="7c4da-133">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="7c4da-133">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="7c4da-134">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="7c4da-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="7c4da-135">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="7c4da-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

