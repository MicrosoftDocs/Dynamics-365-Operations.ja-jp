---
title: デリゲートを使用してアプリケーション起動をカスタマイズする
description: このトピックでは、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。
author: robadawy
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 8fbf5d231816e8238d1a84787157adc61eb37624
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183311"
---
# <a name="customize-application-startup-by-using-delegates"></a><span data-ttu-id="2b018-103">デリゲートを使用してアプリケーション起動をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="2b018-103">Customize application startup by using delegates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b018-104">Dynamics AX 2012 では、クライアントが初期化中に発生したイベント (Application.Startup デリゲート) をサブスクライブできるカスタマイズ ポイントがありました。</span><span class="sxs-lookup"><span data-stu-id="2b018-104">In Dynamics AX 2012, there were customization points that allowed you to subscribe to events (Application.Startup delegates) that were raised when the client was initializing.</span></span> <span data-ttu-id="2b018-105">これらのイベントはリッチ クライアントの概念がないため推奨されません。</span><span class="sxs-lookup"><span data-stu-id="2b018-105">These events were deprecated because there is no concept of a rich client.</span></span> <span data-ttu-id="2b018-106">サーバーで、サーバー セッションのみが考慮されますが、以前のリリースからロジックを移行できるため、新しいイベントが **ApplicationStartupEventManager** クラスに追加されました。</span><span class="sxs-lookup"><span data-stu-id="2b018-106">On the server, only server sessions are considered, however because you can migrate logic from previous releases, new events have been added to the **ApplicationStartupEventManager** class.</span></span> 

<span data-ttu-id="2b018-107">次のセクションでは、拡張機能を使用して既存のフォームに追加できる新しいデータ ソースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2b018-107">The following sections highlight the new data sources that you can add to existing forms by using extensions.</span></span>

## <a name="static-delegate-void-onsystemstartup"></a><span data-ttu-id="2b018-108">static delegate void onSystemStartup()</span><span class="sxs-lookup"><span data-stu-id="2b018-108">static delegate void onSystemStartup()</span></span>
- <span data-ttu-id="2b018-109">このイベントは、システムの起動時に発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-109">This event occurs when the system starts up.</span></span> 
- <span data-ttu-id="2b018-110">これは起動時に AOS につき 1 回発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-110">It is raised once per AOS upon startup.</span></span>

## <a name="static-delegate-void-onfirsttimeuserinteractivesessioncreated"></a><span data-ttu-id="2b018-111">static delegate void onFirstTimeUserInteractiveSessionCreated()</span><span class="sxs-lookup"><span data-stu-id="2b018-111">static delegate void onFirstTimeUserInteractiveSessionCreated()</span></span>
- <span data-ttu-id="2b018-112">このイベントは、ユーザーが初めてインタラクティブ セッションを作成しているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-112">This event occurs when the system is creating an interactive session for the first time for a user.</span></span> 
- <span data-ttu-id="2b018-113">これは AOS ごとのユーザーにつき 1 回発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-113">It is raised once per user per AOS.</span></span>

## <a name="static-delegate-void-onfirsttimeusernoninteractivesessioncreated"></a><span data-ttu-id="2b018-114">static delegate void onFirstTimeUserNonInteractiveSessionCreated()</span><span class="sxs-lookup"><span data-stu-id="2b018-114">static delegate void onFirstTimeUserNonInteractiveSessionCreated()</span></span>
- <span data-ttu-id="2b018-115">このイベントは、ユーザーが初めて非インタラクティブ セッションを作成しているときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-115">This event occurs when the system is creating a non-interactive session for the first time for a user.</span></span> 
- <span data-ttu-id="2b018-116">これは AOS ごとのユーザーにつき 1 回発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-116">It is raised once per user per AOS.</span></span>

## <a name="static-delegate-void-oninteractivesessioncreated"></a><span data-ttu-id="2b018-117">static delegate void onInteractiveSessionCreated()</span><span class="sxs-lookup"><span data-stu-id="2b018-117">static delegate void onInteractiveSessionCreated()</span></span>
- <span data-ttu-id="2b018-118">このイベントは、インタラクティブ セッションが作成され、使用できる状態になったときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-118">This event occurs when an interactive session is created and ready for use.</span></span> 
- <span data-ttu-id="2b018-119">これは、すべてのユーザーのインタラクティブ セッション作成につき 1 回発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-119">It is raised once per interactive session creation for any user.</span></span>

## <a name="static-delegate-void-onsessioncreatedboolean-_isbatch-boolean-_isinteractive"></a><span data-ttu-id="2b018-120">static delegate void onSessionCreated(boolean _isBatch, boolean _isInteractive)</span><span class="sxs-lookup"><span data-stu-id="2b018-120">static delegate void onSessionCreated(boolean _isBatch, boolean _isInteractive)</span></span>
- <span data-ttu-id="2b018-121">このイベントは、セッションが作成され、使用できる状態になったときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-121">This event occurs when the session is created and ready for use.</span></span> 
- <span data-ttu-id="2b018-122">これは、すべてのユーザーのインタラクティブ セッション作成につき 1 回発生します。</span><span class="sxs-lookup"><span data-stu-id="2b018-122">It is raised once per interactive session creation for any user.</span></span>
- <span data-ttu-id="2b018-123">*_isBatch* はシステムがバッチ ジョブを実行しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2b018-123">*_isBatch* specifies whether the system is running a batch job.</span></span>
- <span data-ttu-id="2b018-124">*_isInteractive* はセッションが対話型であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="2b018-124">*_isInteractive* specifies whether the session is interactive.</span></span>
