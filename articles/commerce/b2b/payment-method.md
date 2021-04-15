---
title: B2B eコマース サイト用の顧客アカウントの支払方法の構成
description: このトピックでは、企業間 (B2B) の eコマースサイトに対して顧客勘定の支払方法を構成する方法について説明します。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799808"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="b8488-103">B2B eコマース サイト用の顧客アカウントの支払方法の構成</span><span class="sxs-lookup"><span data-stu-id="b8488-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8488-104">このトピックでは、企業間 (B2B) の eコマースサイトに対して顧客勘定の支払方法を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b8488-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="b8488-105">小売業者は、eコマースチャネルで販売する商品やサービスと引き換えに、様々なタイプの支払いを受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="b8488-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="b8488-106">小売業者が受け入れる各支払タイプは、システムの設定時に Microsoft Dynamics 365 Commerce でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8488-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="b8488-107">B2B e コマース サイトでは、顧客勘定 (または"勘定上") の支払方法がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8488-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b8488-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="b8488-108">Prerequisites</span></span>

1. <span data-ttu-id="b8488-109">Commerce 本部の顧客勘定の支払い方法を追加します。</span><span class="sxs-lookup"><span data-stu-id="b8488-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="b8488-110">顧客勘定の支払方法を eコマースチャネルに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="b8488-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="b8488-111">Commerce 本部の **小売およびコマース \> 顧客 \> すべての顧客\>支払** で顧客に対して **内金を許可** が有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8488-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="b8488-112">また、Commerce 本部の **小売りとコマース \> 顧客 \> すべての顧客 \> 与信および回収** で **クレジットの制限** パラメーターが顧客に対して適切に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b8488-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="b8488-113">Commerce サイトビルダーで顧客勘定の支払い方法を有効にする</span><span class="sxs-lookup"><span data-stu-id="b8488-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="b8488-114">Commerce サイトビルダーで顧客勘定の支払い方法を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8488-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b8488-115">**サイト 設定 \> 拡張機能** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b8488-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="b8488-116">**顧客勘定支払を有効にする** プロパティを **B2B 顧客に対して有効化する** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b8488-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="b8488-117">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b8488-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="b8488-118">新しいサイト設定は、app.settings.json ファイルがが更新された後にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="b8488-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="b8488-119">詳細については、[SDK およびモジュール ライブラリの更新プログラム](../e-commerce-extensibility/sdk-updates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8488-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="b8488-120">B2B e コマース サイトのチェック アウト ページで顧客勘定の支払方法を有効にする</span><span class="sxs-lookup"><span data-stu-id="b8488-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="b8488-121">B2B e コマース サイトのチェック アウト ページで顧客勘定の支払方法を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8488-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="b8488-122">Commerce サイト ビルダで、B2B 電eコマース サイトのチェックアウト モジュールを含むチェック アウト ページまたはチェックアウト ページの特定部分を編集します。</span><span class="sxs-lookup"><span data-stu-id="b8488-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="b8488-123">**チェックアウト セクションのコンテナ** スロットで、**モジュールの追加** を選択 し、**顧客勘定の支払** モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="b8488-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="b8488-124">省略記号 (**...**) を選択して、必要に応じて **上へ移動** または **下へ移動** を選択して、**顧客アカウントの支払い** モジュールを配置します。</span><span class="sxs-lookup"><span data-stu-id="b8488-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="b8488-125">**保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="b8488-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="b8488-126">顧客勘定の支払い方法が有効化されており、公開されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="b8488-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="b8488-127">顧客勘定の支払い方法が有効化されており、公開されていることを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b8488-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="b8488-128">eコマース サイトにサインインします。</span><span class="sxs-lookup"><span data-stu-id="b8488-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="b8488-129">買い物カゴに製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="b8488-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="b8488-130">チェックアウトのページに移動します。</span><span class="sxs-lookup"><span data-stu-id="b8488-130">Go to the checkout page.</span></span> <span data-ttu-id="b8488-131">新しい **顧客勘定** の支払方法が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8488-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8488-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b8488-132">Additional resources</span></span>

[<span data-ttu-id="b8488-133">B2B eコマース サイトの設定</span><span class="sxs-lookup"><span data-stu-id="b8488-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="b8488-134">B2B 組織の組織モデリング階層の作成</span><span class="sxs-lookup"><span data-stu-id="b8488-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="b8488-135">B2B eコマース サイトでのビジネス パートナー ユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="b8488-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="b8488-136">B2B eコマース サイトの製品数量制限の設定</span><span class="sxs-lookup"><span data-stu-id="b8488-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="b8488-137">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="b8488-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]