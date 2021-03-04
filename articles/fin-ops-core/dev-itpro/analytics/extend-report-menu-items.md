---
title: レポート メニューの項目を拡張してユーザーナビゲーションをリダイレクトします。
description: このトピックでは、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 266674
ms.assetid: 7bf76862-e320-4a81-81a4-5bda7288e573
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: ea070a892da752249fc41d3c90ad18b262adb39e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093991"
---
# <a name="extend-report-menu-items-to-redirect-user-navigation"></a><span data-ttu-id="ec7d6-103">レポート メニューの項目を拡張してユーザーナビゲーションをリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-103">Extend report menu items to redirect user navigation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec7d6-104">このトピックでは、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-104">This topic shows how to extend existing application menu items so that, after only minimal code changes, navigations are redirected to a custom reporting solution.</span></span>

<span data-ttu-id="ec7d6-105">このトピックでは、コード変更を最小限にして、ナビゲーションをカスタム レポート ソリューションにリダイレクトするように、既存のアプリケーション メニュー項目を拡張するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-105">This topic focuses on the process of extending existing application menu items so that, after only minimal code changes, navigations are redirected to a custom reporting solution.</span></span> <span data-ttu-id="ec7d6-106">この手法を使用すると、すべての参照を追跡し既存の申請レポートに置き換えることの不便を避けることができます。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-106">By using this technique, you will avoid the inconvenience of tracking down and replacing all references to an existing application report.</span></span> <span data-ttu-id="ec7d6-107">アプリケーション ナビゲーションを拡張モデルで定義されているレポートにリダイレクトするには、既存のアプリケーションのメニュー項目を拡張します。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-107">Just extend an existing application menu item to redirect application navigations to reports that are defined in an extension model.</span></span> <span data-ttu-id="ec7d6-108">次の図は、一般的なアプリケーションのカスタマイズを示しています。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-108">The following illustration shows a typical application customization.</span></span>

<span data-ttu-id="ec7d6-109">[![extendingmenuitem](./media/extendingmenuitem.png)](./media/extendingmenuitem.png)</span><span class="sxs-lookup"><span data-stu-id="ec7d6-109">[![extendingmenuitem](./media/extendingmenuitem.png)](./media/extendingmenuitem.png)</span></span>

## <a name="whats-important-to-know"></a><span data-ttu-id="ec7d6-110">知っている必要がある重要なこと</span><span class="sxs-lookup"><span data-stu-id="ec7d6-110">What's important to know?</span></span>
<span data-ttu-id="ec7d6-111">このソリューションを適用する前に知っておくべき基本的な前提がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-111">There are a few basic assumptions that you should be aware of before you apply this solution.</span></span>

- <span data-ttu-id="ec7d6-112">拡張メニュー項目を使用して、表示文字列およびターゲットの両方を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-112">Extended menu items let you override both the display string and the target.</span></span>
- <span data-ttu-id="ec7d6-113">この方法は、単純なクエリに基づくレポートから複雑なレポート データ プロバイダー (RDP) に基づくレポートまで、すべてのタイプのレポートに使用できます。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-113">This technique can be used for all types of reports, from simple query-based reports to complex report data provider (RDP)–based reports.</span></span>
- <span data-ttu-id="ec7d6-114">拡張メニュー項目は、コントローラ クラスを使用してレポート セッションを編成するレポートおよびソリューションへ直接参照に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-114">Extended menu items are available for direct references to reports and solutions that orchestrate the reporting session by using a controller class.</span></span>

## <a name="extend-report-menu-items"></a><span data-ttu-id="ec7d6-115">レポート メニュー項目の拡張</span><span class="sxs-lookup"><span data-stu-id="ec7d6-115">Extend report menu items</span></span>
<span data-ttu-id="ec7d6-116">次のチュートリアルでは、メニュー項目の拡張機能を使用して、アプリケーション内のユーザー ナビゲーションをカスタム ソリューションにリダイレクトする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-116">The following walkthrough shows how to use menu item extensions to redirect user navigations in the application to a custom solution.</span></span> <span data-ttu-id="ec7d6-117">このソリューションには、Fleet Management アプリケーション用のカスタム **顧客リスト** レポートが含まれており、純粋な拡張モデルですべてのアプリケーションのカスタマイズが定義されています。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-117">The solution includes a custom **Customer list** report for the Fleet Management application and defines all the application customizations in a pure extension model.</span></span> <span data-ttu-id="ec7d6-118">次の図は、カスタムの **顧客リスト** レポートにアクセスするために使用するメニュー項目を示しています。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-118">The following illustration shows the menu item that you use to access the custom **Customer list** report.</span></span>

<span data-ttu-id="ec7d6-119">[![fleet-workspace-customer-list](./media/fleet-workspace-customer-list.png)](./media/fleet-workspace-customer-list.png)</span><span class="sxs-lookup"><span data-stu-id="ec7d6-119">[![fleet-workspace-customer-list](./media/fleet-workspace-customer-list.png)](./media/fleet-workspace-customer-list.png)</span></span>

1. <span data-ttu-id="ec7d6-120">**アプリケーション カスタマイズの新しいモデルを作成します。**</span><span class="sxs-lookup"><span data-stu-id="ec7d6-120">**Create a new model for your application customizations.**</span></span> <span data-ttu-id="ec7d6-121">拡張モデルに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-121">For more information about extension models, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span>
2. <span data-ttu-id="ec7d6-122">**Microsoft Visual Studioで新しいプロジェクトを作成し、** **カスタム レポートを追加します。**</span><span class="sxs-lookup"><span data-stu-id="ec7d6-122">**Create a new project in Microsoft Visual Studio,** **and add your custom report.**</span></span> <span data-ttu-id="ec7d6-123">また、すべてのソリューション コンポーネントを追加します。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-123">Additionally, add all the solution artifacts.</span></span> <span data-ttu-id="ec7d6-124">これらのコンポーネントには、RDP クラスまたはソース クエリ、コントローラー クラス、UI ビルダー (ある場合) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-124">These artifacts include the RDP class or source query, the controller class, and UI builders, if they are present.</span></span>
3. <span data-ttu-id="ec7d6-125">**レポートにアクセスするために使用するメニュー項目の拡張機能を作成します。**</span><span class="sxs-lookup"><span data-stu-id="ec7d6-125">**Create an extension of the menu item that is used to access the report.**</span></span> <span data-ttu-id="ec7d6-126">この例では、出力メニュー項目は **FMCustomerListReport** と名前が付けられています。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-126">In this example, the output menu item is named **FMCustomerListReport**.</span></span> <span data-ttu-id="ec7d6-127">メニュー項目の構造を使用して、アプリケーションで公開されているメニュー項目の名前を見つけます。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-127">Use the menu item structure to find the menu item name that is exposed in the application.</span></span> <span data-ttu-id="ec7d6-128">次の図は、アプリケーション エクスプローラーでのアクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-128">The following illustration shows the action in Application Explorer.</span></span>

    <span data-ttu-id="ec7d6-129">[![レポートにアクセスするために使用するメニュー項目の拡張機能の作成](./media/fleet-extension-create-menu-extension-1024x632.png)](./media/fleet-extension-create-menu-extension.png)</span><span class="sxs-lookup"><span data-stu-id="ec7d6-129">[![Creating an extension of the menu item that is used to access the report](./media/fleet-extension-create-menu-extension-1024x632.png)](./media/fleet-extension-create-menu-extension.png)</span></span>

4. <span data-ttu-id="ec7d6-130">**メニュー項目の拡張機能のプロパティの変更。**</span><span class="sxs-lookup"><span data-stu-id="ec7d6-130">**Modify the properties of the menu item extension.**</span></span> <span data-ttu-id="ec7d6-131">メニュー項目のレポート デザインまたはコントローラ＝の参照を更新して、カスタム ソリューションに直接ナビゲートします。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-131">Update the report design or controller reference in the menu item to direct navigations to your custom solution.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ec7d6-132">オブジェクトに対して実行できるプロパティの変更は、元のアプリケーション ソリューションによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-132">The property changes that you can make on the object depend on the original application solution.</span></span> <span data-ttu-id="ec7d6-133">アプリケーションのレポートは、コントローラーを使用してソリューションを管理する場合、コントローラー クラスがレポートに必要になります。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-133">If the application report manages the solution by using a controller, a controller class is required for the report.</span></span>

5. <span data-ttu-id="ec7d6-134">**ソリューションを再構築してカスタム レポートを配置します。**</span><span class="sxs-lookup"><span data-stu-id="ec7d6-134">**Rebuild the solution, and deploy the custom report.**</span></span>

<span data-ttu-id="ec7d6-135">これで、レポート メニュー項目の拡張を完了しました。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-135">You've now finished extending the report menu item.</span></span> <span data-ttu-id="ec7d6-136">標準のメニュー項目へのナビゲーションは、カスタム レポート ソリューションにリダイレクトされるようになります。</span><span class="sxs-lookup"><span data-stu-id="ec7d6-136">Navigations to the standard menu item will now be redirected to your custom reporting solution.</span></span>
