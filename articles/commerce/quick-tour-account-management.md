---
title: アカウント管理ページの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページの概要を示します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cd4ee3ef2b1c3538ec267fe12eef38d525f6a83
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244817"
---
# <a name="account-management-pages-overview"></a><span data-ttu-id="33034-103">アカウント管理ページの概要</span><span class="sxs-lookup"><span data-stu-id="33034-103">Account management pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33034-104">このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="33034-104">This topic provides an overview of account management pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="33034-105">概要</span><span class="sxs-lookup"><span data-stu-id="33034-105">Overview</span></span>

<span data-ttu-id="33034-106">アカウント管理ページにより、顧客は自分のアカウントおよび注文に関連する情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="33034-106">Account management pages let customers view information that is related to their account and orders.</span></span> <span data-ttu-id="33034-107">アカウント管理ページには、アカウント管理ランディング ページと、ユーザー プロファイル、住所、注文履歴、注文詳細、ロイヤルティ ポイント、および欲しい物リストのページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="33034-107">Account management pages include the account management landing page, and pages for the user's profile, addresses, order history, order details, loyalty points, and wish list.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="33034-108">アカウント管理ランディング ページ</span><span class="sxs-lookup"><span data-stu-id="33034-108">Account management landing page</span></span>

<span data-ttu-id="33034-109">顧客がサインインして **マイ アカウント** を選択すると、アカウント管理のランディングページが開きます。</span><span class="sxs-lookup"><span data-stu-id="33034-109">When a customer signs in and selects **My Account**, the account management landing page is opened.</span></span> <span data-ttu-id="33034-110">このページでは、ユーザー プロファイル、注文、欲しい物リスト、住所、ロイヤルティ ポイントなど、アカウントに関連するすべての情報の簡単な概要を示します。</span><span class="sxs-lookup"><span data-stu-id="33034-110">This page provides a quick summary of all account-related information, such as the user's profile, orders, wish list, addresses, loyalty points.</span></span> <span data-ttu-id="33034-111">このページから、顧客は各区分の詳細にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="33034-111">From this page, the customer can access more details for each area.</span></span>

<span data-ttu-id="33034-112">次の図は、アカウント管理ランディング ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="33034-112">The following illustration shows an example of the account management landing page.</span></span>

![アカウント管理ランディング ページの例](./media/Account-Management.PNG)

### <a name="my-profile-page"></a><span data-ttu-id="33034-114">プロファイル ページ</span><span class="sxs-lookup"><span data-stu-id="33034-114">My profile page</span></span>

<span data-ttu-id="33034-115">**マイ プロファイル** ページには、名前および電話番号など、顧客のアカウント情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33034-115">The **My profile** page shows customer's account information, such as his or her name and phone number.</span></span> <span data-ttu-id="33034-116">顧客は、このページでプロファイル情報を更新できます。</span><span class="sxs-lookup"><span data-stu-id="33034-116">The customer can update his or her profile information on this page.</span></span> <span data-ttu-id="33034-117">このページをカスタマイズして、マーケティング メールにオプトインするオプションなど、顧客アカウントに関する追加設定を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="33034-117">This page can be customized so that it includes additional customer account preferences, such as an option for opting in to marketing email.</span></span>

<span data-ttu-id="33034-118">以下の図は、モジュール ライブラリを使用してビルドされた **プロファイル** ページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="33034-118">The following illustration shows an example of a **My profile** page that was built by using the module library.</span></span>

![マイ プロファイル ページの例](./media/Account-Management-MyProfile.PNG)

### <a name="addresses-page"></a><span data-ttu-id="33034-120">住所のページ</span><span class="sxs-lookup"><span data-stu-id="33034-120">Addresses page</span></span>

<span data-ttu-id="33034-121">**住所** のページにより、顧客は自分のアカウントに住所を追加できます。</span><span class="sxs-lookup"><span data-stu-id="33034-121">The **Addresses** page lets the customer add addresses to his or her account.</span></span> <span data-ttu-id="33034-122">また、顧客が以前にアカウントに追加または保存した住所のリストも表示します。</span><span class="sxs-lookup"><span data-stu-id="33034-122">It also shows the list of addresses that the customer has previously added or saved to the account.</span></span> <span data-ttu-id="33034-123">これらの住所は、顧客がこのページで入力、または注文の間に入力した住所です。</span><span class="sxs-lookup"><span data-stu-id="33034-123">These addresses are addresses that the customer entered either on this page or while placing an order.</span></span>

<span data-ttu-id="33034-124">次の図は、**住所** ページの例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="33034-124">The following illustration shows an example of the **Addresses** page.</span></span>

![住所ページの例](./media/Account-Management-Address.png)

### <a name="order-history-and-order-details-pages"></a><span data-ttu-id="33034-126">注文履歴および注文詳細のページ</span><span class="sxs-lookup"><span data-stu-id="33034-126">Order history and Order details pages</span></span>

<span data-ttu-id="33034-127">**注文履歴** ページには、顧客が自分のアカウントを使用して送信したすべての注文の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33034-127">The **Order history** page shows a summary of all orders that the customer has submitted by using his or her account.</span></span> <span data-ttu-id="33034-128">注文された品目の簡単な概要、確認番号、販売 ID、追跡情報、および他の情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="33034-128">It gives a quick summary of the items that were ordered, the confirmation number, sales ID, tracking information, and other information.</span></span> <span data-ttu-id="33034-129">顧客が各注文の詳細な内訳を表示したい場合、**注文の詳細** ページがあります。</span><span class="sxs-lookup"><span data-stu-id="33034-129">If the customer wants to view a more detailed breakdown of each order, there is an **Order details** page.</span></span> <span data-ttu-id="33034-130">このページには、注文の出荷先住所、支払情報、割引、税、および出荷コストなどの情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="33034-130">This page includes information such as the shipping address, payment information, discounts, taxes, and shipping costs for the order.</span></span>

<span data-ttu-id="33034-131">次の図は、**注文履歴** ページの例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="33034-131">The following illustration shows an example of the **Order history** page.</span></span>

![注文履歴ページの例](./media/Account-Management-OrderHistory.PNG)

<span data-ttu-id="33034-133">次の図は、**注文の詳細** ページの例を表示しています。</span><span class="sxs-lookup"><span data-stu-id="33034-133">The following illustration shows an example of the **Order details** page.</span></span>

![注文の詳細ページの例](./media/Account-Management-OrderDetails.PNG)

### <a name="loyalty-program-page"></a><span data-ttu-id="33034-135">ロイヤルティ プログラムのページ</span><span class="sxs-lookup"><span data-stu-id="33034-135">Loyalty program page</span></span>

<span data-ttu-id="33034-136">**ロイヤルティ プログラム** のページにより、顧客はロイヤルティ プログラムのメンバーになります。</span><span class="sxs-lookup"><span data-stu-id="33034-136">The **Loyalty program** page lets the customer become a member of a loyalty program.</span></span> <span data-ttu-id="33034-137">顧客がロイヤルティ プログラムにサインアップした後、**ロイヤルティ プログラム** のページには、取得したポイント数および引き換えたポイント数などの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33034-137">After a customer has signed up for a loyalty program, the **Loyalty program** page include details such as the number of points that have been earned and the number of points that have been redeemed.</span></span>

<span data-ttu-id="33034-138">次の図は、**ロイヤルティ プログラム** のページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="33034-138">The following illustration shows an example of a **Loyalty program** page.</span></span>

![ロイヤルティ プログラムのページの例](./media/Account-Management-Loyalty.PNG)

### <a name="wishlist-page"></a><span data-ttu-id="33034-140">ホワイトリスト ページ</span><span class="sxs-lookup"><span data-stu-id="33034-140">Wishlist page</span></span>

<span data-ttu-id="33034-141">**欲しいものリスト** のページには、顧客が自分の欲しい物リストに追加した品目のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33034-141">The **Wishlist** page shows a list of the items that the customer has added to his or her wish list.</span></span> <span data-ttu-id="33034-142">製品および製品バリアントの両方を欲しい物リストに追加できます。</span><span class="sxs-lookup"><span data-stu-id="33034-142">Both products and product variants can be added to the wish list.</span></span> <span data-ttu-id="33034-143">このページから、顧客は欲しい物リストから品目を削除したり、また買い物カゴに品目を直接追加したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="33034-143">From this page, the customer can remove an item from the wish list or add an item directly to the cart.</span></span>

<span data-ttu-id="33034-144">次の図は、**欲しい物リスト** のページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="33034-144">The following illustration shows an example of a **Wishlist** page.</span></span>

![欲しい物リストのページの例](./media/Account-Management-Wishlist.PNG)

<span data-ttu-id="33034-146">アカウント管理モジュールおよびその作成方法の詳細については、[アカウント管理](account-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33034-146">For more information about account management modules and how to author them, see [Account Management](account-management.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33034-147">追加リソース</span><span class="sxs-lookup"><span data-stu-id="33034-147">Additional resources</span></span>

[<span data-ttu-id="33034-148">ホーム ページの概要</span><span class="sxs-lookup"><span data-stu-id="33034-148">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="33034-149">製品詳細ページの概要</span><span class="sxs-lookup"><span data-stu-id="33034-149">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="33034-150">買い物カゴとチェックアウト ページの概要</span><span class="sxs-lookup"><span data-stu-id="33034-150">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]