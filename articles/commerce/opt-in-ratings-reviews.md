---
title: 評価とレビューを使用するためのオプト イン
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプト イン方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eda7fbaeea8d3c1a07f7b43cafe44886d149a211
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027268"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="d9b2a-103">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="d9b2a-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9b2a-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプト イン方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="d9b2a-105">概要</span><span class="sxs-lookup"><span data-stu-id="d9b2a-105">Overview</span></span>

<span data-ttu-id="d9b2a-106">評価およびレビューのソリューションは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Commerce で利用可能にできるオムニチャネル ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d9b2a-107">LCS は、小売業者が環境を準備から使用停止まで管理するために使用する管理ポータルです。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="d9b2a-108">Commerce Web サイトで評価とレビューのソリューションを使用する場合は、Dynamics 365 Commerce で E コマース サイトを展開する際に、評価とレビューをオプトインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="d9b2a-109">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="d9b2a-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="d9b2a-110">サイトで評価およびレビューを使用しオプト インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="d9b2a-111">[新しい E コマース サイトの配置](deploy-ecommerce-site.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="d9b2a-112">まだ LCS を開いている間に、**小売配置の設定 \> その他の設定** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="d9b2a-113">**評価およびレビュー サービスの有効化**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="d9b2a-114">**評価およびレビュー モデレーター (セキュリティ グループ オブジェクト ID) の AAD セキュリティ グループ** フィールドで、評価およびレビュー モデレーターを含む Microsoft Azure Active Directory (Azure AD) セキュリティ グループの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![評価とレビューを使用するためのオプト イン](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="d9b2a-116">E コマース初期化プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="d9b2a-117">既存の Dynamics 365 Commerce の顧客であり、評価とレビューをオプトインせずに E コマース サイトを既に展開していて、Dynamics 365 Commerce パッケージから評価とレビューを使用する場合は、サービス要求を送信してください。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="d9b2a-118">サービス要求を送信する方法については、[サービス要求送信プロセス](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9b2a-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d9b2a-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d9b2a-119">Additional resources</span></span>

[<span data-ttu-id="d9b2a-120">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="d9b2a-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="d9b2a-121">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="d9b2a-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="d9b2a-122">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d9b2a-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="d9b2a-123">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="d9b2a-123">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


