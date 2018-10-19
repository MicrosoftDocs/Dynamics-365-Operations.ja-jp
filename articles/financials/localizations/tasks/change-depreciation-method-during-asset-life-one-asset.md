--- 
title: "単一資産の資産耐用年数期間中の減価償却方法の変更"
description: "日本では、固定資産の耐用年数期間中、減価償却方法を変更することが許可されています。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, AssetDepProfileChange_JP,  AssetUndepreciatedBalancedSchedule_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: ae83c1ebe1ddad4c4f8afea4dbe5e78dbec1039e
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="change-the-depreciation-method-during-the-asset-life-for-one-asset"></a><span data-ttu-id="44d5e-103">単一資産の資産耐用年数期間中の減価償却方法の変更</span><span class="sxs-lookup"><span data-stu-id="44d5e-103">Change the depreciation method during the asset life for one asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44d5e-104">日本では、固定資産の耐用年数期間中、減価償却方法を変更することが許可されています。</span><span class="sxs-lookup"><span data-stu-id="44d5e-104">In Japan, the depreciation method is permitted to change during the service life of a fixed asset.</span></span>



<span data-ttu-id="44d5e-105">この手順では、固定資産の減価償却プロファイルの変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="44d5e-105">This procedure walks you through changing the depreciation profile for a fixed asset.</span></span>



<span data-ttu-id="44d5e-106">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44d5e-106">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span> <span data-ttu-id="44d5e-107">また、この手順を完了する前に、[未償却残高表] と [経過年数表] をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="44d5e-107">Also, the Undepreciated balance schedule or Years passed schedule has to be configured before you can complete this procedure.</span></span>



<span data-ttu-id="44d5e-108">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="44d5e-108">This procedure was created using the demo data company JPMF.</span></span>


## <a name="change-the-depreciation-profile-for-a-fixed-asset"></a><span data-ttu-id="44d5e-109">固定資産の減価償却プロファイルを変更する</span><span class="sxs-lookup"><span data-stu-id="44d5e-109">Change the depreciation profile for a fixed asset</span></span>
1. <span data-ttu-id="44d5e-110">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="44d5e-110">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="44d5e-111">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="44d5e-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="44d5e-112">たとえば、[固定資産番号] フィールドを「STRUM-000001」の値でフィルタリングします。</span><span class="sxs-lookup"><span data-stu-id="44d5e-112">For example, filter on the Fixed asset number field with a value of 'STRUM-000001'.</span></span>
3. <span data-ttu-id="44d5e-113">[帳簿] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44d5e-113">Click Books.</span></span>
4. <span data-ttu-id="44d5e-114">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44d5e-114">Click Functions.</span></span>
5. <span data-ttu-id="44d5e-115">[減価償却プロファイルの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44d5e-115">Click Change depreciation profile.</span></span>
6. <span data-ttu-id="44d5e-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44d5e-116">Click New.</span></span>
7. <span data-ttu-id="44d5e-117">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="44d5e-117">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="44d5e-118">この日付は、現在の会計カレンダーの会計年度の開始日である必要があります。</span><span class="sxs-lookup"><span data-stu-id="44d5e-118">The date has to be the start date of a fiscal year, in the current fiscal calendar.</span></span>  
8. <span data-ttu-id="44d5e-119">[減価償却プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="44d5e-119">In the Depreciation profile field, type a value.</span></span>
9. <span data-ttu-id="44d5e-120">[耐用年数の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44d5e-120">Click Update service life.</span></span>
    * <span data-ttu-id="44d5e-121">[耐用年数]、[減価償却期間] の残りが更新されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="44d5e-121">Confirm that Service life and Depreciation periods remaining are updated.</span></span>  

## <a name="view-the-undepreciated-balance-schedule-for-fixed-assets"></a><span data-ttu-id="44d5e-122">固定資産の未償却残高表の表示</span><span class="sxs-lookup"><span data-stu-id="44d5e-122">View the undepreciated balance schedule for fixed assets</span></span>
1. <span data-ttu-id="44d5e-123">[固定資産] > [設定] > [償却率表] > [未償却残額表] に移動します。</span><span class="sxs-lookup"><span data-stu-id="44d5e-123">Go to Fixed assets > Setup > Depreciation rate schedules > Undepreciated balance schedules.</span></span>
    * <span data-ttu-id="44d5e-124">償却率表の編集方法を確認する際には [償却率表] の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44d5e-124">Refer to the procedure for Depreciation rate schedules to learn how to edit a depreciation rate schedule.</span></span>  
    * <span data-ttu-id="44d5e-125">減価償却プロファイルの更新には対応するデータが必要です。</span><span class="sxs-lookup"><span data-stu-id="44d5e-125">The corresponding data has to exist for the depreciation profile update.</span></span>  
    * <span data-ttu-id="44d5e-126">[変更元の方法]、[変更後の方法]、[耐用年数] および [経過年数] によって資産の変更に適用されるレコードが決定されます。</span><span class="sxs-lookup"><span data-stu-id="44d5e-126">From method, To method, Service life and Years passed determine the record to apply to the asset change.</span></span>  


