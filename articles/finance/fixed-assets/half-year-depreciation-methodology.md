---
title: 半期の減価償却方法
description: このトピックでは、資産の事業供用年度時に 6 か月間の減価償却を計算する半年簡便法を使用して、固定資産の減価償却を計算する方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977242"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="3a992-103">半期の減価償却方法</span><span class="sxs-lookup"><span data-stu-id="3a992-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3a992-104">このトピックでは、半年簡便法を使用して減価償却を計算するために固定資産で使用される方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a992-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="3a992-105">半年簡便法では、資産の事業供用年度時に 6 か月間の減価償却を計算します。</span><span class="sxs-lookup"><span data-stu-id="3a992-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="3a992-106">減価償却方法の詳細については、[減価償却方法](Fixed-asset-depreciation-conventions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3a992-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="3a992-107">6 か月間の減価償却方法を使用する場合、システムは取得年度または資産の事業供用開始年度を使用して、その年度から 5 年の減価償却を計算してから、6 か月を追加します。</span><span class="sxs-lookup"><span data-stu-id="3a992-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="3a992-108">このプロセスを示すために、価格 50,000 円で取得され、2020 年 4 月に事業供用が開始された資産を考えてみます。</span><span class="sxs-lookup"><span data-stu-id="3a992-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="3a992-109">また、資産の耐用年数を 5 年間と仮定します。</span><span class="sxs-lookup"><span data-stu-id="3a992-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="3a992-110">事業供用の初年度は 2020 年 12 月に終了し、資産の 5 年の耐用年数の終了は 2024 年 12 月となります。</span><span class="sxs-lookup"><span data-stu-id="3a992-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="3a992-111">半期の減価償却方法では、資産の耐用年数に 6 か月が追加され、耐用年数の終了は 2025 年 6 月となります。</span><span class="sxs-lookup"><span data-stu-id="3a992-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="3a992-112">年次減価償却 50,000/5 = 10,000 月次減価償却 10,000/12 = 833.33</span><span class="sxs-lookup"><span data-stu-id="3a992-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="3a992-113">初年度減価償却 10,000/2 = 5,000、それ以降の月次減価償却 5,000/9 = 555.56</span><span class="sxs-lookup"><span data-stu-id="3a992-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="3a992-114">[![半期減価償却方法の減価償却スケジュール](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="3a992-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="3a992-115">半年簡便法によって追加された減価償却期間の延長は、減価償却のより正確な配賦を提供します。</span><span class="sxs-lookup"><span data-stu-id="3a992-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="3a992-116">半年簡便法では、減価償却がより均等になるため、損益計算書の報告に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3a992-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
