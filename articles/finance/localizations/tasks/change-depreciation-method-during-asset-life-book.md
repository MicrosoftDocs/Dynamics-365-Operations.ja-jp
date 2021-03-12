---
title: 帳簿の資産耐用年数期間中の減価償却方法の変更
description: 日本では、固定資産の耐用年数期間中、減価償却方法を変更することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup, AssetDepProfileChangeApply_JP,  AssetUndepreciatedBalancedSchedule_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d88a7cdb63dfdad987d5bf887cfa3ca1e7a23694
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990022"
---
# <a name="change-the-depreciation-method-during-the-asset-life-for-book"></a><span data-ttu-id="14fba-103">帳簿の資産耐用年数期間中の減価償却方法の変更</span><span class="sxs-lookup"><span data-stu-id="14fba-103">Change the depreciation method during the asset life for book</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14fba-104">日本では、固定資産の耐用年数期間中、減価償却方法を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="14fba-104">In Japan, you can change the depreciation method during the service life of a fixed asset.</span></span>



<span data-ttu-id="14fba-105">この手順では、固定資産グループおよび帳簿下の固定資産の減価償却プロファイルの変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="14fba-105">This procedure walks you through changing a depreciation profile for the fixed assets under a fixed asset group and book.</span></span>



<span data-ttu-id="14fba-106">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="14fba-106">In order to complete this procedure, the Fixed Assets configuration key must be selected.</span></span> <span data-ttu-id="14fba-107">また、この手順を完了するためには、[未償却残高表] と [経過年数表] をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="14fba-107">Also, the Undepreciated balance schedule or Years passed schedule has to be configure before you can complete this procedure.</span></span>

<span data-ttu-id="14fba-108">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="14fba-108">This procedure was created using the demo data company JPMF.</span></span>


## <a name="change-a-depreciation-profile"></a><span data-ttu-id="14fba-109">減価償却プロファイルの変更</span><span class="sxs-lookup"><span data-stu-id="14fba-109">Change a depreciation profile</span></span>
1. <span data-ttu-id="14fba-110">[固定資産] > [設定] > [帳簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="14fba-110">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="14fba-111">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="14fba-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="14fba-112">たとえば、[帳簿] フィールドで「250NDB_CUR」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="14fba-112">For example, filter on the Book field with a value of '250NDB_CUR'.</span></span>
3. <span data-ttu-id="14fba-113">[固定資産グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14fba-113">Click Fixed asset groups.</span></span>
4. <span data-ttu-id="14fba-114">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="14fba-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="14fba-115">たとえば、[固定資産グループ] フィールドで「STRU-A」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="14fba-115">For example, filter on the Fixed asset group field with a value of 'STRU-A'.</span></span>
5. <span data-ttu-id="14fba-116">[減価償却プロファイルの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14fba-116">Click Change depreciation profile.</span></span>
6. <span data-ttu-id="14fba-117">[変更後の減価償却プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="14fba-117">In the To depreciation profile field, type a value.</span></span>
7. <span data-ttu-id="14fba-118">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="14fba-118">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="14fba-119">この日付は、現在の会計カレンダーの会計年度の開始日である必要があります。</span><span class="sxs-lookup"><span data-stu-id="14fba-119">The date has to be the start date of a fiscal year in the current fiscal calendar.</span></span>  
8. <span data-ttu-id="14fba-120">[耐用年数の更新] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="14fba-120">Select Yes in the Update service life field.</span></span>
    * <span data-ttu-id="14fba-121">必要に応じてアイドル期間を追加できます。</span><span class="sxs-lookup"><span data-stu-id="14fba-121">You can add an idle period if you need to</span></span>  
9. <span data-ttu-id="14fba-122">[適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14fba-122">Click Apply.</span></span>
10. <span data-ttu-id="14fba-123">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="14fba-123">Click Yes.</span></span>

## <a name="view-the-years-passed-schedule"></a><span data-ttu-id="14fba-124">経過年数表の表示</span><span class="sxs-lookup"><span data-stu-id="14fba-124">View the years passed schedule</span></span>
1. <span data-ttu-id="14fba-125">[固定資産] > [設定] > [償却率表] > [経年表] に移動します。</span><span class="sxs-lookup"><span data-stu-id="14fba-125">Go to Fixed assets > Setup > Depreciation rate schedules > Years passed schedules.</span></span>
    * <span data-ttu-id="14fba-126">減価償却プロファイルの更新には対応するデータが必要です。</span><span class="sxs-lookup"><span data-stu-id="14fba-126">The corresponding data has to exist for the depreciation profile update.</span></span>  

