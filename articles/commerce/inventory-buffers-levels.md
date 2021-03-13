---
title: 在庫バッファーと在庫レベルのコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトで在庫状況のメッセージングを決定する在庫バッファーと在庫レベルをコンフィギュレーションする方法について説明します。
author: boycezhu
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: c519095d174414d6d4a8c86bc171ea62e1c72582
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012435"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a><span data-ttu-id="b6388-103">在庫バッファーと在庫レベルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b6388-103">Configure inventory buffers and inventory levels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6388-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトで在庫状況に関するメッセージングを決定する在庫バッファーと在庫レベルをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6388-104">This topic explains how to configure inventory buffers and inventory levels that determine the messaging about inventory availability on Microsoft Dynamics 365 Commerce sites.</span></span>

## <a name="overview"></a><span data-ttu-id="b6388-105">概要</span><span class="sxs-lookup"><span data-stu-id="b6388-105">Overview</span></span>

<span data-ttu-id="b6388-106">Dynamics 365 Commerce Headquarters には、在庫データと、販売時点管理 (POS) アプリケーション、電子商取引店舗、非同期で在庫をプルおよびプッシュするその他のカスタム統合アプリケーションなど、さまざまなチャネルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6388-106">Dynamics 365 Commerce headquarters holds inventory data and various channels such as point of sale (POS) applications, e-Commerce storefronts, and other custom integrated applications that pull and push inventory around in an asynchronous manner.</span></span> <span data-ttu-id="b6388-107">したがって、Commerce Headquarters の手持在庫ページ、POS ユーザー インターフェイス (UI)、E コマースの在庫状況 API から取得される使用可能な在庫値は、常にリアルタイムで 100% 正確であるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="b6388-107">Therefore, the available inventory values that are obtained through the on-hand inventory page in Commerce headquarters, through the POS user interface (UI), and through e-Commerce inventory availability APIs aren't always 100-percent accurate in real time.</span></span>

<span data-ttu-id="b6388-108">多くの小売業者は、電子商取引店舗で実際の在庫値を表示する代わりに、在庫状況の状態 (例えば、"在庫あり" または "在庫切れ" など) についてメッセージを表示して、顧客に品目が購入可能か、在庫切れの可能性があるかを通知することを希望します。</span><span class="sxs-lookup"><span data-stu-id="b6388-108">Instead of showing actual inventory values in e-Commerce storefronts, many retailers prefer just to show messaging about inventory availability status (for example, "Available" or "Out of stock") to inform customers whether an item is available for purchase or potentially out of stock.</span></span> <span data-ttu-id="b6388-109">このアプローチでは、在庫状況のメッセージングを決定する在庫バッファーと在庫レベルを使用可能にしてコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6388-109">For this approach, inventory buffers and inventory levels that determine the inventory availability messaging must be made available and configured.</span></span>

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a><span data-ttu-id="b6388-110">前提条件: 在庫バッファーと在庫レベル機能を有効する</span><span class="sxs-lookup"><span data-stu-id="b6388-110">Prerequisite: Turn on the inventory buffers and inventory levels feature</span></span>

<span data-ttu-id="b6388-111">在庫バッファーと在庫レベルの機能は、Commerce Headquarters の機能管理を通じて制御されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-111">The feature for inventory buffers and inventory levels is controlled through Feature management in Commerce headquarters.</span></span> <span data-ttu-id="b6388-112">機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-112">To turn on the feature, follow these steps.</span></span>

1. <span data-ttu-id="b6388-113">**システム管理** \> **ワークスペース** \> **機能管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-113">Go to **System administration** \> **Workspaces** \> **Feature management**.</span></span>
1. <span data-ttu-id="b6388-114">**在庫バッファーと在庫レベルの有効化** 機能を検索し、その行を選択してから、**直ちに有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-114">Search for the **Enable inventory buffers and inventory levels** feature, select its row, and then select **Enable now**.</span></span>

<span data-ttu-id="b6388-115">この機能を有効にすると、**Retail と Commerce \> 在庫管理** で在庫レベルを確認できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-115">After the feature is turned on, you can find inventory levels at **Retail and Commerce \> Inventory management**.</span></span>

## <a name="create-and-configure-an-inventory-level-profile"></a><span data-ttu-id="b6388-116">在庫レベル プロファイルの作成とコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b6388-116">Create and configure an inventory level profile</span></span>

<span data-ttu-id="b6388-117">*在庫レベルのプロファイル* は、指定された製品数量の状態が在庫あり、在庫切れ、あるいはその他のカスタム ステータスとみなされるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="b6388-117">An *inventory level profile* determines whether a given product quantity status is considered in stock, out of stock, or some other custom status.</span></span> <span data-ttu-id="b6388-118">法人ごとに複数の在庫レベル プロファイルを作成およびコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b6388-118">You can create and configure multiple inventory level profiles per legal entity.</span></span> <span data-ttu-id="b6388-119">各プロファイルは、一連の在庫レベルで構成され、各レベルは *範囲*、*コード*、および *ラベル* によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-119">Each profile consists of a set of inventory levels, and each level is defined by a *range*, a *code*, and a *label*.</span></span>

- <span data-ttu-id="b6388-120">**範囲** – 各範囲は、*開始数量* と *終了数量* によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-120">**Range** – Each range is defined by a *start quantity* and an *end quantity*.</span></span> <span data-ttu-id="b6388-121">数量値が、その範囲の開始数量よりも多く、かつ終了数量を超えていない場合は、範囲に含まれます。</span><span class="sxs-lookup"><span data-stu-id="b6388-121">A quantity value falls in a range if it's more than the start quantity of that range and not more than the end quantity.</span></span>
- <span data-ttu-id="b6388-122">**コード** – コードは、レベルを表す内部の略語です。</span><span class="sxs-lookup"><span data-stu-id="b6388-122">**Code** – A code is an internal abbreviation that represents the level.</span></span> <span data-ttu-id="b6388-123">在庫 API と直接統合する顧客は、コードを使用して、特定の在庫レベルの追加ロジックを構築できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-123">Customers who directly integrate with the inventory APIs can use codes to build additional logic for a given inventory level.</span></span> <span data-ttu-id="b6388-124">たとえば、在庫レベル コードが **OOS** ("在庫切れ") の場合に、製品の購買機能を無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6388-124">For example, they can turn off the purchase capability for a product when its inventory level code is **OOS** ("out of stock").</span></span>
- <span data-ttu-id="b6388-125">**ラベル** – ラベルは、E コマース サイト上の顧客に在庫レベルを伝える意味のある顧客向けメッセージです。</span><span class="sxs-lookup"><span data-stu-id="b6388-125">**Label** – A label is a meaningful customer-facing message that conveys an inventory level to customers on an e-Commerce site.</span></span>

### <a name="create-an-inventory-level-profile"></a><span data-ttu-id="b6388-126">在庫レベル プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="b6388-126">Create an inventory level profile</span></span>

<span data-ttu-id="b6388-127">在庫レベル プロファイルを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-127">To create an inventory level profile, follow these steps.</span></span>

1. <span data-ttu-id="b6388-128">**Retail と Commerce** \> **在庫管理** \> **在庫レベル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-128">Go to **Retail and Commerce** \> **Inventory management** \> **Inventory levels**.</span></span>
1. <span data-ttu-id="b6388-129">アクション ペインで、**新規** を選択し、**プロファイル ID** フィールドと **説明** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6388-129">On the Action Pane, select **New**, and then enter values in the **Profile ID** and **Description** fields.</span></span>
1. <span data-ttu-id="b6388-130">**範囲** クイックタブで、**追加** を選択して新しいレベルを追加し、そのレベルの **開始数量**、**終了数量**、**コード**、**ラベル** の各列に値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6388-130">On the **Ranges** FastTab, select **Add** to add a new level, and then enter values in the **Start quantity**, **End quantity**, **Code**, and **Label** columns for that level.</span></span> <span data-ttu-id="b6388-131">さらにレベルを追加するには、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="b6388-131">Repeat this step to add more levels.</span></span> <span data-ttu-id="b6388-132">必要に応じて、データ グリッドの値を編集したり、**削除** を選択してレベルを削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="b6388-132">As you require, you can edit the values in the data grid, or you can select **Delete** to remove a level.</span></span>
1. <span data-ttu-id="b6388-133">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-133">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="b6388-134">新しいプロファイルが作成されると、2 つの在庫レベルが自動的に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-134">When a new profile is created, two inventory levels are automatically initialized:</span></span>

- <span data-ttu-id="b6388-135">**OOS** – 範囲の下限が負の無限大である "在庫切れ" レベル。</span><span class="sxs-lookup"><span data-stu-id="b6388-135">**OOS** – The "out of stock" level, where the lower bound of the range is negative infinity.</span></span> <span data-ttu-id="b6388-136">このレベルで開始数量とコードを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="b6388-136">The start quantity and code can't be edited for this level.</span></span>
- <span data-ttu-id="b6388-137">**AVAIL** – 範囲の上限が無限大である、"利用可能" レベル。</span><span class="sxs-lookup"><span data-stu-id="b6388-137">**AVAIL** – The "available" level, where the upper bound of the range is infinity.</span></span> <span data-ttu-id="b6388-138">このレベルで終了数量とコードを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="b6388-138">The end quantity and code can't be edited for this level.</span></span>

> [!NOTE]
> <span data-ttu-id="b6388-139">プロファイル定義で範囲間にギャップや重複はありません。</span><span class="sxs-lookup"><span data-stu-id="b6388-139">There can be no gaps or overlap between ranges in the profile definition.</span></span>

<span data-ttu-id="b6388-140">アクション ペインの **翻訳** ボタンを使用すると、ラベル メッセージのローカライズされた文字列をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="b6388-140">You can use the **Translations** button on the Action Pane to configure localized strings for the label message.</span></span> <span data-ttu-id="b6388-141">次に、ローカライズされた文字列をチャネルに同期するために、**1110** (**グローバル コンフィギュレーション**) 配送スケジュール ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6388-141">You must then run the **1110** (**Global configuration**) distribution schedule job to sync the localized strings to channels.</span></span>

### <a name="configure-an-inventory-level-profile"></a><span data-ttu-id="b6388-142">在庫レベル プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b6388-142">Configure an inventory level profile</span></span>

<span data-ttu-id="b6388-143">在庫レベルのプロファイルは、製品カテゴリ レベルまたは個々の製品レベルのいずれかで構成できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-143">You can configure an inventory level profile at either the product category level or the individual product level.</span></span> <span data-ttu-id="b6388-144">製品に対して在庫レベルのプロファイルがコンフィギュレーションされている場合、在庫レベルは、リンクされたプロファイルで定義されている範囲に基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-144">When an inventory level profile is configured for a product, the inventory level is determined based on the ranges that are defined in the linked profile.</span></span> <span data-ttu-id="b6388-145">それ以外の場合、"利用可能" 在庫レベルまたは "在庫切れ" 在庫レベルは、製品に正の手持在庫数量があるかどうかに基づいて決定されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-145">Otherwise, the "available" or "out of stock" inventory level is determined based on whether the product has a positive on-hand quantity.</span></span>

<span data-ttu-id="b6388-146">カテゴリの在庫レベル プロファイルを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-146">To configure an inventory level profile for a category, follow these steps.</span></span>

1. <span data-ttu-id="b6388-147">**Retail と Commerce** \> **製品とカテゴリ** \> **Commerce 製品階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-147">Go to **Retail and Commerce** \> **Products and categories** \> **Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="b6388-148">在庫レベル プロファイルを構成するカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-148">Select the category to configure an inventory level profile for.</span></span>
1. <span data-ttu-id="b6388-149">**製品の販売プロパティ** クイックタブで、法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-149">On the **Sell product properties** FastTab, select a legal entity.</span></span>
1. <span data-ttu-id="b6388-150">**Commerce の在庫** セクションの **在庫レベル プロファイル** フィールドで、事前定義済の在庫レベル プロファイルのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-150">In the **Commerce inventory** section, in the **Inventory level profile** field, select one of the predefined inventory level profiles.</span></span>

<span data-ttu-id="b6388-151">アクション ペインで **製品の更新** ボタンを使用して、カテゴリの基になる製品にカテゴリ レベルのプロファイルの値を反映できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-151">You can use the **Update products** button on the Action Pane to propagate the value of the category-level profile to the category's underlying products.</span></span> <span data-ttu-id="b6388-152">詳細については、[製品カテゴリおよび製品の管理](category-management-product-creation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6388-152">For more information, see [Manage product categories and products](category-management-product-creation.md).</span></span>

<span data-ttu-id="b6388-153">リリース済み製品の在庫レベル プロファイルを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-153">To configure an inventory level profile for a released product, follow these steps.</span></span>

1. <span data-ttu-id="b6388-154">**Retail と Commerce** \> **製品とカテゴリ** \> **カテゴリ別リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-154">Go to **Retail and Commerce** \> **Products and categories** \> **Released products by category**.</span></span>
1. <span data-ttu-id="b6388-155">製品を選択し、製品の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6388-155">Select a product, and then open its product details page.</span></span>
1. <span data-ttu-id="b6388-156">**販売** クイック タブで、**Commerce の在庫** セクションの **在庫レベル プロファイル** フィールドで、事前定義済の在庫レベル プロファイルのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-156">On the **Sell** FastTab, in the **Commerce inventory** section, in the **Inventory level profile** field, select one of the predefined inventory level profiles.</span></span>

<span data-ttu-id="b6388-157">新しい製品が作成されると、**在庫レベル プロファイル** フィールドは、他の多くの製品レベルの属性と同様に、製品に関連付けられているカテゴリに構成されている値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-157">When a new product is created, the **Inventory level profile** field, like many other product-level attributes, will be set to the value that is configured for the category that the product is associated with.</span></span>

> [!NOTE]
> <span data-ttu-id="b6388-158">在庫レベル プロファイルは、法人固有の属性です。</span><span class="sxs-lookup"><span data-stu-id="b6388-158">The inventory level profile is a legal entity–specific attribute.</span></span> <span data-ttu-id="b6388-159">同じカテゴリまたは製品の場合、在庫レベル プロファイル値は法人ごとに異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b6388-159">For the same category or product, the inventory level profile value can vary across legal entities.</span></span>

<span data-ttu-id="b6388-160">在庫レベル プロファイルのコンフィギュレーションをチャネルに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b6388-160">To sync the configurations of inventory level profiles to channels, follow these steps.</span></span>

1. <span data-ttu-id="b6388-161">**Retail と Commerce** \> **Retail と Commerce IT** \> **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-161">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="b6388-162">**1040** (**製品**) 配送スケジュールを実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-162">Run the **1040** (**Product**) distribution schedule.</span></span>

## <a name="configure-an-inventory-buffer"></a><span data-ttu-id="b6388-163">在庫バッファーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b6388-163">Configure an inventory buffer</span></span>

<span data-ttu-id="b6388-164">*在庫バッファー* は、品目の追加数量を元の数量から減算して見積数量を計算するユーザー定義の値です。</span><span class="sxs-lookup"><span data-stu-id="b6388-164">The *inventory buffer* is a user-defined value that subtracts the additional quantity of an item from the original quantity to calculate the estimated quantity.</span></span> <span data-ttu-id="b6388-165">この見積数量は、小売業者が実際の手持在庫よりも多く販売することで製品を過剰に販売しないようにするための安全なバッファを提供します。</span><span class="sxs-lookup"><span data-stu-id="b6388-165">This estimated quantity gives retailers a safe buffer so that they don't oversell a product by selling more than its actual on-hand inventory.</span></span> <span data-ttu-id="b6388-166">在庫バッファーは、製品カテゴリ レベルまたは個々の製品レベルのいずれかで構成できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-166">You can configure the inventory buffer at either the product category level or the individual product level.</span></span> <span data-ttu-id="b6388-167">在庫バッファーが指定されていない場合は、既定値 **0** (ゼロ) が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-167">If no inventory buffer is specified, the default value of **0** (zero) is used.</span></span>

<span data-ttu-id="b6388-168">カテゴリの在庫バッファーを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-168">To configure the inventory buffer for a category, follow these steps.</span></span>

1. <span data-ttu-id="b6388-169">**Retail と Commerce** \> **製品とカテゴリ** \> **Commerce 製品階層** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-169">Go to **Retail and Commerce** \> **Products and categories** \> **Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="b6388-170">在庫バッファーを構成するカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-170">Select the category to configure the inventory buffer for.</span></span>
1. <span data-ttu-id="b6388-171">**製品の販売プロパティ** クイックタブで、法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-171">On the **Sell product properties** FastTab, select a legal entity.</span></span>
1. <span data-ttu-id="b6388-172">**Commerce の在庫** セクションの **在庫バッファー** フィールドに、正の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6388-172">In the **Commerce inventory** section, in the **Inventory buffer** field, enter a positive value.</span></span>

<span data-ttu-id="b6388-173">アクション ペインで **製品の更新** ボタンを使用して、カテゴリの基になる製品にカテゴリ レベルのバッファーの値を反映できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-173">You can use the **Update products** button on the Action Pane to propagate the value of the category-level buffer to the category's underlying products.</span></span> <span data-ttu-id="b6388-174">詳細については、[製品カテゴリおよび製品の管理](category-management-product-creation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6388-174">For more information, see [Manage product categories and products](category-management-product-creation.md).</span></span>

<span data-ttu-id="b6388-175">リリース済製品の在庫バッファーを構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-175">To configure the inventory buffer for a released product, follow these steps.</span></span>

1. <span data-ttu-id="b6388-176">**Retail と Commerce** \> **製品とカテゴリ** \> **カテゴリ別リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-176">Go to **Retail and Commerce** \> **Products and categories** \> **Released products by category**.</span></span>
1. <span data-ttu-id="b6388-177">製品を選択し、製品の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6388-177">Select a product, and then open its product details page.</span></span>
1. <span data-ttu-id="b6388-178">**販売** クイック タブで、**Commerce の在庫** セクションの **在庫バッファー** フィールドに、正の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b6388-178">On the **Sell** FastTab, in the **Commerce inventory** section, in the **Inventory buffer** field, enter a positive value.</span></span>

<span data-ttu-id="b6388-179">新しい製品が作成されると、**在庫バッファー** フィールドは、製品に関連付けられているカテゴリに構成されている値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-179">When a new product is created, the **Inventory buffer** field will be set to the value that is configured for the category that the product is associated with.</span></span>

> [!NOTE]
> <span data-ttu-id="b6388-180">在庫のバッファーと在庫レベルの両方のプロファイルが製品に対して構成されている場合、製品の見積数量 (つまり、元の数量からバッファーの値を差し引いた数量) は、在庫レベルを決定するために範囲計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6388-180">If both the inventory buffer and inventory level profiles are configured for a product, the product's estimated quantity (that is, the original quantity minus the buffer value) will be used for range calculation to determine the inventory level.</span></span>

<span data-ttu-id="b6388-181">在庫バッファーのコンフィギュレーションをチャネルに同期するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b6388-181">To sync the configurations of inventory buffers to channels, follow these steps.</span></span>

1. <span data-ttu-id="b6388-182">**Retail と Commerce** \> **Retail と Commerce IT** \> **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-182">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="b6388-183">**1040** (**製品**) 配送スケジュールを実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-183">Run the **1040** (**Product**) distribution schedule.</span></span>

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a><span data-ttu-id="b6388-184">Eコマースのシナリオで在庫バッファーと在庫レベルを使用する</span><span class="sxs-lookup"><span data-stu-id="b6388-184">Use inventory buffers and inventory levels in e-Commerce scenario</span></span>

<span data-ttu-id="b6388-185">Commerce サイト ビルダーでは、Commerce Headquarters の在庫バッファーおよび在庫レベル機能を使用して、E コマース サイトの在庫状況のメッセージングを決定します。</span><span class="sxs-lookup"><span data-stu-id="b6388-185">Commerce site builder uses the inventory buffer and inventory level capabilities in Commerce headquarters to determine inventory availability messaging on e-Commerce sites.</span></span> <span data-ttu-id="b6388-186">詳細については、[在庫設定を適用する](inventory-settings.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6388-186">For more information, see [Apply inventory settings](inventory-settings.md).</span></span>

<span data-ttu-id="b6388-187">別の方法として、サードパーティの電子商取引ソリューションと統合する場合は、**GetEstimatedAvailability** と **GetEstimatedProductWarehouseAvailability** API を使用して、Eコマースのシナリオで製品の在庫状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-187">Alternatively, if you integrate with a third-party e-Commerce solution, you can use the **GetEstimatedAvailability** and **GetEstimatedProductWarehouseAvailability** APIs to show inventory availability for a product in your e-Commerce scenario.</span></span> <span data-ttu-id="b6388-188">これらの API の詳細については、[小売チャンネルの引当可能在庫数量の計算](calculated-inventory-retail-channels.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6388-188">For more information about these APIs, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="b6388-189">在庫バッファーと在庫レベルの導入により、これらの API は、使用可能な物理値と使用可能な物理値の合計に基づいて決定される在庫レベル コードとラベル メッセージを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="b6388-189">The introduction of inventory buffers and inventory levels enables these APIs to return inventory level codes and label messages that are determined based on total available and available physical values.</span></span> <span data-ttu-id="b6388-190">この API をさらに構成して、在庫数量がメッセージと共に返されるかどうか、および利用可能な数量を在庫バッファー値によって減少されるかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="b6388-190">The APIs can be further configured to determine whether the inventory quantity is returned together with the message, and whether the available quantity is reduced by the inventory buffer value.</span></span>

<span data-ttu-id="b6388-191">在庫状態 API の応答を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b6388-191">To configure the response of the product availability APIs, follow these steps.</span></span>

1. <span data-ttu-id="b6388-192">**Retail と Commerce** \> **Headquarters の設定** \> **パラメーター** \> **Commerce パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6388-192">Go to **Retail and commerce** \> **Headquarters setup** \> **Parameters** \> **Commerce parameters**.</span></span>
1. <span data-ttu-id="b6388-193">**店舗在庫** セクションの **在庫** タブにある **E コマース向け製品の使用可能性 API** フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6388-193">In the **Store inventory** section, on the **Inventory** tab, in the **Product availability APIs for e-Commerce** field, select a value.</span></span>
1. <span data-ttu-id="b6388-194">チャンネルに設定を適用するには、**1110** (**グローバル コンフィギュレーション**) 配送スケジュール ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="b6388-194">To apply the settings to channels, run the **1110** (**Global configuration**) distribution schedule job.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6388-195">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b6388-195">Additional resources</span></span>

[<span data-ttu-id="b6388-196">製品カテゴリおよび製品の管理</span><span class="sxs-lookup"><span data-stu-id="b6388-196">Manage product categories and products</span></span>](category-management-product-creation.md)

[<span data-ttu-id="b6388-197">在庫設定を適用する</span><span class="sxs-lookup"><span data-stu-id="b6388-197">Apply inventory settings</span></span>](inventory-settings.md)

[<span data-ttu-id="b6388-198">小売チャンネルの引当可能在庫数量の計算</span><span class="sxs-lookup"><span data-stu-id="b6388-198">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
