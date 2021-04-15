---
title: ようこそメッセージの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797386"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="61471-103">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="61471-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61471-104">このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="61471-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="61471-105">E コマース Web サイトのようこそメッセージは、訪問者に実施中のセール、サイトの更新、または季節のコレクションが利用可能であることについて知らせることができます。</span><span class="sxs-lookup"><span data-stu-id="61471-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="61471-106">ようこそメッセージは、警告モジュールを使用して設定されます。</span><span class="sxs-lookup"><span data-stu-id="61471-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="61471-107">警告モジュールをヘッダー フラグメントの **エラー/情報メッセージ** スロットに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61471-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="61471-108">警告モジュールを使用すると、表示されるテキスト、テキストの色、および配置を指定できます。</span><span class="sxs-lookup"><span data-stu-id="61471-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="61471-109">また、サイトの訪問者がメッセージを閉じることができるかどうかを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="61471-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="61471-110">共有ヘッダー フラグメントに追加されたようこそメッセージは、共有ヘッダー フラグメントが使用されているテンプレートを使用するすべてのページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="61471-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="61471-111">サイトにようこそメッセージを追加するには、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="61471-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="61471-112">Commerce サイト ビルダーで、ご利用のサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="61471-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="61471-113">**フラグメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61471-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="61471-114">メッセージを追加するヘッダー フラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="61471-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="61471-115">アウトライン ツリーで、**エラー/情報メッセージ** を展開します。</span><span class="sxs-lookup"><span data-stu-id="61471-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="61471-116">警告モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61471-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="61471-117">警告モジュールがまだ存在しない場合は、まず **エラー/情報メッセージ** の隣にある省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61471-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="61471-118">右側のプロパティ ウィンドウの **データ** タブで、**データ ソースの追加** を選択し、**コンテンツ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="61471-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="61471-119">**入力テキスト** フィールドに、ようこそメッセージのテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="61471-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="61471-120">**保存** を選択し、 **編集の完了** を選択してヘッダー フラグメントにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="61471-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="61471-121">これで、選択したヘッダー フラグメントを使用するすべてのサイト ページの上部にようこそメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="61471-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61471-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="61471-122">Additional resources</span></span>

[<span data-ttu-id="61471-123">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="61471-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="61471-124">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="61471-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="61471-125">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="61471-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="61471-126">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="61471-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="61471-127">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="61471-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="61471-128">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="61471-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="61471-129">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="61471-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
