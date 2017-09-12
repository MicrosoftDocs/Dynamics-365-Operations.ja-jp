---
title: "遅延"
description: "この記事は、マスタ プランの遅延日に関する情報を提供します。 遅延日は、マスター プランで計算される最も早い履行日が、要求日より後になる場合にトランザクションに設定される現実的な期日です。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db5c507fbc68e637dbbc4ef3311d1fbd298f24f
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="delays"></a><span data-ttu-id="81aa2-104">遅延</span><span class="sxs-lookup"><span data-stu-id="81aa2-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="81aa2-105">この記事は、マスタ プランの遅延日に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="81aa2-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="81aa2-106">遅延日は、マスター プランで計算される最も早い履行日が、要求日より後になる場合にトランザクションに設定される現実的な期日です。</span><span class="sxs-lookup"><span data-stu-id="81aa2-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="81aa2-107">マスター プランでは、リード タイム、材料の可用性、能力の利用可能性、計画のさまざまなパラメーターに基づいて、トランザクションの最も早い履行日を計算できます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="81aa2-108">マスター プランの計算で現在の日付より前の注文日付になった場合、注文を時間どおりに履行することはできません。</span><span class="sxs-lookup"><span data-stu-id="81aa2-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="81aa2-109">したがって、注文は遅延します。</span><span class="sxs-lookup"><span data-stu-id="81aa2-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="81aa2-110">この場合、マスター プランは、現在の日付からフォワード プランニングを行い、注文リード タイムを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="81aa2-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="81aa2-111">これらのリード タイムは、任意の下位レベルのコンポーネント品目から開始されます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="81aa2-112">その後、注文は、遅延日付を与えられます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-112">The order then receives a delayed date.</span></span> <span data-ttu-id="81aa2-113">遅延日は、現在のデータに基づく実際的な期日です。</span><span class="sxs-lookup"><span data-stu-id="81aa2-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="81aa2-114">マスター プランは、遅延日数の計算も行います。</span><span class="sxs-lookup"><span data-stu-id="81aa2-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="81aa2-115">代替の荷渡方法を選択してリード タイムを短縮できることをユーザーがわかっている場合など、状況によっては遅延を計算しないように選択することがあります。</span><span class="sxs-lookup"><span data-stu-id="81aa2-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="81aa2-116">補充グループに対して、遅延の計算方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="81aa2-117">その後、補充グループを品目に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="81aa2-118">**マスター プランのパラメーター**ページで、遅延計算の開始時刻を設定できます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="81aa2-119">この時刻以降に注文を履行する場合、注文の遅延日に 1 日が追加されます。</span><span class="sxs-lookup"><span data-stu-id="81aa2-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="81aa2-120">**注記:** 以前のバージョンでは、計算済遅延は*計画メッセージ*、遅延日は*計画期日*、遅延トランザクションは*計画設定済のトランザクション*と呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="81aa2-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="81aa2-121">参照</span><span class="sxs-lookup"><span data-stu-id="81aa2-121">See also</span></span>
--------

[<span data-ttu-id="81aa2-122">補充設定</span><span class="sxs-lookup"><span data-stu-id="81aa2-122">Coverage settings</span></span>](coverage-settings.md)




