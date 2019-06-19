---
title: レポート メニュー項目を拡張して、ユーザーのナビゲーションをリダイレクトする
description: このトピックでは、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 266674
ms.assetid: 7bf76862-e320-4a81-81a4-5bda7288e573
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: fd5203580fff2ebd46fc4e671b25015dd168ac92
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554018"
---
# <a name="extend-report-menu-items-to-redirect-user-navigations"></a><span data-ttu-id="31e1e-103">レポート メニュー項目を拡張して、ユーザーのナビゲーションをリダイレクトする</span><span class="sxs-lookup"><span data-stu-id="31e1e-103">Extend report menu items to redirect user navigations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31e1e-104">このトピックでは、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="31e1e-104">This topic shows how to extend existing application menu items so that, after only minimal code changes, navigations are redirected to a custom reporting solution.</span></span>

<span data-ttu-id="31e1e-105">Microsoft Dynamics 365 for Finance and Operations には、カスタム レポート ソリューションをサポートするためのツールの拡張セットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="31e1e-105">Microsoft Dynamics 365 for Finance and Operations includes an expanded set of tools to support custom reporting solutions.</span></span> <span data-ttu-id="31e1e-106">このトピックでは、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="31e1e-106">This topic focuses on the process of extending existing application menu items so that, after only minimal code changes, navigations are redirected to a custom reporting solution.</span></span> <span data-ttu-id="31e1e-107">この手法を使用すると、すべての参照を追跡し既存の申請レポートに置き換えることの不便を避けることができます。</span><span class="sxs-lookup"><span data-stu-id="31e1e-107">By using this technique, you will avoid the inconvenience of tracking down and replacing all references to an existing application report.</span></span> <span data-ttu-id="31e1e-108">アプリケーション ナビゲーションを拡張モデルで定義されているレポートにリダイレクトするには、既存のアプリケーションのメニュー項目を拡張します。</span><span class="sxs-lookup"><span data-stu-id="31e1e-108">Just extend an existing application menu item to redirect application navigations to reports that are defined in an extension model.</span></span> <span data-ttu-id="31e1e-109">次の図は、一般的なアプリケーションのカスタマイズを示しています。</span><span class="sxs-lookup"><span data-stu-id="31e1e-109">The following illustration shows a typical application customization.</span></span>

<span data-ttu-id="31e1e-110">[![extendingmenuitem](./media/extendingmenuitem.png)](./media/extendingmenuitem.png)</span><span class="sxs-lookup"><span data-stu-id="31e1e-110">[![extendingmenuitem](./media/extendingmenuitem.png)](./media/extendingmenuitem.png)</span></span>

## <a name="whats-important-to-know"></a><span data-ttu-id="31e1e-111">知っている必要がある重要なこと</span><span class="sxs-lookup"><span data-stu-id="31e1e-111">What's important to know?</span></span>
<span data-ttu-id="31e1e-112">このソリューションを適用する前に知っておくべき基本的な前提がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="31e1e-112">There are a few basic assumptions that you should be aware of before you apply this solution.</span></span>

- <span data-ttu-id="31e1e-113">拡張メニュー項目を使用して、表示文字列およびターゲットの両方を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="31e1e-113">Extended menu items let you override both the display string and the target.</span></span>
- <span data-ttu-id="31e1e-114">この方法は、単純なクエリに基づくレポートから複雑なレポート データ プロバイダー (RDP) に基づくレポートまで、すべてのタイプのレポートに使用できます。</span><span class="sxs-lookup"><span data-stu-id="31e1e-114">This technique can be used for all types of reports, from simple query-based reports to complex report data provider (RDP)–based reports.</span></span>
- <span data-ttu-id="31e1e-115">拡張メニュー項目は、コントローラ クラスを使用してレポート セッションを編成するレポートおよびソリューションへ直接参照に使用できます。</span><span class="sxs-lookup"><span data-stu-id="31e1e-115">Extended menu items are available for direct references to reports and solutions that orchestrate the reporting session by using a controller class.</span></span>

## <a name="extend-report-menu-items"></a><span data-ttu-id="31e1e-116">レポート メニュー項目の拡張</span><span class="sxs-lookup"><span data-stu-id="31e1e-116">Extend report menu items</span></span>
<span data-ttu-id="31e1e-117">次のチュートリアルでは、メニュー項目の拡張機能を使用して、アプリケーション内のユーザー ナビゲーションをカスタム ソリューションにリダイレクトする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="31e1e-117">The following walkthrough shows how to use menu item extensions to redirect user navigations in the application to a custom solution.</span></span> <span data-ttu-id="31e1e-118">このソリューションには、Fleet Management アプリケーション用のカスタム**顧客リスト** レポートが含まれており、純粋な拡張モデルですべてのアプリケーションのカスタマイズが定義されています。</span><span class="sxs-lookup"><span data-stu-id="31e1e-118">The solution includes a custom **Customer list** report for the Fleet Management application and defines all the application customizations in a pure extension model.</span></span> <span data-ttu-id="31e1e-119">次の図は、カスタムの **顧客リスト** レポートにアクセスするために使用するメニュー項目を示しています。</span><span class="sxs-lookup"><span data-stu-id="31e1e-119">The following illustration shows the menu item that you use to access the custom **Customer list** report.</span></span>

<span data-ttu-id="31e1e-120">[![fleet-workspace-customer-list](./media/fleet-workspace-customer-list.png)](./media/fleet-workspace-customer-list.png)</span><span class="sxs-lookup"><span data-stu-id="31e1e-120">[![fleet-workspace-customer-list](./media/fleet-workspace-customer-list.png)](./media/fleet-workspace-customer-list.png)</span></span>

1. <span data-ttu-id="31e1e-121">**アプリケーション カスタマイズの新しいモデルを作成します。**</span><span class="sxs-lookup"><span data-stu-id="31e1e-121">**Create a new model for your application customizations.**</span></span> <span data-ttu-id="31e1e-122">拡張モデルに関する詳細については、[カスタマイズ: オーバーレイおよび拡張機能](../extensibility/customization-overlayering-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31e1e-122">For more information about extension models, see [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>
2. <span data-ttu-id="31e1e-123">**Microsoft Visual Studioで新しいプロジェクトを作成し、** **カスタム レポートを追加します。**</span><span class="sxs-lookup"><span data-stu-id="31e1e-123">**Create a new project in Microsoft Visual Studio,** **and add your custom report.**</span></span> <span data-ttu-id="31e1e-124">また、すべてのソリューション コンポーネントを追加します。</span><span class="sxs-lookup"><span data-stu-id="31e1e-124">Additionally, add all the solution artifacts.</span></span> <span data-ttu-id="31e1e-125">これらのコンポーネントには、RDP クラスまたはソース クエリ、コントローラー クラス、UI ビルダー (ある場合) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="31e1e-125">These artifacts include the RDP class or source query, the controller class, and UI builders, if they are present.</span></span>
3. <span data-ttu-id="31e1e-126">**レポートにアクセスするために使用するメニュー項目の拡張機能を作成します。**</span><span class="sxs-lookup"><span data-stu-id="31e1e-126">**Create an extension of the menu item that is used to access the report.**</span></span> <span data-ttu-id="31e1e-127">この例では、出力メニュー項目は **FMCustomerListReport** と名前が付けられています。</span><span class="sxs-lookup"><span data-stu-id="31e1e-127">In this example, the output menu item is named **FMCustomerListReport**.</span></span> <span data-ttu-id="31e1e-128">メニュー項目の構造を使用して、アプリケーションで公開されているメニュー項目の名前を見つけます。</span><span class="sxs-lookup"><span data-stu-id="31e1e-128">Use the menu item structure to find the menu item name that is exposed in the application.</span></span> <span data-ttu-id="31e1e-129">次の図は、アプリケーション エクスプローラーでのアクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="31e1e-129">The following illustration shows the action in Application Explorer.</span></span>

    <span data-ttu-id="31e1e-130">[![レポートにアクセスするために使用するメニュー項目の拡張機能の作成](./media/fleet-extension-create-menu-extension-1024x632.png)](./media/fleet-extension-create-menu-extension.png)</span><span class="sxs-lookup"><span data-stu-id="31e1e-130">[![Creating an extension of the menu item that is used to access the report](./media/fleet-extension-create-menu-extension-1024x632.png)](./media/fleet-extension-create-menu-extension.png)</span></span>

4. <span data-ttu-id="31e1e-131">**メニュー項目の拡張機能のプロパティの変更。**</span><span class="sxs-lookup"><span data-stu-id="31e1e-131">**Modify the properties of the menu item extension.**</span></span> <span data-ttu-id="31e1e-132">メニュー項目のレポート デザインまたはコントローラ＝の参照を更新して、カスタム ソリューションに直接ナビゲートします。</span><span class="sxs-lookup"><span data-stu-id="31e1e-132">Update the report design or controller reference in the menu item to direct navigations to your custom solution.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31e1e-133">オブジェクトに対して実行できるプロパティの変更は、元のアプリケーション ソリューションによって異なります。</span><span class="sxs-lookup"><span data-stu-id="31e1e-133">The property changes that you can make on the object depend on the original application solution.</span></span> <span data-ttu-id="31e1e-134">アプリケーションのレポートは、コントローラーを使用してソリューションを管理する場合、コントローラー クラスがレポートに必要になります。</span><span class="sxs-lookup"><span data-stu-id="31e1e-134">If the application report manages the solution by using a controller, a controller class is required for the report.</span></span>

5. <span data-ttu-id="31e1e-135">**ソリューションを再構築してカスタム レポートを配置します。**</span><span class="sxs-lookup"><span data-stu-id="31e1e-135">**Rebuild the solution, and deploy the custom report.**</span></span>

<span data-ttu-id="31e1e-136">これで、レポート メニュー項目の拡張を完了しました。</span><span class="sxs-lookup"><span data-stu-id="31e1e-136">You've now finished extending the report menu item.</span></span> <span data-ttu-id="31e1e-137">標準のメニュー項目へのナビゲーションは、カスタム レポート ソリューションにリダイレクトされるようになります。</span><span class="sxs-lookup"><span data-stu-id="31e1e-137">Navigations to the standard menu item will now be redirected to your custom reporting solution.</span></span>
