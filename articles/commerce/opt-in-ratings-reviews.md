---
title: 評価とレビューを使用するためのオプト イン
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプト イン方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697983"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="e8401-103">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="e8401-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e8401-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプト イン方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8401-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="e8401-105">概要</span><span class="sxs-lookup"><span data-stu-id="e8401-105">Overview</span></span>

<span data-ttu-id="e8401-106">評価およびレビューのソリューションは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Commerce で利用可能にできる オムニチャネル ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="e8401-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e8401-107">LCS は、小売業者が環境を準備から使用停止まで管理するために使用する管理ポータルです。</span><span class="sxs-lookup"><span data-stu-id="e8401-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="e8401-108">評価を使用し、E コマース Web サイトのソリューションをレビューする場合は、最初にオプト インをクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8401-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="e8401-109">評価とレビューを使用するためのオプト イン</span><span class="sxs-lookup"><span data-stu-id="e8401-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="e8401-110">サイトで評価およびレビューを使用しオプト インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e8401-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="e8401-111">[新しい E コマース サイトの配置](deploy-ecommerce-site.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="e8401-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="e8401-112">まだ LCS を開いている間に、**小売配置の設定 \> その他の設定** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8401-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="e8401-113">**評価およびレビュー サービスの有効化**オプションを、**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="e8401-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="e8401-114">**評価およびレビュー モデレーター (セキュリティ グループ オブジェクト ID) の AAD セキュリティ グループ** フィールドで、評価およびレビュー モデレーターを含む Microsoft Azure Active Directory (Azure AD) セキュリティ グループの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="e8401-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![評価とレビューを使用するためのオプト イン](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="e8401-116">E コマース初期化プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="e8401-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8401-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e8401-117">Additional resources</span></span>

[<span data-ttu-id="e8401-118">評価とレビューの概要</span><span class="sxs-lookup"><span data-stu-id="e8401-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="e8401-119">評価とレビューの管理</span><span class="sxs-lookup"><span data-stu-id="e8401-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="e8401-120">評価とレビューのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e8401-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="e8401-121">Dynamics 365 Retail の商品評価の同期</span><span class="sxs-lookup"><span data-stu-id="e8401-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
