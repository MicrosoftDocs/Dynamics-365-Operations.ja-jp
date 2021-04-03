---
title: 生産現場の実行インターフェイスをデザインする
description: このトピックでは、各コンフィギュレーションのユーザーインターフェイスのコンテンツをデザインする方法について説明します。
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 282785799b6d61a00a356fcc2ae86ff0e3b7b39f
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501033"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="19fd0-103">生産現場の実行インターフェイスをデザインする</span><span class="sxs-lookup"><span data-stu-id="19fd0-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="19fd0-104">生産現場の実行インターフェイスで使用される各コンフィギュレーションのユーザーインターフェイスの内容をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="19fd0-105">たとえば、ある作業セルの作業者が生産現場のジョブ指示を開くことができるようにする必要がありますが、別の作業セルでは指示が不要です。</span><span class="sxs-lookup"><span data-stu-id="19fd0-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="19fd0-106">この場合、ドキュメントの添付ファイルを開くボタンと、このボタンを使用しないコンフィギュレーションの 2 つのコンフィギュレーションを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19fd0-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="19fd0-107">タブのデザイン</span><span class="sxs-lookup"><span data-stu-id="19fd0-107">Design a tab</span></span>

<span data-ttu-id="19fd0-108">**生産現場の実行を構成** ページで、アクション ウィンドウの **タブのデザイン** を選択してタブを作成して構成できます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="19fd0-109">各タブは、次の図に示すように 4 つのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="19fd0-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="19fd0-110">![タブのレイアウト](media/pfe-tab-layout.png "タブのレイアウト")</span><span class="sxs-lookup"><span data-stu-id="19fd0-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="19fd0-111">次の要素が図に示されています:</span><span class="sxs-lookup"><span data-stu-id="19fd0-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="19fd0-112">プライマリ ツールバー</span><span class="sxs-lookup"><span data-stu-id="19fd0-112">Primary toolbar</span></span>
1. <span data-ttu-id="19fd0-113">セカンダリ ツールバー</span><span class="sxs-lookup"><span data-stu-id="19fd0-113">Secondary toolbar</span></span>
1. <span data-ttu-id="19fd0-114">メイン ビュー</span><span class="sxs-lookup"><span data-stu-id="19fd0-114">Main view</span></span>
1. <span data-ttu-id="19fd0-115">詳細な表示</span><span class="sxs-lookup"><span data-stu-id="19fd0-115">Detailed view</span></span>

<span data-ttu-id="19fd0-116">新しいタブを作成して構成するには、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="19fd0-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="19fd0-117">**生産管理 \> 設定 \> 製造実行 \> 生産現場の実行を構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-117">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

1. <span data-ttu-id="19fd0-118">アクション ウィンドウの **タブのデザイン** を選択して、**タブのデザイン** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="19fd0-119">![タブのデザイン ページ](media/pfe-design-tabs.png "タブのデザイン ページ")</span><span class="sxs-lookup"><span data-stu-id="19fd0-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="19fd0-120">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="19fd0-121">ページのヘッダーで次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="19fd0-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="19fd0-122">**タブ名** - タブの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="19fd0-123">**メイン ビュー** - 事前に定義された 2 つのジョブ リスト (*有効なジョブ*、*すべてのジョブ*、または *マイ マシン*) から選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="19fd0-124">**詳細ビュー** - 空白の値または **ジョブの詳細** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="19fd0-125">空白の値を選択すると、詳細な情報はタブに表示されません。**ジョブの詳細** を選択した場合は、メイン ビューのジョブ リストで選択したジョブの詳細な説明が、詳細ビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="19fd0-126">**プライマリ ツールバー** セクションで、プライマリ ツールバーで使用できるボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="19fd0-127">**使用できるアクション** 列には、追加できるすべてのボタンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="19fd0-128">**選択したアクション** 列には、現在のコンフィギュレーションに含まれるすべてのボタンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="19fd0-129">列の間のボタンを使用して、選択した品目を必要に応じて列間で移動します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="19fd0-130">**選択したアクション** 列の横にある上下ボタンを使用して、ユーザー インターフェイスにボタンが表示される順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="19fd0-131">**セカンダリ** **ツールバー** セクションで、セカンダリ ツールバーで使用できるボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="19fd0-132">**使用できるアクション** 列には、追加できるすべてのボタンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="19fd0-133">**選択したアクション** 列には、現在のコンフィギュレーションに含まれるすべてのボタンの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="19fd0-134">列の間のボタンを使用して、選択した品目を必要に応じて列間で移動します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="19fd0-135">**選択したアクション** 列の横にある上下ボタンを使用して、ユーザー インターフェイスにボタンが表示される順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="19fd0-136">構成へのタブの関連付け</span><span class="sxs-lookup"><span data-stu-id="19fd0-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="19fd0-137">必要なタブをすべてデザインしたら、構成に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="19fd0-138">**生産管理 \> 設定 \> 製造実行 \> 生産現場の実行を構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-138">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

    <span data-ttu-id="19fd0-139">![生産フロア実行の構成](media/pfe-config-prod-floor-execution.png "生産フロア実行の構成")</span><span class="sxs-lookup"><span data-stu-id="19fd0-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="19fd0-140">**タブの選択** クイック タブで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="19fd0-141">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="19fd0-141">A new row is added to the grid.</span></span> <span data-ttu-id="19fd0-142">この新しい行で、構成に追加するタブの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="19fd0-143">必要に応じて、追加のタブを追加します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="19fd0-144">必要に応じてタブを配置するには、ツールバーの **上へ移動** または **下へ移動** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="19fd0-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="19fd0-145">上のスクリーンショットに示されている順序で、タブは左から右に表示されます (一番上にあるタブが左側に表示されます)。</span><span class="sxs-lookup"><span data-stu-id="19fd0-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]