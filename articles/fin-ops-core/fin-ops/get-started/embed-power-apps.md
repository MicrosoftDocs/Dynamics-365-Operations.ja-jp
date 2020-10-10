---
title: Power Apps からキャンバス アプリを埋め込む
description: このトピックでは、Microsoft Power Apps のキャンバス アプリをクライアントに埋め込み、製品の機能を拡張する方法について説明します。
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
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
ms.openlocfilehash: e57e4567a80aa9f9ba5ac434b0d71204460e164f
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893110"
---
# <a name="embed-canvas-apps-from-power-apps"></a><span data-ttu-id="475d3-103">Power Apps からキャンバス アプリを埋め込む</span><span class="sxs-lookup"><span data-stu-id="475d3-103">Embed canvas apps from Power Apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="475d3-104">Microsoft Power Apps は開発者と技術者以外のユーザーがコードを記述せずにモバイル デバイス、タブレット、および Web 用のカスタム ビジネス アプリを構築できるようにするサービスです。</span><span class="sxs-lookup"><span data-stu-id="475d3-104">Microsoft Power Apps is a service that lets developers and non-technical users build custom business apps for mobile devices, tablets, and the web without writing code.</span></span> <span data-ttu-id="475d3-105">Finance and Operations アプリは Power Apps との統合をサポートします。</span><span class="sxs-lookup"><span data-stu-id="475d3-105">Finance and Operations apps support integration with Power Apps.</span></span> <span data-ttu-id="475d3-106">ユーザー、組織、またはより幅広いエコシステムが開発するキャンバス アプリは、製品の機能を拡張するために Finance and Operations アプリに組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-106">Canvas apps that you, your organization, or the broader ecosystem develop can be embedded into Finance and Operations apps to augment the product's functionality.</span></span> <span data-ttu-id="475d3-107">たとえば、別のシステムから取得した情報で Finance and Operations アプリを補完するために、Power Apps からキャンバス アプリを構築できます。</span><span class="sxs-lookup"><span data-stu-id="475d3-107">For example, you might build a canvas app from Power Apps to supplement a Finance and Operations app with information that is retrieved from another system.</span></span>

<span data-ttu-id="475d3-108">Power Apps の埋め込みに関する詳細については、短い [Power Apps を組み込む方法](https://www.youtube.com/watch?v=x3qyA1bH-NY) ビデオを確認してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-108">To learn more about embedding Power Apps, watch the short [How to embed Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY) video.</span></span>

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a><span data-ttu-id="475d3-109">埋め込みキャンバス アプリを Power Apps からページに追加する</span><span class="sxs-lookup"><span data-stu-id="475d3-109">Adding an embedded canvas app from Power Apps to a page</span></span>

### <a name="overview"></a><span data-ttu-id="475d3-110">概要</span><span class="sxs-lookup"><span data-stu-id="475d3-110">Overview</span></span>

<span data-ttu-id="475d3-111">Power Apps からクライアントにキャンバス アプリを埋め込む前に、目的のビジュアルまたは機能を備えたアプリを見つけるか構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="475d3-111">Before you embed a canvas app from Power Apps into the client, you must find or build an app that has the desired visuals or functionality.</span></span> <span data-ttu-id="475d3-112">このトピックには、アプリを構築するプロセスの詳細な説明は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="475d3-112">This topic doesn't include a detailed description of the process for building apps.</span></span> <span data-ttu-id="475d3-113">初めて Power Apps を使用する場合は、[Power Apps ドキュメント](https://docs.microsoft.com/powerapps/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-113">If you're new to Power Apps, see the [Power Apps documentation](https://docs.microsoft.com/powerapps/).</span></span>

<span data-ttu-id="475d3-114">アプリを埋め込む準備ができたときにページ上の特定のキャンバス アプリにアクセスするには、2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="475d3-114">There are two ways to access a specific canvas app on a page when you're ready to embed the app.</span></span> <span data-ttu-id="475d3-115">シナリオに適したアプローチを選択できます。</span><span class="sxs-lookup"><span data-stu-id="475d3-115">You can choose whichever approach fits your scenario better.</span></span> <span data-ttu-id="475d3-116">最初のアプローチでは、標準のアクション ペインに追加された **Power Apps** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="475d3-116">The first approach uses the **Power Apps** button that has been added to the standard Action Pane.</span></span> <span data-ttu-id="475d3-117">このアプローチを使用して追加したアプリは、**Power Apps** メニュー ボタン上に項目として表示されます。</span><span class="sxs-lookup"><span data-stu-id="475d3-117">Apps that you add by using this approach appear as items on the **Power Apps** menu button.</span></span> <span data-ttu-id="475d3-118">これらの項目の 1 つを選択すると、埋め込みアプリを含むサイド ペインが表示されます。</span><span class="sxs-lookup"><span data-stu-id="475d3-118">When you select one of these items, a side pane that contains the embedded app appears.</span></span> <span data-ttu-id="475d3-119">または、アプリを新しいタブ、クイック タブ、あるいはブレードとして、またはワークスペースの新しいセクションとしてページに直接埋め込むこともできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-119">Alternatively, you can embed an app directly on a page as a new tab, FastTab, or blade, or as a new section in a workspace.</span></span>

<span data-ttu-id="475d3-120">埋め込みキャンバス アプリを構成するときに、アプリへのコンテキストとして送信する単一のフィールドを選択できます。</span><span class="sxs-lookup"><span data-stu-id="475d3-120">When you configure your embedded canvas app, you can select a single field that you want to send as context to the app.</span></span> <span data-ttu-id="475d3-121">この手順により、現在表示しているデータに基づいてアプリが応答できるようになります。</span><span class="sxs-lookup"><span data-stu-id="475d3-121">This step enables the app to be responsive, based on the data that you're currently viewing.</span></span>

> [!NOTE]
> <span data-ttu-id="475d3-122">現在、このメカニズムを使用して、モデル化されたアプリを埋め込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="475d3-122">You can't currently use this mechanism to embed modeled apps.</span></span>  

### <a name="details"></a><span data-ttu-id="475d3-123">細目</span><span class="sxs-lookup"><span data-stu-id="475d3-123">Details</span></span>

<span data-ttu-id="475d3-124">次の手順では、Power Apps から Web クライアントにキャンバス アプリを埋め込む方法を示します。</span><span class="sxs-lookup"><span data-stu-id="475d3-124">The following procedure shows how to embed a canvas app from Power Apps into the web client.</span></span>

1. <span data-ttu-id="475d3-125">キャンバス アプリを埋め込むページに移動します。</span><span class="sxs-lookup"><span data-stu-id="475d3-125">Go to the page where you want to embed the canvas app.</span></span> <span data-ttu-id="475d3-126">このページは、入力としてアプリに渡す必要があるデータを含むページになります。</span><span class="sxs-lookup"><span data-stu-id="475d3-126">This page will be the page that contains data that must be passed to the app as input.</span></span>
2. <span data-ttu-id="475d3-127">**Power Apps からアプリを追加**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="475d3-127">Open the **Add an app from Power Apps** pane:</span></span>

    - <span data-ttu-id="475d3-128">**オプション**をクリックし、**このページのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-128">Click **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="475d3-129">**挿入**メニューで、**Power Apps** を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-129">Under the **Insert** menu, choose **Power Apps**.</span></span> <span data-ttu-id="475d3-130">最後に、アプリを追加する地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-130">Finally, select the region where you would like to add the app.</span></span> <span data-ttu-id="475d3-131">Power Apps メニュー ボタンの下でアプリを埋め込む場合、アクション ウィンドウを選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-131">If you want to embed the app under the Power Apps menu button, choose the Action Pane.</span></span> <span data-ttu-id="475d3-132">ページに直接アプリを埋め込む場合、適切なタブ、クイック タブ、ブレード、またはセクション (ワークスペースにいる場合) を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-132">If you want to embed the app directly onto the page, choose the appropriate tab, FastTab, blade, or section (if you're on a workspace).</span></span>
    - <span data-ttu-id="475d3-133">Power Apps メニュー ボタンを使用してアプリにアクセスする場合、代わりに標準のアクション ウィンドウの **Power Apps** メニュー ボタンをクリックし、**アプリの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-133">If the app will be accessed using the Power Apps menu button, you can alternatively click the **Power Apps** menu button in the standard Action Pane, and then select **Add an app**.</span></span>

3. <span data-ttu-id="475d3-134">埋め込み型アプリを構成します。</span><span class="sxs-lookup"><span data-stu-id="475d3-134">Configure the embedded app:</span></span>

    - <span data-ttu-id="475d3-135">**名前**フィールドは、埋め込まれたアプリを含むボタンまたはタブのテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="475d3-135">The **Name** field indicates the text shown for the button or tab that will contain the embedded app.</span></span> <span data-ttu-id="475d3-136">多くの場合、このフィールドでアプリの名前を繰り返すことができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-136">Oftentimes, you may want to repeat the name of the app in this field.</span></span>
    - <span data-ttu-id="475d3-137">**アプリ ID** フィールドは、埋め込むキャンバス アプリのグローバル一意識別子 (GUID) を示します。</span><span class="sxs-lookup"><span data-stu-id="475d3-137">The **App ID** field indicates the globally unique identifier (GUID) for the canvas app that you want to embed.</span></span> <span data-ttu-id="475d3-138">この値を取得するには、[web.powerapps.com](https://web.powerapps.com) でアプリを検索し、**詳細** の **アプリ ID** フィールドを確認します。</span><span class="sxs-lookup"><span data-stu-id="475d3-138">To retrieve this value, find the app on [web.powerapps.com](https://web.powerapps.com), and then look in the **App ID** field under **Details**.</span></span>
    - <span data-ttu-id="475d3-139">**アプリのコンテキストを入力する**では、必要に応じて、アプリに入力として渡すデータが含まれているフィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-139">For **Input context for the app**, you can optionally select the field that contains the data that you want to pass to the app as input.</span></span> <span data-ttu-id="475d3-140">アプリが Finance and Operations アプリから送信されるデータにアクセスする方法の詳細に関しては、このトピックの後の [Finance and Operations アプリから送信されるデータを活用するアプリの構築](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-140">See the section later in this topic titled [Building an app that leverages data sent from Finance and Operations apps](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) for details on how the app can access the data sent from Finance and Operations apps.</span></span>
    - <span data-ttu-id="475d3-141">埋め込むアプリのタイプに一致する**アプリケーション サイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-141">Choose the **Application size** that matches the type of app that you're embedding.</span></span> <span data-ttu-id="475d3-142">モバイル デバイス用に作成されたアプリに対しては**シン**を選択し、タブレット用に作成されたアプリに対しては**ワイド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-142">Select **Thin** for apps built for mobile devices, and **Wide** for apps built for tablets.</span></span> <span data-ttu-id="475d3-143">これにより、埋め込みアプリに十分な容量を確保できます。</span><span class="sxs-lookup"><span data-stu-id="475d3-143">This ensures a sufficient amount of space is allotted for the embedded app.</span></span>
    - <span data-ttu-id="475d3-144">**法人**クイック タブには、アプリが利用できる法人を選択する機能があります。</span><span class="sxs-lookup"><span data-stu-id="475d3-144">The **Legal entities** FastTab provides the ability to choose which legal entities the app is available for.</span></span> <span data-ttu-id="475d3-145">既定では、アプリをすべての法人に対してアクセス可能にします。</span><span class="sxs-lookup"><span data-stu-id="475d3-145">The default is to make the app accessible to all legal entities.</span></span> <span data-ttu-id="475d3-146">このオプションは、[保存されたビュー](saved-views.md) が無効になっている場合にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="475d3-146">This option is only available when the [Saved views](saved-views.md) feature is disabled.</span></span> 

4. <span data-ttu-id="475d3-147">構成が正しいことを確認した後、**挿入**をクリックしてページに Power App を埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="475d3-147">After confirming that the configuration is correct, click **Insert** to embed the Power App on the page.</span></span> <span data-ttu-id="475d3-148">組み込みアプリを表示するために、ブラウザを更新するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="475d3-148">You will be prompted to refresh the browser in order to see the embedded app.</span></span>

## <a name="sharing-an-embedded-app"></a><span data-ttu-id="475d3-149">埋め込まれたアプリの共有</span><span class="sxs-lookup"><span data-stu-id="475d3-149">Sharing an embedded app</span></span>

<span data-ttu-id="475d3-150">ページにキャンバス アプリを埋め込み、そのページから渡されたデータ コンテキストで正しく動作することを確認したら、システム内の他のユーザーとアプリを共有できます。</span><span class="sxs-lookup"><span data-stu-id="475d3-150">After you've embedded a canvas app on a page and confirmed that it's working correctly with any data context that is passed from that page, you might want to share the app with other users in the system.</span></span> <span data-ttu-id="475d3-151">埋め込みキャンバス アプリを共有するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="475d3-151">To share an embedded canvas app, follow these steps.</span></span>

1. <span data-ttu-id="475d3-152">適切なユーザーと [キャンバス アプリを共有](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) して、Power Apps でアプリにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="475d3-152">[Share the canvas app](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) with the appropriate users, so that they can access the app in Power Apps.</span></span> 

2. <span data-ttu-id="475d3-153">対象とするユーザーが適切な個人用設定を持っていることを確認して、ユーザーがページを表示したときに埋め込みアプリが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="475d3-153">Make sure that the targeted users have the appropriate personalizations, so that the embedded app appears when those users view the page.</span></span> <span data-ttu-id="475d3-154">次のアプローチのいずれかを使用できます:</span><span class="sxs-lookup"><span data-stu-id="475d3-154">You can use either of the following approaches:</span></span>

    - <span data-ttu-id="475d3-155">推奨: [保存されたビュー](saved-views.md) 機能を使用して、埋め込みアプリを含むビューを作成して公開します。</span><span class="sxs-lookup"><span data-stu-id="475d3-155">Recommended: Use the [Saved views](saved-views.md) feature to create and publish a view that includes the embedded app.</span></span> <span data-ttu-id="475d3-156">このアプローチを使用すると、公開されたビューの対象となるセキュリティ ロールを持つすべてのユーザーが Finance and Operations アプリでアプリを確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="475d3-156">This approach ensures that all users who have the security roles that are targeted by the published view will see the app in Finance and Operations apps.</span></span> 
    - <span data-ttu-id="475d3-157">保存されたビュー機能を有効にしていない場合は、システム管理者が、埋め込みアプリを含む個人用設定をすべてのユーザーまたは一部のユーザーにプッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-157">If you don't have the Saved views feature turned on, you can have the system admin push a personalization that includes the embedded app to all users or a subset of users.</span></span> <span data-ttu-id="475d3-158">また、ページの個人用設定をエクスポートして、1 人または複数のユーザーに送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-158">Alternatively, you can export your page's personalizations, and send them to one or more users.</span></span> <span data-ttu-id="475d3-159">これらの各ユーザーは、個人用設定をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-159">Each of those users can then import the personalizations.</span></span> <span data-ttu-id="475d3-160">個人用設定のツールバーには、個人用設定をエクスポートおよびインポートするためのアクションがあります。</span><span class="sxs-lookup"><span data-stu-id="475d3-160">The personalization toolbar has actions that let you export and import personalizations.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="475d3-161">キャンバス アプリが外部ユーザーと共有されている場合、これらのユーザーは、Finance and Operations アプリ内の埋め込みアプリを使用できません。</span><span class="sxs-lookup"><span data-stu-id="475d3-161">If the canvas app has been shared with external users, those users can't use the embedded app inside Finance and Operations apps.</span></span> <span data-ttu-id="475d3-162">ただし、Power Apps 内でアプリに直接アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-162">However, they can access the app directly inside Power Apps.</span></span> <span data-ttu-id="475d3-163">外部ユーザーには、Finance and Operations アプリが配置されている Microsoft 365 Azure ディレクトリに属さないゲストとユーザーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="475d3-163">External users include guests and users who don't belong to the Microsoft 365 Azure Directory where the Finance and Operations app is deployed.</span></span>

<span data-ttu-id="475d3-164">製品での個人用設定の機能について、およびそれらの使用方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-164">See [Personalize the user experience](personalize-user-experience.md) for more details about the personalization capabilities in the product and how to use them.</span></span>

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a><span data-ttu-id="475d3-165">Finance and Operations アプリから送信されるデータを使用するキャンバス アプリの構築</span><span class="sxs-lookup"><span data-stu-id="475d3-165">Building a canvas app that uses data that is sent from Finance and Operations apps</span></span>

<span data-ttu-id="475d3-166">Finance and Operations アプリに埋め込まれるキャンバス アプリを構築する場合、プロセスの重要な部分の 1 つは、Finance and Operations アプリからの入力データを使用することです。</span><span class="sxs-lookup"><span data-stu-id="475d3-166">When you build a canvas app that will be embedded in a Finance and Operations app, one important part of the process is to use the input data from that Finance and Operations app.</span></span> <span data-ttu-id="475d3-167">Power Apps 開発経験から、Finance and Operations アプリから渡される入力データには、**Param("EntityId")** 変数を使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-167">From the Power Apps development experience, the input data that is passed from a Finance and Operations app can be accessed by using the **Param("EntityId")** variable.</span></span>

<span data-ttu-id="475d3-168">たとえば、アプリの OnStart 機能では、Finance and Operations アプリから次のような変数に入力データを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-168">For example, in the OnStart function of the app, you could set the input data from Finance and Operations apps to a variable like this:</span></span>

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a><span data-ttu-id="475d3-169">キャンバス アプリの表示</span><span class="sxs-lookup"><span data-stu-id="475d3-169">Viewing a canvas app</span></span>

<span data-ttu-id="475d3-170">Finance and Operations アプリのページに埋め込みキャンバス アプリを表示するには、埋め込みアプリがあるページに移動するだけです。</span><span class="sxs-lookup"><span data-stu-id="475d3-170">To view an embedded canvas app on a page in Finance and Operations apps, just go to a page that has an embedded app.</span></span> <span data-ttu-id="475d3-171">標準アクション ペインの **Power Apps** ボタンを使用してアプリにアクセスできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-171">Remember that apps can be accessed by using the **Power Apps** button on the standard Action Pane.</span></span> <span data-ttu-id="475d3-172">または、新しいタブ、クイック タブ、あるいはブレードとして、またはワークスペースの新しいセクションとしてページに直接表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-172">Alternatively, they can appear directly on the page as a new tab, or FastTab, or blade, or as a new section in a workspace.</span></span> <span data-ttu-id="475d3-173">ユーザーがページに最初にアプリを読み込もうとすると、サインインするように求められます。</span><span class="sxs-lookup"><span data-stu-id="475d3-173">When users first try to load an app on a page, they will be prompted to sign in.</span></span> <span data-ttu-id="475d3-174">この手順により、ユーザーはアプリを使用するための適切なアクセス許可を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="475d3-174">This step ensures that the users have the appropriate permissions to use the app.</span></span>

## <a name="editing-an-embedded-app"></a><span data-ttu-id="475d3-175">埋め込まれたアプリの編集</span><span class="sxs-lookup"><span data-stu-id="475d3-175">Editing an embedded app</span></span>

<span data-ttu-id="475d3-176">アプリがページに埋め込まれた後、そのアプリの設定をいくつか変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="475d3-176">After an app has been embedded onto a page, you may need to make some changes to the configuration of the app.</span></span> <span data-ttu-id="475d3-177">たとえば、埋め込まれたアプリに関連付けられたラベルを変更したり、アプリの新しいバージョンが作成された場合に、アプリ ID を最新の時点のものに更新したりする必要があります。</span><span class="sxs-lookup"><span data-stu-id="475d3-177">For example, perhaps you want to modify the label associated with the embedded app or a new version of the app has been created and you need to update the App ID to point at the latest.</span></span>

<span data-ttu-id="475d3-178">埋め込まれたアプリのコンフィギュレーションを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="475d3-178">Follow these steps to edit the configuration of an embedded app:</span></span>

1. <span data-ttu-id="475d3-179">**アプリの編集**ウインドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="475d3-179">Go to the **Edit the app** pane.</span></span>

    - <span data-ttu-id="475d3-180">埋め込み型のアプリが Power Apps メニュー ボタンによりアクセスされた場合、Power Apps メニュー ボタンを右クリックし、**パーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-180">If the embedded app is accessed through the Power Apps menu button, right-click on the Power Apps menu button and select **Personalize**.</span></span> <span data-ttu-id="475d3-181">**アプリの選択**ドロップダウン メニューから構成するアプリを選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-181">Select the app that you want to configure from the **Select an app** drop-down menu.</span></span>
    - <span data-ttu-id="475d3-182">埋め込み型のアプリがページに直接表示されたら、**オプション**を選択し、**このページのパーソナライズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="475d3-182">If the embedded app appears directly on the page, select **Options**, and then select **Personalize this page**.</span></span> <span data-ttu-id="475d3-183">**選択**ツールを使用し、埋め込まれたアプリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="475d3-183">Using the **Select** tool, click the embedded app.</span></span>

2. <span data-ttu-id="475d3-184">アプリ コンフィギュレーションに必要な変更を行ない、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="475d3-184">Make the needed modifications to the app configuration, and then click **Save**.</span></span>

## <a name="removing-an-app"></a><span data-ttu-id="475d3-185">アプリの削除</span><span class="sxs-lookup"><span data-stu-id="475d3-185">Removing an app</span></span>

<span data-ttu-id="475d3-186">アプリがページに埋め込まれた後、必要に応じて削除するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="475d3-186">After an app has been embedded onto a page, there are two ways to remove it if needed:</span></span>

- <span data-ttu-id="475d3-187">このトピックの前半にある [埋め込みアプリの編集](#editing-an-embedded-app) セクションからの手順を使用して、**アプリの編集**ウィンドウに移動します。</span><span class="sxs-lookup"><span data-stu-id="475d3-187">Go to the **Edit an app** pane using the instructions from the [Editing an embedded app](#editing-an-embedded-app) section earlier in this topic.</span></span> <span data-ttu-id="475d3-188">ウィンドウに、削除する埋め込み型アプリの情報が表示されていることを確認してから、**削除**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="475d3-188">Confirm that the pane displays information for the embedded app that you would like to remove, and then click the **Delete** button.</span></span>
- <span data-ttu-id="475d3-189">埋め込まれたアプリは、個人用設定データとして保存されるため、ページの個人用設定をクリアすると、そのページの埋め込まれたアプリも削除されます。</span><span class="sxs-lookup"><span data-stu-id="475d3-189">Because the embedded app is saved as personalization data, clearing your page's personalization will also remove any embedded apps on that page.</span></span> <span data-ttu-id="475d3-190">ページの個人用設定をクリアするのは、永久的なもので元に戻すことはできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-190">Note that clearing the page's personalization is permanent and cannot be undone.</span></span> <span data-ttu-id="475d3-191">ページの個人用設定を削除するには、**オプション**を選択して**このページのパーソナライズ**、最後に**クリア** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="475d3-191">To remove your personalizations on a page, select **Options**, and then **Personalize this page**, and finally the **Clear** button.</span></span> <span data-ttu-id="475d3-192">ブラウザを更新した後、このページの以前のすべての個人用設定は、削除されます。</span><span class="sxs-lookup"><span data-stu-id="475d3-192">After refreshing your browser, all the previous personalizations for this page will be removed.</span></span> <span data-ttu-id="475d3-193">個人用設定を使用してページを最適化する方法の詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="475d3-193">See [Personalize the user experience](personalize-user-experience.md) for more information about how to optimize pages using personalization.</span></span>

## <a name="appendix"></a><span data-ttu-id="475d3-194">付録</span><span class="sxs-lookup"><span data-stu-id="475d3-194">Appendix</span></span>

### <a name="developer-specifying-where-an-app-can-be-embedded"></a><span data-ttu-id="475d3-195">[開発者] アプリの埋め込み先の指定</span><span class="sxs-lookup"><span data-stu-id="475d3-195">[Developer] Specifying where an app can be embedded</span></span>

<span data-ttu-id="475d3-196">既定では、ユーザーは、Power Apps メニュー ボタンの下または、タブ、クイック タブ、ブレード、またはワークスペースの新しいセクションとして任意のページに直接をアプリを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-196">By default, users can embed apps on any page, either under the Power Apps menu button or directly on the page as a tab, FastTab, blade or as a new section in a workspace.</span></span> <span data-ttu-id="475d3-197">ただし、必要に応じて開発者が次の方法を実装することで、アプリの埋め込みを特定のページのみに許可するようこの機能を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="475d3-197">However, if required, developers can also configure this feature to only allow embedding of apps on certain pages by implementing the following methods:</span></span>

- <span data-ttu-id="475d3-198">**isPowerAppPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、Power Apps メニュー ボタンは表示されず、ユーザーは、タブを含むこのページのどこにもアプリを埋め込むことができません。</span><span class="sxs-lookup"><span data-stu-id="475d3-198">**isPowerAppPersonalizationEnabled** – If this method returns false for a specific page, then the Power Apps menu button will not be shown, and users will not be able to embed apps anywhere on this page, including as a tab.</span></span>
- <span data-ttu-id="475d3-199">**isPowerAppTabPersonalizationEnabled** ー このメソッドが、特定のページに対して false を返す場合、タブ、クイック タブ、またはパノラマ セクションとしてページに直接アプリを埋め込むことはできません。</span><span class="sxs-lookup"><span data-stu-id="475d3-199">**isPowerAppTabPersonalizationEnabled** – If this method returns false for a specific page, then users will not be able to embed apps directly on the page as a tab, FastTab, or panorama section.</span></span> <span data-ttu-id="475d3-200">ページで埋め込みが許可されている場合でも、ユーザーは Power Apps メニュー ボタンを使用してアプリを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="475d3-200">Users will still be able to embed apps through the Power Apps menu button if embedding is allowed on the page.</span></span>

<span data-ttu-id="475d3-201">次の例は、アプリを埋め込むための構成をするために必要な 2 つのメソッドを持つ新しいクラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="475d3-201">The following example shows a new class with the two methods needed to configure where apps can be embedded.</span></span>

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
