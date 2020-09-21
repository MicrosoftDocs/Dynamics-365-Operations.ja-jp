---
title: 診断とトラブルシューティングの Commerce コンポーネント イベント
description: このトピックでは、Commerce 固有のコンポーネントからイベントを検索する場所について説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 85493
ms.assetid: a22c9493-c000-4514-bb0d-b3cc674439d9
ms.search.region: Global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4d190b3982f82a5a457c79a25d223ecf0b6266bf
ms.sourcegitcommit: d03f301633175b15d46690fc97067820bf21579f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2020
ms.locfileid: "3775135"
---
# <a name="commerce-component-events-for-diagnostics-and-troubleshooting"></a><span data-ttu-id="202d7-103">診断とトラブルシューティングの Commerce コンポーネント イベント</span><span class="sxs-lookup"><span data-stu-id="202d7-103">Commerce component events for diagnostics and troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="202d7-104">このトピックでは、Commerce 固有のコンポーネントからイベントを検索する場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="202d7-104">This topic explains where to find events from Commerce-specific components.</span></span> <span data-ttu-id="202d7-105">診断とトラブルシューティングを有効にするには、Retail Modern POS などのセルフホスト型のコンポーネントを含むすべての Commerce コンポーネントと Commerce Scale Unit や e コマース モジュールなどのクラウド ホスト型コンポーネントは、それらのイベントにイベント ビューアー (または Retail Cloud F12 などのブラウザー開発ツール コンソール) にローカルでログします。</span><span class="sxs-lookup"><span data-stu-id="202d7-105">To enable diagnostics and troubleshooting, Commerce components, which include self-hosted components such as the Retail Modern POS and cloud-hosted components, such as Commerce Scale Unit and E-Commerce modules, log their events locally to Event Viewer (or to the browser developer tools console such as F12).</span></span> <span data-ttu-id="202d7-106">イベントは、Microsoft Dynamics Lifecycle Services (LCS) ログ検索エクスペリエンスにも記録されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-106">Events are also logged in the Microsoft Dynamics Lifecycle Services (LCS) log search experience.</span></span>


<a name="viewing-events-in-event-viewer"></a><span data-ttu-id="202d7-107">イベント ビューアーでのイベントの表示</span><span class="sxs-lookup"><span data-stu-id="202d7-107">Viewing events in Event Viewer</span></span>
------------------------------

<span data-ttu-id="202d7-108">イベントがログされるコンピューターに対して物理的にアクセスできる場合、イベント ビューアーを使用して、Microsoft Windows を実行するコンピューター上にインストールされたコンポーネント用イベントを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-108">You can use Event Viewer to view events for components that are installed on computers that run Microsoft Windows, if you have physical access to the computer where the events are logged.</span></span> <span data-ttu-id="202d7-109">イベント ビューアーの詳細については、TechNet の [イベント ビューアー](https://technet.microsoft.com/library/4229f239-16a6-4ecd-b3cf-aec03dc08cd5) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="202d7-109">For more information about Event Viewer, see [Event Viewer](https://technet.microsoft.com/library/4229f239-16a6-4ecd-b3cf-aec03dc08cd5) on TechNet.</span></span> <span data-ttu-id="202d7-110">また、イベント ビューアーを使用して、ユーザーがアクセス権を持つコンピューターからリモートでイベントを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-110">You can also use Event Viewer to view events remotely from computers that you have access to.</span></span> <span data-ttu-id="202d7-111">イベント ビューアーを使用して、リモートでイベントを表示する方法の詳細については、TechNet の [リモート コンピューターでイベント ログを使用](https://technet.microsoft.com/library/cc766438.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="202d7-111">For more information about how to use Event Viewer to view events remotely, see [Work with Event Logs on a Remote Computer](https://technet.microsoft.com/library/cc766438.aspx) on TechNet.</span></span> <span data-ttu-id="202d7-112">イベント ビューアは通常、次の使用例でのトラブルシューティングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-112">Typically, Event Viewer is used for troubleshooting in the following use cases:</span></span>

-   <span data-ttu-id="202d7-113">開発者トポロジまたはイベント ビューアーへのアクセスを提供するダウンロード可能な仮想ハードディスク (VHD) での開発。</span><span class="sxs-lookup"><span data-stu-id="202d7-113">Development on a developer topology or on a downloadable virtual hard disk (VHD) that provides access to Event Viewer.</span></span>
-   <span data-ttu-id="202d7-114">会議室パイロットを実行していて、そのコンピューターのイベント ビューアにアクセスできるときのクライアント コンポーネント。</span><span class="sxs-lookup"><span data-stu-id="202d7-114">Client components, when you're running a conference room pilot and have access to Event Viewer for that computer.</span></span>

<span data-ttu-id="202d7-115">ただし、ほとんどの場合、特にコンピューターのイベント ビューアーへのアクセスがない場合、LCS でログ検索を使用できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-115">However, for most other cases, and especially when you don't have access to Event Viewer for the computer, you can use Log Search on LCS.</span></span> <span data-ttu-id="202d7-116">E コマース モジュールに対しては、イベントは現在のところ、ブラウザ開発者ツール (F12キーなど) でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-116">For E-Commerce modules, events are currently available only in browser developer tools (such as F12).</span></span> <span data-ttu-id="202d7-117">ログ検索については、このトピックの後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="202d7-117">Log Search is discussed later in this topic.</span></span> <span data-ttu-id="202d7-118">このセクションは、次のコンポーネントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-118">This section applies to the following components:</span></span>

-   <span data-ttu-id="202d7-119">Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="202d7-119">Commerce Scale Unit</span></span>
-   <span data-ttu-id="202d7-120">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="202d7-120">Retail Modern POS</span></span>
-   <span data-ttu-id="202d7-121">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="202d7-121">Retail Hardware Station</span></span>

### <a name="find-commerce-specific-events-in-event-viewer"></a><span data-ttu-id="202d7-122">イベント ビューアーで、コマース固有のイベントを検索する</span><span class="sxs-lookup"><span data-stu-id="202d7-122">Find Commerce-specific events in Event Viewer</span></span>

<span data-ttu-id="202d7-123">コンピューターでイベント ビューアを起動するには、**開始** ボタンをクリックし、**イベント ビューア** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-123">To start Event Viewer on a computer, right-click the **Start** button, and then click **Event Viewer**.</span></span> 

<span data-ttu-id="202d7-124">[![スタート ボタンのショートカット メニューのイベント ビューアー コマンド](./media/launch-event-viewer.png)](./media/launch-event-viewer.png)</span><span class="sxs-lookup"><span data-stu-id="202d7-124">[![Event Viewer command on the shortcut menu for the Start button](./media/launch-event-viewer.png)](./media/launch-event-viewer.png)</span></span> 

<span data-ttu-id="202d7-125">すべてのコマース固有イベント ログにはイベント ビューアーで次のパスを確認できます。アプリケーションおよびサービス ログ \\Microsoft\\Dynamics 以下のコマース固有のイベント ログを提供します。</span><span class="sxs-lookup"><span data-stu-id="202d7-125">All Commerce-specific event logs can be found under the following path in Event Viewer: Application and Services Logs\\Microsoft\\Dynamics We provide the following Commerce-specific event logs:</span></span>

-   <span data-ttu-id="202d7-126">**Commerce-RetailServer** – このログには、Commerce Scale Unit コンポーネントによって記録されるイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="202d7-126">**Commerce-RetailServer** – This log contains events that are logged by the Commerce Scale Unit components.</span></span>
-   <span data-ttu-id="202d7-127">**Commerce-ModernPos** - このログには、Retail Modern POS によって記録されるイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="202d7-127">**Commerce-ModernPos** – This log contains events that are logged by Retail Modern POS.</span></span> <span data-ttu-id="202d7-128">これらのイベントには、TypeScript および C\# (CRT) レイヤーからのイベントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="202d7-128">These events include events from the TypeScript and C\# (CRT) layer.</span></span>
-   <span data-ttu-id="202d7-129">**Commerce-LoggingProvider** – このログには、この記事の前半で一覧に含まれていない他のすべてのコマース コンポーネントによって記録されるイベントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="202d7-129">**Commerce-LoggingProvider** – This log contains events that are logged by all other Commerce components that aren't included in the list earlier in this article.</span></span>

### <a name="enable-debug-event-logs"></a><span data-ttu-id="202d7-130">デバッグ イベント ログの有効化</span><span class="sxs-lookup"><span data-stu-id="202d7-130">Enable debug event logs</span></span>

<span data-ttu-id="202d7-131">現在、さまざまなコンポーネントによって記録されたイベントの一部がデバッグ イベント ログに送信されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-131">Currently, some of the events that are logged by various components are sent to debug event logs.</span></span> <span data-ttu-id="202d7-132">これらのイベントは非常に高いレートで記録され、詳細なデバッグ シナリオでのみ有用な詳細イベントです。</span><span class="sxs-lookup"><span data-stu-id="202d7-132">These events are verbose events that are logged at very high rates and are useful only for detailed debugging scenarios.</span></span> <span data-ttu-id="202d7-133">イベント ビューアーでのデバッグ イベント ログを有効にするには、この手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="202d7-133">Follow this step to enable the debug event logs in Event Viewer.</span></span>

-   <span data-ttu-id="202d7-134">デバッグ ログを右クリックし、**ログの有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-134">Right-click a debug log, and then click **Enable Log**.</span></span>

<span data-ttu-id="202d7-135">[![デバッグ ログのショートカットメニューでログ コマンドを有効化](./media/enable-debugging-log.png)](./media/enable-debugging-log.png)</span><span class="sxs-lookup"><span data-stu-id="202d7-135">[![Enable Log command on the shortcut menu for a debug log](./media/enable-debugging-log.png)](./media/enable-debugging-log.png)</span></span>

## <a name="viewing-events-by-using-the-f12-browser-developer-tools-console"></a><span data-ttu-id="202d7-136">(F12) ブラウザー開発者ツール コンソールを使用してイベントを表示</span><span class="sxs-lookup"><span data-stu-id="202d7-136">Viewing events by using the (F12) browser developer tools console</span></span>
<span data-ttu-id="202d7-137">Retail Cloud POS と e コマース モジュールはブラウザー ベースのコンポーネントなので、ブラウザー開発者ツール コンソールを使用してそのイベントを表示できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-137">Because Retail Cloud POS and E-Commerce modules are browser-based components, you can use the browser developer tools console to view events for it.</span></span> <span data-ttu-id="202d7-138">Microsoft ブラウザ開発者ツール コンソールの詳細については、[コンソールを使用してエラーとデバッグを表示する](https://docs.microsoft.com/microsoft-edge/devtools-guide/console) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="202d7-138">For information about the Microsoft browser developer tools console, see [Using the Console to view errors and debug](https://docs.microsoft.com/microsoft-edge/devtools-guide/console).</span></span> <span data-ttu-id="202d7-139">Retail Cloud POS または e コマース モジュールのブラウザー開発者ツールを使用するには、サポートされているバージョンのブラウザを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="202d7-139">To use the browser developer tools for Retail Cloud POS or E-Commerce modules, you must use a supported browser version.</span></span>

### <a name="view-events-in-the-browser-developer-tools-console"></a><span data-ttu-id="202d7-140">ブラウザー開発者ツール コンソールでのイベントの表示</span><span class="sxs-lookup"><span data-stu-id="202d7-140">View events in the browser developer tools console</span></span>

1.  <span data-ttu-id="202d7-141">ブラウザーを起動し、Retail Cloud POS または e コマースの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="202d7-141">Start your browser, and navigate to Retail Cloud POS or your E-Commerce website.</span></span>
2.  <span data-ttu-id="202d7-142">F12 キーを押し、**コンソール** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-142">Press F12, and then click the **Console** tab.</span></span>
3.  <span data-ttu-id="202d7-143">Retail Cloud POS または e コマース Web サイトの操作を実行する際に、イベントはコンソールに記録されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-143">As you perform operations on Retail Cloud POS or on your E-Commerce website, events are logged in the console.</span></span> <span data-ttu-id="202d7-144">イベント重要度でフィルター処理して、異なる重要度レベルのイベントを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-144">You can filter by event severity to view events that have different severity levels.</span></span>

<span data-ttu-id="202d7-145">[![ブラウザー開発者ツールのコンソール タブ](./media/browser-console-1024x522.png)](./media/browser-console.png)</span><span class="sxs-lookup"><span data-stu-id="202d7-145">[![Console tab in the browser developer tools](./media/browser-console-1024x522.png)](./media/browser-console.png)</span></span>

## <a name="correlating-events"></a><span data-ttu-id="202d7-146">関連のイベント</span><span class="sxs-lookup"><span data-stu-id="202d7-146">Correlating events</span></span>
<span data-ttu-id="202d7-147">このセクションでは、さまざまなコマース コンポーネントからイベントを関連付ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="202d7-147">This section explains how to correlate events from various Commerce components.</span></span>

### <a name="data-flow-between-a-pos-client-and-commerce-scale-unit"></a><span data-ttu-id="202d7-148">POS クライアントと Commerce Scale Unit 間のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="202d7-148">Data flow between a POS client and Commerce Scale Unit</span></span>

<span data-ttu-id="202d7-149">以下の図は、販売時点管理 (POS) クライアントと Commerce Scale Unit 間のデータ フローを示しています。</span><span class="sxs-lookup"><span data-stu-id="202d7-149">The diagram that follows shows the data flow between a point of sale (POS) client and the Commerce Scale Unit.</span></span>

#### <a name="pos-client-startup"></a><span data-ttu-id="202d7-150">POS クライアントの起動</span><span class="sxs-lookup"><span data-stu-id="202d7-150">POS client startup</span></span>

<span data-ttu-id="202d7-151">ユーザーが POS クライアントを起動すると、新しい AppSessionID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-151">When a user starts a POS client, a new AppSessionID is generated.</span></span> <span data-ttu-id="202d7-152">AppSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-152">The AppSessionID is used to log every event that is instrumented in the POS client.</span></span> <span data-ttu-id="202d7-153">イベント ビューアおよびアプリ インサイトに記録したすべてのイベントはこの ID を持っています。</span><span class="sxs-lookup"><span data-stu-id="202d7-153">All events that are logged to Event Viewer and App Insights have this ID.</span></span>

#### <a name="user-sign-in"></a><span data-ttu-id="202d7-154">ユーザー サインイン</span><span class="sxs-lookup"><span data-stu-id="202d7-154">User sign-in</span></span>

<span data-ttu-id="202d7-155">ユーザーが POS クライアントにサインインすると、新しい UserSessionID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-155">When a user signs in to a POS client, a new UserSessionID is generated.</span></span> <span data-ttu-id="202d7-156">UserSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-156">The UserSessionID is used to log every event that is instrumented in the POS client.</span></span> <span data-ttu-id="202d7-157">イベント ビューアーに記録されたすべてのユーザー イベントはこの ID を持ちます。</span><span class="sxs-lookup"><span data-stu-id="202d7-157">All user events that are logged to Event Viewer have this ID.</span></span> <span data-ttu-id="202d7-158">この ID は、ユーザーがログインしている間維持されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-158">This ID is maintained for as long as the user is signed in.</span></span> <span data-ttu-id="202d7-159">現在のユーザーがサインアウトして、新しいユーザーがログインすると、新しい UserSessionID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-159">When the current user signs out and a new user sign in, a new UserSessionID is generated.</span></span>

#### <a name="pos-client-calls-to-commerce-scale-unit"></a><span data-ttu-id="202d7-160">POS クライアントによる Commerce Scale Unit への呼び出し</span><span class="sxs-lookup"><span data-stu-id="202d7-160">POS client calls to Commerce Scale Unit</span></span>

<span data-ttu-id="202d7-161">POS クライアントが Commerce Scale Unit を呼び出すときはいつでも、AppSessionID と UserSessionID がヘッダーとして送信されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-161">Whenever a POS client makes a call to the Commerce Scale Unit, the AppSessionID and UserSessionID are sent as headers.</span></span> <span data-ttu-id="202d7-162">次に、Commerce Scale Unit は、受信要求 (イベント ID 5000) のイベントを記録します。</span><span class="sxs-lookup"><span data-stu-id="202d7-162">The Commerce Scale Unit then logs an event for the incoming request (Event ID 5000).</span></span> <span data-ttu-id="202d7-163">このイベントには、2 つの ID と ActivityID が含まれます。</span><span class="sxs-lookup"><span data-stu-id="202d7-163">This event includes those two IDs and also an ActivityID.</span></span> <span data-ttu-id="202d7-164">その後、ActivityID はすべての関連するイベントにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-164">The ActivityID is then also used for all related events.</span></span> <span data-ttu-id="202d7-165">AppSessionID、UserSessionID、ActivityID は、Commerce Scale Unit がホストされているイベント ログで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="202d7-165">The AppSessionID, UserSessionID, and ActivityID are available in the event log where Commerce Scale Unit is hosted.</span></span> <span data-ttu-id="202d7-166">LCS ログ検索でも利用できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-166">They are also available in LCS Log Search.</span></span>

#### <a name="request-activity-on-commerce-scale-unit"></a><span data-ttu-id="202d7-167">Commerce Scale Unit での要求の活動</span><span class="sxs-lookup"><span data-stu-id="202d7-167">Request activity on Commerce Scale Unit</span></span>

<span data-ttu-id="202d7-168">Commerce Scale Unit 要求の一部として記録されるすべてのイベントは、最初の受信要求イベント用に記録された初期イベントと同じ ActivityID を持ちます (イベント ID 5000)。</span><span class="sxs-lookup"><span data-stu-id="202d7-168">Every event that is logged as part of a Commerce Scale Unit request has the same ActivityID as the initial event that was logged for the initial incoming request event (Event ID 5000).</span></span> <span data-ttu-id="202d7-169">これらのイベントは、イベント ビューアーと LCS ログ検索の両方で利用できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-169">These events are available in both Event Viewer and LCS Log Search.</span></span> 

<span data-ttu-id="202d7-170">[![POS クライアントと Commerce Scale Unit 間のデータ フロー](./media/event-log-data-flow1-1018x1024.png)](./media/event-log-data-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="202d7-170">[![Data flow between a POS client and Commerce Scale Unit](./media/event-log-data-flow1-1018x1024.png)](./media/event-log-data-flow1.png)</span></span>

### <a name="finding-retail-modern-pos-events-in-event-viewer"></a><span data-ttu-id="202d7-171">イベント ビューアーでの Retail Modern POS イベントの検索</span><span class="sxs-lookup"><span data-stu-id="202d7-171">Finding Retail Modern POS events in Event Viewer</span></span>

<span data-ttu-id="202d7-172">Retail Modern POS によってが記録されたすべてのイベントには、次のデータ点が含まれています。</span><span class="sxs-lookup"><span data-stu-id="202d7-172">Every event that is logged by Retail Modern POS includes the following data points:</span></span>

-   <span data-ttu-id="202d7-173">**AppSessionID** - アプリケーションが最初に起動されたときに生成される一意の ID。</span><span class="sxs-lookup"><span data-stu-id="202d7-173">**AppSessionID** – A unique ID that is generated when the app is first started.</span></span> <span data-ttu-id="202d7-174">これは記録されるすべてのイベントに含まれています。</span><span class="sxs-lookup"><span data-stu-id="202d7-174">It's included with every event that is logged.</span></span>
-   <span data-ttu-id="202d7-175">**UserSessionID** – ユーザーが Retail Modern POS にサインインするときに生成される固有の ID。</span><span class="sxs-lookup"><span data-stu-id="202d7-175">**UserSessionID** – A unique ID that is generated when a user signs in to Retail Modern POS.</span></span> <span data-ttu-id="202d7-176">これはユーザーがサインインしている限り、記録されるすべてのイベントに含まれています。</span><span class="sxs-lookup"><span data-stu-id="202d7-176">It's included with every event that is logged, for as long as the user remains signed in.</span></span> <span data-ttu-id="202d7-177">新しいユーザーがサインインするとき、新しい UserSessionID が作成されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-177">When a new user signs in, a new UserSessionID is created.</span></span>

<span data-ttu-id="202d7-178">AppSessionID 値および UserSessionID 値は、Retail Modern POS がインストールされているマシン上のイベント ビューアーの**詳細**タブで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-178">You can find the AppSessionID and UserSessionID values on the **Details** tab in Event Viewer on the machine where Retail Modern POS is installed.</span></span> 

<span data-ttu-id="202d7-179">[![イベント ビューアーの詳細タブ](./media/correlation-1024x672.png)](./media/correlation.png)</span><span class="sxs-lookup"><span data-stu-id="202d7-179">[![Details tab in Event Viewer](./media/correlation-1024x672.png)](./media/correlation.png)</span></span>

### <a name="finding-incoming-commerce-scale-unit-request-events-in-event-viewer"></a><span data-ttu-id="202d7-180">イベント ビューアーで、受信する Commerce Scale Unit 要求のイベントを検索</span><span class="sxs-lookup"><span data-stu-id="202d7-180">Finding incoming Commerce Scale Unit request events in Event Viewer</span></span>

<span data-ttu-id="202d7-181">イベント ビューアで受信する Commerce Scale Unit 要求のデータを関連付けるには、最初に **Analytic** チャネルを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="202d7-181">To correlate data for incoming Commerce Scale Unit requests in Event Viewer, you must first enable the **Analytic** channel.</span></span> <span data-ttu-id="202d7-182">分析チャネルを有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="202d7-182">To enable the Analytic channel, follow these steps.</span></span>

1.  <span data-ttu-id="202d7-183">イベント ビューアーの左ウィンドウで、**Commerce RetailServer** を選択します。</span><span class="sxs-lookup"><span data-stu-id="202d7-183">In Event Viewer, in the left pane, select **Commerce-RetailServer**.</span></span>
2.  <span data-ttu-id="202d7-184">**表示** &gt; **分析とデバッグ ログを有効にします**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-184">Click **View** &gt; **Enable Analytic and Debug log**.</span></span> <span data-ttu-id="202d7-185">分析チャネルの新しいノードは、**Commerce-RetailServer** ログ プロバイダーの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-185">A new node for the Analytic channel appears under the **Commerce-RetailServer** logging provider.</span></span>
3.  <span data-ttu-id="202d7-186">**分析** ノードを右クリックし、**ログの有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-186">Right-click the **Analytic** node, and then click **Enable log**.</span></span>

<span data-ttu-id="202d7-187">イベント ビューアーでは、受信しているすべての Commerce Scale Unit の要求がイベント 5000 として Commerce-RetailServer ソースの分析チャネルに記録されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-187">In Event Viewer, all incoming Commerce Scale Unit requests are logged to the Analytic channel of the Commerce-RetailServer source as event 5000.</span></span> <span data-ttu-id="202d7-188">これらのイベントには、前述した AppSessionID と UserSessionID もあります。</span><span class="sxs-lookup"><span data-stu-id="202d7-188">These events also have the AppSessionID and UserSessionID that were described earlier.</span></span> <span data-ttu-id="202d7-189">すべてのイベントには、同じ要求のログに記録されたイベントごとに、固有の ActivityID も用意されています。</span><span class="sxs-lookup"><span data-stu-id="202d7-189">Every event also has a unique ActivityID that is instrumented for every logged event for the same request.</span></span>

## <a name="using-lcs-log-search"></a><span data-ttu-id="202d7-190">LCS ログ検索の使用</span><span class="sxs-lookup"><span data-stu-id="202d7-190">Using LCS Log Search</span></span>
<span data-ttu-id="202d7-191">LCS ログ検索で、1 つのポータルからすべてのコンポーネントのデータを表示できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-191">LCS Log Search lets you view data from all the components from a single portal.</span></span> <span data-ttu-id="202d7-192">イベントは、(Commerce Scale Unit などの) クラウドでホストされたコンポーネントと (Retail Modern POS および Retail Hardware Station などの) 店舗内コンポーネントの両方からアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-192">You can access events from both cloud-hosted components (such as Commerce Scale Unit) and in-store components (such as Retail Modern POS and Retail Hardware Station).</span></span> <span data-ttu-id="202d7-193">すべてのクラウドホストおよびストア内コンポーネントからのイベント データは、索引付けされ検索可能になる LCS ログ検索に流れます。</span><span class="sxs-lookup"><span data-stu-id="202d7-193">Event data from all cloud-hosted and in-store components flows to LCS Log Search, where it's indexed and made searchable.</span></span> <span data-ttu-id="202d7-194">データは通常、記録されてから 5 分以内に利用可能です。</span><span class="sxs-lookup"><span data-stu-id="202d7-194">Data is typically available within 5 minutes after it's logged.</span></span> <span data-ttu-id="202d7-195">POS クライアントおよび Retail Hardware Station では、すべてのイベントが永続ストレージにローカルでキュー格納され、キューがいっぱいになった後にバッチでアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="202d7-195">For POS clients and Retail Hardware Station, all events are locally queued in persistent storage and then uploaded in batches after the queue is filled.</span></span> <span data-ttu-id="202d7-196">この動作により、ネットワーク トラフィックを最適化できます。 </span><span class="sxs-lookup"><span data-stu-id="202d7-196">This behavior enables network traffic to be optimized.</span></span> <span data-ttu-id="202d7-197">また、インターネット接続がない場合でもイベントを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-197">It also enables events to be saved even when there is no Internet connectivity.</span></span> <span data-ttu-id="202d7-198">接続が回復した後、すべての保留中のイベントがアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="202d7-198">After connectivity is restored, all pending events are uploaded.</span></span> 

<span data-ttu-id="202d7-199">LCS ログ検索は、HA 運用トポロジに使用できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-199">LCS Log Search is available for the HA production topology.</span></span> <span data-ttu-id="202d7-200">次のコマースのコンポーネントに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-200">It can be used for the following Commerce components:</span></span>

-   <span data-ttu-id="202d7-201">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="202d7-201">Retail Modern POS</span></span>
-   <span data-ttu-id="202d7-202">Retail Cloud POS</span><span class="sxs-lookup"><span data-stu-id="202d7-202">Retail Cloud POS</span></span>
-   <span data-ttu-id="202d7-203">Commerce Scale Unit (Retail Cloud Scale Unit で実行中)</span><span class="sxs-lookup"><span data-stu-id="202d7-203">Commerce Scale Unit (running on Retail Cloud Scale Unit)</span></span>

<span data-ttu-id="202d7-204">LCS ログ検索に、次のコマース コンポーネントからのログは**含まれません**。</span><span class="sxs-lookup"><span data-stu-id="202d7-204">LCS Log Search does **not** include logs from the following Commerce components:</span></span>

-   <span data-ttu-id="202d7-205">コマース レイアウト デザイナー</span><span class="sxs-lookup"><span data-stu-id="202d7-205">Commerce layout designer</span></span>
-   <span data-ttu-id="202d7-206">コマース受領書デザイナー</span><span class="sxs-lookup"><span data-stu-id="202d7-206">Commerce receipt designer</span></span>
-   <span data-ttu-id="202d7-207">Retail Modern POS のセルフ サービス インストーラー</span><span class="sxs-lookup"><span data-stu-id="202d7-207">Self-service installer for Retail Modern POS</span></span>
-   <span data-ttu-id="202d7-208">小売ハードウェア ステーション用のセルフ サービス インストーラー</span><span class="sxs-lookup"><span data-stu-id="202d7-208">Self-service installer for Retail Hardware Station</span></span>
-   <span data-ttu-id="202d7-209">Commerce Scale Unit (Retail Store Scale Unit で実行中)</span><span class="sxs-lookup"><span data-stu-id="202d7-209">Commerce Scale Unit (running on Retail Store Scale Unit)</span></span>
-   <span data-ttu-id="202d7-210">Retail ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="202d7-210">Retail Hardware Station</span></span>

### <a name="access-lcs-log-search"></a><span data-ttu-id="202d7-211">LCS ログ検索にアクセス</span><span class="sxs-lookup"><span data-stu-id="202d7-211">Access LCS Log Search</span></span>

<span data-ttu-id="202d7-212">LCS ログ検索にアクセスするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="202d7-212">To access LCS Log Search, follow these steps.</span></span>

1.  <span data-ttu-id="202d7-213">[Lifecycle Services](https://lcs.dynamics.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="202d7-213">Go to [Lifecycle Services](https://lcs.dynamics.com/).</span></span>
2.  <span data-ttu-id="202d7-214">プロジェクトに関連付けられている資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="202d7-214">Sign in by using the credentials that are associated with your project.</span></span>
3.  <span data-ttu-id="202d7-215">プロジェクト ページで、正しいプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="202d7-215">On the project page, select the correct project.</span></span>
4.  <span data-ttu-id="202d7-216">**プロジェクトの詳細**ページで、正しい環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="202d7-216">On the **Project details** page, select the correct environment.</span></span>
5.  <span data-ttu-id="202d7-217">**環境の詳細**ページで、**環境の監視**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-217">On the **Environment details** page, click **Environment Monitoring**.</span></span>
6.  <span data-ttu-id="202d7-218">**環境の監視**ページで、**未加工ログの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="202d7-218">On the **Environment monitoring** page, click **View raw logs**.</span></span>
7.  <span data-ttu-id="202d7-219">**ログ検索**ページで、次のいずれかのクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="202d7-219">On the **Log Search** page, select one of the following queries:</span></span>
    -   <span data-ttu-id="202d7-220">**コマース クライアント イベント** クエリには、Retail Modern POS、Retail Cloud POS、および Commerce Scale Unit (Retail Cloud Scale Unit で実行中) からのイベントが含まれます</span><span class="sxs-lookup"><span data-stu-id="202d7-220">**Commerce client events** query, which includes events from Retail Modern POS, Retail Cloud POS, and Commerce Scale Unit (running on Retail Cloud Scale Unit)</span></span>
    -   <span data-ttu-id="202d7-221">**すべてのログ** クエリには、Commerce Scale Unit、Commerce Data Exchange、および Commerce Data Exchange: リアルタイム サービスからのデータが含まれます</span><span class="sxs-lookup"><span data-stu-id="202d7-221">**All logs** query, which includes data from Commerce Scale Unit, Commerce Data Exchange, and Commerce Data Exchange: Real-time Service</span></span>

<span data-ttu-id="202d7-222">以下の条件でフィルター処理してクエリを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="202d7-222">You can filter by the following criteria to refine your query:</span></span>

-   <span data-ttu-id="202d7-223">開始および終了日時 (協定世界時 \[UTC\])</span><span class="sxs-lookup"><span data-stu-id="202d7-223">Start and end dates and times (in Coordinated Universal Time \[UTC\])</span></span>
-   <span data-ttu-id="202d7-224">デバイス ID</span><span class="sxs-lookup"><span data-stu-id="202d7-224">Device ID</span></span>
-   <span data-ttu-id="202d7-225">POS ユーザー</span><span class="sxs-lookup"><span data-stu-id="202d7-225">POS user</span></span>
-   <span data-ttu-id="202d7-226">POS アプリケーション セッション ID</span><span class="sxs-lookup"><span data-stu-id="202d7-226">POS application session ID</span></span>
-   <span data-ttu-id="202d7-227">POS ユーザー セッション ID</span><span class="sxs-lookup"><span data-stu-id="202d7-227">POS user session ID</span></span>
-   <span data-ttu-id="202d7-228">重大度</span><span class="sxs-lookup"><span data-stu-id="202d7-228">Severity level</span></span>

<span data-ttu-id="202d7-229">[![環境監視ページの検索結果](./media/log-search-results.png)](./media/log-search-results.png)</span><span class="sxs-lookup"><span data-stu-id="202d7-229">[![Search results on the Environment monitoring page](./media/log-search-results.png)](./media/log-search-results.png)</span></span>

### <a name="e-commerce-events"></a><span data-ttu-id="202d7-230">E コマース イベント</span><span class="sxs-lookup"><span data-stu-id="202d7-230">E-Commerce events</span></span>
<span data-ttu-id="202d7-231">次のイベントは、e コマース Web サイトによって記録され、トラブルシューティングに直接ブラウザーで、または分析、実験、またはその他の目的でパートナー拡張機能を使用してプログラムで処理できます。</span><span class="sxs-lookup"><span data-stu-id="202d7-231">The following events are logged by the E-Commerce website, and can be consumed for troubleshooting directly in the browser, or programmatically by partner extensions for analytics, experimentation, or other purposes.</span></span>

### <a name="button-and-link-clicks"></a><span data-ttu-id="202d7-232">ボタンとリンクのクリック</span><span class="sxs-lookup"><span data-stu-id="202d7-232">Button and link clicks</span></span>
<span data-ttu-id="202d7-233">ボタンとリンクのクリックにより、E コマース Web サイト上の次のタイプの要素がテレメトリイベントとして記録されます。</span><span class="sxs-lookup"><span data-stu-id="202d7-233">Button and link clicks for the following types of elements on an E-Commerce website are logged as telemetry events.</span></span>

- <span data-ttu-id="202d7-234">表題</span><span class="sxs-lookup"><span data-stu-id="202d7-234">Header</span></span>
  - <span data-ttu-id="202d7-235">ナビゲーション階層</span><span class="sxs-lookup"><span data-stu-id="202d7-235">Navigation hierarchy</span></span>
  - <span data-ttu-id="202d7-236">カート アイコン</span><span class="sxs-lookup"><span data-stu-id="202d7-236">Cart icon</span></span>
  - <span data-ttu-id="202d7-237">サインイン</span><span class="sxs-lookup"><span data-stu-id="202d7-237">Sign-in</span></span>
  - <span data-ttu-id="202d7-238">検索アイコン</span><span class="sxs-lookup"><span data-stu-id="202d7-238">Search icon</span></span>
  - <span data-ttu-id="202d7-239">Wishlist アイコン</span><span class="sxs-lookup"><span data-stu-id="202d7-239">Wishlist icon</span></span>
- <span data-ttu-id="202d7-240">コンテンツ ブロック アクション リンク (これは、マーケティング コンテンツ用のヒーロー、タイル、およびフィーチャー の内容を表します)</span><span class="sxs-lookup"><span data-stu-id="202d7-240">Content block action links (This represents the hero, tile, and feature modules for marketing content.)</span></span>
- <span data-ttu-id="202d7-241">ビデオ プレーヤー</span><span class="sxs-lookup"><span data-stu-id="202d7-241">Video player</span></span>
- <span data-ttu-id="202d7-242">製品カード</span><span class="sxs-lookup"><span data-stu-id="202d7-242">Product cards</span></span>
- <span data-ttu-id="202d7-243">フッター リンク</span><span class="sxs-lookup"><span data-stu-id="202d7-243">Footer links</span></span>
- <span data-ttu-id="202d7-244">階層リンク</span><span class="sxs-lookup"><span data-stu-id="202d7-244">Breadcrumbs</span></span>
- <span data-ttu-id="202d7-245">広告バナー</span><span class="sxs-lookup"><span data-stu-id="202d7-245">Promo banner</span></span>
- <span data-ttu-id="202d7-246">カートに追加ボタン</span><span class="sxs-lookup"><span data-stu-id="202d7-246">Add to cart button</span></span>
- <span data-ttu-id="202d7-247">チェックアウト ボタン</span><span class="sxs-lookup"><span data-stu-id="202d7-247">Checkout button</span></span>
- <span data-ttu-id="202d7-248">注文する ボタン</span><span class="sxs-lookup"><span data-stu-id="202d7-248">Place order button</span></span>
