---
title: オンライン機能プロファイルの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce でオンライン機能プロファイルを作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: be78b92858979b8bb009a4699eff96379ef7cef3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791105"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="acf13-103">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="acf13-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="acf13-104">このトピックでは、Microsoft Dynamics 365 Commerce のオンライン機能プロファイルの設定の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="acf13-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="acf13-105">オンライン機能プロファイルは、オンライン チャネルに使用されるさまざまな設定を提供します。</span><span class="sxs-lookup"><span data-stu-id="acf13-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="acf13-106">各オンライン チャネルでは、オンライン機能プロファイルを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="acf13-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="acf13-107">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="acf13-107">Create an online functionality profile</span></span>

<span data-ttu-id="acf13-108">次の手順では、Commerce Headquarters アプリからオンライン機能プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="acf13-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="acf13-109">ナビゲーション ウィンドウで、**モジュール \> チャネル設定 \> オンライン ストア設定 \> 機能プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="acf13-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="acf13-110">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="acf13-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="acf13-111">**プロファイル** フィールドに、プロファイルの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="acf13-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="acf13-112">**説明** フィールドに、値を入力します (以下のサンプル画像の "Adventure Works プロファイル")。</span><span class="sxs-lookup"><span data-stu-id="acf13-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="acf13-113">**機能** セクション **カート**、**小売顧客**、または **チェックアウト** 設定を必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="acf13-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="acf13-114">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="acf13-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="acf13-115">次の図は、オンライン機能プロファイルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="acf13-115">The following image shows an example online functionality profile.</span></span>
  
![オンライン機能プロファイルの例](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="acf13-117">関数</span><span class="sxs-lookup"><span data-stu-id="acf13-117">Functions</span></span>

- <span data-ttu-id="acf13-118">**製品の集計**: この機能を有効にすると、同じ品目が複数回追加された場合に、カートで数量を更新できるようになります。</span><span class="sxs-lookup"><span data-stu-id="acf13-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="acf13-119">**支払なしのチェックアウトを許可**: この機能を有効にすると、カートに追加された品目の価格が $0.00 になったときに、このシナリオが処理されます。</span><span class="sxs-lookup"><span data-stu-id="acf13-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="acf13-120">**非同期モードで顧客を作成する**: これは、サードパーティの E コマース チャネルに適用されるレガシ設定であり、Dynamics 365 E コマース サイトには適用できません。</span><span class="sxs-lookup"><span data-stu-id="acf13-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acf13-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="acf13-121">Additional resources</span></span>

[<span data-ttu-id="acf13-122">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="acf13-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="acf13-123">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="acf13-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="acf13-124">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="acf13-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="acf13-125">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="acf13-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="acf13-126">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="acf13-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
