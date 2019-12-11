---
title: 警告モジュール
description: このトピックでは、警告モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785355"
---
# <a name="alert-module"></a><span data-ttu-id="8e3dd-103">警告モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8e3dd-104">このトピックでは、警告モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8e3dd-105">概要</span><span class="sxs-lookup"><span data-stu-id="8e3dd-105">Overview</span></span>

<span data-ttu-id="8e3dd-106">警告モジュールは、ページにインライン情報メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="8e3dd-107">警告モジュールは、テキストメッセージおよびリンクをサポートします。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="8e3dd-108">電子商取引サイトのすべてのページに表示される、サイト全体のプロモーションを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="8e3dd-109">警告モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="8e3dd-110">電子商取引サイトの警告モジュールの例</span><span class="sxs-lookup"><span data-stu-id="8e3dd-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="8e3dd-111">警告モジュールをサイト ヘッダーで使用して、サイト全体のプロモーションまたはメッセージを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="8e3dd-112">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-112">Here are some examples:</span></span>

<span data-ttu-id="8e3dd-113">"年間販売は残り 10 日間"</span><span class="sxs-lookup"><span data-stu-id="8e3dd-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="8e3dd-114">"新学期割引でお買い得。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-114">"Save big with back to school sale.</span></span> <span data-ttu-id="8e3dd-115">今がチャンス。"</span><span class="sxs-lookup"><span data-stu-id="8e3dd-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="8e3dd-116">警告モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="8e3dd-116">Alert module properties</span></span>

| <span data-ttu-id="8e3dd-117">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="8e3dd-117">Property name</span></span>  | <span data-ttu-id="8e3dd-118">金額</span><span class="sxs-lookup"><span data-stu-id="8e3dd-118">Value</span></span>                              | <span data-ttu-id="8e3dd-119">説明</span><span class="sxs-lookup"><span data-stu-id="8e3dd-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="8e3dd-120">テキスト</span><span class="sxs-lookup"><span data-stu-id="8e3dd-120">Text</span></span>           | <span data-ttu-id="8e3dd-121">テキスト</span><span class="sxs-lookup"><span data-stu-id="8e3dd-121">Text</span></span>                               | <span data-ttu-id="8e3dd-122">警告モジュールに表示されるテキスト メッセージ。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="8e3dd-123">テキスト配置</span><span class="sxs-lookup"><span data-stu-id="8e3dd-123">Text alignment</span></span> | <span data-ttu-id="8e3dd-124">**右**、**左**、または**中央**</span><span class="sxs-lookup"><span data-stu-id="8e3dd-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="8e3dd-125">警告モジュールでテキストをどのように合わせるかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="8e3dd-126">警告を無視</span><span class="sxs-lookup"><span data-stu-id="8e3dd-126">Dismiss alert</span></span>  | <span data-ttu-id="8e3dd-127">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="8e3dd-127">**True** or **False**</span></span>              | <span data-ttu-id="8e3dd-128">値が **True** に設定されている場合、顧客は警告を閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="8e3dd-129">リンク</span><span class="sxs-lookup"><span data-stu-id="8e3dd-129">Link</span></span>           | <span data-ttu-id="8e3dd-130">URL</span><span class="sxs-lookup"><span data-stu-id="8e3dd-130">URL</span></span>                                | <span data-ttu-id="8e3dd-131">オプション リンクの URL</span><span class="sxs-lookup"><span data-stu-id="8e3dd-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="8e3dd-132">警告モジュールをページに追加</span><span class="sxs-lookup"><span data-stu-id="8e3dd-132">Add an alert module to a page</span></span> 

<span data-ttu-id="8e3dd-133">ページに警告モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8e3dd-134">**警告テンプレート**という名前のページ テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="8e3dd-135">既定ページの**メイン** スロットで、警告モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="8e3dd-136">テンプレートをチェックインし、公開します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="8e3dd-137">作成した警告テンプレートを使用して、**警告ページ**という名前のページを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="8e3dd-138">新しいページの**メイン** スロットで、警告モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="8e3dd-139">警告モジュールの設定で、警告テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="8e3dd-140">警告モジュールをさらにカスタマイズする場合は、他のプロパティを編集できます。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="8e3dd-141">ページを保存してプレビューします。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-141">Save and preview the page.</span></span> <span data-ttu-id="8e3dd-142">ページの上部に、追加したテキストを含む警告が表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="8e3dd-143">ページをチェックインしてから公開します。</span><span class="sxs-lookup"><span data-stu-id="8e3dd-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="8e3dd-144">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8e3dd-144">Additional resources</span></span>

[<span data-ttu-id="8e3dd-145">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="8e3dd-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8e3dd-146">カルーセル モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8e3dd-147">コンテンツ リッチ ブロック モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="8e3dd-148">コンテンツ配置モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="8e3dd-149">機能モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="8e3dd-150">ヒーロー モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="8e3dd-151">ビデオ プレーヤー モジュール</span><span class="sxs-lookup"><span data-stu-id="8e3dd-151">Video player module</span></span>](add-video-player.md)
