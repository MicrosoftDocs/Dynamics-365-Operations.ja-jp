---
title: 著作権に関する注意事項の追加
description: このトピックでは、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206370"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="6ad4d-103">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="6ad4d-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ad4d-104">このトピックでは、E コマース Web サイトに著作権に関する注意事項を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6ad4d-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="6ad4d-105">Prerequisites</span></span>

<span data-ttu-id="6ad4d-106">サイトに著作権に関する注意事項を追加する前に、次の項目が必要です。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="6ad4d-107">共有フッター フラグメントを含むテンプレート。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="6ad4d-108">そのテンプレートを使用するページ。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="6ad4d-109">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="6ad4d-109">Add a copyright notice</span></span>

<span data-ttu-id="6ad4d-110">特定のテンプレートを使用する各ページの下に著作権に関する注意事項を追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="6ad4d-111">**フラグメント** に移動し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="6ad4d-112">**新規フラグメント** ダイアログ ボックスで、**フッター** モジュールを選択し、フラグメントに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="6ad4d-113">たとえば、**フッター 著作権** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="6ad4d-114">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-114">Select **OK**.</span></span>
1. <span data-ttu-id="6ad4d-115">ナビゲーション ウィンドウで、**フッター** の横にある省略記号ボタン (**...**) を選択してから、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ad4d-116">ダイアログ ボックスで、**フッター カテゴリ** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad4d-117">ナビゲーション ウィンドウで、**フッター カテゴリ** の横にある省略記号ボタンを選択してから、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ad4d-118">ダイアログ ボックスで、**テキスト ブロック** を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad4d-119">左のナビゲーション ウィンドウで、**テキスト ブロック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="6ad4d-120">右側のプロパティ ウィンドウの、**段落** フィールドで、著作権に関するメッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="6ad4d-121">たとえば、**(C) Fabrikam 2019** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="6ad4d-122">**保存** を選択し、**編集を終了する** を選択し、続いて **公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="6ad4d-123">**テンプレート** に移動し、テンプレートを選択してから、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="6ad4d-124">**ページ アウトライン** で、**本文** を展開してから、**既定のページ** を展開します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="6ad4d-125">**フッター スロット** の横にある省略記号ボタンを選択し、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="6ad4d-126">前に作成したフラグメントを選択し、**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="6ad4d-127">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="6ad4d-128">著作権に関する注意事項を含むフッターは、選択したテンプレートを使用するすべてのページの下部に自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ad4d-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ad4d-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6ad4d-129">Additional resources</span></span>

[<span data-ttu-id="6ad4d-130">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="6ad4d-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="6ad4d-131">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="6ad4d-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="6ad4d-132">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="6ad4d-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="6ad4d-133">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="6ad4d-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="6ad4d-134">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="6ad4d-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="6ad4d-135">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="6ad4d-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="6ad4d-136">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="6ad4d-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]