---
title: アカウント管理ページとモジュール
description: このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページおよびモジュールについて説明します。
author: v-chgri
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885812"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="7993a-103">アカウント管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="7993a-104">このトピックでは、Microsoft Dynamics 365 Commerce のアカウント管理ページおよびモジュールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7993a-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7993a-105">概要</span><span class="sxs-lookup"><span data-stu-id="7993a-105">Overview</span></span>

<span data-ttu-id="7993a-106">アカウント管理とは、Dynamics 365 Commerce のユーザー アカウントに関連する情報を管理するために使用されるページのグループを指します。</span><span class="sxs-lookup"><span data-stu-id="7993a-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="7993a-107">アカウント管理ページには、アカウント管理ランディング ページ、ユーザー プロファイル ページ、ユーザー アドレス ページ、注文履歴ページ、注文詳細ページ、ロイヤルティ ページ、および欲しい物リスト ページが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="7993a-108">アカウント管理ランディング ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-108">Account management landing page</span></span>

<span data-ttu-id="7993a-109">アカウント管理ランディング ページでは、次のモジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="7993a-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="7993a-110">**コンテンツ配置** – このモジュールは、アカウント管理ランディング ページにあるすべてのモジュールを保持するコンテナー モジュールです。</span><span class="sxs-lookup"><span data-stu-id="7993a-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="7993a-111">**アカウント ウェルカム項目** – このモジュールは、アカウント管理ページでウェルカム メッセージを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="7993a-112">ヘッダーのプロパティとタイル サイズが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="7993a-113">**タイル サイズ** プロパティは、コンテンツ配置モジュール内のモジュールの幅を定義します。</span><span class="sxs-lookup"><span data-stu-id="7993a-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="7993a-114">値の範囲は **1** から **12**で、**12** はコンテンツ配置コンテナーの全幅を表します。</span><span class="sxs-lookup"><span data-stu-id="7993a-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="7993a-115">**アカウント注文配置項目** – このモジュールは、ユーザー アカウントによって行われた注文数の集計を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="7993a-116">ヘッダーのプロパティ、タイル サイズ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7993a-117">"詳細の表示" リンクは、注文履歴ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="7993a-118">**アカウント プロファイル配置項目** – このモジュールは、ユーザー プロファイルの概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="7993a-119">ヘッダーのプロパティ、タイル サイズ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7993a-120">"詳細の表示" リンクは、ユーザー プロファイル ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="7993a-121">**アカウント欲しい物リスト項目** – このモジュールは、顧客の欲しい物リストの項目の概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="7993a-122">たとえば、"欲しい物リストに 10 の項目があります" と表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="7993a-123">ヘッダーのプロパティ、タイル サイズ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7993a-124">"詳細の表示" リンクは、欲しい物リスト ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="7993a-125">**アカウント アドレス項目** – このモジュールは、ユーザーのアドレスの概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="7993a-126">たとえば、"アカウントに追加された 2 つのアドレスがあります" と表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="7993a-127">ヘッダーのプロパティ、タイル サイズ、および "詳細の表示" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="7993a-128">"詳細の表示" リンクは、ユーザー アドレス ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="7993a-129">**アカウント ロイヤルティ項目** – このモジュールは、ロイヤルティ プログラム情報を表示およびリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="7993a-130">ヘッダーのプロパティ、タイル サイズ、"詳細の表示" リンク、および "メンバーになる" リンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7993a-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="7993a-131">"詳細の表示" リンクは、ロイヤルティ ページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="7993a-132">"メンバーになる" リンクは、ユーザーがロイヤルティ プログラムに参加できるページにリダイレクトするようコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7993a-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="7993a-133">注文履歴ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-133">Order history page</span></span>

<span data-ttu-id="7993a-134">注文履歴ページでは、注文履歴モジュールを使用して、ユーザーが行った最新のすべての注文を表示します。</span><span class="sxs-lookup"><span data-stu-id="7993a-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="7993a-135">注文詳細ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-135">Order details page</span></span>

<span data-ttu-id="7993a-136">注文詳細ページでは各注文の詳細情報が表示され、注文履歴ページからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7993a-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="7993a-137">このモジュールは注文明細モジュールを使用し、注文の詳細を取得するための販売 ID またはトランザクション ID が必要になります。</span><span class="sxs-lookup"><span data-stu-id="7993a-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="7993a-138">ユーザー プロファイル ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-138">User profile page</span></span>

<span data-ttu-id="7993a-139">ユーザー プロファイル ページには、ユーザー名や電子メール アドレスなど、ユーザー アカウントの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-139">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="7993a-140">ユーザー プロファイル モジュールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-140">It uses the user profile module.</span></span> <span data-ttu-id="7993a-141">電子メール アドレスは削除できませんが、編集はできます。</span><span class="sxs-lookup"><span data-stu-id="7993a-141">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="7993a-142">ユーザー プロファイル ページには、ユーザーが推奨リストのパーソナル化など、特定の機能からのオプトインまたはオプトアウトができるようにするユーザー設定も表示されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-142">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="7993a-143">ユーザー アドレス ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-143">User address page</span></span>

<span data-ttu-id="7993a-144">ユーザー アドレス ページには、ユーザー アカウントに関連付けられているアドレスの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-144">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="7993a-145">ユーザーが、チェックアウト時にこれらのアドレスを提供したか、またはこのページに直接追加したものです。</span><span class="sxs-lookup"><span data-stu-id="7993a-145">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="7993a-146">ユーザー アドレス モジュールは、アドレスの追加と編集、基本住所の設定、およびページの既存の住所を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-146">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="7993a-147">欲しい物リスト ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-147">Wish list page</span></span>

<span data-ttu-id="7993a-148">欲しい物リスト ページには、顧客の欲しい物リストに追加された項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7993a-148">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="7993a-149">欲しい物リスト モジュールを使用して、欲しい物リストの項目を表示します。</span><span class="sxs-lookup"><span data-stu-id="7993a-149">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="7993a-150">ロイヤルティ ページ</span><span class="sxs-lookup"><span data-stu-id="7993a-150">Loyalty page</span></span>

<span data-ttu-id="7993a-151">ロイヤルティ ページにより顧客はロイヤルティ プログラムに参加できます。または既にロイヤルティ プログラム メンバーである場合は、そのプログラムの詳細が表示できます。</span><span class="sxs-lookup"><span data-stu-id="7993a-151">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="7993a-152">最近のトランザクションで取得および償還されるポイントを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="7993a-152">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7993a-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7993a-153">Additional resources</span></span>

[<span data-ttu-id="7993a-154">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="7993a-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7993a-155">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7993a-156">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7993a-157">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7993a-158">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7993a-159">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7993a-160">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7993a-161">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="7993a-161">Footer module</span></span>](author-footer-module.md)
