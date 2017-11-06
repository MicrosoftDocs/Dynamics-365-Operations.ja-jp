--- 
title: "増加償却パラメーターおよび転記プロファイルのコンフィギュレーション (日本)"
description: "日本では、加速償却は [レート係数]、[レートしきい値] および [計算方法] に基づいて計算されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
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
ms.openlocfilehash: f35317c41181834491f0efac05b023e635ee1577
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="configure-accelerated-depreciation-parameters-and-posting-profiles-japan"></a><span data-ttu-id="950c0-103">増加償却パラメーターおよび転記プロファイルのコンフィギュレーション (日本)</span><span class="sxs-lookup"><span data-stu-id="950c0-103">Configure accelerated depreciation parameters and posting profiles (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="950c0-104">日本では、加速償却は [レート係数]、[レートしきい値] および [計算方法] に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="950c0-104">For Japan, the accelerated depreciation is calculated based on Rate factor, Rate threshold and Calculation method.</span></span> <span data-ttu-id="950c0-105">これらのパラメーターは、加速償却ドキュメントで提供されています。</span><span class="sxs-lookup"><span data-stu-id="950c0-105">These parameters are available on the accelerated depreciation document.</span></span> <span data-ttu-id="950c0-106">これらを固定資産パラメーターでコンフィギュレーションすることで、加速償却ドキュメントに対する既定値が提供されます。</span><span class="sxs-lookup"><span data-stu-id="950c0-106">Configuring them on the fixed asset parameter can provide default values for the accelerated depreciation documents.</span></span> 



<span data-ttu-id="950c0-107">加速償却金額を転記するためには、最初に [加速償却] に対する [主勘定] と [相手勘定] を [固定資産転記プロファイル] でコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="950c0-107">In order to post the accelerated depreciation amounts, you must configure the Main account and Offset account for Accelerated depreciation in Fixed asset posting profile first.</span></span>



<span data-ttu-id="950c0-108">この手順では、加速償却パラメーターと転記プロファイルの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="950c0-108">This procedure walks you through setting up the accelerated depreciation parameters and posting profiles.</span></span>



<span data-ttu-id="950c0-109">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="950c0-109">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="950c0-110">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="950c0-110">This procedure was created using the demo data company JPMF.</span></span>


## <a name="configure-parameters-for-accelerated-depreciation"></a><span data-ttu-id="950c0-111">加速償却パラメータのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="950c0-111">Configure parameters for accelerated depreciation</span></span>
1. <span data-ttu-id="950c0-112">[固定資産] > [設定] > [固定資産パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="950c0-112">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="950c0-113">[減価償却] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="950c0-113">Expand or collapse the Depreciation section.</span></span>
3. <span data-ttu-id="950c0-114">[レート係数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="950c0-114">In the Rate factor field, enter a number.</span></span>
    * <span data-ttu-id="950c0-115">これが各加速償却ドキュメントに対する既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="950c0-115">This will provide a default value to each of the Accelerated depreciation documents.</span></span>  
4. <span data-ttu-id="950c0-116">[レートしきい値] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="950c0-116">In the Rate threshold field, enter a number.</span></span>
    * <span data-ttu-id="950c0-117">これが各加速償却ドキュメントに対する既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="950c0-117">This will provide a default value to each of the Accelerated depreciation documents.</span></span>  
    * <span data-ttu-id="950c0-118">どの既定式を使用して毎日の平均過剰使用量時間を計算するかを指定します。</span><span class="sxs-lookup"><span data-stu-id="950c0-118">Specify which default formula to use in calculating the daily average overuse hour.</span></span>  

## <a name="configure-a-posting-profile"></a><span data-ttu-id="950c0-119">転記プロファイルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="950c0-119">Configure a posting profile</span></span>
1. <span data-ttu-id="950c0-120">[固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="950c0-120">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="950c0-121">[加速償却] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="950c0-121">Expand or collapse the Accelerated depreciation section.</span></span>
    * <span data-ttu-id="950c0-122">[加速償却] に使用する [主勘定] と [相手勘定] を指定します。</span><span class="sxs-lookup"><span data-stu-id="950c0-122">Specify the Main account and Offset account to use for Accelerated depreciation.</span></span>  

