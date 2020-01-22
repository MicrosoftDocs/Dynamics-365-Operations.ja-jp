---
title: お気に入りの追加
description: このトピックでは、サイトにお気に入りを追加する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18e12cbe46650fcf024a56b6de9a8cb2903d2bf8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914580"
---
# <a name="add-a-favicon"></a><span data-ttu-id="3deab-103">お気に入りの追加</span><span class="sxs-lookup"><span data-stu-id="3deab-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3deab-104">このトピックでは、サイトにお気に入りを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3deab-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="3deab-105">概要</span><span class="sxs-lookup"><span data-stu-id="3deab-105">Overview</span></span>

<span data-ttu-id="3deab-106">お気に入りは小さなグラフィック ファイルで、Web ブラウザー タブ、アドレス バー、閲覧の履歴、およびブックマークやお気に入りなど、その他の場所内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3deab-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="3deab-107">サイトにお気に入りを追加することをお勧めします。それによりブランドを代表して強化し、顧客が閲覧する他のサイトと区別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3deab-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="3deab-108">サイトにはさまざまなサイズとファイル タイプのお気に入りを追加できますが、このトピックでは、単一のお気に入りを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3deab-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="3deab-109">ただし、同じプロセスと場所を使用して、お気に入りをさらに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3deab-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="3deab-110">サイトのアセット コレクションにお気に入りをアップロードする</span><span class="sxs-lookup"><span data-stu-id="3deab-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="3deab-111">お気に入りをサイトのアセット コレクションにアップロードするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3deab-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="3deab-112">**アセット \> アップロード \> アセットのアップロード**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3deab-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="3deab-113">ローカル ファイル システムでお気に入りを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="3deab-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="3deab-114">タイトルを入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3deab-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="3deab-115">右側のプロパティ ウィンドウで、お気に入りのパブリック URL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="3deab-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="3deab-116">**アップロード後にアセットを公開**オプションを選択しない場合、**アセット** ページに戻り、後でお気に入りを手動で公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3deab-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="3deab-117">お気に入りの HTML を作成する</span><span class="sxs-lookup"><span data-stu-id="3deab-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="3deab-118">お気に入りの HTML を作成するには、次の HTML スニペットを使用します。</span><span class="sxs-lookup"><span data-stu-id="3deab-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="3deab-119">**href** 属性に関しては、**"Public\_URL\_for\_your\_favicon"** を以前にコピーしたパブリック URL に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3deab-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="3deab-120">お気に入りの HTML をページの \<head\> 要素に追加する</span><span class="sxs-lookup"><span data-stu-id="3deab-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="3deab-121">サイトにお気に入りを追加するには、サイト ページの **\<head\>** 要素に任意のタイプの HTML またはスクリプトを追加するのと同じ手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3deab-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3deab-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3deab-122">Additional resources</span></span>

[<span data-ttu-id="3deab-123">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="3deab-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3deab-124">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="3deab-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3deab-125">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="3deab-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3deab-126">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="3deab-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3deab-127">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="3deab-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3deab-128">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="3deab-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3deab-129">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="3deab-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

