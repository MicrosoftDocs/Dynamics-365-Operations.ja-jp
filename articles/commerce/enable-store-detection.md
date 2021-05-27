---
title: 場所に基づく店舗検出の有効化
description: このトピックでは、Dynamics 365 Commerce サイトの場所に基づく店舗検出を有効にする方法について説明します。
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e26c3130914ebef5a63b79c477d7d5846fd5b71
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027603"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="aeda9-103">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="aeda9-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aeda9-104">このトピックでは、Dynamics 365 Commerce サイトの場所に基づく店舗検出を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="aeda9-105">コマースでの場所に基づく店舗検出により、場所に基づいて、関連するサイト コンテンツを顧客に提供することができます。</span><span class="sxs-lookup"><span data-stu-id="aeda9-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="aeda9-106">場所に基づく店舗検出が有効になっている場合、コマースのレンダリング サービスは、顧客の Web ブラウザー IP アドレスの国/地域の情報を使用して、使用可能で最適な地理的サイト構成に顧客を誘導します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="aeda9-107">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="aeda9-107">Privacy notice</span></span>

<span data-ttu-id="aeda9-108">場所に基づく店舗検出機能を有効にすると、顧客のブラウザーからの情報が Microsoft location 位置情報サービスに送信されます。</span><span class="sxs-lookup"><span data-stu-id="aeda9-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="aeda9-109">その後、この情報を使用して、その顧客の場所に関連するコンテンツを顧客に提供します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-109">This information is then used to provide the customer content that is relevant to the customer's location.</span></span> <span data-ttu-id="aeda9-110">顧客のブラウザーから送信される情報と、顧客に返される場所に基づく情報の両方が、プライバシー ポリシーと Cookie コンプライアンス ポリシーの対象となります。</span><span class="sxs-lookup"><span data-stu-id="aeda9-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="aeda9-111">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="aeda9-111">Turn on location-based store detection</span></span>

<span data-ttu-id="aeda9-112">コマースで場所に基づく店舗検出を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="aeda9-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="aeda9-113">オーサリング ツールで、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="aeda9-114">左のナビゲーション ウィンドウで、**サイト管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="aeda9-115">**サイトの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="aeda9-116">**場所に基づく店舗検出を有効にする** のオプションを **オン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="aeda9-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aeda9-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="aeda9-117">Additional resources</span></span>

[<span data-ttu-id="aeda9-118">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="aeda9-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="aeda9-119">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="aeda9-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="aeda9-120">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="aeda9-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="aeda9-121">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="aeda9-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="aeda9-122">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="aeda9-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="aeda9-123">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="aeda9-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="aeda9-124">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="aeda9-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="aeda9-125">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="aeda9-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="aeda9-126">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="aeda9-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="aeda9-127">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="aeda9-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
