---
title: 出荷配送業者の設定
description: このトピックでは、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d157470527a986ea1c9fe0a9a02e2ba6ee8819e
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383001"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="31221-103">出荷配送業者の設定</span><span class="sxs-lookup"><span data-stu-id="31221-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="31221-104">このトピックでは、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="31221-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="31221-105">配送コーディネーターは、出荷の配送業者を入荷または出荷に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="31221-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="31221-106">新しい出荷の配送業者の作成</span><span class="sxs-lookup"><span data-stu-id="31221-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="31221-107">**ナビゲーション ウィンドウ > モジュール > 輸送管理 > 設定 > 配送業者 > 出荷の配送業者**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="31221-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="31221-108">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="31221-109">**出荷の配送業者**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="31221-110">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="31221-111">**モード** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="31221-112">出荷配送業者の一般情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="31221-113">**概要**セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="31221-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="31221-114">**出荷配送業者の有効化**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="31221-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="31221-115">**仕入先**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="31221-116">出荷配送業者の仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="31221-117">**輸送業者タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="31221-118">**マニュアル**を選択して配送業者のページを使用するか、または **EDI** を選択して、電子データ交換 (EDI) で業者を更新できます。</span><span class="sxs-lookup"><span data-stu-id="31221-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="31221-119">**配送業者の評価をアクティブ化**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="31221-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="31221-120">出荷配送業者の必要なサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="31221-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="31221-121">**サービス** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="31221-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="31221-122">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-122">Select **New**.</span></span>
3. <span data-ttu-id="31221-123">**配送サービス** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="31221-124">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="31221-125">**輸送方法**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="31221-126">配送業者の住所の設定 (オプション)</span><span class="sxs-lookup"><span data-stu-id="31221-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="31221-127">**住所**セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="31221-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="31221-128">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-128">Select **New**.</span></span>
3. <span data-ttu-id="31221-129">**名前または説明**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="31221-130">**国/地域**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="31221-131">**配送先郵便番号**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="31221-132">**番地**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="31221-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="31221-134">出荷配送業者の評価プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="31221-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="31221-135">**評価プロファイル** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="31221-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="31221-136">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-136">Select **New**.</span></span>
3. <span data-ttu-id="31221-137">**評価プロファイル** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="31221-138">**名前**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="31221-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="31221-139">**サイト** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="31221-140">**倉庫**フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="31221-141">**レート エンジン** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="31221-142">配送業者との契約に従ってレート エンジンを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="31221-143">**レート マスター** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="31221-144">**輸送時間エンジン** フィールドで、ドロップダウン メニューからオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="31221-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="31221-145">Select **Save**.</span></span>

