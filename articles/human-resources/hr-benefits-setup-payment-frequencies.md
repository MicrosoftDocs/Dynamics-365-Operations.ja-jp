---
title: 支払頻度の設定
description: Microsoft Dynamics 365 Human Resources は、支払頻度を使用して年間給付金給与を計算し、従業員が各支払期間に支払う給付金割増金額とプロバイダーに支払われる頻度を決定します。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a6a638cee08f77ca21f6301730a64102b734887
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793780"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="49359-103">支払頻度の設定</span><span class="sxs-lookup"><span data-stu-id="49359-103">Set up payment frequencies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="49359-104">Microsoft Dynamics 365 Human Resources は、支払頻度を使用して年間給付金給与を計算し、従業員が各支払期間に支払う給付金割増金額とプロバイダーに支払われる頻度を決定します。</span><span class="sxs-lookup"><span data-stu-id="49359-104">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and how often providers are paid.</span></span>

<span data-ttu-id="49359-105">給付金支払頻度は、換算率を使用して毎月、半月毎、隔週毎、毎週、および毎日の支払頻度を給付金支払期間に変換します。</span><span class="sxs-lookup"><span data-stu-id="49359-105">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="49359-106">これにより、会社は給付金プラン内の支払頻度の間で相互依存関係を定義できます。</span><span class="sxs-lookup"><span data-stu-id="49359-106">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="49359-107">換算率フィールドでは、支払頻度から標準支払期間への換算率を識別し、システムが支払頻度間の計算を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="49359-107">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="49359-108">換算率の金額は、従業員が各支払頻度に支払う必要がある給付金割増金額も決定します。</span><span class="sxs-lookup"><span data-stu-id="49359-108">The conversion factor amount also determines the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="49359-109">**給付金管理** ワーク スペースの **設定** で、**支払頻度** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49359-109">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="49359-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49359-110">Select **New**.</span></span>

3. <span data-ttu-id="49359-111">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="49359-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="49359-112">フィールド</span><span class="sxs-lookup"><span data-stu-id="49359-112">Field</span></span> | <span data-ttu-id="49359-113">説明</span><span class="sxs-lookup"><span data-stu-id="49359-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="49359-114">**支払頻度**</span><span class="sxs-lookup"><span data-stu-id="49359-114">**Payment frequency**</span></span> | <span data-ttu-id="49359-115">支払頻度の一意名。</span><span class="sxs-lookup"><span data-stu-id="49359-115">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="49359-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="49359-116">**Description**</span></span> | <span data-ttu-id="49359-117">支払頻度の説明。</span><span class="sxs-lookup"><span data-stu-id="49359-117">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="49359-118">**期間**</span><span class="sxs-lookup"><span data-stu-id="49359-118">**Period**</span></span> | <span data-ttu-id="49359-119">給付金プロバイダーおよび従業員の支払頻度に最も一致する適切な期間。</span><span class="sxs-lookup"><span data-stu-id="49359-119">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="49359-120">期間リストは、標準支払期間で作成されます。</span><span class="sxs-lookup"><span data-stu-id="49359-120">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="49359-121">**支払い期間数**</span><span class="sxs-lookup"><span data-stu-id="49359-121">**Number of pay periods**</span></span> | <span data-ttu-id="49359-122">支払期間数は給付金プロバイダーまたは従業員に支払われる頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="49359-122">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="49359-123">この金額は、従業員の年間給付金給与金額を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="49359-123">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="49359-124">**年次の変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-124">**Annual conversion factor**</span></span> | <span data-ttu-id="49359-125">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-125">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-126">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-126">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-127">(12 か月の支払 / 1 年) = 12</span><span class="sxs-lookup"><span data-stu-id="49359-127">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="49359-128">**半年ごとの変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-128">**Semiannual conversion factor**</span></span> | <span data-ttu-id="49359-129">半年毎の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-129">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-130">たとえば、月次支払頻度の半年毎の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-130">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-131">(12 か月の支払 / 年 2 回) = 6</span><span class="sxs-lookup"><span data-stu-id="49359-131">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="49359-132">**四半期ごとの変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-132">**Quarterly conversion factor**</span></span> | <span data-ttu-id="49359-133">四半期の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-133">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-134">たとえば、月次支払頻度の四半期ごとの変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-134">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-135">(12 か月の支払 / 四半期の 4 期分) = 3</span><span class="sxs-lookup"><span data-stu-id="49359-135">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="49359-136">**月次の変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-136">**Monthly conversion factor**</span></span> | <span data-ttu-id="49359-137">支払頻度の毎月の変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-137">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-138">たとえば、月次支払頻度の毎月の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-138">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-139">(12 か月の支払 / 12 か月) = 1</span><span class="sxs-lookup"><span data-stu-id="49359-139">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="49359-140">**半月ごとの変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-140">**Semimonthly conversion factor**</span></span> | <span data-ttu-id="49359-141">半月毎の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-141">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-142">たとえば、月次支払頻度の半月毎の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-142">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-143">(12 か月の支払 / 24 (月 2 回)) = 0.5</span><span class="sxs-lookup"><span data-stu-id="49359-143">(12 monthly payments / 24 (2x a month)) = 0.5</span></span> | 
   | <span data-ttu-id="49359-144">**隔週の変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-144">**Biweekly conversion factor**</span></span> | <span data-ttu-id="49359-145">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-145">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-146">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-146">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-147">(12 か月の支払 / 26 週間) = 0.461538</span><span class="sxs-lookup"><span data-stu-id="49359-147">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="49359-148">**週次の変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-148">**Weekly conversion factor**</span></span> | <span data-ttu-id="49359-149">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-149">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-150">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-150">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-151">(12 か月の支払 / 52 週間) = 0.230769</span><span class="sxs-lookup"><span data-stu-id="49359-151">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="49359-152">**日次の変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-152">**Daily conversion factor**</span></span> | <span data-ttu-id="49359-153">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-153">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-154">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-154">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-155">(12 か月の支払 / 365 日) = 0.032877</span><span class="sxs-lookup"><span data-stu-id="49359-155">(12 monthly payments / 365 days) = 0.032877</span></span> |
   | <span data-ttu-id="49359-156">**時間ごとの変換係数**</span><span class="sxs-lookup"><span data-stu-id="49359-156">**Hourly conversion factor**</span></span> | <span data-ttu-id="49359-157">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="49359-157">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="49359-158">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="49359-158">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="49359-159">(12 か月の支払 / 2080 時間) = 0.005769</span><span class="sxs-lookup"><span data-stu-id="49359-159">(12 monthly payments / 2080 hours) = 0.005769</span></span>

4. <span data-ttu-id="49359-160">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="49359-160">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]