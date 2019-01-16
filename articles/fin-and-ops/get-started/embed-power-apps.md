---
title: "PowerApps アプリの埋め込み"
description: "このトピックでは、PowerApps を Finance and Operations クライアントに組み込んで製品の機能を拡張する方法について説明します。"
author: jasongre
manager: AnnBe
ms.date: 09/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 262d34cbc50251595d22c27387fbd3f1045d1fbb
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="embed-powerapps-apps"></a><span data-ttu-id="6b336-103">PowerApps アプリの埋め込み</span><span class="sxs-lookup"><span data-stu-id="6b336-103">Embed PowerApps apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b336-104">プラットフォーム update 14 で、Microsoft Dynamics 365 for Finance and Operations は Microsoft PowerApps との統合をサポートし、コードの記述なしでモバイル デバイス、タブレット、および Web のカスタム ビジネス アプリを構築するため、開発者および技術者以外のユーザー向けのサービスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6b336-104">In Platform update 14, Microsoft Dynamics 365 for Finance and Operations supports integration with Microsoft PowerApps, a service for developers and non-technical users to build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="6b336-105">ユーザー、組織、またはより幅広いエコシステムによって開発された PowerApps を、Finance and Operations のクライアントに組み込み、製品の機能を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-105">PowerApps developed by you, your organization, or the broader ecosystem can then be embedded in the Finance and Operations client to augment the product's functionality.</span></span> <span data-ttu-id="6b336-106">たとえば、PowerApp を構築して、別のシステムから取得した情報で Finance and Operations を補足することができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-106">For example, you might build a PowerApp to supplement Finance and Operations with information retrieved from another system.</span></span>

<span data-ttu-id="6b336-107">PowerApps の組み込みに関する詳細については、短い [PowerApps を Dynamics 365 for Finance and Operations に組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6b336-107">To learn more about embedding PowerApps, watch the short [How to embed PowerApps in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-powerapp-to-a-page"></a><span data-ttu-id="6b336-108">埋め込まれた PowerApp をページに追加する。</span><span class="sxs-lookup"><span data-stu-id="6b336-108">Adding an embedded PowerApp to a page</span></span>

### <a name="overview"></a><span data-ttu-id="6b336-109">概要</span><span class="sxs-lookup"><span data-stu-id="6b336-109">Overview</span></span>

<span data-ttu-id="6b336-110">Finance and Operations クライアントに PowerApp を埋め込む前に、最初に、必要なビジュアルまたは機能を備えた PowerApp を見つけたり構築したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b336-110">Before embedding a PowerApp into the Finance and Operations client, you first need to find or build a PowerApp with the desired visuals and/or functionality.</span></span> <span data-ttu-id="6b336-111">ここでは、PowerApp を構築するための詳細なプロセスについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="6b336-111">We will not describe the detailed process for building a PowerApp here.</span></span> <span data-ttu-id="6b336-112">[PowerApps の概要](https://docs.microsoft.com/powerapps/getting-started) トピックは、PowerApps を初めて使用する場合に有用です。</span><span class="sxs-lookup"><span data-stu-id="6b336-112">The [Introduction to PowerApps](https://docs.microsoft.com/powerapps/getting-started) topic is a good starting point if you are new to PowerApps.</span></span>

<span data-ttu-id="6b336-113">特定の PowerApp を組み込む準備ができたら、ページ上の PowerApp にアクセスする 2 つの方法のうち、いずれかシナリオに適したルートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6b336-113">When you are ready to embed a specific PowerApp, you can choose between one of two ways of accessing the PowerApp on a page, whichever route better fits your scenario.</span></span> <span data-ttu-id="6b336-114">最初の方法は、標準のアクション ペインに追加された PowerApps ボタンを使用することです。</span><span class="sxs-lookup"><span data-stu-id="6b336-114">The first way is through the PowerApps button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="6b336-115">このメカニズムを使用して追加された PowerApps は、PowerApps メニュー ボタンのメニュー項目として表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b336-115">PowerApps added using this mechanism will appear as menu items inside the PowerApps menu button.</span></span> <span data-ttu-id="6b336-116">これらのメニュー項目を選択すると、埋め込まれた PowerApp を含む作業ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="6b336-116">When selected, each of these menu items will open a side pane that contains the embedded PowerApp.</span></span> <span data-ttu-id="6b336-117">または、PowerApp を新しいタブ、クイック タブ、ブレード、またはワークスペースで新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b336-117">Alternatively, you may choose to show a PowerApp directly on a page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="6b336-118">組み込みの PowerApp を Finance and Operations で設定するときは、PowerApp への入力として送信する単一のフィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6b336-118">When configuring your embedded PowerApp in Finance and Operations, you can select a single field that you want to send as input to the PowerApp.</span></span> <span data-ttu-id="6b336-119">これにより、現在 Finance and Operations で表示しているデータに基づいて PowerApp を応答させることができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-119">This allows the PowerApp to be responsive based on the data that you are currently viewing in Finance and Operations.</span></span>

### <a name="details"></a><span data-ttu-id="6b336-120">細目</span><span class="sxs-lookup"><span data-stu-id="6b336-120">Details</span></span>

<span data-ttu-id="6b336-121">次の手順では、Finance and Operations Web クライアントに、PowerApp を組み込む方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6b336-121">The following instructions show how to embed a PowerApp into the Finance and Operations web client.</span></span>

1. <span data-ttu-id="6b336-122">PowerApp を埋め込むページに移動します。</span><span class="sxs-lookup"><span data-stu-id="6b336-122">Go to the page where you would like to embed the PowerApp.</span></span> <span data-ttu-id="6b336-123">これは、入力として PowerApp に渡す必要があるデータを含む同じページになります。</span><span class="sxs-lookup"><span data-stu-id="6b336-123">This will be the same page that contains any data that needs to be passed to the PowerApp as input.</span></span>
2. <span data-ttu-id="6b336-124">**PowerApp を挿入**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b336-124">Open the **Insert a PowerApp** pane:</span></span>

    - <span data-ttu-id="6b336-125">**オプション**をクリックし、**このフォームのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-125">Click **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="6b336-126">**挿入**メニューで、**PowerApp** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-126">Under the **Insert** menu, choose **PowerApp**.</span></span> <span data-ttu-id="6b336-127">最後に、PowerApp を追加する地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-127">Finally, select the region where you would like to add the PowerApp.</span></span> <span data-ttu-id="6b336-128">PowerApps メニュー ボタンの下で PowerApp を埋め込む場合、アクション ウィンドウを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-128">If you want to embed the PowerApp under the PowerApps menu button, choose the Action Pane.</span></span> <span data-ttu-id="6b336-129">ページに直接 PowerApp を埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-129">If you want to embed the PowerApp directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="6b336-130">PowerApps メニュー ボタンを使用して PowerApp にアクセスする場合、代わりに標準のアクション ウィンドウの **PowerApps** メニュー ボタンをクリックし、**PowerApp の挿入**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-130">If the PowerApp will be accessed using the PowerApps menu button, you can alternatively click the **PowerApps** menu button in the standard Action Pane, and then select **Insert a PowerApp**.</span></span>

3. <span data-ttu-id="6b336-131">埋め込み型 PowerApps を構成します。</span><span class="sxs-lookup"><span data-stu-id="6b336-131">Configure the embedded PowerApp:</span></span>

    - <span data-ttu-id="6b336-132">**名前**フィールドは、埋め込まれた PowerApp を含むボタンまたはタブのテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="6b336-132">The **Name** field indicates the text shown for the button or tab that will contain the embedded PowerApp.</span></span> <span data-ttu-id="6b336-133">多くの場合、このフィールドで PowerApp の名前を繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-133">Oftentimes, you may want to repeat the name of the PowerApp in this field.</span></span>
    - <span data-ttu-id="6b336-134">**アプリ ID** は、埋め込む PowerApp の GUID です。</span><span class="sxs-lookup"><span data-stu-id="6b336-134">**App ID** is the GUID for the PowerApp that you want to embed.</span></span> <span data-ttu-id="6b336-135">この値を取得するには、[web.powerapps.com](https://web.powerapps.com) で PowerApp を検索し、**詳細**の**アプリ ID** フィールドを探します。</span><span class="sxs-lookup"><span data-stu-id="6b336-135">To retrieve this value, find the PowerApp on [web.powerapps.com](https://web.powerapps.com) and then locate the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="6b336-136">**PowerApp のデータを入力する**では、必要に応じて、 PowerApp に入力として渡すデータが含まれているフィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-136">For **Input data for the PowerApp**, you can optionally select the field that contains the data that you want to pass to the PowerApp as input.</span></span> <span data-ttu-id="6b336-137">PowerApp が Finance and Operations から送信されるデータにどのようにアクセスするかの詳細に関しては、このトピックの後の [Finance and Operations からのデータを活用する PowerApp の構築](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b336-137">See the section later in this topic titled [Building a PowerApp that leverages data from Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) for details on how the PowerApp can access the data sent from Finance and Operations.</span></span>
    - <span data-ttu-id="6b336-138">埋め込む PowerApp のタイプに一致する**アプリケーション サイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-138">Choose the **Application size** that matches the type of PowerApp that you're embedding.</span></span> <span data-ttu-id="6b336-139">モバイル デバイス用に作成された PowerApps に対しては**シン**を選択し、タブレット用に作成された PowerApps に対しては**ワイド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-139">Select **Thin** for PowerApps built for mobile devices, and **Wide** for PowerApps built for tablets.</span></span> <span data-ttu-id="6b336-140">これにより、埋め込み PowerApp に十分な容量を確保できます。</span><span class="sxs-lookup"><span data-stu-id="6b336-140">This ensures a sufficient amount of space is allotted for the embedded PowerApp.</span></span>
    - <span data-ttu-id="6b336-141">**法人**クイック タブには、PowerApp が利用できる法人を選択する機能があります。</span><span class="sxs-lookup"><span data-stu-id="6b336-141">The **Legal entities** FastTab provides the ability to choose which legal entities the PowerApp is available for.</span></span> <span data-ttu-id="6b336-142">既定では、PowerApp はすべての法人で表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b336-142">The default is to show the PowerApp in all legal entities.</span></span>

4. <span data-ttu-id="6b336-143">コンフィギュレーションが正しいことを確認した後、**挿入**をクリックしてページに PowerApp を埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="6b336-143">After confirming that the configuration is correct, click **Insert** to embed the PowerApp on the page.</span></span> <span data-ttu-id="6b336-144">組み込みの PowerApp を表示するために、ブラウザを更新するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="6b336-144">You will be prompted to refresh the browser in order to see the embedded PowerApp.</span></span>

## <a name="sharing-an-embedded-powerapp"></a><span data-ttu-id="6b336-145">埋め込まれた PowerApp の共有</span><span class="sxs-lookup"><span data-stu-id="6b336-145">Sharing an embedded PowerApp</span></span>

<span data-ttu-id="6b336-146">ページに PowerApp を埋め込み、ページから渡されたデータ コンテキストで正しく動作がしていることを確認したら、この埋め込まれた PowerApp をシステムで他のユーザーと共有することができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-146">After you have embedded a PowerApp on a page and confirmed that it is working correctly with any data context passed from the page, you might want to share this embedded PowerApp with other users in the system.</span></span> <span data-ttu-id="6b336-147">これは、製品の個人用設定機能を使用して、2つの異なる方法で実行できます。</span><span class="sxs-lookup"><span data-stu-id="6b336-147">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="6b336-148">推奨されるシナリオは、すべてのユーザーまたはユーザーのサブセットに個人用設定をプッシュできる、システム管理者によるものです。</span><span class="sxs-lookup"><span data-stu-id="6b336-148">The recommended scenario is through the system administrator, who can push a personalization to all users or a subset of users.</span></span>
- <span data-ttu-id="6b336-149">または、ページの個人用設定をエクスポートし、1 つまたは複数のユーザーに送信し、これらの各ユーザーにその変更をインポートさせることもできます。</span><span class="sxs-lookup"><span data-stu-id="6b336-149">Alternatively, you can export your page's personalizations, send them to one or more users, and have each of those users import those changes.</span></span> <span data-ttu-id="6b336-150">個人用設定のツールバー上の [管理] オプションで、個人用設定をエクスポートし、インポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-150">The Manage option on the personalization toolbar enables you to export and import personalizations.</span></span>

<span data-ttu-id="6b336-151">製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b336-151">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a><span data-ttu-id="6b336-152">Finance and Operations から送信されたデータを活用する PowerApp の構築</span><span class="sxs-lookup"><span data-stu-id="6b336-152">Building a PowerApp that leverages data sent from Finance and Operations</span></span>

<span data-ttu-id="6b336-153">Finance and Operations に埋め込まれる PowerApp を構築するのに重要なのは、Finance and Operations からの入力データを使用することです。</span><span class="sxs-lookup"><span data-stu-id="6b336-153">An important part of building a PowerApp that will be embedded in Finance and Operations is utilizing the input data from Finance and Operations.</span></span> <span data-ttu-id="6b336-154">PowerApp 内で、Param("EntityId") 変数を使用して入力データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6b336-154">Inside the PowerApp, that input data can be accessed using the Param("EntityId") variable.</span></span>

<span data-ttu-id="6b336-155">たとえば、PowerApp の OnStart 機能では、Finance and Operations から次のような変数に入力データを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-155">For example, in the OnStart function of the PowerApp, you could set the input data from Finance and Operations to a variable like this:</span></span>

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a><span data-ttu-id="6b336-156">埋め込まれた PowerApp の表示</span><span class="sxs-lookup"><span data-stu-id="6b336-156">Viewing an embedded PowerApp</span></span>

<span data-ttu-id="6b336-157">Finance and Operations のページに埋め込まれた PowerApp を表示するには、PowerApp が埋め込まれたページにそのまま移動します。</span><span class="sxs-lookup"><span data-stu-id="6b336-157">To view an embedded PowerApp on a page in Finance and Operations, simply go to a page with an embedded PowerApp.</span></span> <span data-ttu-id="6b336-158">PowerApps は、標準アクション ペインの PowerApps ボタンからアクセスできます。また、新しいタブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b336-158">Recall that PowerApps can be accessed through the PowerApps button in the standard Action Pane, or can appear directly on the page as a new tab, FastTab, blade, or as a new section in a workspace.</span></span> <span data-ttu-id="6b336-159">ユーザーが最初に、ページ上に PowerApp を読み込もうとすると、PowerApps にサインインするように表示され、ユーザーにPowerApp を使用する適切なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b336-159">When a user first attempts to load a PowerApp on a page, he or she will be prompted to sign in to PowerApps to ensure the user has the approrpiate permissions to use the PowerApp.</span></span>

## <a name="editing-an-embedded-powerapp"></a><span data-ttu-id="6b336-160">埋め込まれた PowerApp の編集</span><span class="sxs-lookup"><span data-stu-id="6b336-160">Editing an embedded PowerApp</span></span>

<span data-ttu-id="6b336-161">PowerApp がページに埋め込まれた後、その PowerApp の設定をいくつか変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b336-161">After a PowerApp has been embedded onto a page, you may need to make some changes to the configuration of that PowerApp.</span></span> <span data-ttu-id="6b336-162">たとえば、埋め込まれた PowerApp に関連付けられたラベルを変更したり、PowerApp の新しいバージョンが作成された場合に、最新の PowerApp を参照するようアプリ ID を更新したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b336-162">For example, perhaps you want to modify the label associated with the embedded PowerApp or a new version of a PowerApp has been created and you need to update the App ID to point at the latest PowerApp.</span></span>

<span data-ttu-id="6b336-163">埋め込まれた PowerApp のコンフィギュレーションを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6b336-163">Follow these steps to edit the configuration of an embedded PowerApp:</span></span>

1. <span data-ttu-id="6b336-164">**PowerApp を編集**ウインドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="6b336-164">Go to the **Edit a PowerApp** pane.</span></span>

    - <span data-ttu-id="6b336-165">埋め込み型の PowerApp が PowerApps メニュー ボタンによりアクセスされた場合、PowerApps メニュー ボタンを右クリックし、**パーソナライズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-165">If the embedded PowerApp is accessed through the PowerApps menu button, right-click on the PowerApps menu button and select **Personalize**.</span></span> <span data-ttu-id="6b336-166">**Select PowerApp** ドロップダウン メニューから構成する PowerApp を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-166">Select the PowerApp that you want to configure from the **Select PowerApp** drop-down menu.</span></span>
    - <span data-ttu-id="6b336-167">埋め込み型の PowerApp がページに直接表示されたら、**オプション** を選択し、**このフォームのパーソナライズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-167">If the embedded PowerApp appears directly on the page, select **Options**, and then select **Personalize this form**.</span></span> <span data-ttu-id="6b336-168">**選択** ツールを使用し、埋め込まれた PowerApp をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b336-168">Using the **Select** tool, click the embedded PowerApp.</span></span>

2. <span data-ttu-id="6b336-169">PowerApps コンフィギュレーションに必要な変更を行ない、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b336-169">Make the needed modifications to the PowerApps configuration, and then click **Save**.</span></span>

## <a name="removing-an-embedded-powerapp"></a><span data-ttu-id="6b336-170">埋め込まれた PowerApp の削除</span><span class="sxs-lookup"><span data-stu-id="6b336-170">Removing an embedded PowerApp</span></span>

<span data-ttu-id="6b336-171">PowerApp がページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="6b336-171">After a PowerApp has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="6b336-172">このトピックの前半にある [埋め込み PowerApp を編集](#editing-an-embedded-powerapp) セクションからの手順を使用して、**PowerApp を編集**ウィンドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="6b336-172">Go to the **Edit a PowerApp** pane using the instructions from the [Editing an embedded PowerApp](#editing-an-embedded-powerapp) section earlier in this topic.</span></span> <span data-ttu-id="6b336-173">ウィンドウに、削除する埋め込み型 PowerApp の情報が表示されていることを確認してから、**削除**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b336-173">Confirm that the pane displays information for the embedded PowerApp that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="6b336-174">埋め込まれた PowerApp は、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれた PowerApps も削除されます。</span><span class="sxs-lookup"><span data-stu-id="6b336-174">Because an embedded PowerApp is saved as personalization data, clearing your page's personalization will also remove any embedded PowerApps on that page.</span></span> <span data-ttu-id="6b336-175">ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6b336-175">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="6b336-176">ページの個人用設定を削除するには、**オプション**を選択し、**このフォームのパーソナライズ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b336-176">To remove your personalizations on a page, select **Options** and then click **Personalize this form**.</span></span> <span data-ttu-id="6b336-177">**管理**メニューで**クリア**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6b336-177">Under the **Manage** menu, select the **Clear** button.</span></span> <span data-ttu-id="6b336-178">ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。</span><span class="sxs-lookup"><span data-stu-id="6b336-178">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="6b336-179">個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスの個人用設定](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b336-179">See [Personalization the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="6b336-180">付録</span><span class="sxs-lookup"><span data-stu-id="6b336-180">Appendix</span></span>

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a><span data-ttu-id="6b336-181">PowerApp 埋め込み可能な場所についての開発者制御</span><span class="sxs-lookup"><span data-stu-id="6b336-181">Developer control over where a PowerApp can be embedded</span></span>

<span data-ttu-id="6b336-182">既定では、ユーザーは、PowerApps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接 PowerApps を埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-182">By default, users can embed PowerApps on any page, either under the PowerApps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="6b336-183">ただし、必要に応じて開発者が次の方法を実装することで、PowerApps の埋め込みを特定のページのみに許可するようこの機能を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b336-183">However, if required, developers can also configure this feature to only allow embedding of PowerApps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="6b336-184">**isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、PowerApps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにも PowerApps を埋め込むことができません。</span><span class="sxs-lookup"><span data-stu-id="6b336-184">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the PowerApps menu button will not be shown, and users will not be able to embed PowerApps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="6b336-185">**isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接 PowerApps を埋め込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="6b336-185">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed PowerApps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="6b336-186">ページで埋め込みが許可されている場合でも、ユーザーは PowerApps メニュー ボタンを使用して PowerApps を埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="6b336-186">Users will still be able to embed PowerApps through the PowerApps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="6b336-187">次の例は、PowerApps を埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="6b336-187">The following example shows a new class with the two methods needed to configure where PowerApps can be embedded.</span></span>

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return true;
    }
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return true;
    }
}
```

