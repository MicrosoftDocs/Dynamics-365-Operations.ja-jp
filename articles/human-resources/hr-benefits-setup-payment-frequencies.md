---
title: 支払頻度の設定
description: ''
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
ms.openlocfilehash: e5fe0a16c4abbb9241fcdac88fd56e92bf04788c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009733"
---
# <a name="set-up-payment-frequencies"></a><span data-ttu-id="3d7cf-102">支払頻度の設定</span><span class="sxs-lookup"><span data-stu-id="3d7cf-102">Set up payment frequencies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3d7cf-103">Microsoft Dynamics 365 Human Resources は、支払頻度を使用して年間給付金給与を計算し、従業員が各支払期間に支払う給付金割増金額を決定し、支払いがプロバイダーに行われる頻度を定義します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-103">Microsoft Dynamics 365 Human Resources uses payment frequencies to calculate the annual benefit salary, determine the benefit premium amount an employee pays each pay period, and define the frequency payments are made to providers.</span></span>

<span data-ttu-id="3d7cf-104">給付金支払頻度は、換算率を使用して毎月、半月毎、隔週毎、毎週、および毎日の支払頻度を給付金支払期間に変換します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-104">Benefit payment frequencies use conversion factors to convert benefit payment periods between monthly, semi-monthly, biweekly, weekly, and daily payment frequencies.</span></span> <span data-ttu-id="3d7cf-105">これにより、会社は給付金プラン内の支払頻度の間で相互依存関係を定義できます。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-105">This allows companies to define the interdependence between the payment frequencies within a benefit plan.</span></span>

<span data-ttu-id="3d7cf-106">換算率フィールドでは、支払頻度から標準支払期間への換算率を識別し、システムが支払頻度間の計算を行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-106">The conversion factors fields identify the conversion factor from the payment frequency to the standard payment periods and allow the system to do calculations between payment frequencies.</span></span> <span data-ttu-id="3d7cf-107">換算率の金額は、従業員が各支払頻度に支払う必要がある給付金割増金額を決定するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-107">The conversion factor amount is also used to determine the benefit premium amount that an employee should pay each pay frequency.</span></span>

1. <span data-ttu-id="3d7cf-108">**給付金管理**ワーク スペースの**設定**で、**支払頻度**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-108">In the **Benefits management** workspace, under **Setup**, select **Payment frequencies**.</span></span>

2. <span data-ttu-id="3d7cf-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-109">Select **New**.</span></span>

3. <span data-ttu-id="3d7cf-110">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3d7cf-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="3d7cf-111">Field</span></span> | <span data-ttu-id="3d7cf-112">説明</span><span class="sxs-lookup"><span data-stu-id="3d7cf-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3d7cf-113">支払頻度</span><span class="sxs-lookup"><span data-stu-id="3d7cf-113">Payment frequency</span></span> | <span data-ttu-id="3d7cf-114">支払頻度の一意名。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-114">A unique payment frequency name.</span></span> |
   | <span data-ttu-id="3d7cf-115">説明</span><span class="sxs-lookup"><span data-stu-id="3d7cf-115">Description</span></span> | <span data-ttu-id="3d7cf-116">支払頻度の説明。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-116">A description of the payment frequency.</span></span> |
   | <span data-ttu-id="3d7cf-117">期間</span><span class="sxs-lookup"><span data-stu-id="3d7cf-117">Period</span></span> | <span data-ttu-id="3d7cf-118">給付金プロバイダーおよび従業員の支払頻度に最も一致する適切な期間。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-118">The appropriate period that best matches the benefit provider’s and employee’s payment frequency.</span></span> <span data-ttu-id="3d7cf-119">期間リストは、標準支払期間で作成されます。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-119">The period list is composed of the standard payment periods.</span></span> |
   | <span data-ttu-id="3d7cf-120">支払い期間数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-120">Number of pay periods</span></span> | <span data-ttu-id="3d7cf-121">支払期間数は給付金プロバイダーまたは従業員に支払われる頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-121">The number of pay periods that represents how often the benefit provider or employees are paid.</span></span> <span data-ttu-id="3d7cf-122">この金額は、従業員の年間給付金給与金額を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-122">This amount will be used to calculate the employee‘s annual benefit salary amount.</span></span> |
   | <span data-ttu-id="3d7cf-123">年次の変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-123">Annual conversion factor</span></span> | <span data-ttu-id="3d7cf-124">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-124">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-125">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-125">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-126">(12 か月の支払 / 1 年) = 12</span><span class="sxs-lookup"><span data-stu-id="3d7cf-126">(12 monthly payments / 1 year) = 12</span></span> |
   | <span data-ttu-id="3d7cf-127">半年ごとの変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-127">Semiannual conversion factor</span></span> | <span data-ttu-id="3d7cf-128">半年毎の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-128">The semiannual conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-129">たとえば、月次支払頻度の半年毎の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-129">For example, the semiannual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-130">(12 か月の支払 / 年 2 回) = 6</span><span class="sxs-lookup"><span data-stu-id="3d7cf-130">(12 monthly payments / 2 times a year) = 6</span></span> |
   | <span data-ttu-id="3d7cf-131">四半期ごとの変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-131">Quarterly conversion factor</span></span> | <span data-ttu-id="3d7cf-132">四半期の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-132">The quarterly conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-133">たとえば、月次支払頻度の四半期ごとの変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-133">For example, the quarterly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-134">(12 か月の支払 / 四半期の 4 期分) = 3</span><span class="sxs-lookup"><span data-stu-id="3d7cf-134">(12 monthly payments / 4 quarters) = 3</span></span> |
   | <span data-ttu-id="3d7cf-135">月次の変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-135">Monthly conversion factor</span></span> | <span data-ttu-id="3d7cf-136">支払頻度の毎月の変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-136">The monthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-137">たとえば、月次支払頻度の毎月の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-137">For example, the monthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-138">(12 か月の支払 / 12 か月) = 1</span><span class="sxs-lookup"><span data-stu-id="3d7cf-138">(12 monthly payments / 12 months) = 1</span></span> |
   | <span data-ttu-id="3d7cf-139">半月ごとの変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-139">Semimonthly conversion factor</span></span> | <span data-ttu-id="3d7cf-140">半月毎の支払頻度の変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-140">The semimonthly conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-141">たとえば、月次支払頻度の半月毎の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-141">For example, the semimonthly conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-142">(12 か月の支払 / 24 (月 2 回)) = .5</span><span class="sxs-lookup"><span data-stu-id="3d7cf-142">(12 monthly payments / 24 (2x a month)) = .5</span></span> | 
   | <span data-ttu-id="3d7cf-143">隔週の変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-143">Biweekly conversion factor</span></span> | <span data-ttu-id="3d7cf-144">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-144">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-145">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-145">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-146">(12 か月の支払 / 26 週間) = 0.461538</span><span class="sxs-lookup"><span data-stu-id="3d7cf-146">(12 monthly payments / 26 weeks) = 0.461538</span></span> |
   | <span data-ttu-id="3d7cf-147">週次の変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-147">Weekly conversion factor</span></span> | <span data-ttu-id="3d7cf-148">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-148">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-149">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-149">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-150">(12 か月の支払 / 52 週間) = 0.230769</span><span class="sxs-lookup"><span data-stu-id="3d7cf-150">(12 monthly payments / 52 weeks) = 0.230769</span></span> |
   | <span data-ttu-id="3d7cf-151">日次の変換係数</span><span class="sxs-lookup"><span data-stu-id="3d7cf-151">Daily conversion factor</span></span> | <span data-ttu-id="3d7cf-152">支払頻度の年間変換率。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-152">The annual conversion factor for the payment frequency.</span></span> <span data-ttu-id="3d7cf-153">たとえば、月次支払頻度の年間の変換率は次のようになります:</span><span class="sxs-lookup"><span data-stu-id="3d7cf-153">For example, the annual conversion factor for the monthly pay frequency is:</span></span> </br></br><span data-ttu-id="3d7cf-154">(12 か月の支払 / 365 日) = 0.032877</span><span class="sxs-lookup"><span data-stu-id="3d7cf-154">(12 monthly payments / 365 days) = 0.032877</span></span> |

4. <span data-ttu-id="3d7cf-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d7cf-155">Select **Save**.</span></span> 
