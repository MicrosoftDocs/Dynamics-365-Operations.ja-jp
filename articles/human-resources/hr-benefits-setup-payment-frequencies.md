---
title: 支払頻度の設定
description: Microsoft Dynamics 365 Human Resources は、支払頻度を使用して年間給付金給与を計算し、従業員が各支払期間に支払う給付金割増金額を決定し、支払いがプロバイダーに行われる頻度を定義します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b786485ab53dcdb3b7e5ff02562f674a7f8e6eae
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092594"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="52fac-103">支払頻度の設定</span><span class="sxs-lookup"><span data-stu-id="52fac-103">Set up payment frequencies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="52fac-104">Microsoft Dynamics 365 Human Resources は、支払頻度を使用して年間給付金給与を計算し、従業員が各支払期間に支払う給付金割増金額を決定し、支払いがプロバイダーに行われる頻度を定義します。</span><span class="sxs-lookup"><span data-stu-id="52fac-104">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and define the frequency payments are made to providers.</span></span>

<span data-ttu-id="52fac-105">給付金支払頻度は、換算率を使用して毎月、半月毎、隔週毎、毎週、および毎日の支払頻度を給付金支払期間に変換します。</span><span class="sxs-lookup"><span data-stu-id="52fac-105">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="52fac-106">これにより、会社は給付金プラン内の支払頻度の間で相互依存関係を定義できます。</span><span class="sxs-lookup"><span data-stu-id="52fac-106">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="52fac-107">換算率フィールドでは、支払頻度から標準支払期間への換算率を識別し、システムが支払頻度間の計算を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="52fac-107">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="52fac-108">換算率の金額は、従業員が各支払頻度に支払う必要がある給付金割増金額を決定するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="52fac-108">The conversion factor amount is also used to determine the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="52fac-109">**給付金管理**ワーク スペースの**設定**で、**支払頻度**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52fac-109">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="52fac-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52fac-110">Select **New**.</span></span>

3. <span data-ttu-id="52fac-111">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="52fac-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="52fac-112">フィールド</span><span class="sxs-lookup"><span data-stu-id="52fac-112">Field</span></span> | <span data-ttu-id="52fac-113">説明</span><span class="sxs-lookup"><span data-stu-id="52fac-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="52fac-114">支払頻度</span><span class="sxs-lookup"><span data-stu-id="52fac-114">Payment frequency</span></span> | <span data-ttu-id="52fac-115">支払頻度の一意名。</span><span class="sxs-lookup"><span data-stu-id="52fac-115">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="52fac-116">説明</span><span class="sxs-lookup"><span data-stu-id="52fac-116">Description</span></span> | <span data-ttu-id="52fac-117">支払頻度の説明。</span><span class="sxs-lookup"><span data-stu-id="52fac-117">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="52fac-118">期間</span><span class="sxs-lookup"><span data-stu-id="52fac-118">Period</span></span> | <span data-ttu-id="52fac-119">給付金プロバイダーおよび従業員の支払頻度に最も一致する適切な期間。</span><span class="sxs-lookup"><span data-stu-id="52fac-119">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="52fac-120">期間リストは、標準支払期間で作成されます。</span><span class="sxs-lookup"><span data-stu-id="52fac-120">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="52fac-121">支払い期間数</span><span class="sxs-lookup"><span data-stu-id="52fac-121">Number of pay periods</span></span> | <span data-ttu-id="52fac-122">支払期間数は給付金プロバイダーまたは従業員に支払われる頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="52fac-122">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="52fac-123">この金額は、従業員の年間給付金給与金額を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="52fac-123">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="52fac-124">年次の変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-124">Annual conversion factor</span></span> | <span data-ttu-id="52fac-125">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-125">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-126">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-126">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-127">(12 か月の支払 / 1 年) = 12</span><span class="sxs-lookup"><span data-stu-id="52fac-127">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="52fac-128">半年ごとの変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-128">Semiannual conversion factor</span></span> | <span data-ttu-id="52fac-129">半年毎の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-129">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-130">たとえば、月次支払頻度の半年毎の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-130">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-131">(12 か月の支払 / 年 2 回) = 6</span><span class="sxs-lookup"><span data-stu-id="52fac-131">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="52fac-132">四半期ごとの変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-132">Quarterly conversion factor</span></span> | <span data-ttu-id="52fac-133">四半期の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-133">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-134">たとえば、月次支払頻度の四半期ごとの変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-134">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-135">(12 か月の支払 / 四半期の 4 期分) = 3</span><span class="sxs-lookup"><span data-stu-id="52fac-135">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="52fac-136">月次の変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-136">Monthly conversion factor</span></span> | <span data-ttu-id="52fac-137">支払頻度の毎月の変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-137">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-138">たとえば、月次支払頻度の毎月の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-138">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-139">(12 か月の支払 / 12 か月) = 1</span><span class="sxs-lookup"><span data-stu-id="52fac-139">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="52fac-140">半月ごとの変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-140">Semimonthly conversion factor</span></span> | <span data-ttu-id="52fac-141">半月毎の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-141">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-142">たとえば、月次支払頻度の半月毎の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-142">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-143">(12 か月の支払 / 24 (月 2 回)) = .5</span><span class="sxs-lookup"><span data-stu-id="52fac-143">(12 monthly payments / 24 (2x a month)) = .5</span></span> | 
   | <span data-ttu-id="52fac-144">隔週の変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-144">Biweekly conversion factor</span></span> | <span data-ttu-id="52fac-145">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-145">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-146">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-146">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-147">(12 か月の支払 / 26 週間) = 0.461538</span><span class="sxs-lookup"><span data-stu-id="52fac-147">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="52fac-148">週次の変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-148">Weekly conversion factor</span></span> | <span data-ttu-id="52fac-149">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-149">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-150">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-150">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-151">(12 か月の支払 / 52 週間) = 0.230769</span><span class="sxs-lookup"><span data-stu-id="52fac-151">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="52fac-152">日次の変換係数</span><span class="sxs-lookup"><span data-stu-id="52fac-152">Daily conversion factor</span></span> | <span data-ttu-id="52fac-153">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="52fac-153">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="52fac-154">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="52fac-154">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="52fac-155">(12 か月の支払 / 365 日) = 0.032877</span><span class="sxs-lookup"><span data-stu-id="52fac-155">(12 monthly payments / 365 days) = 0.032877</span></span> |

4. <span data-ttu-id="52fac-156">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52fac-156">Select **Save**.</span></span> 
