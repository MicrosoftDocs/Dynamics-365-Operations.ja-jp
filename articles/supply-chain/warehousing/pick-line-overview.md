---
title: モバイル デバイスのメニュー項目を設定して、ピッキング行の概要を提供する
description: このトピックでは、モバイル デバイス上で倉庫作業を処理する倉庫作業者に、いつすべての作業明細行リストを表示するかを定義する方法について説明します。 この機能は、作業指示書でピッキング行の概要を必要とすることが多い倉庫作業者が、ピッキング順序を最適化できるので役立ちます。
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: a52a789044ca66c6771224a6cf0be8749bc99e5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2020
ms.locfileid: "3837315"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="e0402-104">モバイル デバイスのメニュー項目を設定して、ピッキング行の概要を提供する</span><span class="sxs-lookup"><span data-stu-id="e0402-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e0402-105">このトピックでは、ピッキング作業の処理に使用するモバイル デバイスのメニュー項目のピッキング行の概要に関連するオプションを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e0402-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="e0402-106">ピッキング行の概要を使用すると、倉庫作業者は現在のタスクに関連するすべての作業明細行の一覧を表示して選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0402-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="e0402-107">この機能は、作業者がピッキング順序を最適化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e0402-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="e0402-108">この機能には、作業員が固定された順序で一度に 1 行ずつ切り替えることができる標準の **スキップ** ボタンに代わるオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e0402-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="e0402-109">(ただし、このボタンを使用するオプションは引き続き使用できます。)</span><span class="sxs-lookup"><span data-stu-id="e0402-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="e0402-110">管理者は、各メニュー項目を個別に設定して、倉庫アプリがピッキング行の概要を表示する方法、時期、および場所を制御できます。</span><span class="sxs-lookup"><span data-stu-id="e0402-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="e0402-111">作業ピッキング行の概要機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="e0402-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="e0402-112">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0402-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e0402-113">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0402-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e0402-114">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="e0402-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e0402-115">**モジュール:** _倉庫管理_</span><span class="sxs-lookup"><span data-stu-id="e0402-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="e0402-116">**機能名:** _作業ピッキング行の概要_</span><span class="sxs-lookup"><span data-stu-id="e0402-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="e0402-117">すべての作業明細行の一覧を表示するメニュー項目を設定する</span><span class="sxs-lookup"><span data-stu-id="e0402-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="e0402-118">ピッキング行の概要を提供するモバイル デバイスのメニュー項目を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e0402-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="e0402-119">**倉庫管理 \> 設定 \> モバイル デバイス \> モバイル デバイスのメニュー品目**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0402-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e0402-120">ピッキング作業に関連するメニュー項目を選択または作成し、次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="e0402-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="e0402-121">**モード:** *作業*</span><span class="sxs-lookup"><span data-stu-id="e0402-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e0402-122">**既存の作業を使用:** *はい*</span><span class="sxs-lookup"><span data-stu-id="e0402-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="e0402-123">**指示者:** *ユーザー主導* または *システム主導*</span><span class="sxs-lookup"><span data-stu-id="e0402-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="e0402-124">**モバイル デバイスのメニュー項目** ページで使用できるメニュー項目の作成方法とさまざまな設定の使用方法の詳細については、[倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0402-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="e0402-125">**全般** クイック タブで、**作業明細行の一覧を表示** フィールドを次のいずれかの値に設定して、機能を設定します:</span><span class="sxs-lookup"><span data-stu-id="e0402-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="e0402-126">**要求時にのみ表示** – 作業者は、倉庫アプリの **スキップ** ボタンを選択することで、ピッキング行の一覧の表示を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0402-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="e0402-127">**すべてのピッキングの開始時に表示** – 作業者は、ピッキング行を開始または終了するたびに一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="e0402-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="e0402-128">倉庫アプリの **スキップ** ボタンを選択することで、再度一覧を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0402-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="e0402-129">**初回のピッキング開始時のみ表示** – 作業者は、新しいピッキング作業を開始するたびに一覧を表示しますが、各明細行の後には表示しません。</span><span class="sxs-lookup"><span data-stu-id="e0402-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="e0402-130">倉庫アプリの **スキップ** ボタンを選択することで、再度一覧を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0402-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="e0402-131">**表示しない** – 標準の **スキップ** ボタンが倉庫アプリに表示され、作業明細行の一覧表示がオフになります。</span><span class="sxs-lookup"><span data-stu-id="e0402-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="e0402-132">**スキップ** ボタンを使用すると、作業者は固定された順序で一度に 1 行ずつ切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="e0402-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="e0402-133">また、すべての行が処理されるまで、必要な回数だけ一覧を切り替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="e0402-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="e0402-134">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0402-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="e0402-135">**作業明細行の一覧を表示** フィールドを *表示しない* 以外の任意の値に設定すると、アクション ペインの **フィールド リスト** ボタンが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="e0402-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="e0402-136">アクション ペインで **フィールド リスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0402-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="e0402-137">**フィールド リスト** ページで、倉庫アプリが一覧の各行に対して表示する情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="e0402-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="e0402-138">**プライマリ コントロール** フィールドは常に *LineNum* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e0402-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="e0402-139">したがって、リストの各行は行番号で始まります。</span><span class="sxs-lookup"><span data-stu-id="e0402-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="e0402-140">必要に応じて、残りの **表示フィールド** フィールドを使用して、最大 7 つの追加表示フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0402-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="e0402-141">各 **表示フィールド** フィールドで、作業明細行フィールドの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0402-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="e0402-142">各行には、そのフィールドの値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0402-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="e0402-143">値は、ここで選択した順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0402-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="e0402-144">7 つの値すべてを必要としない場合は、**表示フィールド** フィールドの一部を空白のままにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="e0402-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="e0402-145">アクション ペインで **保存** を選択し、**フィールド リスト** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0402-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>
