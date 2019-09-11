---
title: 場所プロファイルの作成
description: このトピックでは、Dynamics 365 for Finance and Operations で場所プロファイルを作成する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46aa1001c21ae39c158062444303ca02c0f41a45
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866982"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="ded3c-103">場所プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="ded3c-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ded3c-104">このトピックでは、Dynamics 365 for Finance and Operations で場所プロファイルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-104">This topic explains how to create a location profile in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ded3c-105">倉庫の場所は、場所のプロパティに関連したプロファイルを有している必要があります。たとえば、ある場所では品目の混合が許容されているかどうかなどです。</span><span class="sxs-lookup"><span data-stu-id="ded3c-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="ded3c-106">この手順では、ライセンスプレートの管理が必要ない場所のプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="ded3c-107">混合された品目と混合された在庫の状況を有効にして、循環棚卸を可能にします。</span><span class="sxs-lookup"><span data-stu-id="ded3c-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="ded3c-108">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ded3c-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="ded3c-109">ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > 倉庫 > 場所プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="ded3c-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-110">Select **New**.</span></span>
3. <span data-ttu-id="ded3c-111">**場所プロファイル ID** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="ded3c-112">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ded3c-113">**場所形式**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="ded3c-114">**場所タイプ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="ded3c-115">**ドック管理プロファイル ID** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="ded3c-116">**混合保管を許可**フィールドで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="ded3c-117">**混合在庫状態を許可**フィールドで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="ded3c-118">**循環棚卸**フィールドで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="ded3c-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ded3c-119">Select **Save**.</span></span>

