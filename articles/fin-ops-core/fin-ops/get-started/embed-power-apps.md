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
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870244"
---
# <a name="embed-microsoft-power-apps"></a><span data-ttu-id="795b7-103">埋め込み Microsoft Power Apps</span><span class="sxs-lookup"><span data-stu-id="795b7-103">Embed Microsoft Power Apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="795b7-104">プラットフォーム更新 14 で、Microsoft Power Apps との統合をサポートし、コードの記述なしでモバイル デバイス、タブレット、および Web のカスタム ビジネス アプリを構築するため、開発者および技術者以外のユーザー向けのサービスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="795b7-104">Platform update 14 supports integration with Microsoft Power Apps, a service for developers and non-technical users to build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="795b7-105">Power Appsユーザー、組織、またはより幅広いエコシステムによって開発された PowerApps を、Finance and Operations アプリに組み込み、製品の機能を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-105">Power Apps developed by you, your organization, or the broader ecosystem can then be embedded in the Finance and Operations apps to augment the product's functionality.</span></span> <span data-ttu-id="795b7-106">たとえば、Power App を構築して、別のシステムから取得した情報で Finance and Operations アプリを補足することができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-106">For example, you might build a Power App to supplement Finance and Operations apps with information retrieved from another system.</span></span>

<span data-ttu-id="795b7-107">Power Apps の埋め込みに関する詳細については、短い [Power Apps を組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="795b7-107">To learn more about embedding Power Apps, watch the short [How to embed Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-power-app-to-a-page"></a><span data-ttu-id="795b7-108">埋め込まれた Power App をページに追加する。</span><span class="sxs-lookup"><span data-stu-id="795b7-108">Adding an embedded Power App to a page</span></span>

### <a name="overview"></a><span data-ttu-id="795b7-109">概要</span><span class="sxs-lookup"><span data-stu-id="795b7-109">Overview</span></span>

<span data-ttu-id="795b7-110">クライアントに Power App を埋め込む前に、最初に、必要なビジュアルまたは機能を備えた Power App を見つけたり構築したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="795b7-110">Before embedding a Power App into the client, you first need to find or build a Power App with the desired visuals and/or functionality.</span></span> <span data-ttu-id="795b7-111">ここでは、Power App を構築するための詳細なプロセスについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="795b7-111">We will not describe the detailed process for building a Power App here.</span></span> <span data-ttu-id="795b7-112">[Power Apps の概要](https://docs.microsoft.com/powerapps/getting-started) トピックは、Power Apps を初めて使用する場合に有用です。</span><span class="sxs-lookup"><span data-stu-id="795b7-112">The [Introduction to Power Apps](https://docs.microsoft.com/powerapps/getting-started) topic is a good starting point if you are new to Power Apps.</span></span>

<span data-ttu-id="795b7-113">特定の Power App を組み込む準備ができたら、ページ上の Power App にアクセスする 2 つの方法のうち、いずれかシナリオに適したルートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="795b7-113">When you are ready to embed a specific Power App, you can choose between one of two ways of accessing the Power App on a page, whichever route better fits your scenario.</span></span> <span data-ttu-id="795b7-114">最初の方法は、標準のアクション ペインに追加された Power Apps ボタンを使用することです。</span><span class="sxs-lookup"><span data-stu-id="795b7-114">The first way is through the Power Apps button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="795b7-115">このメカニズムを使用して追加された Power Apps は、Power Apps メニュー ボタンのメニュー項目として表示されます。</span><span class="sxs-lookup"><span data-stu-id="795b7-115">Power Apps added using this mechanism will appear as menu items inside the Power Apps menu button.</span></span> <span data-ttu-id="795b7-116">これらのメニュー項目を選択すると、埋め込まれた Power App を含む作業ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="795b7-116">When selected, each of these menu items will open a side pane that contains the embedded Power App.</span></span> <span data-ttu-id="795b7-117">または、Power App を新しいタブ、クイック タブ、ブレード、またはワークスペースで新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="795b7-117">Alternatively, you may choose to show a Power App directly on a page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="795b7-118">組み込みの Power App を設定するときは、Power App への入力として送信する単一のフィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="795b7-118">When configuring your embedded Power App, you can select a single field that you want to send as input to the Power App.</span></span> <span data-ttu-id="795b7-119">これにより、現在表示しているデータに基づいて Power App を応答させることができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-119">This allows the Power App to be responsive based on the data that you are currently viewing.</span></span>

### <a name="details"></a><span data-ttu-id="795b7-120">詳細情報</span><span class="sxs-lookup"><span data-stu-id="795b7-120">Details</span></span>

<span data-ttu-id="795b7-121">次の手順では、Web クライアントに Power App を埋め込む方法を示します。</span><span class="sxs-lookup"><span data-stu-id="795b7-121">The following instructions show how to embed a Power App into the web client.</span></span>

1. <span data-ttu-id="795b7-122">Power App を埋め込むページに移動します。</span><span class="sxs-lookup"><span data-stu-id="795b7-122">Go to the page where you would like to embed the Power App.</span></span> <span data-ttu-id="795b7-123">これは、入力として Power App に渡す必要があるデータを含む同じページになります。</span><span class="sxs-lookup"><span data-stu-id="795b7-123">This will be the same page that contains any data that needs to be passed to the Power App as input.</span></span>
2. <span data-ttu-id="795b7-124">**Power App を挿入**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="795b7-124">Open the **Insert a Power App** pane:</span></span>

    - <span data-ttu-id="795b7-125">**オプション**をクリックし、**このフォームのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-125">Click **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="795b7-126">**挿入**メニューで、**Power App** を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-126">Under the **Insert** menu, choose **Power App**.</span></span> <span data-ttu-id="795b7-127">最後に、Power App を追加する地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-127">Finally, select the region where you would like to add the Power App.</span></span> <span data-ttu-id="795b7-128">Power Apps メニュー ボタンの下で Power App を埋め込む場合、アクション ウィンドウを選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-128">If you want to embed the Power App under the Power Apps menu button, choose the Action Pane.</span></span> <span data-ttu-id="795b7-129">ページに直接 Power App を埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-129">If you want to embed the Power App directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="795b7-130">Power Apps メニュー ボタンを使用して Power App にアクセスする場合、代わりに標準のアクション ウィンドウの **Power Apps** メニュー ボタンをクリックし、**Power App の挿入**を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-130">If the Power App will be accessed using the Power Apps menu button, you can alternatively click the **Power Apps** menu button in the standard Action Pane, and then select **Insert a Power App**.</span></span>

3. <span data-ttu-id="795b7-131">埋め込み型 Power Apps を構成します。</span><span class="sxs-lookup"><span data-stu-id="795b7-131">Configure the embedded Power App:</span></span>

    - <span data-ttu-id="795b7-132">**名前**フィールドは、埋め込まれた Power App を含むボタンまたはタブのテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="795b7-132">The **Name** field indicates the text shown for the button or tab that will contain the embedded Power App.</span></span> <span data-ttu-id="795b7-133">多くの場合、このフィールドで Power App の名前を繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-133">Oftentimes, you may want to repeat the name of the Power App in this field.</span></span>
    - <span data-ttu-id="795b7-134">**アプリ ID** は、埋め込む Power App の GUID です。</span><span class="sxs-lookup"><span data-stu-id="795b7-134">**App ID** is the GUID for the Power App that you want to embed.</span></span> <span data-ttu-id="795b7-135">この値を取得するには、[web.powerapps.com](https://web.powerapps.com) で Power App を検索し、**詳細**の**アプリ ID** フィールドを探します。</span><span class="sxs-lookup"><span data-stu-id="795b7-135">To retrieve this value, find the Power App on [web.powerapps.com](https://web.powerapps.com) and then locate the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="795b7-136">**Power App のデータを入力する**では、必要に応じて、 Power App に入力として渡すデータが含まれているフィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-136">For **Input data for the Power App**, you can optionally select the field that contains the data that you want to pass to the Power App as input.</span></span> <span data-ttu-id="795b7-137">Power App が Finance and Operations アプリから送信されるデータにどのようにアクセスするかの詳細に関しては、このトピックの後の [Finance and Operations アプリからのデータを活用する Power App の構築](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="795b7-137">See the section later in this topic titled [Building a Power App that leverages data from Finance and Operations apps](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps) for details on how the Power App can access the data sent from Finance and Operations apps.</span></span>
    - <span data-ttu-id="795b7-138">埋め込む Power App のタイプに一致する**アプリケーション サイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-138">Choose the **Application size** that matches the type of Power App that you're embedding.</span></span> <span data-ttu-id="795b7-139">モバイル デバイス用に作成された Power Apps に対しては**シン**を選択し、タブレット用に作成された Power Apps に対しては**ワイド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-139">Select **Thin** for Power Apps built for mobile devices, and **Wide** for Power Apps built for tablets.</span></span> <span data-ttu-id="795b7-140">これにより、埋め込み Power App に十分な容量を確保できます。</span><span class="sxs-lookup"><span data-stu-id="795b7-140">This ensures a sufficient amount of space is allotted for the embedded Power App.</span></span>
    - <span data-ttu-id="795b7-141">**法人**クイック タブには、Power App が利用できる法人を選択する機能があります。</span><span class="sxs-lookup"><span data-stu-id="795b7-141">The **Legal entities** FastTab provides the ability to choose which legal entities the Power App is available for.</span></span> <span data-ttu-id="795b7-142">既定では、Power App はすべての法人で表示されます。</span><span class="sxs-lookup"><span data-stu-id="795b7-142">The default is to show the Power App in all legal entities.</span></span>

4. <span data-ttu-id="795b7-143">構成が正しいことを確認した後、**挿入**をクリックしてページに Power App を埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="795b7-143">After confirming that the configuration is correct, click **Insert** to embed the Power App on the page.</span></span> <span data-ttu-id="795b7-144">組み込みの Power App を表示するために、ブラウザを更新するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="795b7-144">You will be prompted to refresh the browser in order to see the embedded Power App.</span></span>

## <a name="sharing-an-embedded-power-app"></a><span data-ttu-id="795b7-145">埋め込まれた Power App の共有</span><span class="sxs-lookup"><span data-stu-id="795b7-145">Sharing an embedded Power App</span></span>

<span data-ttu-id="795b7-146">ページに Power App を埋め込み、ページから渡されたデータ コンテキストで正しく動作がしていることを確認したら、この埋め込まれた Power App をシステムで他のユーザーと共有することができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-146">After you have embedded a Power App on a page and confirmed that it is working correctly with any data context passed from the page, you might want to share this embedded Power App with other users in the system.</span></span> <span data-ttu-id="795b7-147">これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="795b7-147">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="795b7-148">推奨されるシナリオは、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできる、システム管理者によるものです。</span><span class="sxs-lookup"><span data-stu-id="795b7-148">The recommended scenario is through the system administrator, who can push a personalization to all users or a subset of users.</span></span>
- <span data-ttu-id="795b7-149">または、ページの個人用設定をエクスポートし、1 つまたは複数のユーザーに送信し、これらの各ユーザーにその変更をインポートさせることもできます。</span><span class="sxs-lookup"><span data-stu-id="795b7-149">Alternatively, you can export your page's personalizations, send them to one or more users, and have each of those users import those changes.</span></span> <span data-ttu-id="795b7-150">個人用設定のツールバー上の [管理] オプションで、個人用設定をエクスポートし、インポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-150">The Manage option on the personalization toolbar enables you to export and import personalizations.</span></span>

<span data-ttu-id="795b7-151">製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="795b7-151">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a><span data-ttu-id="795b7-152">Finance and Operations アプリから送信されたデータを活用する Power App の構築</span><span class="sxs-lookup"><span data-stu-id="795b7-152">Building a Power App that leverages data sent from Finance and Operations apps</span></span>

<span data-ttu-id="795b7-153">Finance and Operations アプリに埋め込まれる Power App を構築するのに重要なのは、Finance and Operations アプリからの入力データを使用することです。</span><span class="sxs-lookup"><span data-stu-id="795b7-153">An important part of building a Power App that will be embedded in Finance and Operations apps is utilizing the input data from Finance and Operations apps.</span></span> <span data-ttu-id="795b7-154">Power App 内で、Param("EntityId") 変数を使用して入力データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="795b7-154">Inside the Power App, that input data can be accessed using the Param("EntityId") variable.</span></span>

<span data-ttu-id="795b7-155">たとえば、Power App の OnStart 機能では、Finance and Operations アプリから次のような変数に入力データを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-155">For example, in the OnStart function of the Power App, you could set the input data from Finance and Operations apps to a variable like this:</span></span>

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a><span data-ttu-id="795b7-156">埋め込まれた Power App の表示</span><span class="sxs-lookup"><span data-stu-id="795b7-156">Viewing an embedded Power App</span></span>

<span data-ttu-id="795b7-157">Finance and Operations アプリのページに埋め込まれた Power App を表示するには、Power App が埋め込まれたページにそのまま移動します。</span><span class="sxs-lookup"><span data-stu-id="795b7-157">To view an embedded Power App on a page in Finance and Operations apps, simply go to a page with an embedded Power App.</span></span> <span data-ttu-id="795b7-158">Power Apps は、標準アクション ペインの Power Apps ボタンからアクセスできます。また、新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="795b7-158">Recall that Power Apps can be accessed through the Power Apps button in the standard Action Pane, or can appear directly on the page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> <span data-ttu-id="795b7-159">ユーザーが最初に、ページ上に Power App を読み込もうとすると、Power Apps にサインインするように表示され、ユーザーに Power App を使用する適切なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="795b7-159">When a user first attempts to load a Power App on a page, he or she will be prompted to sign in to Power Apps to ensure the user has the appropriate permissions to use the Power App.</span></span>

## <a name="editing-an-embedded-power-app"></a><span data-ttu-id="795b7-160">埋め込まれた Power App の編集</span><span class="sxs-lookup"><span data-stu-id="795b7-160">Editing an embedded Power App</span></span>

<span data-ttu-id="795b7-161">Power App がページに埋め込まれた後、その Power App の設定をいくつか変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="795b7-161">After a Power App has been embedded onto a page, you may need to make some changes to the configuration of that Power App.</span></span> <span data-ttu-id="795b7-162">たとえば、埋め込まれた Power App に関連付けられたラベルを変更したり、Power App の新しいバージョンが作成された場合に、最新の Power App を参照するようアプリ ID を更新したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="795b7-162">For example, perhaps you want to modify the label associated with the embedded Power App or a new version of a Power App has been created and you need to update the App ID to point at the latest Power App.</span></span>

<span data-ttu-id="795b7-163">埋め込まれた Power App のコンフィギュレーションを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="795b7-163">Follow these steps to edit the configuration of an embedded Power App:</span></span>

1. <span data-ttu-id="795b7-164">**Power App を編集**ウインドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="795b7-164">Go to the **Edit a Power App** pane.</span></span>

    - <span data-ttu-id="795b7-165">埋め込み型の Power App が Power Apps メニュー ボタンによりアクセスされた場合、Power Apps メニュー ボタンを右クリックし、**パーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-165">If the embedded Power App is accessed through the Power Apps menu button, right-click on the Power Apps menu button and select **Personalize**.</span></span> <span data-ttu-id="795b7-166">**Select Power App** ドロップダウン メニューから構成する Power App を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-166">Select the Power App that you want to configure from the **Select Power App** drop-down menu.</span></span>
    - <span data-ttu-id="795b7-167">埋め込み型の Power App がページに直接表示されたら、**オプション**を選択し、**このフォームのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-167">If the embedded Power App appears directly on the page, select **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="795b7-168">**選択**ツールを使用し、埋め込まれた Power App をクリックします。</span><span class="sxs-lookup"><span data-stu-id="795b7-168">Using the **Select** tool, click the embedded Power App.</span></span>

2. <span data-ttu-id="795b7-169">Power Apps コンフィギュレーションに必要な変更を行ない、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="795b7-169">Make the needed modifications to the Power Apps configuration, and then click **Save**.</span></span>

## <a name="removing-an-embedded-power-app"></a><span data-ttu-id="795b7-170">埋め込まれた Power App の削除</span><span class="sxs-lookup"><span data-stu-id="795b7-170">Removing an embedded Power App</span></span>

<span data-ttu-id="795b7-171">Power App がページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="795b7-171">After a Power App has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="795b7-172">このトピックの前半にある[埋め込み Power App を編集](#editing-an-embedded-power-app)セクションからの手順を使用して、**Power App を編集**ウィンドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="795b7-172">Go to the **Edit a Power App** pane using the instructions from the [Editing an embedded Power App](#editing-an-embedded-power-app) section earlier in this topic.</span></span> <span data-ttu-id="795b7-173">ウィンドウに、削除する埋め込み型 Power App の情報が表示されていることを確認してから、**削除**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="795b7-173">Confirm that the pane displays information for the embedded Power App that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="795b7-174">埋め込まれた Power App は、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれた Power Apps も削除されます。</span><span class="sxs-lookup"><span data-stu-id="795b7-174">Because an embedded Power App is saved as personalization data, clearing your page's personalization will also remove any embedded Power Apps on that page.</span></span> <span data-ttu-id="795b7-175">ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="795b7-175">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="795b7-176">ページの個人用設定を削除するには、**オプション**を選択し、**このフォームのパーソナライズ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="795b7-176">To remove your personalizations on a page, select **Options** and then click **Personalize this form**.</span></span> <span data-ttu-id="795b7-177">**管理**メニューで**クリア**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="795b7-177">Under the **Manage** menu, select the **Clear** button.</span></span> <span data-ttu-id="795b7-178">ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。</span><span class="sxs-lookup"><span data-stu-id="795b7-178">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="795b7-179">個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="795b7-179">See [Personalize the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="795b7-180">付録</span><span class="sxs-lookup"><span data-stu-id="795b7-180">Appendix</span></span>

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a><span data-ttu-id="795b7-181">Power App 埋め込み可能な場所についての開発者制御</span><span class="sxs-lookup"><span data-stu-id="795b7-181">Developer control over where a Power App can be embedded</span></span>

<span data-ttu-id="795b7-182">既定では、ユーザーは、Power Apps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接 Power Apps を埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-182">By default, users can embed Power Apps on any page, either under the Power Apps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="795b7-183">ただし、必要に応じて開発者が次の方法を実装することで、Power Apps の埋め込みを特定のページのみに許可するようこの機能を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="795b7-183">However, if required, developers can also configure this feature to only allow embedding of Power Apps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="795b7-184">**isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、Power Apps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにも Power Apps を埋め込むことができません。</span><span class="sxs-lookup"><span data-stu-id="795b7-184">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the Power Apps menu button will not be shown, and users will not be able to embed Power Apps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="795b7-185">**isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接 Power Apps を埋め込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="795b7-185">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed Power Apps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="795b7-186">ページで埋め込みが許可されている場合でも、ユーザーは Power Apps メニュー ボタンを使用して Power Apps を埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="795b7-186">Users will still be able to embed Power Apps through the Power Apps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="795b7-187">次の例は、Power Apps を埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="795b7-187">The following example shows a new class with the two methods needed to configure where Power Apps can be embedded.</span></span>

```
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
