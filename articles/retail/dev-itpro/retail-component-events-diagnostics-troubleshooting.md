---
title: 診断とトラブルシューティングの Retail コンポーネント イベント
description: 診断とトラブルシューティングを有効にするため、Retail Modern POS などのクライアントを含むすべての Retail コンポーネントと Retail Server などのサーバー コンポーネントは、イベントをイベント ビューアー (または Retail Cloud POS の場合はブラウザー開発ツール コンソール) にローカルで記録します。 この記事では、Retail 固有のコンポーネントからイベントを検索する場所について説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 85493
ms.assetid: a22c9493-c000-4514-bb0d-b3cc674439d9
ms.search.region: Global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: bb977cd3962725dd219ae8c7b6dabecd32e4b821
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369277"
---
# <a name="retail-component-events-for-diagnostics-and-troubleshooting"></a><span data-ttu-id="292a1-104">診断とトラブルシューティングの Retail コンポーネント イベント</span><span class="sxs-lookup"><span data-stu-id="292a1-104">Retail component events for diagnostics and troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="292a1-105">診断とトラブルシューティングを有効にするため、Retail Modern POS などのクライアントを含むすべての Retail コンポーネントと Retail Server などのサーバー コンポーネントは、イベントをイベント ビューアー (または Retail Cloud POS の場合はブラウザー開発ツール コンソール) にローカルで記録します。</span><span class="sxs-lookup"><span data-stu-id="292a1-105">To enable diagnostics and troubleshooting, all Retail components, which include clients such as the Retail Modern POS and server components such as Retail Server, log their events locally to Event Viewer (or to the browser developer tools console, in case of Retail Cloud POS).</span></span> <span data-ttu-id="292a1-106">この記事では、Retail 固有のコンポーネントからイベントを検索する場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="292a1-106">This article explains where to find events from Retail-specific components.</span></span>

<a name="viewing-events-in-event-viewer"></a><span data-ttu-id="292a1-107">イベント ビューアーでのイベントの表示</span><span class="sxs-lookup"><span data-stu-id="292a1-107">Viewing events in Event Viewer</span></span>
------------------------------

<span data-ttu-id="292a1-108">イベントがログされるコンピューターに対して物理的にアクセスできる場合、イベント ビューアーを使用して、Microsoft Windows を実行するコンピューター上にインストールされたコンポーネント用イベントを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-108">You can use Event Viewer to view events for components that are installed on computers that run Microsoft Windows, if you have physical access to the computer where the events are logged.</span></span> <span data-ttu-id="292a1-109">イベント ビューアーの詳細については、TechNet の [イベント ビューアー](https://technet.microsoft.com/en-us/library/4229f239-16a6-4ecd-b3cf-aec03dc08cd5) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="292a1-109">For more information about Event Viewer, see [Event Viewer](https://technet.microsoft.com/en-us/library/4229f239-16a6-4ecd-b3cf-aec03dc08cd5) on TechNet.</span></span> <span data-ttu-id="292a1-110">また、イベント ビューアーを使用して、ユーザーがアクセス権を持つコンピューターからリモートでイベントを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-110">You can also use Event Viewer to view events remotely from computers that you have access to.</span></span> <span data-ttu-id="292a1-111">イベント ビューアーを使用して、リモートでイベントを表示する方法の詳細については、TechNet の [リモート コンピューターでイベント ログを使用](https://technet.microsoft.com/en-us/library/cc766438.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="292a1-111">For more information about how to use Event Viewer to view events remotely, see [Work with Event Logs on a Remote Computer](https://technet.microsoft.com/en-us/library/cc766438.aspx) on TechNet.</span></span> <span data-ttu-id="292a1-112">イベント ビューアは通常、次の使用例でのトラブルシューティングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-112">Typically, Event Viewer is used for troubleshooting in the following use cases:</span></span>

-   <span data-ttu-id="292a1-113">開発者トポロジまたはイベント ビューアーへのアクセスを提供するダウンロード可能な仮想ハードディスク (VHD) での開発</span><span class="sxs-lookup"><span data-stu-id="292a1-113">Development on a developer topology or on a downloadable virtual hard disk (VHD) that provides access to Event Viewer</span></span>
-   <span data-ttu-id="292a1-114">会議室パイロットを実行していて、そのコンピューティングのイベント ビューアにアクセスできるときのクライアント コンポーネント</span><span class="sxs-lookup"><span data-stu-id="292a1-114">Client components, when you're running a conference room pilot and have access to Event Viewer for that computer</span></span>

<span data-ttu-id="292a1-115">ただし、ほとんどの場合、特にコンピューターのイベント ビューアーへのアクセスがない場合、Microsoft Dynamics Lifecycle Services (LCS) でログ検索を使用できます。</span><span class="sxs-lookup"><span data-stu-id="292a1-115">However, for most other cases, and especially when you don't have access to Event Viewer for the computer, you can use Log Search on Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="292a1-116">ログ検索については、この記事の後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="292a1-116">Log Search is discussed later in this article.</span></span> <span data-ttu-id="292a1-117">このセクションは、次のコンポーネントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-117">This section applies to the following components:</span></span>

-   <span data-ttu-id="292a1-118">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="292a1-118">Retail Server</span></span>
-   <span data-ttu-id="292a1-119">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="292a1-119">Retail Modern POS</span></span>
-   <span data-ttu-id="292a1-120">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="292a1-120">Retail Hardware Station</span></span>

### <a name="find-retail-specific-events-in-event-viewer"></a><span data-ttu-id="292a1-121">イベント ビューアーで、小売固有のイベントを検索します</span><span class="sxs-lookup"><span data-stu-id="292a1-121">Find Retail-specific events in Event Viewer</span></span>

<span data-ttu-id="292a1-122">コンピューターでイベント ビューアを起動するには、**開始** ボタンをクリックし、**イベント ビューア** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-122">To start Event Viewer on a computer, right-click the **Start** button, and then click **Event Viewer**.</span></span> 

<span data-ttu-id="292a1-123">[![スタート ボタンのショートカット メニューのイベント ビューアー コマンド](./media/launch-event-viewer.png)](./media/launch-event-viewer.png)</span><span class="sxs-lookup"><span data-stu-id="292a1-123">[![Event Viewer command on the shortcut menu for the Start button](./media/launch-event-viewer.png)](./media/launch-event-viewer.png)</span></span> 

<span data-ttu-id="292a1-124">すべての Retail 固有イベント ログにはイベント ビューアーで次のパスを確認できます。アプリケーションおよびサービス ログ \\Microsoft\\Dynamics 以下の Retail 固有のイベント ログを提供します。</span><span class="sxs-lookup"><span data-stu-id="292a1-124">All Retail-specific event logs can be found under the following path in Event Viewer: Application and Services Logs\\Microsoft\\Dynamics We provide the following Retail-specific event logs:</span></span>

-   <span data-ttu-id="292a1-125">**Commerce-RetailServer** - このログには、Retail サーバー コンポーネントによって記録されるイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="292a1-125">**Commerce-RetailServer** – This log contains events that are logged by the Retail Server components.</span></span>
-   <span data-ttu-id="292a1-126">**Commerce-ModernPos** - このログには、Retail Modern POS によって記録されるイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="292a1-126">**Commerce-ModernPos** – This log contains events that are logged by Retail Modern POS.</span></span> <span data-ttu-id="292a1-127">これらのイベントには、TypeScript および C\# (CRT) レイヤーからのイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="292a1-127">These events include events from the TypeScript and C\# (CRT) layer.</span></span>
-   <span data-ttu-id="292a1-128">**Commerce-LoggingProvider** - このログには、この記事の前半で一覧に含まれていない他のすべての小売コンポーネントによって記録されるイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="292a1-128">**Commerce-LoggingProvider** – This log contains events that are logged by all other Retail components that aren't included in the list earlier in this article.</span></span>

### <a name="enable-debug-event-logs"></a><span data-ttu-id="292a1-129">デバッグ イベント ログの有効化</span><span class="sxs-lookup"><span data-stu-id="292a1-129">Enable debug event logs</span></span>

<span data-ttu-id="292a1-130">現在、さまざまな小売コンポーネントによって記録されたイベントの一部がデバッグ イベント ログに送信されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-130">Currently, some of the events that are logged by various Retail components are sent to debug event logs.</span></span> <span data-ttu-id="292a1-131">これらのイベントは非常に高いレートで記録され、詳細なデバッグ シナリオでのみ有用な詳細イベントです。</span><span class="sxs-lookup"><span data-stu-id="292a1-131">These events are verbose events that are logged at very high rates and are useful only for detailed debugging scenarios.</span></span> <span data-ttu-id="292a1-132">イベント ビューアーでのデバッグ イベント ログを有効にするには、この手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="292a1-132">Follow this step to enable the debug event logs in Event Viewer.</span></span>

-   <span data-ttu-id="292a1-133">デバッグ ログを右クリックし、**ログの有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-133">Right-click a debug log, and then click **Enable Log**.</span></span>

<span data-ttu-id="292a1-134">[![デバッグ ログのショートカットメニューでログ コマンドを有効化](./media/enable-debugging-log.png)](./media/enable-debugging-log.png)</span><span class="sxs-lookup"><span data-stu-id="292a1-134">[![Enable Log command on the shortcut menu for a debug log](./media/enable-debugging-log.png)](./media/enable-debugging-log.png)</span></span>

## <a name="viewing-events-by-using-the-f12-browser-developer-tools-console"></a><span data-ttu-id="292a1-135">(F12) ブラウザー開発者ツール コンソールを使用してイベントを表示</span><span class="sxs-lookup"><span data-stu-id="292a1-135">Viewing events by using the (F12) browser developer tools console</span></span>
<span data-ttu-id="292a1-136">Retail Cloud POS はブラウザー ベースのコンポーネントなので、ブラウザー開発者ツール コンソールを使用してそのイベントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="292a1-136">Because Retail Cloud POS is a browser-based component, you can use the browser developer tools console to view events for it.</span></span> <span data-ttu-id="292a1-137">Microsoft ブラウザ開発者ツール コンソールの詳細については、MSDN の [コンソールを使用してエラーとデバッグを表示する](https://msdn.microsoft.com/en-us/library/dn255006(v=vs.85).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="292a1-137">For information about the Microsoft browser developer tools console, see [Using the Console to view errors and debug](https://msdn.microsoft.com/en-us/library/dn255006(v=vs.85).aspx) on MSDN.</span></span> <span data-ttu-id="292a1-138">Retail Cloud POS のブラウザー開発者ツールを使用するには、サポートされているバージョンのブラウザを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="292a1-138">To use the browser developer tools for Retail Cloud POS, you must use a supported browser version.</span></span>

### <a name="view-events-in-the-browser-developer-tools-console"></a><span data-ttu-id="292a1-139">ブラウザー開発者ツール コンソールでのイベントの表示</span><span class="sxs-lookup"><span data-stu-id="292a1-139">View events in the browser developer tools console</span></span>

1.  <span data-ttu-id="292a1-140">Internet Explorer または Microsoft Edge を開始し、Retail クラウド POS に移動します。</span><span class="sxs-lookup"><span data-stu-id="292a1-140">Start Internet Explorer or Microsoft Edge, and go to Retail Cloud POS.</span></span>
2.  <span data-ttu-id="292a1-141">F12 キーを押し、**コンソール** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-141">Press F12, and then click the **Console** tab.</span></span>
3.  <span data-ttu-id="292a1-142">Retail Cloud POS の操作を実行する際に、イベントはコンソールに記録されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-142">As you perform operations on Retail Cloud POS, events are logged in the console.</span></span> <span data-ttu-id="292a1-143">イベント重要度でフィルター処理して、異なる重要度レベルのイベントを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-143">You can filter by event severity to view events that have different severity levels.</span></span>

<span data-ttu-id="292a1-144">[![ブラウザー開発者ツールのコンソール タブ](./media/browser-console-1024x522.png)](./media/browser-console.png)</span><span class="sxs-lookup"><span data-stu-id="292a1-144">[![Console tab in the browser developer tools](./media/browser-console-1024x522.png)](./media/browser-console.png)</span></span>

## <a name="correlating-events"></a><span data-ttu-id="292a1-145">関連のイベント</span><span class="sxs-lookup"><span data-stu-id="292a1-145">Correlating events</span></span>
<span data-ttu-id="292a1-146">このセクションでは、さまざまな Retail コンポーネントからイベントを関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="292a1-146">This sections explains how to correlate events from various Retail components.</span></span>

### <a name="data-flow-between-a-pos-client-and-retail-server"></a><span data-ttu-id="292a1-147">POS クライアントと Retail サーバー間のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="292a1-147">Data flow between a POS client and Retail Server</span></span>

<span data-ttu-id="292a1-148">以下の図は、販売時点管理 (POS) クライアントと Retail Server 間のデータ フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="292a1-148">The diagram that follows shows the data flow between a point of sale (POS) client and the Retail Server.</span></span>

#### <a name="pos-client-startup"></a><span data-ttu-id="292a1-149">POS クライアントの起動</span><span class="sxs-lookup"><span data-stu-id="292a1-149">POS client startup</span></span>

<span data-ttu-id="292a1-150">ユーザーが POS クライアントを起動すると、新しい AppSessionID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-150">When a user starts a POS client, a new AppSessionID is generated.</span></span> <span data-ttu-id="292a1-151">AppSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-151">The AppSessionID is used to log every event that is instrumented in the POS client.</span></span> <span data-ttu-id="292a1-152">イベント ビューアおよびアプリ インサイトに記録したすべてのイベントはこの ID を持っています。</span><span class="sxs-lookup"><span data-stu-id="292a1-152">All events that are logged to Event Viewer and App Insights have this ID.</span></span>

#### <a name="user-sign-in"></a><span data-ttu-id="292a1-153">ユーザー サインイン</span><span class="sxs-lookup"><span data-stu-id="292a1-153">User sign-in</span></span>

<span data-ttu-id="292a1-154">ユーザーが POS クライアントにサインインすると、新しい UserSessionID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-154">When a user signs in to a POS client, a new UserSessionID is generated.</span></span> <span data-ttu-id="292a1-155">UserSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-155">The UserSessionID is used to log every event that is instrumented in the POS client.</span></span> <span data-ttu-id="292a1-156">イベント ビューアーに記録されたすべてのユーザー イベントはこの ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="292a1-156">All user events that are logged to Event Viewer have this ID.</span></span> <span data-ttu-id="292a1-157">この ID は、ユーザーがログインしている間維持されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-157">This ID is maintained for as long as the user is signed in.</span></span> <span data-ttu-id="292a1-158">現在のユーザーがサインアウトして、新しいユーザーがログインすると、新しい UserSessionID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-158">When the current user signs out and a new user sign in, a new UserSessionID is generated.</span></span>

#### <a name="pos-client-calls-to-retail-server"></a><span data-ttu-id="292a1-159">Retail サーバーへの POS クライアントの呼び出し</span><span class="sxs-lookup"><span data-stu-id="292a1-159">POS client calls to Retail Server</span></span>

<span data-ttu-id="292a1-160">POS クライアントが Retail サーバーを呼び出すときはいつでも、AppSessionID と UserSessionID がヘッダーとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-160">Whenever a POS client makes a call to the Retail Server, the AppSessionID and UserSessionID are sent as headers.</span></span> <span data-ttu-id="292a1-161">次に、Retail Server は、受信要求 (イベント ID 5000) のイベントを記録します。</span><span class="sxs-lookup"><span data-stu-id="292a1-161">The Retail Server then logs an event for the incoming request (Event ID 5000).</span></span> <span data-ttu-id="292a1-162">このイベントには、2 つの ID と ActivityID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="292a1-162">This event includes those two IDs and also an ActivityID.</span></span> <span data-ttu-id="292a1-163">その後、ActivityID はすべての関連する Retail Server イベントにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-163">The ActivityID is then also used for all related Retail Server events.</span></span> <span data-ttu-id="292a1-164">AppSessionID、UserSessionID、ActivityID は、Retail Server がホストされているイベント ログで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="292a1-164">The AppSessionID, UserSessionID, and ActivityID are available in the event log where Retail Server is hosted.</span></span> <span data-ttu-id="292a1-165">LCS ログ検索でも利用できます。</span><span class="sxs-lookup"><span data-stu-id="292a1-165">They are also available in LCS Log Search.</span></span>

#### <a name="request-activity-on-retail-server"></a><span data-ttu-id="292a1-166">Retail サーバーのアクティビティを要求</span><span class="sxs-lookup"><span data-stu-id="292a1-166">Request activity on Retail Server</span></span>

<span data-ttu-id="292a1-167">Retail サーバー要求の一部として記録されるすべてのイベントは、最初の受信要求イベント用に記録された初期イベントと同じ ActivityID を持ちます (イベント ID 5000)。</span><span class="sxs-lookup"><span data-stu-id="292a1-167">Every event that is logged as part of a Retail Server request has the same ActivityID as the initial event that was logged for the initial incoming request event (Event ID 5000).</span></span> <span data-ttu-id="292a1-168">これらのイベントは、イベント ビューアーと LCS ログ検索の両方で利用できます。</span><span class="sxs-lookup"><span data-stu-id="292a1-168">These events are available in both Event Viewer and LCS Log Search.</span></span> 

<span data-ttu-id="292a1-169">[![POS クライアントおよび Retail サーバー間のデータ フロー](./media/event-log-data-flow1-1018x1024.png)](./media/event-log-data-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="292a1-169">[![Data flow between a POS client and Retail Server](./media/event-log-data-flow1-1018x1024.png)](./media/event-log-data-flow1.png)</span></span>

### <a name="finding-retail-modern-pos-events-in-event-viewer"></a><span data-ttu-id="292a1-170">イベント ビューアーでの Retail Modern POS イベントの検索</span><span class="sxs-lookup"><span data-stu-id="292a1-170">Finding Retail Modern POS events in Event Viewer</span></span>

<span data-ttu-id="292a1-171">Retail Modern POS によってが記録されたすべてのイベントには、次のデータ点が含まれています。</span><span class="sxs-lookup"><span data-stu-id="292a1-171">Every event that is logged by Retail Modern POS includes the following data points:</span></span>

-   <span data-ttu-id="292a1-172">**AppSessionID** - アプリケーションが最初に起動されたときに生成される一意の ID。</span><span class="sxs-lookup"><span data-stu-id="292a1-172">**AppSessionID** – A unique ID that is generated when the app is first started.</span></span> <span data-ttu-id="292a1-173">これは Retail Modern POS で記録されるすべてのイベントに含まれています。</span><span class="sxs-lookup"><span data-stu-id="292a1-173">It's included with every event that is logged from Retail Modern POS.</span></span>
-   <span data-ttu-id="292a1-174">**UserSessionID** – ユーザーが Retail Modern POS にサインインするときに生成される固有の ID。</span><span class="sxs-lookup"><span data-stu-id="292a1-174">**UserSessionID** – A unique ID that is generated when a user signs in to Retail Modern POS.</span></span> <span data-ttu-id="292a1-175">これはユーザーがサインインしている限り、Retail Modern POS で記録されるすべてのイベントに含まれています。</span><span class="sxs-lookup"><span data-stu-id="292a1-175">It's included with every event that is logged from Retail Modern POS, for as long as the user remains signed in.</span></span> <span data-ttu-id="292a1-176">新しいユーザーがサインインするとき、新しい UserSessionID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-176">When a new user signs in, a new UserSessionID is created.</span></span>

<span data-ttu-id="292a1-177">AppSessionID 値および UserSessionID 値は、Retail Modern POS がインストールされているマシン上のイベント ビューアーの**詳細**タブで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-177">You can find the AppSessionID and UserSessionID values on the **Details** tab in Event Viewer on the machine where Retail Modern POS is installed.</span></span> 

<span data-ttu-id="292a1-178">[![イベント ビューアーの詳細タブ](./media/correlation-1024x672.png)](./media/correlation.png)</span><span class="sxs-lookup"><span data-stu-id="292a1-178">[![Details tab in Event Viewer](./media/correlation-1024x672.png)](./media/correlation.png)</span></span>

### <a name="finding-incoming-retail-server-request-events-in-event-viewer"></a><span data-ttu-id="292a1-179">イベント ビューアーで、受信する Retail サーバー要求のイベントを検索</span><span class="sxs-lookup"><span data-stu-id="292a1-179">Finding incoming Retail Server request events in Event Viewer</span></span>

<span data-ttu-id="292a1-180">イベント ビューアで受信する Retail サーバー要求のデータを関連付けるには、最初に **Analytic** チャネルを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="292a1-180">To correlate data for incoming Retail Server requests in Event Viewer, you must first enable the **Analytic** channel.</span></span> <span data-ttu-id="292a1-181">分析チャネルを有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="292a1-181">To enable the Analytic channel, follow these steps.</span></span>

1.  <span data-ttu-id="292a1-182">イベント ビューアーの左ウィンドウで、**Commerce RetailServer** を選択します。</span><span class="sxs-lookup"><span data-stu-id="292a1-182">In Event Viewer, in the left pane, select **Commerce-RetailServer**.</span></span>
2.  <span data-ttu-id="292a1-183">**表示** &gt; **分析とデバッグ ログを有効にします**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-183">Click **View** &gt; **Enable Analytic and Debug log**.</span></span> <span data-ttu-id="292a1-184">分析チャネルの新しいノードは、**Commerce-RetailServer** ログ プロバイダーの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-184">A new node for the Analytic channel appears under the **Commerce-RetailServer** logging provider.</span></span>
3.  <span data-ttu-id="292a1-185">**分析** ノードを右クリックし、**ログの有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-185">Right-click the **Analytic** node, and then click **Enable log**.</span></span>

<span data-ttu-id="292a1-186">イベント ビューアーでは、受信しているすべての Retail サーバーの要求がイベント 5000 として Commerce-RetailServer ソースの分析チャネルに記録されます。</span><span class="sxs-lookup"><span data-stu-id="292a1-186">In Event Viewer, all incoming Retail Server requests are logged to the Analytic channel of the Commerce-RetailServer source as event 5000.</span></span> <span data-ttu-id="292a1-187">これらのイベントには、前述した AppSessionID と UserSessionID もあります。</span><span class="sxs-lookup"><span data-stu-id="292a1-187">These events also have the AppSessionID and UserSessionID that were described earlier.</span></span> <span data-ttu-id="292a1-188">すべてのイベントには、同じ Retail サーバー要求のログに記録されたイベントごとに、固有の ActivityID も用意されています。</span><span class="sxs-lookup"><span data-stu-id="292a1-188">Every event also has a unique ActivityID that is instrumented for every logged event for the same Retail Server request.</span></span>

## <a name="using-lcs-log-search"></a><span data-ttu-id="292a1-189">LCS ログ検索の使用</span><span class="sxs-lookup"><span data-stu-id="292a1-189">Using LCS Log Search</span></span>
<span data-ttu-id="292a1-190">LCS ログ検索で、1 つのポータルからすべてのコンポーネントのデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="292a1-190">LCS Log Search lets you view data from all the components from a single portal.</span></span> <span data-ttu-id="292a1-191">イベントは、(Retail サーバーなどの) クラウドでホストされたコンポーネントと (Retail Modern POS および Retail Hardware Station などの) 店舗内コンポーネントの両方からアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-191">You can access events from both cloud-hosted components (such as Retail Server) and in-store components (such as Retail Modern POS and Retail Hardware Station).</span></span> <span data-ttu-id="292a1-192">すべてのクラウドホストおよびストア内コンポーネントからのイベント データは、索引付けされ検索可能になる LCS ログ検索に流れます。</span><span class="sxs-lookup"><span data-stu-id="292a1-192">Event data from all cloud-hosted and in-store components flows to LCS Log Search, where it's indexed and made searchable.</span></span> <span data-ttu-id="292a1-193">データは通常、記録されてから 5 分以内に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="292a1-193">Data is typically available within 5 minutes after it's logged.</span></span> <span data-ttu-id="292a1-194">POS クライアントおよび Retail Hardware Station では、すべてのイベントが永続ストレージにローカルでキュー格納され、キューがいっぱいになった後にバッチでアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="292a1-194">For POS clients and Retail Hardware Station, all events are locally queued in persistent storage and then uploaded in batches after the queue is filled.</span></span> <span data-ttu-id="292a1-195">この動作により、ネットワーク トラフィックを最適化できます。 </span><span class="sxs-lookup"><span data-stu-id="292a1-195">This behavior enables network traffic to be optimized.</span></span> <span data-ttu-id="292a1-196">また、インターネット接続がない場合でもイベントを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-196">It also enables events to be saved even when there is no Internet connectivity.</span></span> <span data-ttu-id="292a1-197">接続が回復した後、すべての保留中のイベントがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="292a1-197">After connectivity is restored, all pending events are uploaded.</span></span> <span data-ttu-id="292a1-198">LCS ログ検索は、HA 運用トポロジに使用できます。</span><span class="sxs-lookup"><span data-stu-id="292a1-198">LCS Log Search is available for the HA production topology.</span></span> <span data-ttu-id="292a1-199">次の Retail のコンポーネントに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-199">It can be used for the following Retail components:</span></span>

-   <span data-ttu-id="292a1-200">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="292a1-200">Retail Modern POS</span></span>
-   <span data-ttu-id="292a1-201">小売クラウド POS</span><span class="sxs-lookup"><span data-stu-id="292a1-201">Retail Cloud POS</span></span>
-   <span data-ttu-id="292a1-202">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="292a1-202">Retail Hardware Station</span></span>
-   <span data-ttu-id="292a1-203">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="292a1-203">Retail Server</span></span>

<span data-ttu-id="292a1-204">LCS ログ検索に、次の Retail コンポーネントからのログは**含まれません**。</span><span class="sxs-lookup"><span data-stu-id="292a1-204">LCS Log Search does **not** include logs from the following Retail components:</span></span>

-   <span data-ttu-id="292a1-205">Retail レイアウト デザイナー</span><span class="sxs-lookup"><span data-stu-id="292a1-205">Retail layout designer</span></span>
-   <span data-ttu-id="292a1-206">小売受領書デザイナー</span><span class="sxs-lookup"><span data-stu-id="292a1-206">Retail receipt designer</span></span>
-   <span data-ttu-id="292a1-207">Retail Modern POS のセルフ サービス インストーラー</span><span class="sxs-lookup"><span data-stu-id="292a1-207">Self-service installer for Retail Modern POS</span></span>
-   <span data-ttu-id="292a1-208">小売ハードウェア ステーション用のセルフ サービス インストーラー</span><span class="sxs-lookup"><span data-stu-id="292a1-208">Self-service installer for Retail Hardware Station</span></span>

### <a name="access-lcs-log-search"></a><span data-ttu-id="292a1-209">LCS ログ検索にアクセス</span><span class="sxs-lookup"><span data-stu-id="292a1-209">Access LCS Log Search</span></span>

<span data-ttu-id="292a1-210">LCS ログ検索にアクセスするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="292a1-210">To access LCS Log Search, follow these steps.</span></span>

1.  <span data-ttu-id="292a1-211">[Lifecycle Services](https://lcs.dynamics.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="292a1-211">Go to [Lifecycle Services](https://lcs.dynamics.com/).</span></span>
2.  <span data-ttu-id="292a1-212">プロジェクトに関連付けられている資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="292a1-212">Sign in by using the credentials that are associated with your project.</span></span>
3.  <span data-ttu-id="292a1-213">プロジェクト ページで、正しいプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="292a1-213">On the project page, select the correct project.</span></span>
4.  <span data-ttu-id="292a1-214">**プロジェクトの詳細**ページで、正しい環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="292a1-214">On the **Project details** page, select the correct environment.</span></span>
5.  <span data-ttu-id="292a1-215">**環境の詳細**ページで、**環境の監視**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-215">On the **Environment details** page, click **Environment Monitoring**.</span></span>
6.  <span data-ttu-id="292a1-216">**環境の監視**ページで、**未加工ログの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="292a1-216">On the **Environment monitoring** page, click **View raw logs**.</span></span>
7.  <span data-ttu-id="292a1-217">**ログ検索**ページで、次のいずれかのクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="292a1-217">On the **Log Search** page, select one of the following queries:</span></span>
    -   <span data-ttu-id="292a1-218">**小売クライアント イベント** クエリには、Retail Modern POS、Retail Cloud POS、および Retail Hardware Station からのイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="292a1-218">**Retail client events** query, which includes events from Retail Modern POS, Retail Cloud POS, and Retail Hardware Station</span></span>
    -   <span data-ttu-id="292a1-219">Retail Server、Commerce Data Exchange、Commerce Data Exchange: リアルタイム サービス のデータが含まれている**すべてのログ** クエリ</span><span class="sxs-lookup"><span data-stu-id="292a1-219">**All logs** query, which includes data from Retail Server, Commerce Data Exchange, and Commerce Data Exchange: Real-time Service</span></span>

<span data-ttu-id="292a1-220">以下の条件でフィルター処理してクエリを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="292a1-220">You can filter by the following criteria to refine your query:</span></span>

-   <span data-ttu-id="292a1-221">開始および終了日時 (協定世界時 \[UTC\])</span><span class="sxs-lookup"><span data-stu-id="292a1-221">Start and end dates and times (in Coordinated Universal Time \[UTC\])</span></span>
-   <span data-ttu-id="292a1-222">デバイス ID</span><span class="sxs-lookup"><span data-stu-id="292a1-222">Device ID</span></span>
-   <span data-ttu-id="292a1-223">POS ユーザー</span><span class="sxs-lookup"><span data-stu-id="292a1-223">POS user</span></span>
-   <span data-ttu-id="292a1-224">POS アプリケーション セッション ID</span><span class="sxs-lookup"><span data-stu-id="292a1-224">POS application session ID</span></span>
-   <span data-ttu-id="292a1-225">POS ユーザー セッション ID</span><span class="sxs-lookup"><span data-stu-id="292a1-225">POS user session ID</span></span>
-   <span data-ttu-id="292a1-226">重大度</span><span class="sxs-lookup"><span data-stu-id="292a1-226">Severity level</span></span>

<span data-ttu-id="292a1-227">[![環境監視ページの検索結果](./media/log-search-results.png)](./media/log-search-results.png)</span><span class="sxs-lookup"><span data-stu-id="292a1-227">[![Search results on the Environment monitoring page](./media/log-search-results.png)](./media/log-search-results.png)</span></span>



