---
title: ようこそメッセージの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。
author: psimolin
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d17ad7cfd6f11e84fdd1c8ebccca6f786b83c62d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209158"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="0b3a5-103">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="0b3a5-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0b3a5-104">このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="0b3a5-105">概要</span><span class="sxs-lookup"><span data-stu-id="0b3a5-105">Overview</span></span>

<span data-ttu-id="0b3a5-106">E コマース Web サイトのようこそメッセージは、訪問者に実施中のセール、サイトの更新、または季節のコレクションが利用可能であることについて知らせることができます。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="0b3a5-107">ようこそメッセージは、警告モジュールを使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="0b3a5-108">警告モジュールをヘッダー フラグメントの **エラー/情報メッセージ** スロットに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="0b3a5-109">警告モジュールを使用すると、表示されるテキスト、テキストの色、および配置を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="0b3a5-110">また、サイトの訪問者がメッセージを閉じることができるかどうかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="0b3a5-111">共有ヘッダー フラグメントに追加されたようこそメッセージは、共有ヘッダー フラグメントが使用されているテンプレートを使用するすべてのページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="0b3a5-112">サイトにようこそメッセージを追加するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="0b3a5-113">Commerce サイト ビルダーで、ご利用のサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="0b3a5-114">**フラグメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="0b3a5-115">メッセージを追加するヘッダー フラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="0b3a5-116">アウトライン ツリーで、**エラー/情報メッセージ** を展開します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="0b3a5-117">警告モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="0b3a5-118">警告モジュールがまだ存在しない場合は、まず **エラー/情報メッセージ** の隣にある省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="0b3a5-119">右側のプロパティ ウィンドウの **データ** タブで、**データ ソースの追加** を選択し、**コンテンツ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="0b3a5-120">**入力テキスト** フィールドに、ようこそメッセージのテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="0b3a5-121">**保存** を選択し、 **編集の完了** を選択してヘッダー フラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="0b3a5-122">これで、選択したヘッダー フラグメントを使用するすべてのサイト ページの上部にようこそメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b3a5-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b3a5-123">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0b3a5-123">Additional resources</span></span>

[<span data-ttu-id="0b3a5-124">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="0b3a5-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0b3a5-125">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="0b3a5-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0b3a5-126">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="0b3a5-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0b3a5-127">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="0b3a5-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0b3a5-128">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="0b3a5-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0b3a5-129">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="0b3a5-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0b3a5-130">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="0b3a5-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]