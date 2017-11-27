---
title: "モバイル デバイスで倉庫内の古いバッチの表示をコンフィギュレーション"
description: "このトピックでは、作業明細行の現在のロケーションより古いバッチのロケーションのリストを表示するようにモバイル デバイスを設定する方法について説明します"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cd0a9c2e9fbfea987b045e301fb73a505a0f2a4e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="dc45b-103">モバイル デバイスで倉庫内の古いバッチの表示をコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dc45b-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dc45b-104">[**倉庫内の古いバッチの表示**] コンフィギュレーションにより、作業明細行の現在の場所よりも古いバッチの場所の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="dc45b-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="dc45b-105">表示される場所のリストには、有効期限のある古いバッチに関する情報と各バッチの現物在庫が含まれています。</span><span class="sxs-lookup"><span data-stu-id="dc45b-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="dc45b-106">新しい場所から選択するか、現在の場所から引き続き選択することができます。</span><span class="sxs-lookup"><span data-stu-id="dc45b-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="dc45b-107">新しい場所からのピッキング - ピッキングする新しい場所を選択すると、現在の作業明細行は新しい場所を使用するように更新され、新しい場所で通常通り作業が続行されます。</span><span class="sxs-lookup"><span data-stu-id="dc45b-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="dc45b-108">新しい場所を有効にするには、作業明細行全体に十分な利用可能な数量がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc45b-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="dc45b-109">必要な数量が利用できない場合、作業明細行は更新されず、リストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc45b-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="dc45b-110">現在の場所からピッキングを続行 - 現在の作業明細行の場所を続行すると、作業明細行の数量は元の場所から引き続き選択されます。</span><span class="sxs-lookup"><span data-stu-id="dc45b-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="dc45b-111">該当する場所</span><span class="sxs-lookup"><span data-stu-id="dc45b-111">Where it applies</span></span>
<span data-ttu-id="dc45b-112">倉庫内の古いバッチをモバイル デバイス メニュー項目で設定し、アイテムより下のバッチの選択に影響します。</span><span class="sxs-lookup"><span data-stu-id="dc45b-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="dc45b-113">倉庫内の古いバッチの表示を設定する</span><span class="sxs-lookup"><span data-stu-id="dc45b-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="dc45b-114">[**最も古いバッチのピッキング**] オプションを [**警告**] に設定すると、[**倉庫内の古いバッチの表示**] コンフィギュレーションはモバイル デバイスのメニュー項目で使用できます。</span><span class="sxs-lookup"><span data-stu-id="dc45b-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="dc45b-115">[**倉庫管理**] > [**設定**] > [**モバイル デバイス**] > [**モバイル デバイスのメニュー項目**] の順に、メニュー項目で [**既存の作業の使用**] を [**はい**] に設定し、[**最も古いバッチのピッキング**] フィールドで [**警告**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc45b-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 


