---
title: テストまたは開発中の店舗へのアクセスを制限する
description: このトピックでは、内部のテストまたは開発を行っている間に Microsoft Dynamics 365 Commerce の店舗へのアクセスを制限する方法について説明します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585415"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="46bfc-103">テストまたは開発中の店舗へのアクセスを制限する</span><span class="sxs-lookup"><span data-stu-id="46bfc-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46bfc-104">このトピックでは、内部のテストまたは開発を行っている間に Microsoft Dynamics 365 Commerce の店舗へのアクセスを制限する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="46bfc-105">説明</span><span class="sxs-lookup"><span data-stu-id="46bfc-105">Description</span></span>

<span data-ttu-id="46bfc-106">内部のテストや現在開発中の間は、外部ユーザーが公開された店舗ページにアクセスできないように、サイトへのアクセスを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="46bfc-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="46bfc-107">解像度</span><span class="sxs-lookup"><span data-stu-id="46bfc-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="46bfc-108">標準のユーザー フローを使用して Azure AD B2C を設定する</span><span class="sxs-lookup"><span data-stu-id="46bfc-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="46bfc-109">eコマース サイトの Azure Active Directory B2C (Azure AD B2C) を構成する方法の詳細については、[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="46bfc-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="46bfc-110">店舗ページへのユーザー アクセスを制限して新しいユーザーの作成をブロックする</span><span class="sxs-lookup"><span data-stu-id="46bfc-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="46bfc-111">Commerce サイト ビルダーで店舗ページへのユーザー アクセスを制限するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="46bfc-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="46bfc-112">サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-112">Go to your site.</span></span>
1. <span data-ttu-id="46bfc-113">**ページ** を選択し、ユーザー アクセスを制限するページを選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="46bfc-114">モジュールまたはフラグメント スロットを選択して、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="46bfc-115">プロパティ ウィンドウで、**サインインが必要?** を選択して、**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="46bfc-116">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-116">Select **Publish**.</span></span>

<span data-ttu-id="46bfc-117">Azure AD の新しいユーザーの作成をブロックするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="46bfc-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="46bfc-118">[Azure ポータル](https://portal.azure.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="46bfc-119">サイト アクセス用に作成した Azure AD B2C アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="46bfc-120">左のナビゲーション ウィンドウで、**ユーザー フロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="46bfc-121">**ユーザー フロー** ページの上部で、**新しいユーザー フロー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="46bfc-122">**ユーザー フロー タイプの選択** ページで、**プレビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="46bfc-123">ページの中程で、**v2 にサインイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="46bfc-124">次に、[Commerce での B2C テナントの設定](../set-up-b2c-tenant.md) の手順に従って、テストまたは開発中に Azure AD B2C のサイトの標準ユーザー フローとしてフローを構成します。</span><span class="sxs-lookup"><span data-stu-id="46bfc-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46bfc-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="46bfc-125">Additional resources</span></span>

[<span data-ttu-id="46bfc-126">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="46bfc-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="46bfc-127">ユーザーのサインインに対するカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="46bfc-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
