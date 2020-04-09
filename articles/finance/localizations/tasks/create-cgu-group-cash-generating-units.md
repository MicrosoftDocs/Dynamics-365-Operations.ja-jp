---
title: CGU グループおよび資産グループの作成
description: 日本では、固定資産の減損は、個々の固定資産または資産グループに基づき決定することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentCashGenUnitGroup_JP, SysQueryForm, AssetImpairmentCashGenUnit_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5148915db82126c00c848eb12059cc0b7599a35
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138985"
---
# <a name="create-cgu-group-and-cash-generating-units"></a><span data-ttu-id="48952-103">CGU グループおよび資産グループの作成</span><span class="sxs-lookup"><span data-stu-id="48952-103">Create CGU group and cash generating units</span></span>

<span data-ttu-id="48952-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="48952-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="48952-105">日本では、固定資産の減損は、個々の固定資産または資産グループに基づき決定することができます。</span><span class="sxs-lookup"><span data-stu-id="48952-105">In Japan, an impairment on fixed assets can be based on either individual fixed assets or cash generating units.</span></span> <span data-ttu-id="48952-106">資産グループに基づき減損を評価する場合の最初のステップは、固定資産を資産グループにグループ化することです。</span><span class="sxs-lookup"><span data-stu-id="48952-106">When measuring impairment based on cash generating units, the first step is to group the fixed assets into cash generating units.</span></span> 



<span data-ttu-id="48952-107">最適な CGU を選択できるよう、キャッシュ生成単位の複数のセットが許可されています。</span><span class="sxs-lookup"><span data-stu-id="48952-107">Multiple sets of cash generating units are allowed so that you can choose the most appropriate CGU.</span></span> <span data-ttu-id="48952-108">これは、CGU グループを作成することで達成されます。</span><span class="sxs-lookup"><span data-stu-id="48952-108">This is achieved through the creation of CGU groups.</span></span> 



<span data-ttu-id="48952-109">この手順では、CGU グループと資産グループの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="48952-109">This procedure walks you through creating CGU groups and cash generating units.</span></span> <span data-ttu-id="48952-110">また、固定資産の資産グループへの割当方法と、共有資産および営業権の CGU グループへの割当方法も確認することができます。</span><span class="sxs-lookup"><span data-stu-id="48952-110">You will also learn how to assign fixed assets to cash generating units and how to assign shared assets and goodwill to CGU groups.</span></span> 



<span data-ttu-id="48952-111">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48952-111">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="48952-112">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="48952-112">This procedure was created using the demo data company JPMF.</span></span>


## <a name="create-a-cgu-group"></a><span data-ttu-id="48952-113">CGU グループの作成</span><span class="sxs-lookup"><span data-stu-id="48952-113">Create a CGU group</span></span>
1. <span data-ttu-id="48952-114">[固定資産] > [設定] > [減損] > [CGU グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48952-114">Go to Fixed assets > Setup > Impairment > CGU groups.</span></span>
2. <span data-ttu-id="48952-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-115">Click New.</span></span>
    * <span data-ttu-id="48952-116">固定資産と資産グループの適切な組み合わせが不明な場合は、テスト用に複数の CGU グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="48952-116">You can create multiple CGU groups for testing if you are not sure about the appropriate combinations of fixed assets and cash generating units.</span></span>  
3. <span data-ttu-id="48952-117">[CGU グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-117">In the CGU group field, type a value.</span></span>
4. <span data-ttu-id="48952-118">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="48952-119">[営業権と共有資産の減損] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="48952-119">In the Impairment of goodwill and shared asset field, select an option.</span></span>
    * <span data-ttu-id="48952-120">会社のポリシーに従って方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="48952-120">Select the method according to your corporate policy.</span></span>  
6. <span data-ttu-id="48952-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-121">Click Save.</span></span>

## <a name="create-cash-generating-units-under-the-cgu-group"></a><span data-ttu-id="48952-122">CGU グループ下での資産グループの作成</span><span class="sxs-lookup"><span data-stu-id="48952-122">Create cash generating units under the CGU group</span></span>
1. <span data-ttu-id="48952-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-123">Click New.</span></span>
2. <span data-ttu-id="48952-124">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-124">In the Name field, type a value.</span></span>
3. <span data-ttu-id="48952-125">後で参照できるよう、[資産グループ番号] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="48952-125">Note the value in the Cash generating unit number field to reference later</span></span>
    * <span data-ttu-id="48952-126">資産グループをコンフィギュレーションする場合は、この値を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48952-126">You will need to reference this value when you configure the cash generating unit.</span></span>  
4. <span data-ttu-id="48952-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-127">Click New.</span></span>
5. <span data-ttu-id="48952-128">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-128">In the Name field, type a value.</span></span>
6. <span data-ttu-id="48952-129">後で参照できるよう、[資産グループ番号] フィールドの値をメモします。</span><span class="sxs-lookup"><span data-stu-id="48952-129">Note the value in the Cash generating unit number field to reference later</span></span>
    * <span data-ttu-id="48952-130">資産グループをコンフィギュレーションする場合は、この値を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48952-130">You will need to reference this value when you configure the cash generating unit.</span></span>  

## <a name="assign-shared-assets-and-goodwill-to-the-cgu-group"></a><span data-ttu-id="48952-131">共有資産と営業権の CGU グループへの割り当て</span><span class="sxs-lookup"><span data-stu-id="48952-131">Assign shared assets and goodwill to the CGU group</span></span>
1. <span data-ttu-id="48952-132">[共有資産と営業権] のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="48952-132">Expand the Shared assets and goodwill section.</span></span>
2. <span data-ttu-id="48952-133">[一括インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-133">Click Massive import.</span></span>
    * <span data-ttu-id="48952-134">その条件と一致するすべての資産を一度に追加する条件を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="48952-134">We recommend that you specify a condition that adds all the assets with that hit with the condition at once.</span></span>   <span data-ttu-id="48952-135">グリッドに、資産を 1 つずつ入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="48952-135">You can also enter asset one by one in the grid.</span></span>  
3. <span data-ttu-id="48952-136">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-136">In the Criteria field, type a value.</span></span>
4. <span data-ttu-id="48952-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-137">Click OK.</span></span>

## <a name="configure-cash-generating-units"></a><span data-ttu-id="48952-138">資産グループのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="48952-138">Configure cash generating units</span></span>
1. <span data-ttu-id="48952-139">[固定資産の割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-139">Click Assign fixed assets.</span></span>
2. <span data-ttu-id="48952-140">[クイック フィルター] を使用して編集する CGU を検索します。</span><span class="sxs-lookup"><span data-stu-id="48952-140">Use the Quick Filter to find the CGU to edit.</span></span>
    * <span data-ttu-id="48952-141">以前にメモした最初の資産グループ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-141">Enter the first cash generating unit number that you noted previously.</span></span>  
3. <span data-ttu-id="48952-142">[一括インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-142">Click Massive import.</span></span>
    * <span data-ttu-id="48952-143">その条件と一致するすべての資産を一度に追加する条件を指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="48952-143">We recommend you to specify a condition that adds all the assets with that hit with the condition at once.</span></span>   <span data-ttu-id="48952-144">グリッドに、資産を 1 つずつ入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="48952-144">You can also enter asset one by one in the grid.</span></span>  
4. <span data-ttu-id="48952-145">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-145">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="48952-146">例: 場所 = 福岡</span><span class="sxs-lookup"><span data-stu-id="48952-146">For example: Location = FUKUOKA</span></span>  
5. <span data-ttu-id="48952-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-147">Click OK.</span></span>
6. <span data-ttu-id="48952-148">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-148">In the Undiscounted cash flow field, enter a number.</span></span>
7. <span data-ttu-id="48952-149">[回収可能価額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-149">In the Recoverable value field, enter a number.</span></span>
8. <span data-ttu-id="48952-150">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-150">Click Save.</span></span>
9. <span data-ttu-id="48952-151">[クイック フィルター] を使用して編集する資産グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="48952-151">Use the Quick Filter to find the cash generating unit to edit.</span></span>
    * <span data-ttu-id="48952-152">以前にメモした 2 番目の資産グループ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-152">Enter the second cash generating unit number that you noted previously.</span></span>  
10. <span data-ttu-id="48952-153">[一括インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-153">Click Massive import.</span></span>
11. <span data-ttu-id="48952-154">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-154">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="48952-155">例: 場所 = 大阪</span><span class="sxs-lookup"><span data-stu-id="48952-155">For example: Location = OSAKA</span></span>  
12. <span data-ttu-id="48952-156">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-156">Click OK.</span></span>
13. <span data-ttu-id="48952-157">[割引前キャッシュ フロー] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-157">In the Undiscounted cash flow field, enter a number.</span></span>
14. <span data-ttu-id="48952-158">[回収可能価額] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48952-158">In the Recoverable value field, enter a number.</span></span>
15. <span data-ttu-id="48952-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-159">Click Save.</span></span>

## <a name="activate-the-cgu-group"></a><span data-ttu-id="48952-160">CGU グループの有効化</span><span class="sxs-lookup"><span data-stu-id="48952-160">Activate the CGU group</span></span>
1. <span data-ttu-id="48952-161">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-161">Click Activate.</span></span>
    * <span data-ttu-id="48952-162">認識テストの実行に使用できるのは、有効な CGU グループだけです。</span><span class="sxs-lookup"><span data-stu-id="48952-162">Only active CGU groups are allowed to run recognition tests.</span></span>  
2. <span data-ttu-id="48952-163">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48952-163">Click Yes.</span></span>

