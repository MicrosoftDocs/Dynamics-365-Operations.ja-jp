--- 
title: "CGU グループおよび資産グループの作成 (日本)"
description: "日本では、固定資産の減損は、個々の固定資産または資産グループに基づき決定することができます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bfa7ecbe2b0b5dafd5bc229ce29864b69b62f0c8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-cgu-group-and-cash-generating-units-japan"></a><span data-ttu-id="34e38-103">CGU グループおよび資産グループの作成 (日本)</span><span class="sxs-lookup"><span data-stu-id="34e38-103">Create CGU group and cash generating units (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34e38-104">日本では、固定資産の減損は、個々の固定資産または資産グループに基づき決定することができます。</span><span class="sxs-lookup"><span data-stu-id="34e38-104">In Japan, an impairment on fixed assets can be based on either individual fixed assets or cash generating units.</span></span> <span data-ttu-id="34e38-105">資産グループに基づき減損を評価する場合の最初のステップは、固定資産を資産グループにグループ化することです。</span><span class="sxs-lookup"><span data-stu-id="34e38-105">When measuring impairment based on cash generating units, the first step is to group the fixed assets into cash generating units.</span></span> 



<span data-ttu-id="34e38-106">最適な CGU を選択できるよう、キャッシュ生成単位の複数のセットが許可されています。</span><span class="sxs-lookup"><span data-stu-id="34e38-106">Multiple sets of cash generating units are allowed so that you can choose the most appropriate CGU.</span></span> <span data-ttu-id="34e38-107">これは、CGU グループを作成することで達成されます。</span><span class="sxs-lookup"><span data-stu-id="34e38-107">This is achieved through the creation of CGU groups.</span></span> 



<span data-ttu-id="34e38-108">この手順では、CGU グループと資産グループの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="34e38-108">This procedure walks you through creating CGU groups and cash generating units.</span></span> <span data-ttu-id="34e38-109">また、固定資産の資産グループへの割当方法と、共有資産および営業権の CGU グループへの割当方法も確認することができます。</span><span class="sxs-lookup"><span data-stu-id="34e38-109">You will also learn how to assign fixed assets to cash generating units and how to assign shared assets and goodwill to CGU groups.</span></span> 



<span data-ttu-id="34e38-110">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34e38-110">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="34e38-111">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="34e38-111">This procedure was created using the demo data company JPMF.</span></span>


## <a name="create-a-cgu-group"></a><span data-ttu-id="34e38-112">CGU グループの作成</span><span class="sxs-lookup"><span data-stu-id="34e38-112">Create a CGU group</span></span>
1. <span data-ttu-id="34e38-113">[固定資産] > [設定] > [減損] > [CGU グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="34e38-113">Go to Fixed assets > Setup > Impairment > CGU groups.</span></span>
2. <span data-ttu-id="34e38-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-114">Click New.</span></span>
    * <span data-ttu-id="34e38-115">固定資産と資産グループの適切な組み合わせが不明な場合は、テスト用に複数の CGU グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="34e38-115">You can create multiple CGU groups for testing if you are not sure about the appropriate combinations of fixed assets and cash generating units.</span></span>  
3. <span data-ttu-id="34e38-116">[CGU グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-116">In the CGU group field, type a value.</span></span>
4. <span data-ttu-id="34e38-117">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-117">In the Description field, type a value.</span></span>
5. <span data-ttu-id="34e38-118">[営業権と共有資産の減損] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="34e38-118">In the Impairment of goodwill and shared asset field, select an option.</span></span>
    * <span data-ttu-id="34e38-119">会社のポリシーに従って方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="34e38-119">Select the method according to your corporate policy.</span></span>  
6. <span data-ttu-id="34e38-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-120">Click Save.</span></span>

## <a name="create-cash-generating-units-under-the-cgu-group"></a><span data-ttu-id="34e38-121">CGU グループ下での資産グループの作成</span><span class="sxs-lookup"><span data-stu-id="34e38-121">Create cash generating units under the CGU group</span></span>
1. <span data-ttu-id="34e38-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-122">Click New.</span></span>
2. <span data-ttu-id="34e38-123">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-123">In the Name field, type a value.</span></span>
3. <span data-ttu-id="34e38-124">後で参照できるよう、[資産グループ番号] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="34e38-124">Note the value in the Cash generating unit number field to reference later</span></span>
    * <span data-ttu-id="34e38-125">資産グループをコンフィギュレーションする場合は、この値を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34e38-125">You will need to reference this value when you configure the cash generating unit.</span></span>  
4. <span data-ttu-id="34e38-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-126">Click New.</span></span>
5. <span data-ttu-id="34e38-127">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-127">In the Name field, type a value.</span></span>
6. <span data-ttu-id="34e38-128">後で参照できるよう、[資産グループ番号] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="34e38-128">Note the value in the Cash generating unit number field to reference later</span></span>
    * <span data-ttu-id="34e38-129">資産グループをコンフィギュレーションする場合は、この値を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="34e38-129">You will need to reference this value when you configure the cash generating unit.</span></span>  

## <a name="assign-shared-assets-and-goodwill-to-the-cgu-group"></a><span data-ttu-id="34e38-130">共有資産と営業権の CGU グループへの割り当て</span><span class="sxs-lookup"><span data-stu-id="34e38-130">Assign shared assets and goodwill to the CGU group</span></span>
1. <span data-ttu-id="34e38-131">[共有資産と営業権] のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="34e38-131">Expand the Shared assets and goodwill section.</span></span>
2. <span data-ttu-id="34e38-132">[一括インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-132">Click Massive import.</span></span>
    * <span data-ttu-id="34e38-133">その条件と一致するすべての資産を一度に追加する条件を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="34e38-133">We recommend that you specify a condition that adds all the assets with that hit with the condition at once.</span></span>   <span data-ttu-id="34e38-134">グリッドに、資産を 1 つずつ入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="34e38-134">You can also enter asset one by one in the grid.</span></span>  
3. <span data-ttu-id="34e38-135">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-135">In the Criteria field, type a value.</span></span>
4. <span data-ttu-id="34e38-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-136">Click OK.</span></span>

## <a name="configure-cash-generating-units"></a><span data-ttu-id="34e38-137">資産グループのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="34e38-137">Configure cash generating units</span></span>
1. <span data-ttu-id="34e38-138">[固定資産の割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-138">Click Assign fixed assets.</span></span>
2. <span data-ttu-id="34e38-139">[クイック フィルター] を使用して編集する CGU を検索します。</span><span class="sxs-lookup"><span data-stu-id="34e38-139">Use the Quick Filter to find the CGU to edit.</span></span>
    * <span data-ttu-id="34e38-140">以前にメモした最初の資産グループ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-140">Enter the first cash generating unit number that you noted previously.</span></span>  
3. <span data-ttu-id="34e38-141">[一括インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-141">Click Massive import.</span></span>
    * <span data-ttu-id="34e38-142">その条件と一致するすべての資産を一度に追加する条件を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="34e38-142">We recommend you to specify a condition that adds all the assets with that hit with the condition at once.</span></span>   <span data-ttu-id="34e38-143">グリッドに、資産を 1 つずつ入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="34e38-143">You can also enter asset one by one in the grid.</span></span>  
4. <span data-ttu-id="34e38-144">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-144">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="34e38-145">例: 場所 = 福岡</span><span class="sxs-lookup"><span data-stu-id="34e38-145">For example: Location = FUKUOKA</span></span>  
5. <span data-ttu-id="34e38-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-146">Click OK.</span></span>
6. <span data-ttu-id="34e38-147">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-147">In the Undiscounted cash flow field, enter a number.</span></span>
7. <span data-ttu-id="34e38-148">[回収可能価額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-148">In the Recoverable value field, enter a number.</span></span>
8. <span data-ttu-id="34e38-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-149">Click Save.</span></span>
9. <span data-ttu-id="34e38-150">[クイック フィルター] を使用して編集する資産グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="34e38-150">Use the Quick Filter to find the cash generating unit to edit.</span></span>
    * <span data-ttu-id="34e38-151">以前にメモした 2 番目の資産グループ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-151">Enter the second cash generating unit number that you noted previously.</span></span>  
10. <span data-ttu-id="34e38-152">[一括インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-152">Click Massive import.</span></span>
11. <span data-ttu-id="34e38-153">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-153">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="34e38-154">例: 場所 = 大阪</span><span class="sxs-lookup"><span data-stu-id="34e38-154">For example: Location = OSAKA</span></span>  
12. <span data-ttu-id="34e38-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-155">Click OK.</span></span>
13. <span data-ttu-id="34e38-156">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-156">In the Undiscounted cash flow field, enter a number.</span></span>
14. <span data-ttu-id="34e38-157">[回収可能価額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="34e38-157">In the Recoverable value field, enter a number.</span></span>
15. <span data-ttu-id="34e38-158">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-158">Click Save.</span></span>

## <a name="activate-the-cgu-group"></a><span data-ttu-id="34e38-159">CGU グループの有効化</span><span class="sxs-lookup"><span data-stu-id="34e38-159">Activate the CGU group</span></span>
1. <span data-ttu-id="34e38-160">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-160">Click Activate.</span></span>
    * <span data-ttu-id="34e38-161">認識テストの実行に使用できるのは、有効な CGU グループだけです。</span><span class="sxs-lookup"><span data-stu-id="34e38-161">Only active CGU groups are allowed to run recognition tests.</span></span>  
2. <span data-ttu-id="34e38-162">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="34e38-162">Click Yes.</span></span>

