---
title: "モバイル プラットフォームのホーム ページ"
description: "モバイル プラットフォームを使用して、ワークスペースのモバイル アプリを作成できます。"
author: RobinARH
manager: AnnBe
ms.date: 05/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: 
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: f53ecd61cdfbc9d93c9658b433a6bc9a591892c4
ms.openlocfilehash: 084a3cd5b03a9c31610b9dd38bb2ec254899d7e9
ms.contentlocale: ja-jp
ms.lasthandoff: 06/08/2018

---

# <a name="mobile-platform"></a><span data-ttu-id="12412-103">モバイル プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="12412-103">Mobile platform</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12412-104">モバイル アプリケーションを使用することにより、Microsoft Dynamics 365 for Finance and Operations からビジネス ロジックおよびモデリングを再利用することができます。</span><span class="sxs-lookup"><span data-stu-id="12412-104">By using mobile apps, you can reuse business logic and modeling from Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="12412-105">モバイル アプリで、豊富なオフラインおよびモバイルの相互関係と、扱いやすいデザイナー体験を可能にします。</span><span class="sxs-lookup"><span data-stu-id="12412-105">Mobile apps enable rich offline and mobile interactions, and provide an easy-to-use designer experience.</span></span> <span data-ttu-id="12412-106">開発者は、Microsoft Visual Studio で簡単なフォームを作成し、この機能を公開するモバイル アプリを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="12412-106">Developers can create simplified forms in Microsoft Visual Studio and then design mobile apps that expose this functionality.</span></span> <span data-ttu-id="12412-107">モバイル プラットフォームを使用すると、フォームやモバイル アプリの定義を簡単に変更して、Finance and Operations に加えられたカスタマイズを組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="12412-107">The mobile platform makes it easy to change the forms and mobile app definitions to include customizations that are made to Finance and Operations.</span></span> 

## <a name="get-started"></a><span data-ttu-id="12412-108">使用開始</span><span class="sxs-lookup"><span data-stu-id="12412-108">Get started</span></span>

+ [<span data-ttu-id="12412-109">はじめに</span><span class="sxs-lookup"><span data-stu-id="12412-109">Getting started</span></span>](mobile-platform-getting-started.md) 
+ [<span data-ttu-id="12412-110">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="12412-110">Architecture</span></span>](mobile-platform-architecture.md) 
+ [<span data-ttu-id="12412-111">ページ デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="12412-111">Page design guidelines</span></span>](page-design-guidelines.md)
+ [<span data-ttu-id="12412-112">アクション デザインのガイドライン</span><span class="sxs-lookup"><span data-stu-id="12412-112">Action design guidelines</span></span>](action-design-guidelines.md)
+ [<span data-ttu-id="12412-113">フォーム デザインの要件</span><span class="sxs-lookup"><span data-stu-id="12412-113">Form design requirements</span></span>](form-design-requirements.md)

<span data-ttu-id="12412-114">モバイル アプリの作成方法を示す次のハウツー ビデオ シリーズをチェック アウトしてください。</span><span class="sxs-lookup"><span data-stu-id="12412-114">Check out the following series of how-to videos that show how to create a mobile app.</span></span>

+ [<span data-ttu-id="12412-115">チュートリアル 1: 販売注文のページを構築する</span><span class="sxs-lookup"><span data-stu-id="12412-115">Tutorial 1: Building the sales order page</span></span>](https://youtu.be/PdegfBxifl8)
+ [<span data-ttu-id="12412-116">チュートリアル 2: 販売注文詳細ページを構築する</span><span class="sxs-lookup"><span data-stu-id="12412-116">Tutorial 2: Building the sales order details page</span></span>](https://youtu.be/mF-vlbnRte0)
+ [<span data-ttu-id="12412-117">チュートリアル 3: 新しい販売注文アクション作成を構築する</span><span class="sxs-lookup"><span data-stu-id="12412-117">Tutorial 3: Building the create new sales order action</span></span>](https://youtu.be/VYw9oTv9t3o)
+ [<span data-ttu-id="12412-118">チュートリアル 4: 新しい販売注文アクション作成にルックアップを追加する</span><span class="sxs-lookup"><span data-stu-id="12412-118">Tutorial 4: Adding a lookup to the create new sales order action</span></span>](https://youtu.be/eNJKd0IYmZk)
+ [<span data-ttu-id="12412-119">チュートリアル 5: ルックアップの追加し、モバイル ビジネス ロジックを使用してページを非表示にする</span><span class="sxs-lookup"><span data-stu-id="12412-119">Tutorial 5: Adding a lookup and hiding pages using mobile business logic</span></span>](https://youtu.be/kIJKk9J8FvI)

## <a name="common-configurations"></a><span data-ttu-id="12412-120">一般的な構成</span><span class="sxs-lookup"><span data-stu-id="12412-120">Common configurations</span></span>
<span data-ttu-id="12412-121">これらのトピックでは、モバイル アプリに追加できる一般的なカスタマイズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="12412-121">These topics describe some common customizations that you can add to your mobile app.</span></span>

+ [<span data-ttu-id="12412-122">モバイル ワークスペースのローカライズ</span><span class="sxs-lookup"><span data-stu-id="12412-122">Localize mobile workspaces</span></span>](scenarios/localize-workspaces-on-server.md)
+ [<span data-ttu-id="12412-123">モバイル ワークスペースのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="12412-123">Help secure mobile workspaces</span></span>](scenarios/secure-mobile-workspace.md)
+ [<span data-ttu-id="12412-124">クリック可能なフィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="12412-124">Set up clickable fields</span></span>](scenarios/make-workspace-field-clickable.md)
+ [<span data-ttu-id="12412-125">ワークスペース クラスを使用して必須フィールドを設定する</span><span class="sxs-lookup"><span data-stu-id="12412-125">Set up mandatory fields through workspace classes</span></span>](scenarios/make-field-mandatory.md)
+ [<span data-ttu-id="12412-126">フィールドに品目数を表示する</span><span class="sxs-lookup"><span data-stu-id="12412-126">Display item counts in a field</span></span>](scenarios/display-count-workspace.md)

## <a name="client-side-development"></a><span data-ttu-id="12412-127">クライアント側の開発</span><span class="sxs-lookup"><span data-stu-id="12412-127">Client-side development</span></span>

<span data-ttu-id="12412-128">クライアント側の API はビジネス ロジック ファイルで使用されます。この API は、カスタマイズ可能なモバイルワーク スペースに拡張レイヤーを提供します。</span><span class="sxs-lookup"><span data-stu-id="12412-128">Client-side APIs are used in the business logic file, which provides an extensibility layer to the mobile workspace that allows for customization.</span></span> <span data-ttu-id="12412-129">クライアント側の API を通じてアクセスしたり操作したりできるものは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="12412-129">Some things that you can access and influence through the client-side APIs include:</span></span>
+ <span data-ttu-id="12412-130">メタデータ</span><span class="sxs-lookup"><span data-stu-id="12412-130">Metadata</span></span>
+ <span data-ttu-id="12412-131">ランタイム コントロール/ページ インスタンス</span><span class="sxs-lookup"><span data-stu-id="12412-131">Runtime control/page instances</span></span>
+ <span data-ttu-id="12412-132">業務データ</span><span class="sxs-lookup"><span data-stu-id="12412-132">Business data</span></span>
+ <span data-ttu-id="12412-133">オフライン-最初の業務動作</span><span class="sxs-lookup"><span data-stu-id="12412-133">Offline-first business behaviors</span></span>
+ <span data-ttu-id="12412-134">レイアウトおよびスタイル</span><span class="sxs-lookup"><span data-stu-id="12412-134">Layout and style</span></span>

<span data-ttu-id="12412-135">クライアント側の開発のプロセスは次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="12412-135">The process for client-side development is described in these topics:</span></span>
+ [<span data-ttu-id="12412-136">クライアント側の設計 API の概要</span><span class="sxs-lookup"><span data-stu-id="12412-136">Client-side design APIs overview</span></span>](scenarios/client-api-design-overview.md)
+ [<span data-ttu-id="12412-137">ビジネス ロジック イベントの概要</span><span class="sxs-lookup"><span data-stu-id="12412-137">Business logic events overview</span></span>](business-logic-events-overview.md)
+ [<span data-ttu-id="12412-138">クライアント API</span><span class="sxs-lookup"><span data-stu-id="12412-138">Client APIs</span></span>](client-apis/client-apis-reference.md)

<span data-ttu-id="12412-139">引当管理ワークスペースのためにサンプルのビジネス ロジック ファイル (.js ファイル名拡張子付き) をダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="12412-139">You can download a sample business logic file (with a .js file name extension) for the Reservation management workspace.</span></span> <span data-ttu-id="12412-140">[Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) に移動し、**business_logic フォルダ**を開き、FM.js ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="12412-140">Go to [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples), open the **business_logic folder**, and locate the FM.js file</span></span>

## <a name="server-side-development"></a><span data-ttu-id="12412-141">サーバー側の開発</span><span class="sxs-lookup"><span data-stu-id="12412-141">Server-side development</span></span>

<span data-ttu-id="12412-142">ワークスペースの属性とクラスは、サーバー上でワークスペースを作成、構成、および公開するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="12412-142">Workspace attributes and classes are used to create, configure, and publish workspaces on the server.</span></span> <span data-ttu-id="12412-143">タスク レコーダー ベースのメカニズムを使用してワークスペースを構築する代わりに、これらのサーバー側 X++ API を使用できます。</span><span class="sxs-lookup"><span data-stu-id="12412-143">These server-side X++ APIs can be used instead of using the task recorder-based mechanism to build a workspace.</span></span> <span data-ttu-id="12412-144">いずれかのメカニズムを使用して作成されたワークスペースは、クライアント側 API を使用してスタイルを設定して強化することができます。</span><span class="sxs-lookup"><span data-stu-id="12412-144">Workspaces created using either mechanism can then be styled and augmented using the client-side APIs.</span></span>

<span data-ttu-id="12412-145">サーバー側開発は、次のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="12412-145">Server-side development is described in these topics:</span></span>
+ [<span data-ttu-id="12412-146">ワークスペース クラスの概要</span><span class="sxs-lookup"><span data-stu-id="12412-146">Workspace class overview</span></span>](scenarios/mobile-workspace-configuration.md)
+ [<span data-ttu-id="12412-147">サーバー APIs (X++)</span><span class="sxs-lookup"><span data-stu-id="12412-147">Server APIs (X++)</span></span>](mobile-workspace-server-apis.md)

<span data-ttu-id="12412-148">フリート管理モバイル アプリのサンプル プロジェクト (.axpp ファイル名拡張子付き) をダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="12412-148">You can download the sample project (with an .axpp file name extension) for the Fleet Management mobile app.</span></span> <span data-ttu-id="12412-149">[Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) に移動し、**FMMobileApp.axpp** ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="12412-149">Go to [Dynamics365-for-Operations-mobile-FleetManagementSamples](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) and download the **FMMobileApp.axpp** file.</span></span>

## <a name="debugging-during-development"></a><span data-ttu-id="12412-150">開発時のデバッグ</span><span class="sxs-lookup"><span data-stu-id="12412-150">Debugging during development</span></span>

<span data-ttu-id="12412-151">展開中に、バックグラウンドで何が起きているのかをより詳細な情報と洞察を得るために、デバッガーを添付すると便利です。</span><span class="sxs-lookup"><span data-stu-id="12412-151">During development it can be useful to attach a debugger to get more detailed information and insight into what is happening in the background.</span></span> <span data-ttu-id="12412-152">Web デバッガーは、クライアント側の JavaScript ロジックとスタイルで使用することができ、Visual Studio デバッガーは、サーバー側の X++ ビジネス ロジックで使用できます。</span><span class="sxs-lookup"><span data-stu-id="12412-152">A web debugger can be used with the client-side JavaScript logic and styling and the Visual Studio debugger can be used with the server-side X++ business logic.</span></span>

### <a name="debugging-the-client-side"></a><span data-ttu-id="12412-153">クライアント側のデバッグ</span><span class="sxs-lookup"><span data-stu-id="12412-153">Debugging the client side</span></span> 

#### <a name="prerequisites"></a><span data-ttu-id="12412-154">前提条件</span><span class="sxs-lookup"><span data-stu-id="12412-154">Prerequisites</span></span>
- <span data-ttu-id="12412-155">Android デバイスに加えて PC</span><span class="sxs-lookup"><span data-stu-id="12412-155">Android device plus PC</span></span>
- <span data-ttu-id="12412-156">Azure でホストされた開発マシン (モバイル デバイスで指定できます)</span><span class="sxs-lookup"><span data-stu-id="12412-156">Azure-hosted development machine (so the mobile device can point to it)</span></span>

#### <a name="steps-to-debug-the-client-side"></a><span data-ttu-id="12412-157">クライアント側をデバッグする手順</span><span class="sxs-lookup"><span data-stu-id="12412-157">Steps to debug the client side</span></span>
1. <span data-ttu-id="12412-158">Azure でホストされた開発マシンで公開されている Web クライアントで、Unified Operations アプリ用に公開されたモバイル ワークスペースがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12412-158">On the web client that is exposed by the Azure-hosted development machine, ensure that there are mobile workspaces published for the Unified Operations app.</span></span> <span data-ttu-id="12412-159">モバイル ワークスペースを公開する方法については、[モバイル ワークスペースの公開](../publish-mobile-workspace.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12412-159">For information about publishing a mobile workspace, see [Publish a mobile workspace](../publish-mobile-workspace.md).</span></span>

2. <span data-ttu-id="12412-160">Android デバイスで Unified Operations アプリの Android デバッグ apk をインストールします。</span><span class="sxs-lookup"><span data-stu-id="12412-160">Install the Android debug apk for the Unified Operations app on an Android device:</span></span>
    - <span data-ttu-id="12412-161">1 回のみ、apk ファイルのインストールを許可 -  **メニュー** > **設定** > **セキュリティ**の順に移動し、電話が Google Play ストア以外のソースからアプリをインストールするのを許可するよう**未知のソース**を確認します。</span><span class="sxs-lookup"><span data-stu-id="12412-161">One time only, allow the installation of apk files -  Go to **Menu** > **Settings** > **Security** and then check **Unknown Sources** to allow the phone to install apps from sources other than the Google Play Store.</span></span>
    - <span data-ttu-id="12412-162">Unified Operations アプリケーションのアンインストール - Unified Operations アプリケーションの以前のバージョンがアンインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12412-162">Uninstall the Unified Operations app - Ensure that any previous version of the Unified Operations app has been uninstalled.</span></span>
    - <span data-ttu-id="12412-163">デバイスのブラウザーから apk ファイルをダウンロードして、[Unified Operations Android debug apk on Github](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples/blob/master/android-debug.apk) に移動し、**ダウンロード** (または [ファイルへの直接リンク](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples/raw/master/android-debug.apk)) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12412-163">Download the apk file - From the device’s browser, navigate to the latest [Unified Operations Android debug apk on Github](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples/blob/master/android-debug.apk) and click **Download** (or use [this direct link to the file](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples/raw/master/android-debug.apk)).</span></span>
    - <span data-ttu-id="12412-164">Unified Operations apk ファイルをインストール - apk ファイル経由で Unified Operations アプリのインストールを確認します。</span><span class="sxs-lookup"><span data-stu-id="12412-164">Install the Unified Operations apk file - Confirm install of the Unified Operations app via the apk file.</span></span>
    - <span data-ttu-id="12412-165">デバイスのデバッグ Unified Operations アプリケーションを実行し、サインインします。</span><span class="sxs-lookup"><span data-stu-id="12412-165">Run the debug Unified Operations app on the device and sign in.</span></span>

3. <span data-ttu-id="12412-166">デバッグ マシンからデバイスに接続します。</span><span class="sxs-lookup"><span data-stu-id="12412-166">Connect to the device from the debugging machine.</span></span>

    - <span data-ttu-id="12412-167">Azure でホストされた開発マシンまたは別の PC で、[リモート デバッグ Android デバイスで開始](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/) する Android 開発者指示に従います。</span><span class="sxs-lookup"><span data-stu-id="12412-167">On the Azure-hosted development machine or a separate PC, follow Android developer instructions to [Get Started with Remote Debugging Android Devices](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/).</span></span> <span data-ttu-id="12412-168">また、[Android 用 Chrome のリモート デバッグ](https://www.youtube.com/results?search_query=chrome+for+android+remote+debugging) を検索することにより、YouTube 上で多様な説明ビデオを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="12412-168">You can also find a wide selection of instructional videos on YouTube by searching for [Chrome for Android remote debugging](https://www.youtube.com/results?search_query=chrome+for+android+remote+debugging).</span></span> 
    
4. <span data-ttu-id="12412-169">デバッガーに接続した後は、デバイスの有効タブを見つけます。</span><span class="sxs-lookup"><span data-stu-id="12412-169">After you connect the debugger, find the active tab on your device.</span></span> <span data-ttu-id="12412-170">Android で **その他のタブを表示** をクリックすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="12412-170">You may need to click **View more tabs** on Android.</span></span> <span data-ttu-id="12412-171">タブのいずれかは、`/www.index.html#/app/appList`または`/www.index.html#/app/app_landing`のようになります。</span><span class="sxs-lookup"><span data-stu-id="12412-171">One of the tabs should look similar to `/www.index.html#/app/appList` or `/www.index.html#/app/app_landing`.</span></span> 

    <span data-ttu-id="12412-172">**ファイル** > (ドメインなし) > **ExpenseMobile.js** などのワークスペース JavaScript を表示するには、ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="12412-172">Expand the nodes to find the workspace JavaScript, such as **File** > (no domain) > **ExpenseMobile.js**.</span></span> <span data-ttu-id="12412-173">JavaScript ファイルをクリックして表示し、ブレークポイントを追加します。</span><span class="sxs-lookup"><span data-stu-id="12412-173">Click the JavaScript file to view it and add breakpoints.</span></span>
    
    ![経費管理モバイル ワークスペース](./media/expense-management-mobile-workspace.png)
    
5. <span data-ttu-id="12412-175">デスクトップ画面に操作できるように、デスクトップにモバイル デバイスを反映します。</span><span class="sxs-lookup"><span data-stu-id="12412-175">Reflect the mobile device on your desktop so that you can interact with it on the desktop screen.</span></span> 

6. <span data-ttu-id="12412-176">目的のワークスペースとフォームを通して移動します。</span><span class="sxs-lookup"><span data-stu-id="12412-176">Go to through the desired workspace and forms.</span></span>

7. <span data-ttu-id="12412-177">ブレークポイントが発生した場合、ブラウザーの開発者ツールにより実行フローの管理が可能となり、値と渡されるパラメーターが参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="12412-177">If breakpoints are encountered, then the browser developer tools will allow you to control the flow of execution and see the values and parameters being passed.</span></span> 

8. <span data-ttu-id="12412-178">実行時にスタイル設定を変更するのにには、要素タブを使用してスタイル設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="12412-178">To change styling at runtime, use the elements tab to alter the styling.</span></span> <span data-ttu-id="12412-179">これは、JavaScript がどの要素を対象にすべきかを決定し、要素のスタイルを設定する方法を決定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="12412-179">This will help you determine what elements JavaScript should target and how those elements should be styled.</span></span>

9. <span data-ttu-id="12412-180">必要な変更が指定された場合は、JavaScript では、それらの変更がなされ、環境にこれらの変更をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="12412-180">If a needed change is identified, make those changes in JavaScript, and then push those changes into the environment.</span></span>

10. <span data-ttu-id="12412-181">詳細の変更や検証が必要な場合は、プロセスを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="12412-181">If more changes or validation is needed, repeat the process.</span></span>

### <a name="debugging-the-server-side"></a><span data-ttu-id="12412-182">サーバー側のデバッグ</span><span class="sxs-lookup"><span data-stu-id="12412-182">Debugging the server side</span></span>

#### <a name="prerequisites"></a><span data-ttu-id="12412-183">前提条件</span><span class="sxs-lookup"><span data-stu-id="12412-183">Prerequisites</span></span>
- <span data-ttu-id="12412-184">Azure でホストされた開発マシン (モバイル デバイスで指定できます)</span><span class="sxs-lookup"><span data-stu-id="12412-184">Azure-hosted development machine (so the mobile device can point to it)</span></span>

#### <a name="steps-to-debug-the-serverside"></a><span data-ttu-id="12412-185">サーバー側をデバッグする手順</span><span class="sxs-lookup"><span data-stu-id="12412-185">Steps to debug the serverside</span></span>
1. <span data-ttu-id="12412-186">Azure でホストされた開発マシンで公開されている Web クライアントで、Unified Operations アプリ用に公開されたモバイル ワークスペースがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="12412-186">On the web client exposed by the Azure-hosted development machine, ensure that there are mobile workspaces published for the Unified Operations app.</span></span> <span data-ttu-id="12412-187">モバイル ワークスペースを公開する方法については、[モバイル ワークスペースの公開](../publish-mobile-workspace.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12412-187">For information about publishing a mobile workspace, see [Publish a mobile workspace](../publish-mobile-workspace.md).</span></span>

2. <span data-ttu-id="12412-188">Unified Operations アプリをデバイスで開いて、Azure でホストされた開発マシンを参照し、サインインします。</span><span class="sxs-lookup"><span data-stu-id="12412-188">Open the Unified Operations app on your device, point to the Azure-hosted development machine, and sign in.</span></span>

3. <span data-ttu-id="12412-189">開発マシンでホストされる Azure で Visual Studio を開き、w3wp プロセスにデバッガーを追加します。</span><span class="sxs-lookup"><span data-stu-id="12412-189">Open Visual Studio on the Azure-hosted development machine and attach the debugger to the w3wp process.</span></span>

4. <span data-ttu-id="12412-190">デバッガーに接続した後、目的のビジネス ロジックを見つけ、必要に応じてブレークポイントを挿入します。</span><span class="sxs-lookup"><span data-stu-id="12412-190">After you connect the debugger, find the desired business logic, and insert breakpoints as needed.</span></span>

5. <span data-ttu-id="12412-191">通常どおりデバイスでアプリを使用するか、またはデスクトップにモバイル デバイスを反映させて、デスクトップ画面でモバイル デバイスとやりとりすることが可能です。</span><span class="sxs-lookup"><span data-stu-id="12412-191">Either use the app on your device as usual, or reflect the mobile device on your desktop so you can interact with it on the desktop screen.</span></span>

6. <span data-ttu-id="12412-192">目的のワークスペースとフォームを通して移動します。</span><span class="sxs-lookup"><span data-stu-id="12412-192">Navigate through the desired workspace and forms.</span></span>

7. <span data-ttu-id="12412-193">ブレークポイントが発生した場合、Visual Studio により実行フローの管理が可能となり、値と渡されるパラメーターが参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="12412-193">If breakpoints are encountered, then Visual Studio will allow you to control the flow of execution and see the values and parameters being passed.</span></span> 

8. <span data-ttu-id="12412-194">必要な変更が指定された場合は、X++ では、それらの変更がなされ、環境にこれらの変更をプッシュします。</span><span class="sxs-lookup"><span data-stu-id="12412-194">If a needed change is identified, make those changes in X++, and push those changes into the environment.</span></span>

9. <span data-ttu-id="12412-195">詳細の変更や検証が必要な場合は、プロセスを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="12412-195">If more changes or validation is needed, repeat the process.</span></span>

## <a name="change-needed-for-adfs-to-support-mobile-client-in-on-premises-environments"></a><span data-ttu-id="12412-196">ADFS がオンプレミス環境でモバイル クライアントをサポートするために必要な変更</span><span class="sxs-lookup"><span data-stu-id="12412-196">Change needed for ADFS to support Mobile Client in on-premises environments</span></span> 
<span data-ttu-id="12412-197">ADFS がドメインで使用されており、環境がオンプレミスである場合、Windows 統合認証 (WIA) を使用する代わりに **ADFS は標準のフォームベースの認証画面を提供するように構成する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="12412-197">If ADFS is in use on the domain and the environment is on-premises, then **ADFS must be configured to provide a regular forms-based authentication screen** instead of using Windows Integrated Authentication (WIA).</span></span> <span data-ttu-id="12412-198">iOS と Android の Microsoft Dynamics Unified Operations アプリには、標準のフォーム ベースの認証画面が必要です。</span><span class="sxs-lookup"><span data-stu-id="12412-198">The Microsoft Dynamics Unified Operations apps for iOS and Android require the regular forms-based authentication screen.</span></span> <span data-ttu-id="12412-199">ADFS は、ブラウザー クライアント (ユース ケース) のみ WIA を提供するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12412-199">ADFS should be configured to only provide WIA for browser clients (use cases).</span></span> <span data-ttu-id="12412-200">詳細については、[WIA をサポートしていないデバイスのイントラネット フォーム ベースの認証を構成する](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-intranet-forms-based-authentication-for-devices-that-do-not-support-wia)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12412-200">For more information, see [Configure intranet forms based authentication for devices that do not support wia](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-intranet-forms-based-authentication-for-devices-that-do-not-support-wia)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12412-201">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="12412-201">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="12412-202">新機能および開発中の機能</span><span class="sxs-lookup"><span data-stu-id="12412-202">What's new and in development</span></span>
<span data-ttu-id="12412-203">リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12412-203">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="12412-204">ブログ</span><span class="sxs-lookup"><span data-stu-id="12412-204">Blogs</span></span>
<span data-ttu-id="12412-205">Retail およびその他のソリューションに関する意見、ニュース、その他の情報については、[Microsoft Dynamics 365 blog (Microsoft Dynamics 365 ブログ)](https://community.dynamics.com/b/msftdynamicsblog) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="12412-205">You can find opinions, news, and other information about Retail and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


