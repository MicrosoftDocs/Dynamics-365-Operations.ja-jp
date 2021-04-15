---
title: アカウント管理ページとモジュール
description: このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページおよびモジュールについて説明します。
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: df4959a61f1b2948c62a558523a848ff8b2fe0a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796297"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="96350-103">アカウント管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="96350-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96350-104">このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページおよびモジュールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96350-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="96350-105">アカウント管理とは、Dynamics 365 Commerce のユーザー アカウントに関連する情報を管理するために使用されるページのグループを指します。</span><span class="sxs-lookup"><span data-stu-id="96350-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="96350-106">アカウント管理ページには、アカウント管理ランディング ページ、ユーザー プロファイル ページ、ユーザー アドレス ページ、注文履歴ページ、注文詳細ページ、ロイヤルティ ページ、および欲しい物リスト ページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96350-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="96350-107">アカウント管理ランディング ページ</span><span class="sxs-lookup"><span data-stu-id="96350-107">Account management landing page</span></span>

<span data-ttu-id="96350-108">アカウント管理ランディング ページでは、次のモジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="96350-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="96350-109">**コンテナー** : すべてのアカウント管理ランディング ページのモジュールは、コンテナー内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96350-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="96350-110">**アカウント ウェルカム タイル** – このモジュールは、アカウント管理ページでウェルカム メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96350-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="96350-111">これには、ヘッダーのプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96350-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="96350-112">**アカウント汎用タイル**: このモジュールを使用すると、"注文履歴" ページや "個人プロファイル" ページなど、アカウント管理ページへのヘッダーおよびリンクを提供できます。</span><span class="sxs-lookup"><span data-stu-id="96350-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="96350-113">汎用タイル モジュールを使用して、任意のページのタイルをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="96350-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="96350-114">Fabrikam では、このモジュールは、アカウント管理ランディングページの "注文履歴" および "マイ プロファイル" ページのリンクに使用されます。</span><span class="sxs-lookup"><span data-stu-id="96350-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="96350-115">**アカウント欲しい物リストタイル** – このモジュールは、顧客の欲しい物リストの項目の概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96350-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="96350-116">たとえば、"欲しい物リストに 10 の項目があります" と表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="96350-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="96350-117">ヘッダーのプロパティ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96350-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="96350-118">"詳細の表示" リンクは、欲しい物リスト ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96350-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="96350-119">**アカウント アドレス タイル** – このモジュールは、ユーザーのアドレスの概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96350-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="96350-120">たとえば、"アカウントに追加された 2 つのアドレスがあります" と表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="96350-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="96350-121">ヘッダーのプロパティ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96350-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="96350-122">"詳細の表示" リンクは、ユーザー アドレス ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96350-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="96350-123">**アカウント ロイヤルティ タイル** – このモジュールは、ロイヤルティ プログラム情報を表示およびリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96350-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="96350-124">このタイルには次の 2 つの状態があります : 1 つの状態は、ユーザーが既にメンバーではない場合に、ロイヤルティ プログラムに参加するためのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="96350-124">This tile has two states: one state shows links to join a loyalty program if the user is not a member already.</span></span> <span data-ttu-id="96350-125">もう一方の状態は、ユーザーが既にメンバーになっている場合にロイヤルティの詳細ページを表示するためのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="96350-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="96350-126">プロパティには、ヘッダー、"サインアップ" リンク、および "ロイヤルティの表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="96350-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="96350-127">"ロイヤルティの表示" リンクは、ロイヤルティ ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96350-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="96350-128">"サインアップ" リンクは、ユーザーがロイヤルティ プログラムに参加できるページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96350-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="96350-129">注文履歴ページ</span><span class="sxs-lookup"><span data-stu-id="96350-129">Order history page</span></span>

<span data-ttu-id="96350-130">注文履歴ページでは、注文履歴モジュールを使用して、ユーザーが行った最新のすべての注文を表示します。</span><span class="sxs-lookup"><span data-stu-id="96350-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="96350-131">注文詳細ページ</span><span class="sxs-lookup"><span data-stu-id="96350-131">Order details page</span></span>

<span data-ttu-id="96350-132">注文詳細ページでは各注文の詳細情報が表示され、注文履歴ページからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="96350-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="96350-133">このモジュールは注文明細モジュールを使用し、注文の詳細を取得するための販売 ID またはトランザクション ID が必要になります。</span><span class="sxs-lookup"><span data-stu-id="96350-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="my-profile-page"></a><span data-ttu-id="96350-134">プロファイル ページ</span><span class="sxs-lookup"><span data-stu-id="96350-134">My profile page</span></span>

<span data-ttu-id="96350-135">[自分のプロファイル] ページには、アカウント プロファイル モジュールを使用しているユーザーのアカウント プロファイルの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="96350-135">The My profile page shows the user's account profile details using the account profile module.</span></span> <span data-ttu-id="96350-136">このページには、ユーザーのアカウントに関連付けられているメール アドレスと、そのアカウントに設定されている基本設定が表示されます。</span><span class="sxs-lookup"><span data-stu-id="96350-136">The page shows the email address associated with the user's account, as well as preferences set up for the account.</span></span> <span data-ttu-id="96350-137">カスタム顧客属性を設定すると、[追加情報] セクションにもそれらの属性が表示されます。</span><span class="sxs-lookup"><span data-stu-id="96350-137">If setting up custom customer attributes, an "Additional Information" section will also display those attributes.</span></span> <span data-ttu-id="96350-138">ユーザーは、名前、基本設定、追加情報を編集できます (可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="96350-138">Users can edit their name, preferences, or additional information (if available).</span></span>

### <a name="user-address-page"></a><span data-ttu-id="96350-139">ユーザー アドレス ページ</span><span class="sxs-lookup"><span data-stu-id="96350-139">User address page</span></span>

<span data-ttu-id="96350-140">ユーザー アドレス ページには、ユーザー アカウントに関連付けられているアドレスの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="96350-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="96350-141">ユーザーが、チェックアウト時にこれらのアドレスを提供したか、またはこのページに直接追加したものです。</span><span class="sxs-lookup"><span data-stu-id="96350-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="96350-142">ユーザー アドレス モジュールは、アドレスの追加と編集、基本住所の設定、およびページの既存の住所を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96350-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="96350-143">欲しい物リスト ページ</span><span class="sxs-lookup"><span data-stu-id="96350-143">Wish list page</span></span>

<span data-ttu-id="96350-144">欲しい物リスト ページには、顧客の欲しい物リストに追加された項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="96350-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="96350-145">欲しい物リスト モジュールを使用して、欲しい物リストの項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="96350-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="96350-146">ロイヤルティ ページ</span><span class="sxs-lookup"><span data-stu-id="96350-146">Loyalty page</span></span>

<span data-ttu-id="96350-147">ロイヤルティ ページでは、顧客が既にはロイヤルティ プログラムのメンバーである場合に、ロイヤルティの詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="96350-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="96350-148">最近のトランザクションで取得および償還されるポイントを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="96350-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="96350-149">このページでは、ロイヤルティの詳細モジュールを使用して、ロイヤルティの詳細を紹介しています。</span><span class="sxs-lookup"><span data-stu-id="96350-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="96350-150">ロイヤルティ プログラムに参加するには、ロイヤルティ サインアップおよびロイヤルティ条件モジュールを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="96350-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="96350-151">ユーザーがロイヤルティ プログラムのメンバーではない場合、これらのモジュールによって、ユーザーはサインアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="96350-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96350-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="96350-152">Additional resources</span></span>

[<span data-ttu-id="96350-153">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="96350-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="96350-154">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="96350-155">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="96350-156">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="96350-157">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="96350-158">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="96350-159">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="96350-160">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="96350-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]