---
title: オンライン機能プロファイルの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce でオンライン機能プロファイルを作成する方法について説明します。
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
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003375"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="338e8-103">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="338e8-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="338e8-104">このトピックでは、Microsoft Dynamics 365 Commerce オンライン機能プロファイルの設定の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="338e8-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="338e8-105">概要</span><span class="sxs-lookup"><span data-stu-id="338e8-105">Overview</span></span>

<span data-ttu-id="338e8-106">オンライン機能プロファイルは、オンライン チャネルに使用されるさまざまな設定を提供します。</span><span class="sxs-lookup"><span data-stu-id="338e8-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="338e8-107">各オンライン チャネルでは、オンライン機能プロファイルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="338e8-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="338e8-108">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="338e8-108">Create an online functionality profile</span></span>

<span data-ttu-id="338e8-109">次の手順では、Commerce Headquarters アプリからオンライン機能プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="338e8-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="338e8-110">ナビゲーション ウィンドウで、**モジュール \> チャネル設定 \> オンライン ストア設定 \> 機能プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="338e8-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="338e8-111">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="338e8-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="338e8-112">**プロファイル** フィールドに、プロファイルの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="338e8-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="338e8-113">**説明**フィールドに、値を入力します (以下のサンプル画像の "Adventure Works プロファイル")。</span><span class="sxs-lookup"><span data-stu-id="338e8-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="338e8-114">**機能**セクション**カート**、**小売顧客**、または**チェックアウト**設定を必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="338e8-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="338e8-115">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="338e8-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="338e8-116">次の図は、オンライン機能プロファイルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="338e8-116">The following image shows an example online functionality profile.</span></span>
  
![オンライン機能プロファイルの例](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="338e8-118">関数</span><span class="sxs-lookup"><span data-stu-id="338e8-118">Functions</span></span>

- <span data-ttu-id="338e8-119">**製品の集計**: この機能を有効にすると、同じ品目が複数回追加された場合に、カートで数量を更新できるようになります。</span><span class="sxs-lookup"><span data-stu-id="338e8-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="338e8-120">**支払なしのチェックアウトを許可**: この機能を有効にすると、カートに追加された品目の価格が $0.00 になったときに、このシナリオが処理されます。</span><span class="sxs-lookup"><span data-stu-id="338e8-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="338e8-121">**非同期モードで顧客を作成する**: これは、サードパーティの E コマース チャネルに適用されるレガシ設定であり、Dynamics 365 E コマース サイトには適用できません。</span><span class="sxs-lookup"><span data-stu-id="338e8-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="338e8-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="338e8-122">Additional resources</span></span>

[<span data-ttu-id="338e8-123">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="338e8-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="338e8-124">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="338e8-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="338e8-125">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="338e8-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="338e8-126">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="338e8-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="338e8-127">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="338e8-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
