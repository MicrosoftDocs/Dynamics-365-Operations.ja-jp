--- 
title: "品目再配賦の未処理ピッキングの設定"
description: "この手順では、倉庫の在庫が不十分な場合、倉庫従事者はどのようにすれば他の倉庫を素早く見つけることができるか説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="5b13f-103">品目再配賦の未処理ピッキングの設定</span><span class="sxs-lookup"><span data-stu-id="5b13f-103">Set up short picking item reallocation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b13f-104">この手順では、倉庫の在庫が不十分な場合、倉庫従事者はどのようにすれば他の倉庫を素早く見つけることができるか説明します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="5b13f-105">自動的な再配分をすることは可能で、他の場所が手配できる場合、製品を再配分させる指示があります。</span><span class="sxs-lookup"><span data-stu-id="5b13f-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="5b13f-106">また手動再配分を行う場合、有効数量の対応が可能な場所の一覧がモバイル端末に表示され、これにより倉庫従事者は在庫にはどの場所がよいか選択することができます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="5b13f-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="5b13f-108">この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="5b13f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="5b13f-109">作業例外を設定します</span><span class="sxs-lookup"><span data-stu-id="5b13f-109">Set up work exceptions</span></span>
1. <span data-ttu-id="5b13f-110">[倉庫管理] > [セットアップ] > [作業] > [例外作業] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="5b13f-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b13f-111">Click New.</span></span>
    * <span data-ttu-id="5b13f-112">倉庫従事者が処理している出荷のニーズに基づいて品目を選択できるよう、品目再配置ポリシーに複数の例外作業を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="5b13f-113">[例外作業コード] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="5b13f-114">例外作業の使途がわかるように例外作業にタイトルを付けます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="5b13f-115">たとえば、ショートピッキングに関するマニュアルなど。</span><span class="sxs-lookup"><span data-stu-id="5b13f-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="5b13f-116">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5b13f-117">[例外タイプ] のフィールドで、「ショートピック」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="5b13f-118">[在庫調整] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="5b13f-119">このオプションでは、在庫が簡単なピッキング場所の0に自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="5b13f-120">[既定の調整タイプコード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="5b13f-121">たとえば、USMFでは「 Res Adj Outを削除」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="5b13f-122">[品目再配置] フィールドで、「手作業」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="5b13f-123">手動または自動および手動を選択した場合、倉庫従事者は手動での再配分を実行できなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5b13f-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="5b13f-124">手作業による品目再配分を使用する作業者を設定します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="5b13f-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5b13f-125">Close the page.</span></span>
2. <span data-ttu-id="5b13f-126">[倉庫管理] > [セットアップ] > [作業者] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="5b13f-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5b13f-127">Click Edit.</span></span>
4. <span data-ttu-id="5b13f-128">リストで、[作業者 24] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="5b13f-129">作業セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-129">Expand the Work section.</span></span>
6. <span data-ttu-id="5b13f-130">[手動による再配置を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5b13f-130">Select Yes in the Allow manual item reallocation field.</span></span>

