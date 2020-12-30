---
title: チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413657"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="1b79a-103">チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="1b79a-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1b79a-104">このトピックでは、Microsoft Dynamics 365 Commerce のチャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1b79a-105">概要</span><span class="sxs-lookup"><span data-stu-id="1b79a-105">Overview</span></span>

<span data-ttu-id="1b79a-106">チャンネル ナビゲーション階層は、製品を E コマース サイトまたは販売時点管理 (POS) で参照できるように、製品をカテゴリに編成します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="1b79a-107">チャンネル ナビゲーション階層を使用して、小売とオンライン チャンネルをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b79a-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="1b79a-108">チャンネルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1b79a-108">Configure the channel</span></span>

<span data-ttu-id="1b79a-109">チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1b79a-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1b79a-110">ナビゲーション ウィンドウで、**モジュール \> 小売とコマース \> チャネル設定 \> チャネル カテゴリと製品属性** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="1b79a-111">コンフィギュレーションするチェンネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="1b79a-112">アクション ウィンドウで、**属性メタデータの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="1b79a-113">**カテゴリ階層** のドロップダウン リストで該当するチャンネル ナビゲーション階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="1b79a-114">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="1b79a-115">**属性グループ** で、すべてのノードのグローバル属性となる属性グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="1b79a-116">次の図は、チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b79a-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![チャネル コンフィギュレーションの例](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="1b79a-118">属性メタデータの設定</span><span class="sxs-lookup"><span data-stu-id="1b79a-118">Set attribute metadata</span></span>

<span data-ttu-id="1b79a-119">属性メタデータを設定すると、各ノードの属性をコンフィギュレーションできるようになります。</span><span class="sxs-lookup"><span data-stu-id="1b79a-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="1b79a-120">属性メタデータを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1b79a-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="1b79a-121">アクション ウィンドウで、**属性メタデータの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="1b79a-122">各ノードについて、**チャンネル製品属性** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="1b79a-123">**チャンネルの属性を表示** を **はい** に設定し、**絞り込み可能** を **はい** に設定すると、そのチャンネルで絞り込み条件を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="1b79a-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="1b79a-124">必要に応じて各ノードをコンフィギュレーションした後、**アクション ウィンドウ** で、**保存** ボタンを選択して保存します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="1b79a-125">右上隅の **X** を選択すると、この画面を終了して **チャンネル カテゴリと製品属性** のページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="1b79a-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="1b79a-126">次の図は、チャンネル カテゴリ ノードにコンフィギュレーションされているチャンネル製品属性の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b79a-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![チャンネル カテゴリ ノードのチャンネル属性](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="1b79a-128">変更の公開</span><span class="sxs-lookup"><span data-stu-id="1b79a-128">Publish changes</span></span>

<span data-ttu-id="1b79a-129">変更を有効にするには、チャンネルを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b79a-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="1b79a-130">変更を公開するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1b79a-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="1b79a-131">アクション ウィンドウで、**チャンネル更新の公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="1b79a-132">**チャンネル更新を公開** のウィンドウで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b79a-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="1b79a-133">次の図は、チャンネルの更新を公開する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1b79a-133">The following image shows how to publish channel updates.</span></span>

![チャネル更新の公開](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="1b79a-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1b79a-135">Additional resources</span></span>

[<span data-ttu-id="1b79a-136">チャンネル ナビゲーション階層を作成する</span><span class="sxs-lookup"><span data-stu-id="1b79a-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


