---
title: 場所に基づく店舗検出の有効化
description: このトピックでは、Dynamics 365 Commerce サイトの場所に基づく店舗検出を有効にする方法について説明します。
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003099"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="e6bfd-103">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="e6bfd-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e6bfd-104">このトピックでは、Dynamics 365 Commerce サイトの場所に基づく店舗検出を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="e6bfd-105">概要</span><span class="sxs-lookup"><span data-stu-id="e6bfd-105">Overview</span></span>

<span data-ttu-id="e6bfd-106">コマースでの場所に基づく店舗検出により、場所に基づいて、関連するサイト コンテンツを顧客に提供することができます。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="e6bfd-107">場所に基づく店舗検出が有効になっている場合、コマースのレンダリング サービスは、顧客の Web ブラウザー IP アドレスの国/地域の情報を使用して、使用可能で最適な地理的サイト構成に顧客を誘導します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e6bfd-108">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="e6bfd-108">Privacy notice</span></span>

<span data-ttu-id="e6bfd-109">場所に基づく店舗検出機能を有効にすると、顧客のブラウザーからの情報が Microsoft location 位置情報サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="e6bfd-110">その後、この情報を使用して、その場所に関連するコンテンツを顧客に提供します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="e6bfd-111">顧客のブラウザーから送信される情報と、顧客に返される場所に基づく情報の両方が、プライバシー ポリシーと Cookie コンプライアンス ポリシーの対象となります。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="e6bfd-112">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="e6bfd-112">Turn on location-based store detection</span></span>

<span data-ttu-id="e6bfd-113">コマースで場所に基づく店舗検出を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e6bfd-114">オーサリング ツールで、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="e6bfd-115">左のナビゲーション ウィンドウで、**サイト管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="e6bfd-116">**サイトの設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="e6bfd-117">**場所に基づく店舗検出を有効にする**のオプションを**オン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e6bfd-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6bfd-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e6bfd-118">Additional resources</span></span>

[<span data-ttu-id="e6bfd-119">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e6bfd-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e6bfd-120">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="e6bfd-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e6bfd-121">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="e6bfd-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e6bfd-122">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="e6bfd-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e6bfd-123">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="e6bfd-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e6bfd-124">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="e6bfd-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e6bfd-125">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="e6bfd-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
