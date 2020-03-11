---
title: 埋め込み Power Apps
description: このトピックでは、Power Apps をクライアントに組み込んで製品の機能を拡張する方法について説明します。
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042945"
---
# <a name="embed-microsoft-power-apps"></a><span data-ttu-id="38a81-103">埋め込み Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="38a81-103">Embed Microsoft Power Apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38a81-104">Finance and Operations で、Microsoft Power Apps との統合をサポートし、コードの記述なしでモバイル デバイス、タブレット、および Web のカスタム ビジネス アプリを構築するため、開発者および技術者以外のユーザー向けのサービスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="38a81-104">Finance and Operations supports integration with Microsoft Power Apps, a service for developers and non-technical users to build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="38a81-105">ユーザー、組織、またはより幅広いエコシステムによって開発された Power Apps を、Finance and Operations アプリに組み込み、製品の機能を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-105">Power Apps developed by you, your organization, or the broader ecosystem can then be embedded in Finance and Operations apps to augment the product's functionality.</span></span> <span data-ttu-id="38a81-106">たとえば、別のシステムから取得した情報を使用して Power Apps から Finance and Operations アプリを補足するアプリを構築する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="38a81-106">For example, you might build an app from Power Apps to supplement a Finance and Operations app with information retrieved from another system.</span></span>

<span data-ttu-id="38a81-107">Power Apps の埋め込みに関する詳細については、短い [Power Apps を組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="38a81-107">To learn more about embedding Power Apps, watch the short [How to embed Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a><span data-ttu-id="38a81-108">埋め込まれたアプリを Power Apps からページに追加する</span><span class="sxs-lookup"><span data-stu-id="38a81-108">Adding an embedded app from Power Apps to a page</span></span>

### <a name="overview"></a><span data-ttu-id="38a81-109">概要</span><span class="sxs-lookup"><span data-stu-id="38a81-109">Overview</span></span>

<span data-ttu-id="38a81-110">Power Apps からクライアントにアプリを埋め込む前に、最初に、必要なビジュアルまたは機能を備えたアプリを見つけたり構築したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="38a81-110">Before embedding an app fro Power Apps into the client, you first need to find or build an app with the desired visuals and/or functionality.</span></span> <span data-ttu-id="38a81-111">ここでは、アプリを構築するための詳細なプロセスについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="38a81-111">We will not describe the detailed process for building apps here.</span></span> <span data-ttu-id="38a81-112">[Power Apps の概要](https://docs.microsoft.com/powerapps/getting-started) トピックは、Power Apps を初めて使用する場合に有用です。</span><span class="sxs-lookup"><span data-stu-id="38a81-112">The [Introduction to Power Apps](https://docs.microsoft.com/powerapps/getting-started) topic is a good starting point if you are new to Power Apps.</span></span>

<span data-ttu-id="38a81-113">特定のアプリを組み込む準備ができたら、ページ上のアプリにアクセスする 2 つの方法のうち、いずれかシナリオに適したルートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="38a81-113">When you are ready to embed a specific app, you can choose between one of two ways of accessing the app on a page, whichever route better fits your scenario.</span></span> <span data-ttu-id="38a81-114">最初の方法は、標準のアクション ペインに追加された Power Apps ボタンを使用することです。</span><span class="sxs-lookup"><span data-stu-id="38a81-114">The first way is through the Power Apps button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="38a81-115">このメカニズムを使用して追加されたアプリは、Power Apps メニュー ボタンのメニュー項目として表示されます。</span><span class="sxs-lookup"><span data-stu-id="38a81-115">Apps added using this mechanism will appear as menu items inside the Power Apps menu button.</span></span> <span data-ttu-id="38a81-116">これらのメニュー項目を選択すると、埋め込まれたアプリを含む作業ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="38a81-116">When selected, each of these menu items will open a side pane that contains the embedded app.</span></span> <span data-ttu-id="38a81-117">または、アプリを新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接埋め込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="38a81-117">Alternatively, you may choose to embed an app directly on a page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="38a81-118">組み込みのアプリを設定するときは、アプリへのコンテキストとして送信する単一のフィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="38a81-118">When configuring your embedded app, you can select a single field that you want to send as context to the app.</span></span> <span data-ttu-id="38a81-119">これにより、現在表示しているデータに基づいてアプリを応答させることができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-119">This allows the app to be responsive based on the data that you are currently viewing.</span></span>

### <a name="details"></a><span data-ttu-id="38a81-120">詳細情報</span><span class="sxs-lookup"><span data-stu-id="38a81-120">Details</span></span>

<span data-ttu-id="38a81-121">次の手順では、Power Apps から Web クライアントにアプリを埋め込む方法を示します。</span><span class="sxs-lookup"><span data-stu-id="38a81-121">The following instructions show how to embed an app from Power Apps into the web client.</span></span>

1. <span data-ttu-id="38a81-122">アプリを埋め込むページに移動します。</span><span class="sxs-lookup"><span data-stu-id="38a81-122">Go to the page where you would like to embed the app.</span></span> <span data-ttu-id="38a81-123">これは、入力としてアプリに渡す必要があるデータを含む同じページになります。</span><span class="sxs-lookup"><span data-stu-id="38a81-123">This will be the same page that contains any data that needs to be passed to the app as as input.</span></span>
2. <span data-ttu-id="38a81-124">**Power Apps からアプリを追加**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="38a81-124">Open the **Add an app from Power Apps** pane:</span></span>

    - <span data-ttu-id="38a81-125">**オプション**をクリックし、**このページのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-125">Click **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="38a81-126">**挿入**メニューで、**Power Apps** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-126">Under the **Insert** menu, choose **Power Apps**.</span></span> <span data-ttu-id="38a81-127">最後に、アプリを追加する地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-127">Finally, select the region where you would like to add the app.</span></span> <span data-ttu-id="38a81-128">Power Apps メニュー ボタンの下でアプリを埋め込む場合、アクション ウィンドウを選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-128">If you want to embed the app under the Power Apps menu button, choose the Action Pane.</span></span> <span data-ttu-id="38a81-129">ページに直接アプリを埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-129">If you want to embed the app directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="38a81-130">Power Apps メニュー ボタンを使用してアプリにアクセスする場合、代わりに標準のアクション ウィンドウの **Power Apps** メニュー ボタンをクリックし、**アプリの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-130">If the app will be accessed using the Power Apps menu button, you can alternatively click the **Power Apps** menu button in the standard Action Pane, and then select **Add an app**.</span></span>

3. <span data-ttu-id="38a81-131">埋め込み型アプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="38a81-131">Configure the embedded app:</span></span>

    - <span data-ttu-id="38a81-132">**名前**フィールドは、埋め込まれたアプリを含むボタンまたはタブのテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="38a81-132">The **Name** field indicates the text shown for the button or tab that will contain the embedded app.</span></span> <span data-ttu-id="38a81-133">多くの場合、このフィールドでアプリの名前を繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-133">Oftentimes, you may want to repeat the name of the app in this field.</span></span>
    - <span data-ttu-id="38a81-134">**アプリ ID** は、埋め込むアプリの GUID です。</span><span class="sxs-lookup"><span data-stu-id="38a81-134">**App ID** is the GUID for the app  that you want to embed.</span></span> <span data-ttu-id="38a81-135">この値を取得するには、[web.powerapps.com](https://web.powerapps.com) でアプリを検索し、**詳細**の**アプリ ID** フィールドを探します。</span><span class="sxs-lookup"><span data-stu-id="38a81-135">To retrieve this value, find the app on [web.powerapps.com](https://web.powerapps.com) and then locate the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="38a81-136">**アプリのコンテキストを入力する**では、必要に応じて、アプリに入力として渡すデータが含まれているフィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-136">For **Input context for the app**, you can optionally select the field that contains the data that you want to pass to the app as input.</span></span> <span data-ttu-id="38a81-137">アプリが Finance and Operations アプリから送信されるデータにアクセスする方法の詳細に関しては、このトピックの後の [Finance and Operations アプリから送信されるデータを活用するアプリの構築](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="38a81-137">See the section later in this topic titled [Building an app that leverages data sent from Finance and Operations apps](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps) for details on how the app can access the data sent from Finance and Operations apps.</span></span>
    - <span data-ttu-id="38a81-138">埋め込むアプリのタイプに一致する**アプリケーション サイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-138">Choose the **Application size** that matches the type of app that you're embedding.</span></span> <span data-ttu-id="38a81-139">モバイル デバイス用に作成されたアプリに対しては**シン**を選択し、タブレット用に作成されたアプリに対しては**ワイド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-139">Select **Thin** for apps built for mobile devices, and **Wide** for apps built for tablets.</span></span> <span data-ttu-id="38a81-140">これにより、埋め込みアプリに十分な容量を確保できます。</span><span class="sxs-lookup"><span data-stu-id="38a81-140">This ensures a sufficient amount of space is allotted for the embedded app.</span></span>
    - <span data-ttu-id="38a81-141">**法人**クイック タブには、アプリが利用できる法人を選択する機能があります。</span><span class="sxs-lookup"><span data-stu-id="38a81-141">The **Legal entities** FastTab provides the ability to choose which legal entities the app is available for.</span></span> <span data-ttu-id="38a81-142">既定では、アプリをすべての法人に対してアクセス可能にします。</span><span class="sxs-lookup"><span data-stu-id="38a81-142">The default is to make the app accessible to all legal entities.</span></span> <span data-ttu-id="38a81-143">このオプションは、[保存されたビュー](saved-views.md) が無効になっている場合にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="38a81-143">This option is only available when the [Saved views](saved-views.md) feature is disabled.</span></span> 

4. <span data-ttu-id="38a81-144">構成が正しいことを確認した後、**挿入**をクリックしてページに Power App を埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="38a81-144">After confirming that the configuration is correct, click **Insert** to embed the Power App on the page.</span></span> <span data-ttu-id="38a81-145">組み込みアプリを表示するために、ブラウザを更新するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="38a81-145">You will be prompted to refresh the browser in order to see the embedded app.</span></span>

## <a name="sharing-an-embedded-app"></a><span data-ttu-id="38a81-146">埋め込まれたアプリの共有</span><span class="sxs-lookup"><span data-stu-id="38a81-146">Sharing an embedded app</span></span>

<span data-ttu-id="38a81-147">ページにアプリを埋め込み、ページから渡されたデータ コンテキストで正しく動作していることを確認したら、システムで他のユーザーと共有することができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-147">After you have embedded app on a page and confirmed that it is working correctly with any data context passed from the page, you might want to share this with other users in the system.</span></span> <span data-ttu-id="38a81-148">これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="38a81-148">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="38a81-149">推奨されるシナリオは、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできる、システム管理者によるものです。</span><span class="sxs-lookup"><span data-stu-id="38a81-149">The recommended scenario is through the system administrator, who can push a personalization to all users or a subset of users.</span></span>
- <span data-ttu-id="38a81-150">または、ページの個人用設定をエクスポートし、1 つまたは複数のユーザーに送信し、これらの各ユーザーにその変更をインポートさせることもできます。</span><span class="sxs-lookup"><span data-stu-id="38a81-150">Alternatively, you can export your page's personalizations, send them to one or more users, and have each of those users import those changes.</span></span> <span data-ttu-id="38a81-151">個人用設定のツールバーには、個人用設定のエクスポートおよびインポートをするアクションがあります。</span><span class="sxs-lookup"><span data-stu-id="38a81-151">The personalization toolbar has actions that allow you to export and import personalizations.</span></span>

<span data-ttu-id="38a81-152">製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38a81-152">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a><span data-ttu-id="38a81-153">Finance and Operations アプリから送信されたデータを活用するアプリの構築</span><span class="sxs-lookup"><span data-stu-id="38a81-153">Building an app that leverages data sent from Finance and Operations apps</span></span>

<span data-ttu-id="38a81-154">Finance and Operations アプリに埋め込まれる Power Apps からアプリをビルドする際の重要な部分は、そのアプリケーションからの入力データを使用することです。</span><span class="sxs-lookup"><span data-stu-id="38a81-154">An important part of building an app from Power Apps that will be embedded in a Finance and Operations app is utilizing the input data from that application.</span></span> <span data-ttu-id="38a81-155">Power Apps 開発経験から、Finance and Operations から渡された入力データには Param("EntityId") 変数を使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="38a81-155">From the Power Apps development experience, the input data passed from a Finance and Operations app can be accessed using the Param("EntityId") variable.</span></span>

<span data-ttu-id="38a81-156">たとえば、アプリの OnStart 機能では、Finance and Operations アプリから次のような変数に入力データを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-156">For example, in the OnStart function of the app, you could set the input data from Finance and Operations apps to a variable like this:</span></span>

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a><span data-ttu-id="38a81-157">アプリの表示</span><span class="sxs-lookup"><span data-stu-id="38a81-157">Viewing an app</span></span>

<span data-ttu-id="38a81-158">Finance and Operations アプリのページに埋め込まれたアプリを表示するには、アプリが埋め込まれたページにそのまま移動します。</span><span class="sxs-lookup"><span data-stu-id="38a81-158">To view an embedded app on a page in Finance and Operations apps, simply go to a page with an embedded app.</span></span> <span data-ttu-id="38a81-159">アプリは、標準アクション ウィンドウの Power Apps ボタンからアクセスでき、また新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="38a81-159">Recall that apps can be accessed through the Power Apps button in the standard Action Pane, or can appear directly on the page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> <span data-ttu-id="38a81-160">ユーザーが最初に、ページ上にアプリを読み込もうとするとサインインするように表示され、ユーザーにアプリを使用する適切なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="38a81-160">When a user first attempts to load an app on a page, he or she will be prompted to sign in to ensure the user has the appropriate permissions to use the app.</span></span>

## <a name="editing-an-embedded-app"></a><span data-ttu-id="38a81-161">埋め込まれたアプリの編集</span><span class="sxs-lookup"><span data-stu-id="38a81-161">Editing an embedded app</span></span>

<span data-ttu-id="38a81-162">アプリがページに埋め込まれた後、そのアプリの設定をいくつか変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="38a81-162">After an app has been embedded onto a page, you may need to make some changes to the configuration of the app.</span></span> <span data-ttu-id="38a81-163">たとえば、埋め込まれたアプリに関連付けられたラベルを変更したり、アプリの新しいバージョンが作成された場合に、アプリ ID を最新の時点のものに更新したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="38a81-163">For example, perhaps you want to modify the label associated with the embedded app or a new version of the app has been created and you need to update the App ID to point at the latest.</span></span>

<span data-ttu-id="38a81-164">埋め込まれたアプリのコンフィギュレーションを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="38a81-164">Follow these steps to edit the configuration of an embedded app:</span></span>

1. <span data-ttu-id="38a81-165">**アプリの編集**ウインドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="38a81-165">Go to the **Edit the app** pane.</span></span>

    - <span data-ttu-id="38a81-166">埋め込み型のアプリが Power Apps メニュー ボタンによりアクセスされた場合、Power Apps メニュー ボタンを右クリックし、**パーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-166">If the embedded app is accessed through the Power Apps menu button, right-click on the Power Apps menu button and select **Personalize**.</span></span> <span data-ttu-id="38a81-167">**アプリの選択**ドロップダウン メニューから構成するアプリを選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-167">Select the app that you want to configure from the **Select an app** drop-down menu.</span></span>
    - <span data-ttu-id="38a81-168">埋め込み型のアプリがページに直接表示されたら、**オプション**を選択し、**このページのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="38a81-168">If the embedded app appears directly on the page, select **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="38a81-169">**選択**ツールを使用し、埋め込まれたアプリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="38a81-169">Using the **Select** tool, click the embedded app.</span></span>

2. <span data-ttu-id="38a81-170">アプリ コンフィギュレーションに必要な変更を行ない、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="38a81-170">Make the needed modifications to the app configuration, and then click **Save**.</span></span>

## <a name="removing-an-app"></a><span data-ttu-id="38a81-171">アプリの削除</span><span class="sxs-lookup"><span data-stu-id="38a81-171">Removing an app</span></span>

<span data-ttu-id="38a81-172">アプリがページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="38a81-172">After an app has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="38a81-173">このトピックの前半にある [埋め込みアプリの編集](#editing-an-embedded-app) セクションからの手順を使用して、**アプリの編集**ウィンドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="38a81-173">Go to the **Edit an app** pane using the instructions from the [Editing an embedded app](#editing-an-embedded-app) section earlier in this topic.</span></span> <span data-ttu-id="38a81-174">ウィンドウに、削除する埋め込み型アプリの情報が表示されていることを確認してから、**削除**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="38a81-174">Confirm that the pane displays information for the embedded app that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="38a81-175">埋め込まれたアプリは、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれたアプリも削除されます。</span><span class="sxs-lookup"><span data-stu-id="38a81-175">Because the embedded app is saved as personalization data, clearing your page's personalization will also remove any embedded apps on that page.</span></span> <span data-ttu-id="38a81-176">ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="38a81-176">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="38a81-177">ページの個人用設定を削除するには、**オプション**を選択して**このページのパーソナライズ**、最後に**クリア** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="38a81-177">To remove your personalizations on a page, select **Options**, and then **Personalize this page**, and finally the **Clear** button.</span></span> <span data-ttu-id="38a81-178">ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。</span><span class="sxs-lookup"><span data-stu-id="38a81-178">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="38a81-179">個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38a81-179">See [Personalize the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="38a81-180">付録</span><span class="sxs-lookup"><span data-stu-id="38a81-180">Appendix</span></span>

### <a name="developer-control-over-where-an-app-can-be-embedded"></a><span data-ttu-id="38a81-181">アプリが埋め込み可能な場所についての開発者制御</span><span class="sxs-lookup"><span data-stu-id="38a81-181">Developer control over where an app can be embedded</span></span>

<span data-ttu-id="38a81-182">既定では、ユーザーは、Power Apps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接をアプリを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-182">By default, users can embed apps on any page, either under the Power Apps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="38a81-183">ただし、必要に応じて開発者が次の方法を実装することで、アプリの埋め込みを特定のページのみに許可するようこの機能を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="38a81-183">However, if required, developers can also configure this feature to only allow embedding of apps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="38a81-184">**isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、Power Apps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにもアプリを埋め込むことができません。</span><span class="sxs-lookup"><span data-stu-id="38a81-184">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the Power Apps menu button will not be shown, and users will not be able to embed apps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="38a81-185">**isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接アプリを埋め込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="38a81-185">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed apps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="38a81-186">ページで埋め込みが許可されている場合でも、ユーザーは Power Apps メニュー ボタンを使用してアプリを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="38a81-186">Users will still be able to embed apps through the Power Apps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="38a81-187">次の例は、アプリを埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="38a81-187">The following example shows a new class with the two methods needed to configure where apps can be embedded.</span></span>

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
