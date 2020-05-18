---
title: クライアント インターネット接続
description: このトピックは、オンプレミス配置で、クライアント マシンがインターネットにアクセスできない場合に何が起きるかについて説明します。
author: jasongre
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 29151
ms.assetid: ''
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: 7dc6d4ede3ca6081bd564189c8eeaa47b8de8cbf
ms.sourcegitcommit: 4d5bcda288341572076364559125c86e2ec05273
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2020
ms.locfileid: "3334721"
---
# <a name="client-internet-connectivity"></a><span data-ttu-id="abc63-103">クライアントのインターネット接続</span><span class="sxs-lookup"><span data-stu-id="abc63-103">Client internet connectivity</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="abc63-104">Dynamics 365 Finance + Operations (オンプレミス) 展開用のローカル ネットワークの構成は、Web クライアントで利用可能な機能に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="abc63-104">The configuration of the local network for a deployment of Dynamics 365 Finance + Operations (on-premises) can affect the features that are available in the web client.</span></span> <span data-ttu-id="abc63-105">特に、ネットワーク構成がインターネットにアクセスするクライアント マシンを許可していない場合、Web クライアントで複数のパフォーマンス低下が発生します。</span><span class="sxs-lookup"><span data-stu-id="abc63-105">In particular, if the network configuration does not allow a client machine to access the internet, several degradations in the web client will occur.</span></span> <span data-ttu-id="abc63-106">コピーされるフィールドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="abc63-106">These include:</span></span>    

+ <span data-ttu-id="abc63-107">ナビゲーション バーにおける Office アプリ ランチャおよび Dynamics 365 領域はクリック可能でなくなりました。</span><span class="sxs-lookup"><span data-stu-id="abc63-107">The Office app launcher and Dynamics 365 areas in the navigation bar will no longer be clickable.</span></span>
+ <span data-ttu-id="abc63-108">ヘルプ ウィンドウにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="abc63-108">The Help pane will not be accessible.</span></span>  
+ <span data-ttu-id="abc63-109">Ideas ポータルは、Web クライアントからアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="abc63-109">The Ideas portal will not be accessible from the web client.</span></span> 
+ <span data-ttu-id="abc63-110">ユーザー イメージではなく、ユーザーのイニシャルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="abc63-110">Users will see their initials instead of a user image.</span></span> 
+ <span data-ttu-id="abc63-111">Skype 統合が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="abc63-111">Skype integration will not be available.</span></span>  
+ <span data-ttu-id="abc63-112">ブラウザー タブに表示されるお気に入りのアイコンは、アプリケーションのアイコンではなく、ブラウザーの既定のお気に入りのアイコンになります。</span><span class="sxs-lookup"><span data-stu-id="abc63-112">The favorite icon shown in the browser tab will be the browser's default favorite icon instead of the application icon.</span></span> 
+ <span data-ttu-id="abc63-113">Excel アドインが実行されないため、Excel で開くオプションは表示されません。</span><span class="sxs-lookup"><span data-stu-id="abc63-113">The Open in Excel options are hidden because the Excel Add-in will not run.</span></span>

<span data-ttu-id="abc63-114">クライアントがインターネットにアクセスできない場合にアクセスできない可能性があるプラットフォーム機能に加えて、開発者が非表示にするかオフにする必要がある、インターネット接続に依存したアプリケーション機能もある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="abc63-114">In addition to platform features that may not be accessible when the client can't access the internet, there may also be application features that rely on an internet connection that developers will need to hide or turn off.</span></span> <span data-ttu-id="abc63-115">これを容易にするために、開発者は**セッション**クラスに追加された **clientHasRestrictedInternet()** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="abc63-115">To facilitate this, developers can use the **clientHasRestrictedInternet()** method that has been added to the **Session** class.</span></span> <span data-ttu-id="abc63-116">このメソッドは、クライアントがインターネットにアクセスできない場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="abc63-116">This method will return true if the client does not have access to the internet.</span></span>

## <a name="client-internet-connectivity-options"></a><span data-ttu-id="abc63-117">クライアント インターネット接続オプション</span><span class="sxs-lookup"><span data-stu-id="abc63-117">Client internet connectivity options</span></span>

<span data-ttu-id="abc63-118">クライアント インターネット接続オプションにより、管理者は、インターネット接続が利用可能であってもクライアントが行う外部接続を手動でオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="abc63-118">Client internet connectivity options allow an administrator to manually turn off the external connections that the client makes even when internet connectivity is available.</span></span> <span data-ttu-id="abc63-119">これらは、問題のトラブルシューティングや、インターネット接続が利用できない場合にクライアントがどのように見えるか確認するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="abc63-119">These can be used for troubleshooting issues or to see what the client will look like when internet connectivity is not available.</span></span> <span data-ttu-id="abc63-120">これらのクライアント インターネット接続オプションは、プラットフォーム アップデート 16 からすぐに利用できますが、プラットフォーム アップデート 15 ([KB 4091764](https://fix.lcs.dynamics.com/Issue/Details?kb=4091764&bugId=3934774&qc=245bb2cc9839fa2a2ecf6bfffc48c3dec102a3c1047e5e755387d00148db18cb) 経由) およびプラットフォーム アップデート 12 ([KB 4091763](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=19e9634da3297903a2ac51cf291a4770fd4532c9767ca7b5cefbe1bccb5d4d9f) 経由) でも利用できます。</span><span class="sxs-lookup"><span data-stu-id="abc63-120">These client internet connectivity options are available out-of-the-box starting in Platform update 16 but are also available in Platform update 15 (via [KB 4091764](https://fix.lcs.dynamics.com/Issue/Details?kb=4091764&bugId=3934774&qc=245bb2cc9839fa2a2ecf6bfffc48c3dec102a3c1047e5e755387d00148db18cb)) and Platform update 12 (via [KB 4091763](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=19e9634da3297903a2ac51cf291a4770fd4532c9767ca7b5cefbe1bccb5d4d9f)).</span></span> 


<span data-ttu-id="abc63-121">クライアント インターネット接続オプションは、**システム管理** > **設定** > **クライアント パフォーマンス オプション**ページにあります。</span><span class="sxs-lookup"><span data-stu-id="abc63-121">The client internet connectivity options can be found on the **System administration** > **Setup** > **Client performance options** page.</span></span> 

- <span data-ttu-id="abc63-122">**インターネット接続が有効** - 管理者は、Web クライアントが外部から行う外部接続をすべてオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="abc63-122">**Internet connectivity enabled** - Allows an administrator to turn off all external connections that the web client would otherwise make.</span></span>
- <span data-ttu-id="abc63-123">**Skype プレゼンスが有効** - 管理者がスカイプへの外部接続をオフにし、そうでなければWeb クライアントが行います。</span><span class="sxs-lookup"><span data-stu-id="abc63-123">**Skype presence enabled** - Allows an administrator to turn off external connections to Skype that the web client would otherwise make.</span></span>

## <a name="why-does-the-client-connect-to-the-skype-for-business-api-when-it-first-loads"></a><span data-ttu-id="abc63-124">クライアントが最初に読み込まれたときに Skype for Business API に接続する理由。</span><span class="sxs-lookup"><span data-stu-id="abc63-124">Why does the client connect to the Skype for Business API when it first loads?</span></span>

<span data-ttu-id="abc63-125">クライアントの読み込み時に、インターネット接続が使用可能かどうかを確認するために、Skype for Business API へのクイック コール (ping) が実行されます。</span><span class="sxs-lookup"><span data-stu-id="abc63-125">When the client loads, it performs a quick call (ping) to the Skype for Business API to check if an internet connection is available.</span></span> <span data-ttu-id="abc63-126">使用できない場合は、クライアントは切断された方法で機能します。</span><span class="sxs-lookup"><span data-stu-id="abc63-126">If it isn’t available then the client functions in a disconnected fashion.</span></span> <span data-ttu-id="abc63-127">環境では、このチェックを実行するために Skype for Business を表示するかどうかを指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="abc63-127">An environment doesn’t need to have Skype for Business visible/enabled for this check to be made.</span></span>
