---
title: 出荷配送業者の設定
description: このトピックでは、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a43a99e10b915f1265be14f2442069dae3a22e5
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867030"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="ad369-103">出荷配送業者の設定</span><span class="sxs-lookup"><span data-stu-id="ad369-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad369-104">このトピックでは、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ad369-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="ad369-105">配送コーディネーターは、出荷の配送業者を入荷または出荷に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="ad369-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="ad369-106">新しい出荷の配送業者の作成</span><span class="sxs-lookup"><span data-stu-id="ad369-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="ad369-107">**ナビゲーション ウィンドウ > モジュール > 輸送管理 > 設定 > 配送業者 > 出荷の配送業者**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad369-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="ad369-108">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="ad369-109">**出荷の配送業者**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="ad369-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ad369-111">**モード** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="ad369-112">出荷配送業者の一般情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="ad369-113">**概要**セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ad369-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="ad369-114">**出荷配送業者の有効化**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="ad369-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="ad369-115">**仕入先**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ad369-116">出荷配送業者の仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="ad369-117">**輸送業者タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="ad369-118">**マニュアル**を選択して配送業者のページを使用するか、または **EDI** を選択して、電子データ交換 (EDI) で業者を更新できます。</span><span class="sxs-lookup"><span data-stu-id="ad369-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="ad369-119">**配送業者の評価をアクティブ化**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="ad369-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="ad369-120">出荷配送業者の必要なサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ad369-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="ad369-121">**サービス** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ad369-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="ad369-122">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-122">Select **New**.</span></span>
3. <span data-ttu-id="ad369-123">**配送サービス** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="ad369-124">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ad369-125">**輸送方法**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="ad369-126">配送業者の住所の設定 (オプション)</span><span class="sxs-lookup"><span data-stu-id="ad369-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="ad369-127">**住所**セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ad369-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="ad369-128">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-128">Select **New**.</span></span>
3. <span data-ttu-id="ad369-129">**名前または説明**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="ad369-130">**国/地域**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="ad369-131">**配送先郵便番号**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ad369-132">**番地**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="ad369-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="ad369-134">出荷配送業者の評価プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="ad369-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="ad369-135">**評価プロファイル** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ad369-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="ad369-136">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-136">Select **New**.</span></span>
3. <span data-ttu-id="ad369-137">**評価プロファイル** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="ad369-138">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad369-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ad369-139">**サイト** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ad369-140">**倉庫**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="ad369-141">**レート エンジン** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ad369-142">配送業者との契約に従ってレート エンジンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="ad369-143">**レート マスター** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="ad369-144">**輸送時間エンジン** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="ad369-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad369-145">Select **Save**.</span></span>

