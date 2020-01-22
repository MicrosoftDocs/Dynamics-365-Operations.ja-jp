---
title: ようこそメッセージの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914519"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="f7e71-103">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="f7e71-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f7e71-104">このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="f7e71-105">概要</span><span class="sxs-lookup"><span data-stu-id="f7e71-105">Overview</span></span>

<span data-ttu-id="f7e71-106">E コマース Web サイトのようこそメッセージは、訪問者に実施中のセール、サイトの更新、または季節のコレクションが利用可能であることについて知らせることができます。</span><span class="sxs-lookup"><span data-stu-id="f7e71-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="f7e71-107">ようこそメッセージは、警告モジュールを使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="f7e71-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="f7e71-108">警告モジュールをヘッダー フラグメントの**エラー/情報メッセージ** スロットに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e71-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="f7e71-109">警告モジュールを使用すると、表示されるテキスト、テキストの色、および配置を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7e71-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="f7e71-110">また、サイトの訪問者がメッセージを閉じることができるかどうかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f7e71-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="f7e71-111">共有ヘッダー フラグメントに追加されたようこそメッセージは、共有ヘッダー フラグメントが使用されているテンプレートを使用するすべてのページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7e71-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="f7e71-112">サイトにようこそメッセージを追加するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="f7e71-113">Dynamics 365 Commerce で、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="f7e71-114">**フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="f7e71-115">メッセージを追加するヘッダー フラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="f7e71-116">アウトライン ツリーで、**エラー/情報メッセージ**を展開します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="f7e71-117">警告モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-117">Select the alert module.</span></span>

    <span data-ttu-id="f7e71-118">警告モジュールがまだ存在しない場合は、**エラー/情報メッセージ**の隣にある省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="f7e71-119">警告モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="f7e71-120">右側のプロパティ ウィンドウの**データ** タブで、**データ ソースの追加**を選択し、**コンテンツ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="f7e71-121">**入力テキスト** フィールドに、ようこそメッセージのテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="f7e71-122">ヘッダー フラグメントを保存し、チェック イン後に公開します。</span><span class="sxs-lookup"><span data-stu-id="f7e71-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="f7e71-123">これで、選択したヘッダー フラグメントを使用するすべてのサイト ページの上部にようこそメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7e71-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7e71-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f7e71-124">Additional resources</span></span>

[<span data-ttu-id="f7e71-125">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="f7e71-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f7e71-126">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="f7e71-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f7e71-127">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="f7e71-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="f7e71-128">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="f7e71-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f7e71-129">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="f7e71-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f7e71-130">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="f7e71-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f7e71-131">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="f7e71-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

