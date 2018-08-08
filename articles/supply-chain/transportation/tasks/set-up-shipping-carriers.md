--- 
title: "出荷配送業者の設定"
description: "この手順では、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="2cd97-103">出荷配送業者の設定</span><span class="sxs-lookup"><span data-stu-id="2cd97-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cd97-104">この手順では、出荷の配送業者を設定し、サービス、出荷モード、輸送入札、輸送機関の制約、および出荷レートなどの詳細を定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="2cd97-105">配送コーディネーターは、出荷の配送業者を入荷または出荷に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="2cd97-106">新しい出荷の配送業者の作成</span><span class="sxs-lookup"><span data-stu-id="2cd97-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="2cd97-107">[輸送管理] > [設定] > [配送業者] > [出荷の配送業者] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="2cd97-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-108">Click New.</span></span>
3. <span data-ttu-id="2cd97-109">[出荷の配送業者] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="2cd97-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2cd97-111">[モード] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2cd97-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2cd97-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="2cd97-114">出荷配送業者の一般情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="2cd97-115">[概要] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="2cd97-116">[出荷配送業者の有効化] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="2cd97-117">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2cd97-118">出荷配送業者の仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="2cd97-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2cd97-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2cd97-121">[輸送業者タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="2cd97-122">マニュアルを選択して配送業者のページを使用するか、または EDI を選択して、電子データ交換 (EDI) で入金を更新できます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="2cd97-123">[配送業者の評価をアクティブ化] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="2cd97-124">出荷配送業者の必要なサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="2cd97-125">[サービス] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="2cd97-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-126">Click New.</span></span>
3. <span data-ttu-id="2cd97-127">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2cd97-128">[配送サービス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="2cd97-129">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="2cd97-130">[輸送方法] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2cd97-131">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2cd97-132">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="2cd97-133">配送業者の住所の設定 (オプション)</span><span class="sxs-lookup"><span data-stu-id="2cd97-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="2cd97-134">[住所] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="2cd97-135">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-135">Click New.</span></span>
3. <span data-ttu-id="2cd97-136">[名前または説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="2cd97-137">[国/地域] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="2cd97-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="2cd97-139">[配送先郵便番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2cd97-140">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2cd97-141">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2cd97-142">[番地] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="2cd97-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="2cd97-144">出荷配送業者の評価プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="2cd97-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="2cd97-145">[評価プロファイル] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="2cd97-146">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-146">Click New.</span></span>
3. <span data-ttu-id="2cd97-147">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2cd97-148">[評価プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="2cd97-149">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="2cd97-150">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2cd97-151">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="2cd97-152">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2cd97-153">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="2cd97-154">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="2cd97-155">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2cd97-156">[レート エンジン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2cd97-157">配送業者との契約に従ってレート エンジンを選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="2cd97-158">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="2cd97-159">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="2cd97-160">[レート マスター] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="2cd97-161">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2cd97-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="2cd97-162">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="2cd97-163">[輸送時間エンジン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2cd97-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="2cd97-164">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="2cd97-165">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2cd97-165">Click Save.</span></span>


