---
title: 割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション
description: この手順を使用して、特別償却の減価償却プロファイルと転記プロファイルを構成する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile,  AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30fde58554c23fec0f2a2ad4490615dd301190d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236668"
---
# <a name="configure-depreciation-profile-and-posting-profile-for-additional-depreciation"></a><span data-ttu-id="358a9-103">割増償却に対する減価償却プロファイルおよび転記プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="358a9-103">Configure depreciation profile and posting profile for additional depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="358a9-104">この手順を使用して、特別償却の減価償却プロファイルと転記プロファイルを構成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="358a9-104">Use this procedure to learn how to configure a depreciation profile and a posting profile for special depreciation.</span></span>

<span data-ttu-id="358a9-105">日本では、特定の条件下で特別償却が許可されます。</span><span class="sxs-lookup"><span data-stu-id="358a9-105">In Japan, special depreciation is permitted under certain conditions.</span></span> <span data-ttu-id="358a9-106">これは特別償却として扱われます。</span><span class="sxs-lookup"><span data-stu-id="358a9-106">It is treated as extraordinary depreciation.</span></span> 

<span data-ttu-id="358a9-107">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="358a9-107">In order to complete this procedure, the Fixed Assets configuration key must be selected.</span></span>

<span data-ttu-id="358a9-108">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="358a9-108">This procedure was created using the demo data company JPMF.</span></span>




## <a name="configure-a-depreciation-profile"></a><span data-ttu-id="358a9-109">減価償却プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="358a9-109">Configure a depreciation profile</span></span>
1. <span data-ttu-id="358a9-110">[固定資産] > [設定] > [減価償却プロファイル] に移動します。</span><span class="sxs-lookup"><span data-stu-id="358a9-110">Go to Fixed assets > Setup > Depreciation profiles.</span></span>
2. <span data-ttu-id="358a9-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="358a9-111">Click New.</span></span>
3. <span data-ttu-id="358a9-112">[減価償却プロファイル] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-112">In the Depreciation profile field, type a value.</span></span>
4. <span data-ttu-id="358a9-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="358a9-114">[方法] フィールドで、「特別償却」を選択します。</span><span class="sxs-lookup"><span data-stu-id="358a9-114">In the Method field, select 'Special depreciation'.</span></span>
6. <span data-ttu-id="358a9-115">[会計方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="358a9-115">In the Accounting method field, select an option.</span></span>
    * <span data-ttu-id="358a9-116">引当メソッドに [準備金] を選択し、仕分のダイレクト オフ メソッドにダイレクト オフを選択します。</span><span class="sxs-lookup"><span data-stu-id="358a9-116">Choose Reserve for reserve method, choose direct-off for direct off method for journalization.</span></span> <span data-ttu-id="358a9-117">通常、財務諸表で推奨される表示方法は、引当メソッドです。</span><span class="sxs-lookup"><span data-stu-id="358a9-117">Reserve method is usually a more preferred representation on the financial statement.</span></span>  
7. <span data-ttu-id="358a9-118">[特別償却適用期間] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-118">In the Apply number of periods field, enter a number.</span></span>
8. <span data-ttu-id="358a9-119">[基準取得価額割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-119">In the Base ratio field, enter a number.</span></span>
    * <span data-ttu-id="358a9-120">100% として「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-120">Enter 1 for 100%.</span></span> <span data-ttu-id="358a9-121">実際の値は固定資産によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="358a9-121">The actual value can vary depending on the fixed asset.</span></span>  
9. <span data-ttu-id="358a9-122">[特別償却率] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-122">In the Special depreciation rate field, enter a number.</span></span>
    * <span data-ttu-id="358a9-123">特別減価償却額は、所得原価、基準取得価額割合、および特別減価償却率の結果として計算されます。</span><span class="sxs-lookup"><span data-stu-id="358a9-123">The special depreciation amount is calculated as the product of Acquisition cost, Base ratio and Special depreciation rate.</span></span>  <span data-ttu-id="358a9-124">30% として「0.3」を入力します。</span><span class="sxs-lookup"><span data-stu-id="358a9-124">Enter 0.3 for 30%.</span></span> <span data-ttu-id="358a9-125">実際の値は固定資産によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="358a9-125">The actual value can vary depending on the fixed asset.</span></span>  
10. <span data-ttu-id="358a9-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="358a9-126">Click Save.</span></span>

## <a name="configure-a-posting-profile"></a><span data-ttu-id="358a9-127">転記プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="358a9-127">Configure a posting profile</span></span>
1. <span data-ttu-id="358a9-128">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="358a9-128">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="358a9-129">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="358a9-129">Click Edit.</span></span>
3. <span data-ttu-id="358a9-130">[トランザクション タイプ] フィールドで「特別減価償却」を選択します。</span><span class="sxs-lookup"><span data-stu-id="358a9-130">In the Transaction type field, select 'Extraordinary depreciation'.</span></span>
    * <span data-ttu-id="358a9-131">特別償却は特別減価償却として転記されます。</span><span class="sxs-lookup"><span data-stu-id="358a9-131">Special depreciation is posted as extraordinary depreciation.</span></span>  
    * <span data-ttu-id="358a9-132">オプション: [主勘定] および [相手勘定] をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="358a9-132">Optional: configure the Main account and Offset account.</span></span>  
    * <span data-ttu-id="358a9-133">これらの勘定のフィールドを変更するためには [編集] をクリックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="358a9-133">You must click Edit before you can modify these account fields.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]