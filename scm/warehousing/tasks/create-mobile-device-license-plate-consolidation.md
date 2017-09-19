--- 
title: "ライセンス プレートの連結用のモバイル デバイス メニュー項目の作成"
description: "この手順では、ライセンスプレート結合作業に必要なモバイル端末のメニュー項目を作成する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7b8d20561ff092bd64c17c5d9335e9f54a1d191b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="36559-103">ライセンス プレートの連結用のモバイル デバイス メニュー項目の作成</span><span class="sxs-lookup"><span data-stu-id="36559-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36559-104">この手順では、ライセンスプレート結合作業に必要なモバイル端末のメニュー項目を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="36559-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="36559-105">これにより、倉庫従事者は同じ場所内で、品目付きライセンスプレートと別の場所のライセンスプレートとを結合することができます。</span><span class="sxs-lookup"><span data-stu-id="36559-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="36559-106">たとえば、この方法を用いると両方の作業指示で手順が同一の場合、結合された品目についての作業は1回で済むわけです。</span><span class="sxs-lookup"><span data-stu-id="36559-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="36559-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="36559-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="36559-108">通常、この作業を行うのは倉庫責任者です。</span><span class="sxs-lookup"><span data-stu-id="36559-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="36559-109">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="36559-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="36559-110">[倉庫管理] > [設定] > [モバイル デバイス] > [モバイル デバイスのメニュー品目] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="36559-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="36559-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36559-111">Click New.</span></span>
3. <span data-ttu-id="36559-112">[メニュー項目名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="36559-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="36559-113">[タイトル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="36559-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="36559-114">[モード] フィールドで [間接] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36559-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="36559-115">[活動コード] フィールドでは、[ライセンスプレートを結合する] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36559-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

