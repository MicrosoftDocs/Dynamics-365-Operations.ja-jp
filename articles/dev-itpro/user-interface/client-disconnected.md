---
title: "クライアント インターネット接続"
description: "このトピックは、オンプレミス配置で、クライアント マシンがインターネットにアクセスできない場合に何が起きるかについて説明します。"
author: jasongre
manager: AnnBe
ms.date: 03/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29151
ms.assetid: 
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b0869b12e3f806b36868e798d081692e14cc5781
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="client-internet-connection"></a><span data-ttu-id="bba81-103">クライアント インターネット接続</span><span class="sxs-lookup"><span data-stu-id="bba81-103">Client internet connection</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bba81-104">Finance and Operations 用の Dynamics 365 のオンプレミス配置用のローカル ネットワークの構成は、Web クライアントの利用可能な機能に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bba81-104">The configuration of the local network for an on-premises deployment of Dynamics 365 for Finance and Operations can affect the available features in the web client.</span></span> <span data-ttu-id="bba81-105">特に、ネットワーク構成がインターネットにアクセスするクライアント マシンを許可していない場合、Web クライアントで複数のパフォーマンス低下が発生します。</span><span class="sxs-lookup"><span data-stu-id="bba81-105">In particular, if the network configuration does not allow a client machine to access the internet, several degradations in the web client will occur.</span></span> <span data-ttu-id="bba81-106">コピーされるフィールドは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bba81-106">These include:</span></span>    

+ <span data-ttu-id="bba81-107">ナビゲーション バーにおける Office ワッフルおよび Dynamics 365 領域はクリック可能でなくなりました。</span><span class="sxs-lookup"><span data-stu-id="bba81-107">The Office waffle and Dynamics 365 areas in the navigation bar will no longer be clickable.</span></span>
+ <span data-ttu-id="bba81-108">ヘルプ ウィンドウにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="bba81-108">The Help pane will not be accessible.</span></span>  
+ <span data-ttu-id="bba81-109">Ideas ポータルは、Web クライアントからアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="bba81-109">The Ideas portal will not be accessible from the web client.</span></span> 
+ <span data-ttu-id="bba81-110">ユーザー イメージではなく、ユーザーのイニシャルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bba81-110">Users will see their initials instead of a user image.</span></span> 
+ <span data-ttu-id="bba81-111">Skype 統合が使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="bba81-111">Skype integration will not be available.</span></span>  
+ <span data-ttu-id="bba81-112">ブラウザー タブに表示されるお気に入りのアイコンは、[Finance and Operations] アイコンではなく、ブラウザーの既定のお気に入りのアイコンになります。</span><span class="sxs-lookup"><span data-stu-id="bba81-112">The favorite icon shown in the browser tab will be the browser's default favorite icon instead of the Finance and Operations icon.</span></span> 

<span data-ttu-id="bba81-113">クライアントがインターネットにアクセスできない場合にアクセスできない可能性があるプラットフォーム機能に加えて、開発者が非表示にするかオフにする必要がある、インターネット接続に依存したアプリケーション機能もある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bba81-113">In addition to platform features that may not be accessible when the client can't access the internet, there may also be application features that rely on an internet connection that developers will need to hide or switch off.</span></span> <span data-ttu-id="bba81-114">これを容易にするために、開発者は**セッション**クラスに追加された **clientHasRestrictedInternet()** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bba81-114">To facilitate this, developers can use the **clientHasRestrictedInternet()** method that has been added to the **Session** class.</span></span> <span data-ttu-id="bba81-115">このメソッドは、クライアントがインターネットにアクセスできない場合は true を返します。</span><span class="sxs-lookup"><span data-stu-id="bba81-115">This method will return true if the client does not have access to the internet.</span></span>

## <a name="client-internet-connectivity-options"></a><span data-ttu-id="bba81-116">クライアント インターネット接続オプション</span><span class="sxs-lookup"><span data-stu-id="bba81-116">Client internet connectivity options</span></span>

<span data-ttu-id="bba81-117">クライアント インターネット接続オプション (次によって追加された [KB 4091763](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=19e9634da3297903a2ac51cf291a4770fd4532c9767ca7b5cefbe1bccb5d4d9f)) により、管理者は、インターネット接続が利用可能であってもクライアントが行う外部接続を手動でオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="bba81-117">Client internet connectivity options (added by [KB 4091763](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=19e9634da3297903a2ac51cf291a4770fd4532c9767ca7b5cefbe1bccb5d4d9f)) allow an administrator to manually switch off the external connections that the client makes even when internet connectivity is available.</span></span> <span data-ttu-id="bba81-118">これらは、問題のトラブルシューティングや、インターネット接続が利用できない場合にクライアントがどのように見えるかを確認するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="bba81-118">These can be used for troubleshooting issues or just to see what the client will look like when internet connectivity is not available.</span></span>

<span data-ttu-id="bba81-119">これらのオプションは、**システム管理 > 設定 > クライアント パフォーマンス オプション** ページにあります。</span><span class="sxs-lookup"><span data-stu-id="bba81-119">These options can be found on the **System administration > Setup > Client performance options** page.</span></span>

- <span data-ttu-id="bba81-120">**インターネット接続が有効** - 管理者は、Web クライアントが外部から行う外部接続をすべてオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="bba81-120">**Internet connectivity enabled** - Allows an administrator to switch off all external connections that the web client would otherwise make.</span></span>
- <span data-ttu-id="bba81-121">**Skype プレゼンスが有効** - 管理者は、Web クライアントが外部から行う外部接続をすべてオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="bba81-121">**Skype presence enabled** - Allows an administrator to switch off external connections to Skype that the web client would otherwise make.</span></span>

