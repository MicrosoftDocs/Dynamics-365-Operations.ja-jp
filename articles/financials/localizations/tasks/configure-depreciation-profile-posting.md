--- 
title: "割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション (日本)"
description: "この手順を使用して、特別償却の減価償却プロファイルと転記プロファイルを構成する方法を説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c300f9cca6dd49c8fcafd972d250a801cf84672d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="configure-depreciation-profile-and-posting-profile-for-additional-depreciation-japan"></a><span data-ttu-id="c59bb-103">割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション (日本)</span><span class="sxs-lookup"><span data-stu-id="c59bb-103">Configure depreciation profile and posting profile for additional depreciation (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c59bb-104">この手順を使用して、特別償却の減価償却プロファイルと転記プロファイルを構成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-104">Use this procedure to learn how to configure a depreciation profile and a posting profile for special depreciation.</span></span>

<span data-ttu-id="c59bb-105">日本では、特定の条件下で特別償却が許可されます。</span><span class="sxs-lookup"><span data-stu-id="c59bb-105">In Japan, special depreciation is permitted under certain conditions.</span></span> <span data-ttu-id="c59bb-106">これは特別償却として扱われます。</span><span class="sxs-lookup"><span data-stu-id="c59bb-106">It is treated as extraordinary depreciation.</span></span> 

<span data-ttu-id="c59bb-107">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c59bb-107">In order to complete this procedure, the Fixed Assets configuration key must be selected.</span></span>

<span data-ttu-id="c59bb-108">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="c59bb-108">This procedure was created using the demo data company JPMF.</span></span>




## <a name="configure-a-depreciation-profile"></a><span data-ttu-id="c59bb-109">減価償却プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c59bb-109">Configure a depreciation profile</span></span>
1. <span data-ttu-id="c59bb-110">[固定資産] > [設定] > [減価償却プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-110">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="c59bb-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c59bb-111">Click New.</span></span>
3. <span data-ttu-id="c59bb-112">[減価償却プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-112">In the Depreciation profile field, type a value.</span></span>
4. <span data-ttu-id="c59bb-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c59bb-114">[方法] フィールドで、「特別償却」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-114">In the Method field, select 'Special depreciation'.</span></span>
6. <span data-ttu-id="c59bb-115">[会計方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-115">In the Accounting method field, select an option.</span></span>
    * <span data-ttu-id="c59bb-116">引当メソッドに [準備金] を選択し、仕分のダイレクト オフ メソッドにダイレクト オフを選択します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-116">Choose Reserve for reserve method, choose direct-off for direct off method for journalization.</span></span> <span data-ttu-id="c59bb-117">通常、財務諸表で推奨される表示方法は、引当メソッドです。</span><span class="sxs-lookup"><span data-stu-id="c59bb-117">Reserve method is usually a more preferred representation on the financial statement.</span></span>  
7. <span data-ttu-id="c59bb-118">[特別償却適用期間] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-118">In the Apply number of periods field, enter a number.</span></span>
8. <span data-ttu-id="c59bb-119">[基準取得価額割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-119">In the Base ratio field, enter a number.</span></span>
    * <span data-ttu-id="c59bb-120">100% として「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-120">Enter 1 for 100%.</span></span> <span data-ttu-id="c59bb-121">実際の値は固定資産によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c59bb-121">The actual value can vary depending on the fixed asset.</span></span>  
9. <span data-ttu-id="c59bb-122">[特別償却率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-122">In the Special depreciation rate field, enter a number.</span></span>
    * <span data-ttu-id="c59bb-123">特別減価償却額は、所得原価、基準取得価額割合、および特別減価償却率の結果として計算されます。</span><span class="sxs-lookup"><span data-stu-id="c59bb-123">The special depreciation amount is calculated as the product of Acquisition cost, Base ratio and Special depreciation rate.</span></span>  <span data-ttu-id="c59bb-124">30% として「0.3」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-124">Enter 0.3 for 30%.</span></span> <span data-ttu-id="c59bb-125">実際の値は固定資産によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c59bb-125">The actual value can vary depending on the fixed asset.</span></span>  
10. <span data-ttu-id="c59bb-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c59bb-126">Click Save.</span></span>

## <a name="configure-a-posting-profile"></a><span data-ttu-id="c59bb-127">転記プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c59bb-127">Configure a posting profile</span></span>
1. <span data-ttu-id="c59bb-128">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-128">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="c59bb-129">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c59bb-129">Click Edit.</span></span>
3. <span data-ttu-id="c59bb-130">[トランザクション タイプ] フィールドで「特別減価償却」を選択します。</span><span class="sxs-lookup"><span data-stu-id="c59bb-130">In the Transaction type field, select 'Extraordinary depreciation'.</span></span>
    * <span data-ttu-id="c59bb-131">特別償却は特別減価償却として転記されます。</span><span class="sxs-lookup"><span data-stu-id="c59bb-131">Special depreciation is posted as extraordinary depreciation.</span></span>  
    * <span data-ttu-id="c59bb-132">オプション: [主勘定] および [相手勘定] をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="c59bb-132">Optional: configure the Main account and Offset account.</span></span>  
    * <span data-ttu-id="c59bb-133">これらの勘定のフィールドを変更するためには [編集] をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c59bb-133">You must click Edit before you can modify these account fields.</span></span>  

