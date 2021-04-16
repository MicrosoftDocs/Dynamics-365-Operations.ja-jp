---
title: 評価とレビューを使用するためのオプト イン
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプトイン方法について説明します。
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9e3f2a17e182c0e3efc8b90380eff74f350c3278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804652"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="b0a80-103">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="b0a80-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b0a80-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプトイン方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b0a80-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="b0a80-105">概要</span><span class="sxs-lookup"><span data-stu-id="b0a80-105">Overview</span></span>

<span data-ttu-id="b0a80-106">評価およびレビューのソリューションは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Commerce で利用可能にできるオムニチャネル ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="b0a80-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b0a80-107">LCS は、小売業者が環境を準備から使用停止まで管理するために使用する管理ポータルです。</span><span class="sxs-lookup"><span data-stu-id="b0a80-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="b0a80-108">Commerce Web サイトで評価とレビューのソリューションを使用する場合は、Dynamics 365 Commerce で E コマース サイトを展開する際に、評価とレビューをオプトインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0a80-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="b0a80-109">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="b0a80-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="b0a80-110">サイトで評価およびレビューを使用しオプト インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b0a80-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="b0a80-111">[新しい E コマース サイトの配置](deploy-ecommerce-site.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b0a80-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="b0a80-112">まだ LCS を開いている間に、**小売配置の設定 \> その他の設定** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b0a80-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="b0a80-113">**評価およびレビュー サービスの有効化** オプションを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b0a80-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="b0a80-114">**評価およびレビュー モデレーター (セキュリティ グループ オブジェクト ID) の AAD セキュリティ グループ** フィールドで、評価およびレビュー モデレーターを含む Microsoft Azure Active Directory (Azure AD) セキュリティ グループの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="b0a80-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![評価とレビューを使用するためのオプト イン](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="b0a80-116">E コマース初期化プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="b0a80-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="b0a80-117">既存の Dynamics 365 Commerce の顧客であり、評価とレビューをオプトインせずに E コマース サイトを既に展開していて、Dynamics 365 Commerce パッケージから評価とレビューを使用する場合は、サービス要求を送信してください。</span><span class="sxs-lookup"><span data-stu-id="b0a80-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="b0a80-118">サービス要求を送信する方法については、[サービス要求送信プロセス](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0a80-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b0a80-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b0a80-119">Additional resources</span></span>

[<span data-ttu-id="b0a80-120">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="b0a80-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="b0a80-121">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="b0a80-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="b0a80-122">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b0a80-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="b0a80-123">Dynamics 365 Commerce の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="b0a80-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]