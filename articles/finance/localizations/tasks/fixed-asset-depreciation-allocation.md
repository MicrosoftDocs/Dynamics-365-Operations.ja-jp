---
title: 固定資産減価償却配賦の設定
description: 日本では、特定の固定資産の減価償却費は複数の部門間で共有できます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetAllocationRuleSetup_CN,  AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: China (PRC), Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28a7841fd90d0ae3f987eda8d2cae2103955b8b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408158"
---
# <a name="setup-fixed-asset-depreciation-allocation"></a><span data-ttu-id="172de-103">固定資産減価償却配賦の設定</span><span class="sxs-lookup"><span data-stu-id="172de-103">Setup fixed asset depreciation allocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="172de-104">日本では、特定の固定資産の減価償却費は複数の部門間で共有できます。</span><span class="sxs-lookup"><span data-stu-id="172de-104">In Japan, the depreciation expenses of a particular fixed asset can be shared among multiple departments.</span></span> 



<span data-ttu-id="172de-105">このタスクは、固定資産の減価償却の配賦について説明します。</span><span class="sxs-lookup"><span data-stu-id="172de-105">This task walks you through setting up fixed asset depreciation allocation.</span></span> 



<span data-ttu-id="172de-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="172de-106">This task was created using the demo data company JPMF.</span></span>


## <a name="create-a-fixed-asset-allocation-rule"></a><span data-ttu-id="172de-107">固定資産配賦ルールの作成</span><span class="sxs-lookup"><span data-stu-id="172de-107">Create a Fixed asset allocation rule</span></span>
1. <span data-ttu-id="172de-108">[固定資産] > [設定] > [減価償却配賦ルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="172de-108">Go to Fixed assets > Setup > Depreciation allocation rules.</span></span>
2. <span data-ttu-id="172de-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="172de-109">Click New.</span></span>
3. <span data-ttu-id="172de-110">[ルール ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-110">In the Rule ID field, type a value.</span></span>
4. <span data-ttu-id="172de-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="172de-112">[分析コード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-112">In the Dimension name field, type a value.</span></span>
6. <span data-ttu-id="172de-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="172de-113">Click Add.</span></span>
7. <span data-ttu-id="172de-114">BusinessUnit フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-114">In the BusinessUnit field, type a value.</span></span>
    * <span data-ttu-id="172de-115">最初の配賦のターゲットに関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-115">Enter the information for the first allocation target.</span></span>  
8. <span data-ttu-id="172de-116">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-116">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="172de-117">すべての配賦のターゲットの合計は 100 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="172de-117">The total of all the allocation target must be 100.</span></span>  
9. <span data-ttu-id="172de-118">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="172de-118">In the Offset account field, specify the desired values.</span></span>
10. <span data-ttu-id="172de-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="172de-119">Click Add.</span></span>
11. <span data-ttu-id="172de-120">BusinessUnit フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-120">In the BusinessUnit field, type a value.</span></span>
12. <span data-ttu-id="172de-121">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-121">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="172de-122">すべての配賦のターゲットの合計は 100 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="172de-122">The total of all the allocation target must be 100.</span></span>  
13. <span data-ttu-id="172de-123">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="172de-123">In the Offset account field, specify the desired values.</span></span>
14. <span data-ttu-id="172de-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="172de-124">Click Save.</span></span>

## <a name="assign-a-fixed-asset-allocation-rule-to-a-posting-profile"></a><span data-ttu-id="172de-125">固定資産配賦ルールの転記プロファイルへの割り当て</span><span class="sxs-lookup"><span data-stu-id="172de-125">Assign a fixed asset allocation rule to a posting profile</span></span>
1. <span data-ttu-id="172de-126">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="172de-126">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="172de-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="172de-127">Click Edit.</span></span>
3. <span data-ttu-id="172de-128">[トランザクション タイプ] フィールドで [減価償却] を選択します。</span><span class="sxs-lookup"><span data-stu-id="172de-128">In the Transaction type field, select 'Depreciation'.</span></span>
4. <span data-ttu-id="172de-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="172de-129">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="172de-130">配賦ルールをリンクするレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="172de-130">Select the record that you want to link the allocation rule to.</span></span>  
5. <span data-ttu-id="172de-131">[減価償却配賦ルール] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="172de-131">Expand the Depreciation allocation rules section.</span></span>
6. <span data-ttu-id="172de-132">[減価償却の資産の配賦ルール] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="172de-132">In the Asset allocation rule for depreciation field, type a value.</span></span>
7. <span data-ttu-id="172de-133">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="172de-133">Click Save.</span></span>

