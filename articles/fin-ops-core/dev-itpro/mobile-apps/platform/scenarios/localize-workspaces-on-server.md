---
title: モバイル ワークスペースのローカライズ
description: このトピックでは、ワークスペース クラスを使用して、ワークスペースにローカライゼーション サポートを提供する方法について説明します。
author: robinarh
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: a7a236e3492e861976a747e4c4d0d97a357c4f14
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745215"
---
# <a name="localize-mobile-workspaces"></a><span data-ttu-id="cf48a-103">モバイル ワークスペースのローカライズ</span><span class="sxs-lookup"><span data-stu-id="cf48a-103">Localize mobile workspaces</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="cf48a-104">いくつかの方法でワークスペース クラスを使用すると、ワークスペースにローカライゼーション サポートを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-104">You can use workspace classes in several ways to provide localization support to workspaces.</span></span>

## <a name="use-config-objects-to-pass-localized-labels"></a><span data-ttu-id="cf48a-105">Config オブジェクトを使用して、ローカライズされたラベルを渡す</span><span class="sxs-lookup"><span data-stu-id="cf48a-105">Use config objects to pass localized labels</span></span>
<span data-ttu-id="cf48a-106">コンフィギュレーション オブジェクトは、モバイル アプリケーションから要求されたときに、ワークスペース メタデータに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-106">A config object can be added to the workspace metadata when it's requested by the mobile app.</span></span> <span data-ttu-id="cf48a-107">後で、config オブジェクトは、ローカライズ サポートを提供するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-107">Later, the config object can be used to provide localization support.</span></span> 

<span data-ttu-id="cf48a-108">たとえば、次のワークスペースは、ビジネス ロジックを通して追加された **pageLink** コントロールの、ローカライズされたラベルを必要とします。</span><span class="sxs-lookup"><span data-stu-id="cf48a-108">For example, the following workspace requires localized labels for the **pageLink** control that you added via the business logic.</span></span>

 ![レンタル リンクのテキストがローカライズされていないお客様の詳細ワークスペース](media/workspace-api/ConfigObjectsPage.png)

<span data-ttu-id="cf48a-110">アプリケーションのビジネス ロジックには、次の図に示すように、**addLink** メソッドの呼び出しが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf48a-110">The business logic for the app contains a call to the **addLink** method, as shown in the following illustration.</span></span> <span data-ttu-id="cf48a-111">この **addLink** メソッドは、現在のお客様の **レンタル** ページへリンクを追加します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-111">This **addLink** method adds a link to the **Rentals** page for the current customer.</span></span> <span data-ttu-id="cf48a-112">この場合、リンクのラベルは **レンタル** です。</span><span class="sxs-lookup"><span data-stu-id="cf48a-112">In this case, the label for the link is **Rentals**.</span></span> <span data-ttu-id="cf48a-113">ただし、リンクのローカライズされたラベルがないため、リンクは常に **レンタル** として表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-113">However, because there isn't a localized label for the link, the link always appears as **Rentals**.</span></span>

![metadataService.addLink への呼び出し](media/workspace-api/ConfigObjectsBusinessLogicOriginal.png)

<span data-ttu-id="cf48a-115">構成オブジェクトを使用してローカライズされたラベルを提供するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-115">To use a config object to provide localized labels, follow these steps.</span></span>

1. <span data-ttu-id="cf48a-116">ラベルのフィールドを含む config クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-116">Create a config class that contains the fields for the labels.</span></span> <span data-ttu-id="cf48a-117">1 つのフィールド、**rentalLinkLabel** が、**pageLink** コントロールのラベルを含むクラスに追加されます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-117">One field, **rentalLinkLabel**, is added to the class that will contain the label for the **pageLink** control.</span></span> <span data-ttu-id="cf48a-118">コンフィギュレーション クラスは、データ契約クラスでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="cf48a-118">The config class must be a data contract class.</span></span>

    ![クラス コード コンフィギュレーション](media/workspace-api/ConfigClass.png)

2. <span data-ttu-id="cf48a-120">コンフィギュレーション クラスは、ワークスペースのワークスペース クラスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-120">The config class is used by a workspace class for the workspace.</span></span> <span data-ttu-id="cf48a-121">ワークスペース クラスには、ワークスペースの **appId** 値が必要です。</span><span class="sxs-lookup"><span data-stu-id="cf48a-121">The workspace class requires the **appId** value of the workspace.</span></span> <span data-ttu-id="cf48a-122">次の図に示すように、アプリ デザイナーでアプリの ID を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-122">You can find the app ID in the App designer, as shown in the following illustration.</span></span>

    ![ワークスペース概要のアプリ ID](media/workspace-api/ConfigWorkspaceSummary.png)

    <span data-ttu-id="cf48a-124">次の図は、**appId** 値が属性に設定されているときのワークスペース クラスの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf48a-124">The following illustration shows what the workspace class looks like when the **appId** value is set on the attribute.</span></span> <span data-ttu-id="cf48a-125">このクラスには、ラベルの値を含む設定オブジェクトを設定するメソッド、**addConfig** も含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf48a-125">The class also contains a method, **addConfig**, that sets a config object that contains the value for the label.</span></span>

    ![ワークスペース クラス](media/workspace-api/ConfigWorkspace.png)

    <span data-ttu-id="cf48a-127">次の図は、モバイル アプリの **appInit** コールの config オブジェクトを示しています。</span><span class="sxs-lookup"><span data-stu-id="cf48a-127">The following illustration shows the config object in the **appInit** call in the mobile app.</span></span>

    ![モバイル アプリのコンフィギュレーション オブジェクト](media/workspace-api/ConfigClientSide.png)

3. <span data-ttu-id="cf48a-129">これで、コンフィギュレーション オブジェクトを使用し、ハードコーディングされたラベルの代わりに **addLink** メソッドに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-129">The config object can now be used and passed to the **addLink** method instead of the hard-coded label.</span></span>

    ![config オブジェクトの呼び出しによる metadataService.addLink](media/workspace-api/ConfigObjectsBusinessLogicFinal.png)

## <a name="use-a-workspace-class-to-update-the-workspace-title-and-description"></a><span data-ttu-id="cf48a-131">ワークスペース クラスを使用して、ワークスペースのタイトルと説明を更新する</span><span class="sxs-lookup"><span data-stu-id="cf48a-131">Use a workspace class to update the workspace title and description</span></span>
<span data-ttu-id="cf48a-132">ワークスペース クラスは、ワークスペースのタイトルと説明のローカライズされた文字列を提供するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf48a-132">A workspace class can be used to provide localized strings for the workspace title and description.</span></span> <span data-ttu-id="cf48a-133">タイトルと説明をローカライズしていない場合、それらを実装した言語がフィールドの言語になります。</span><span class="sxs-lookup"><span data-stu-id="cf48a-133">If you don't localize the title and description, the fields will be in the language that you implemented them in.</span></span> <span data-ttu-id="cf48a-134">この例では、**MyWorkspace** がタイトルで、**サンプル ワークスペース** が説明となっているワークスペースをローカライズします。</span><span class="sxs-lookup"><span data-stu-id="cf48a-134">In this example, we will localize a workspace where **MyWorkspace** is the title and **A sample workspace** is the description.</span></span>

![ワークスペースのリスト](media/workspace-api/LocalizeWorkspaceTitle.png) 

![選択されたワークスペース](media/workspace-api/LocalizeWorkspaceOriginal.png)

1. <span data-ttu-id="cf48a-137">ワークスペースのワークスペース クラスを持っていない場合、ワークスペースのクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-137">If you don't have a workspace class for your workspace, create a workspace class.</span></span>
2. <span data-ttu-id="cf48a-138">**getWorkspaceMetadata** メソッドをオーバーライドし、ワークスペース メタデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-138">Override the **getWorkspaceMetadata** method to get the workspace metadata.</span></span> <span data-ttu-id="cf48a-139">ワークスペースのタイトルおよび説明フィールドのラベルにするワークスペース メタデータが必要です。</span><span class="sxs-lookup"><span data-stu-id="cf48a-139">You must have the workspace metadata to provide labels for the workspace title and description fields.</span></span>
3. <span data-ttu-id="cf48a-140">ワークスペースのタイトルと説明をラベルから設定するには、**workspaceTitle** および **workspaceDescription** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-140">Use the **workspaceTitle** and **workspaceDescription** properties to set the workspace title and description from a label.</span></span> <span data-ttu-id="cf48a-141">次の図では、プレースホルダーが **workspaceTitle** および **workspaceDescription** プロパティに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="cf48a-141">In the following illustration, placeholders are assigned to the **workspaceTitle** and **workspaceDescription** properties.</span></span>

    ![ワークスペース クラスのタイトルと説明を提供](media/workspace-api/LocalizeWorkspaceClass.png)

4. <span data-ttu-id="cf48a-143">ワークスペース クラスをビルドします。</span><span class="sxs-lookup"><span data-stu-id="cf48a-143">Build the workspace class.</span></span>
5. <span data-ttu-id="cf48a-144">モバイル クライアントのアプリ リストを更新します。</span><span class="sxs-lookup"><span data-stu-id="cf48a-144">Update the app list on the mobile client.</span></span>

<span data-ttu-id="cf48a-145">次の図は、英語とデンマーク語を使用する電話機のタイトルと説明を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf48a-145">The following illustration shows the title and description on a phone that uses English and Danish.</span></span>

![最終ワークスペース](media/workspace-api/LocalizeWorkspaceFinal.png)


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]