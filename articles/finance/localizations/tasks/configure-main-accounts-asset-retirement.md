---
title: 資産除去責務の転記および市場割引率のための主勘定のコンフィギュレーション
description: 日本では、法的な除去責務のある固定資産を取得した場合、除去する際には資産除去責務を評価し転記する必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting, AssetDiscountRateSchedule_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d04507d851c5594bf9077de6581793d405c8d09
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183749"
---
# <a name="configure-main-accounts-for-asset-retirement-obligation-posting-and-market-discount-rates"></a><span data-ttu-id="5ae3e-103">資産除去責務の転記および市場割引率のための主勘定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ae3e-103">Configure main accounts for asset retirement obligation posting and market discount rates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ae3e-104">日本では、法的な除去責務のある固定資産を取得した場合、除去する際には資産除去責務を評価し転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-104">For Japan, asset retirement obligation needs to be assessed and posted when acquiring a fixed asset with legal obligations at retirement.</span></span> 



<span data-ttu-id="5ae3e-105">ユーザーは、資産の除去責務のトランザクションを転記できるようにするには、すべての主勘定を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-105">The user needs to configure all the main accounts before any transaction of asset retirement obligation can be posted.</span></span>



<span data-ttu-id="5ae3e-106">このタスクでは、資産の除去責務の転記のために主勘定を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-106">Use this task to learn how to configure the main accounts for asset retirement obligation posting.</span></span>



<span data-ttu-id="5ae3e-107">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-107">In order to complete this task, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="5ae3e-108">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-108">This task uses the JPMF demo company data.</span></span>


## <a name="configure-ledger-accounts-for-asset-retirement-obligation-posting"></a><span data-ttu-id="5ae3e-109">資産除去責務の転記のための勘定科目のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ae3e-109">Configure ledger accounts for asset retirement obligation posting</span></span>
1. <span data-ttu-id="5ae3e-110">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-110">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="5ae3e-111">[資産除去責務] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-111">Expand the Asset retirement obligation section.</span></span>
3. <span data-ttu-id="5ae3e-112">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-112">Click Add.</span></span>
4. <span data-ttu-id="5ae3e-113">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-113">In the Book field, type a value.</span></span>
5. <span data-ttu-id="5ae3e-114">[グループ化] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-114">In the Groupings field, select an option.</span></span>
6. <span data-ttu-id="5ae3e-115">[固定資産番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-115">In the Fixed asset number field, type a value.</span></span>
    * <span data-ttu-id="5ae3e-116">オプション: [グループ] または [テーブル] として「グループ化」を選択した場合は、固定資産グループまたは固定資産を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-116">Optional: when you select 'Groupings' as Group or Table, you will need to specify a fixed asset group or a fixed asset.</span></span>  
7. <span data-ttu-id="5ae3e-117">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-117">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="5ae3e-118">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-118">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="5ae3e-119">[選択] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-119">In the Select field, select an option.</span></span>
10. <span data-ttu-id="5ae3e-120">[文書種類ごとの廃棄パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-120">Expand the Disposal parameters by document type section.</span></span>
11. <span data-ttu-id="5ae3e-121">[売却または仕損] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-121">In the Sale or scrap field, select an option.</span></span>
    * <span data-ttu-id="5ae3e-122">[販売] および [仕損] の両方のタイプのトランザクションを転記する前に、これらの処分勘定を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-122">You must set up both the Sales and Scrap type of disposal accounts before you can post transactions of those types.</span></span>  
12. <span data-ttu-id="5ae3e-123">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-123">Click New.</span></span>
13. <span data-ttu-id="5ae3e-124">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-124">In the Book field, type a value.</span></span>
14. <span data-ttu-id="5ae3e-125">[有効] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-125">In the Valid for field, select an option.</span></span>
15. <span data-ttu-id="5ae3e-126">[固定資産関係] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-126">In the Fixed asset relation field, type a value.</span></span>
    * <span data-ttu-id="5ae3e-127">オプション: [グループ] または [テーブル] として「有効」を選択した場合は、固定資産グループまたは固定資産を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-127">Optional: when you select 'Valid for' as Group or Table, you will need to specify a fixed asset group or a fixed asset.</span></span>  
16. <span data-ttu-id="5ae3e-128">[主勘定] フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-128">In the Main account field, specify the desired values.</span></span>
17. <span data-ttu-id="5ae3e-129">[相殺勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-129">In the Offset account field, specify the desired values.</span></span>
    * <span data-ttu-id="5ae3e-130">トランザクションの他の組み合わせに対して、主勘定のコンフィギュレーション ステップを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-130">Repeat these steps to configure main accounts for other combinations of transactions.</span></span>  
    * <span data-ttu-id="5ae3e-131">コンフィギュレーションの各行は転記金額の 1 つのタイプに必要です。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-131">Each line of configuration is needed for one type of Post value.</span></span>  

## <a name="configure-market-discount-rates"></a><span data-ttu-id="5ae3e-132">市場割引率のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5ae3e-132">Configure market discount rates</span></span>
1. <span data-ttu-id="5ae3e-133">[固定資産] > [設定] > [キャッシュフロー割引率] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-133">Go to Fixed assets > Setup > Cashflow discount rates.</span></span>
2. <span data-ttu-id="5ae3e-134">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-134">Click New.</span></span>
3. <span data-ttu-id="5ae3e-135">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-135">In the Start date field, enter a date.</span></span>
4. <span data-ttu-id="5ae3e-136">[市場割引率] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ae3e-136">In the Market discount rate percentage field, enter a number.</span></span>
