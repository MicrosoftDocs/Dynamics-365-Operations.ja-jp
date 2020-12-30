---
title: アカウント管理ページとモジュール
description: このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページおよびモジュールについて説明します。
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413673"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="b6ea0-103">アカウント管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6ea0-104">このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページおよびモジュールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b6ea0-105">概要</span><span class="sxs-lookup"><span data-stu-id="b6ea0-105">Overview</span></span>

<span data-ttu-id="b6ea0-106">アカウント管理とは、Dynamics 365 Commerce のユーザー アカウントに関連する情報を管理するために使用されるページのグループを指します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b6ea0-107">アカウント管理ページには、アカウント管理ランディング ページ、ユーザー プロファイル ページ、ユーザー アドレス ページ、注文履歴ページ、注文詳細ページ、ロイヤルティ ページ、および欲しい物リスト ページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="b6ea0-108">アカウント管理ランディング ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-108">Account management landing page</span></span>

<span data-ttu-id="b6ea0-109">アカウント管理ランディング ページでは、次のモジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="b6ea0-110">**コンテナー** : すべてのアカウント管理ランディング ページのモジュールは、コンテナー内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="b6ea0-111">**アカウント ウェルカム タイル** – このモジュールは、アカウント管理ページでウェルカム メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="b6ea0-112">これには、ヘッダーのプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="b6ea0-113">**アカウント汎用タイル**: このモジュールを使用すると、"注文履歴" ページや "個人プロファイル" ページなど、アカウント管理ページへのヘッダーおよびリンクを提供できます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="b6ea0-114">汎用タイル モジュールを使用して、任意のページのタイルをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="b6ea0-115">Fabrikam では、このモジュールは、アカウント管理ランディングページの "注文履歴" および "マイ プロファイル" ページのリンクに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="b6ea0-116">**アカウント欲しい物リストタイル** – このモジュールは、顧客の欲しい物リストの項目の概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="b6ea0-117">たとえば、"欲しい物リストに 10 の項目があります" と表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="b6ea0-118">ヘッダーのプロパティ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="b6ea0-119">"詳細の表示" リンクは、欲しい物リスト ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="b6ea0-120">**アカウント アドレス タイル** – このモジュールは、ユーザーのアドレスの概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="b6ea0-121">たとえば、"アカウントに追加された 2 つのアドレスがあります" と表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="b6ea0-122">ヘッダーのプロパティ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="b6ea0-123">"詳細の表示" リンクは、ユーザー アドレス ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="b6ea0-124">**アカウント ロイヤルティ タイル** – このモジュールは、ロイヤルティ プログラム情報を表示およびリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="b6ea0-125">このタイルには次の 2 つの状態があります。1 つの状態は、ユーザーが既にメンバーではない場合に、ロイヤルティ プログラムに参加するためのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="b6ea0-126">もう一方の状態は、ユーザーが既にメンバーになっている場合にロイヤルティの詳細ページを表示するためのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="b6ea0-127">プロパティには、ヘッダー、"サインアップ" リンク、および "ロイヤルティの表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="b6ea0-128">"ロイヤルティの表示" リンクは、ロイヤルティ ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="b6ea0-129">"サインアップ" リンクは、ユーザーがロイヤルティ プログラムに参加できるページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="b6ea0-130">注文履歴ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-130">Order history page</span></span>

<span data-ttu-id="b6ea0-131">注文履歴ページでは、注文履歴モジュールを使用して、ユーザーが行った最新のすべての注文を表示します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="b6ea0-132">注文詳細ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-132">Order details page</span></span>

<span data-ttu-id="b6ea0-133">注文詳細ページでは各注文の詳細情報が表示され、注文履歴ページからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="b6ea0-134">このモジュールは注文明細モジュールを使用し、注文の詳細を取得するための販売 ID またはトランザクション ID が必要になります。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="b6ea0-135">ユーザー プロファイル ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-135">User profile page</span></span>

<span data-ttu-id="b6ea0-136">ユーザー プロファイル ページには、ユーザー名や電子メール アドレスなど、ユーザー アカウントの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="b6ea0-137">ユーザー プロファイルの詳細とユーザー プロファイル編集モジュールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="b6ea0-138">電子メール アドレスは削除できませんが、編集はできます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="b6ea0-139">ユーザー プロファイル ページには、ユーザーが推奨リストのパーソナル化など、特定の機能からのオプトインまたはオプトアウトができるようにするユーザー設定も表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="b6ea0-140">ユーザー アドレス ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-140">User address page</span></span>

<span data-ttu-id="b6ea0-141">ユーザー アドレス ページには、ユーザー アカウントに関連付けられているアドレスの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="b6ea0-142">ユーザーが、チェックアウト時にこれらのアドレスを提供したか、またはこのページに直接追加したものです。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="b6ea0-143">ユーザー アドレス モジュールは、アドレスの追加と編集、基本住所の設定、およびページの既存の住所を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="b6ea0-144">欲しい物リスト ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-144">Wish list page</span></span>

<span data-ttu-id="b6ea0-145">欲しい物リスト ページには、顧客の欲しい物リストに追加された項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="b6ea0-146">欲しい物リスト モジュールを使用して、欲しい物リストの項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="b6ea0-147">ロイヤルティ ページ</span><span class="sxs-lookup"><span data-stu-id="b6ea0-147">Loyalty page</span></span>

<span data-ttu-id="b6ea0-148">ロイヤルティ ページでは、顧客が既にはロイヤルティ プログラムのメンバーである場合に、ロイヤルティの詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="b6ea0-149">最近のトランザクションで取得および償還されるポイントを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="b6ea0-150">このページでは、ロイヤルティの詳細モジュールを使用して、ロイヤルティの詳細を紹介しています。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="b6ea0-151">ロイヤルティ プログラムに参加するには、ロイヤルティ サインアップおよびロイヤルティ条件モジュールを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="b6ea0-152">ユーザーがロイヤルティ プログラムのメンバーではない場合、これらのモジュールによって、ユーザーはサインアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6ea0-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6ea0-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b6ea0-153">Additional resources</span></span>

[<span data-ttu-id="b6ea0-154">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="b6ea0-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b6ea0-155">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b6ea0-156">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b6ea0-157">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b6ea0-158">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b6ea0-159">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b6ea0-160">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b6ea0-161">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="b6ea0-161">Footer module</span></span>](author-footer-module.md)
