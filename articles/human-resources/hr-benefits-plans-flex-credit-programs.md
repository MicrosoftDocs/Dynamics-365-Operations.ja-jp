---
title: フレックス クレジット プログラムの設定
description: Microsoft Dynamics 365 Human Resources のフレックス クレジット プログラムを使用して、所定のフレックス クレジットの数に応じて従業員を給付金に登録できます。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: be5b845337f2ac0ec608b48c209abd36443e7b89
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805757"
---
# <a name="set-up-flex-credit-programs"></a><span data-ttu-id="3dc72-103">フレックス クレジット プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="3dc72-103">Set up flex credit programs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3dc72-104">Microsoft Dynamics 365 Human Resources のフレックス クレジット プログラムを使用して、所定のフレックス クレジットの数に応じて従業員を給付金に登録できます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-104">You can use flex credit programs in Microsoft Dynamics 365 Human Resources to enroll employees in benefits according to a predetermined number of flex credits.</span></span> <span data-ttu-id="3dc72-105">従業員は、フレックス クレジットの配賦方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-105">Employees can choose how to allocate their flex credits.</span></span> <span data-ttu-id="3dc72-106">たとえば、ある従業員が配偶者の健康保険プランでカバーされている場合、他の給付金に対して使用の可能性があるクレジットを使うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3dc72-106">For example, if an employee is covered under their spouse’s health insurance plan, they may want to use the credits they would have otherwise used on health coverage toward other benefits.</span></span> 

1. <span data-ttu-id="3dc72-107">**給付金管理** ワーク スペースの **プラン** で、**フレックス クレジット プログラム** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc72-107">In the **Benefits management** workspace, under **Plans**, select **Flex credit programs**.</span></span>

2. <span data-ttu-id="3dc72-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc72-108">Select **New**.</span></span>

3. <span data-ttu-id="3dc72-109">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3dc72-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3dc72-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="3dc72-110">Field</span></span> | <span data-ttu-id="3dc72-111">説明</span><span class="sxs-lookup"><span data-stu-id="3dc72-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3dc72-112">**給付金クレジット ID**</span><span class="sxs-lookup"><span data-stu-id="3dc72-112">**Benefit credit ID**</span></span> | <span data-ttu-id="3dc72-113">フレックス クレジット プログラムの固有 ID。</span><span class="sxs-lookup"><span data-stu-id="3dc72-113">The unique identifier of the flex credit program.</span></span> |
   | <span data-ttu-id="3dc72-114">**説明**</span><span class="sxs-lookup"><span data-stu-id="3dc72-114">**Description**</span></span> | <span data-ttu-id="3dc72-115">フレックス クレジット プログラムの説明。</span><span class="sxs-lookup"><span data-stu-id="3dc72-115">A description of the flex credit program.</span></span> | 
   | <span data-ttu-id="3dc72-116">**自**</span><span class="sxs-lookup"><span data-stu-id="3dc72-116">**From date**</span></span> | <span data-ttu-id="3dc72-117">フレックス クレジット プログラムがアクティブになる日付。</span><span class="sxs-lookup"><span data-stu-id="3dc72-117">The date the flex credit program becomes active.</span></span> |
   | <span data-ttu-id="3dc72-118">**至**</span><span class="sxs-lookup"><span data-stu-id="3dc72-118">**To date**</span></span> | <span data-ttu-id="3dc72-119">フレックス クレジット プログラムの終了日。</span><span class="sxs-lookup"><span data-stu-id="3dc72-119">The end date of the flex credit program.</span></span> <span data-ttu-id="3dc72-120">既定値 (12/31/2154) をそのまま使用すると、フレックス クレジット プログラムの有効期限がスケジュールされていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="3dc72-120">You can leave the default value (12/31/2154) to indicate that the flex credit program doesn’t have a scheduled expiration.</span></span> |
   | <span data-ttu-id="3dc72-121">**合計クレジット値**</span><span class="sxs-lookup"><span data-stu-id="3dc72-121">**Total credit value**</span></span> | <span data-ttu-id="3dc72-122">各従業員が給付金に対して使用する必要があるクレジット数。</span><span class="sxs-lookup"><span data-stu-id="3dc72-122">The number of credits each employee will have to use for their benefits.</span></span> |
   | <span data-ttu-id="3dc72-123">**比例配分ルール**</span><span class="sxs-lookup"><span data-stu-id="3dc72-123">**Prorate rule**</span></span> | <span data-ttu-id="3dc72-124">従業員がフレックス クレジット期間の中間に雇用された場合に、比例配分のフレックス クレジットに使用するルール。</span><span class="sxs-lookup"><span data-stu-id="3dc72-124">The rule to use for prorating flex credits when an employee is hired in the middle of the flex credit period.</span></span> </br></br><ul><li><span data-ttu-id="3dc72-125">**なし** – フレックス クレジット期間の開始後に雇用された場合、従業員はフレックス クレジットを受け取りません。</span><span class="sxs-lookup"><span data-stu-id="3dc72-125">**None** – The employee receives no flex credits if they are hired after the flex credit program period begins.</span></span></li><li><span data-ttu-id="3dc72-126">**フル クレジット** – 雇用された時期に関係なく、従業員はフレックス クレジットの全額を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3dc72-126">**Full credit** – The employee receives the full amount of flex credits, regardless of when they are hired.</span></span></li><li><span data-ttu-id="3dc72-127">**比例配分** – 開始日に基づいて、従業員はフレックス クレジットの比例配分を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="3dc72-127">**Prorate** – The employee receives a prorated amount of flex credits based on their start date.</span></span></li></ul> |
   | <span data-ttu-id="3dc72-128">**フレックス クレジット比例配分式**</span><span class="sxs-lookup"><span data-stu-id="3dc72-128">**Flex credit prorate formula**</span></span> | <span data-ttu-id="3dc72-129">フレックス クレジット プログラムの給付金期間の中間に、雇用された従業員に対する比例配分のフレックス クレジットに使用するルール。</span><span class="sxs-lookup"><span data-stu-id="3dc72-129">The rule to use for prorating flex credits for employees who are hired in the middle of a benefit period for the flex credit program.</span></span> <span data-ttu-id="3dc72-130">比例配分は、従業員の雇用開始日に基づきます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-130">The proration is based on the employment start date.</span></span> <span data-ttu-id="3dc72-131">このフィールドは、**比例配分ルール** フィールドの **比例配分** を選択した場合のみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-131">This field is only used if you select **Prorate** in the **Prorate rule** field.</span></span> </br></br><ul><li><span data-ttu-id="3dc72-132">**毎日** – 従業員が日付レベルに対して受け取るフレックス クレジット数を比例配分。</span><span class="sxs-lookup"><span data-stu-id="3dc72-132">**Daily** – Prorates the number of flex credits an employee receives to the day level.</span></span> <span data-ttu-id="3dc72-133">フレックス クレジットの合計数は、期間の日数で除算されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-133">The total number of flex credits is divided by the number of days in the period.</span></span> <span data-ttu-id="3dc72-134">たとえば、給付期間が 400 日である場合、フレックス クレジットの合計数が 400 に分割され、1 日あたりに入庫するフレックス クレジットの数が計算されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-134">For example, if your benefit period is 400 days, the system will divide the total number of flex credits by 400 to calculate the number of flex credits employees receive per day.</span></span></li><li><span data-ttu-id="3dc72-135">**当月** – 従業員が当月に丸められた月レベルに受け取るフレックス クレジットの数値を比例配分。</span><span class="sxs-lookup"><span data-stu-id="3dc72-135">**Current month** – Prorates the number of flex credits an employee receives to the month level, rounded to the current month.</span></span> <span data-ttu-id="3dc72-136">フレックス クレジットの合計数は、期間の月数で除算されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-136">The total number of flex credits is divided by the number of months in the period.</span></span> <span data-ttu-id="3dc72-137">たとえば、給付期間が 15 月である場合、フレックス クレジットの合計数が 15 ごとに分割され、月あたりに入庫するフレックス クレジットの数が計算されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-137">For example, if your benefit period is 15 months, the system will divide the total number of flex credits by 15 to calculate the number of flex credits employees receive per month.</span></span></li><li><span data-ttu-id="3dc72-138">**翌月** – 従業員が翌月に丸められた月レベルに受け取るフレックス クレジットの数値を比例配分。</span><span class="sxs-lookup"><span data-stu-id="3dc72-138">**Following month** – Prorates the number of flex credits an employee receives to the month level, rounded to the next month.</span></span> <span data-ttu-id="3dc72-139">フレックス クレジットの合計数は、期間の月数で除算されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-139">The total number of flex credits is divided by the number of months in the period.</span></span> <span data-ttu-id="3dc72-140">たとえば、給付期間が 15 月である場合、フレックス クレジットの合計数が 15 で分割され、月あたりに入庫するフレックス クレジットの数が計算されます。</span><span class="sxs-lookup"><span data-stu-id="3dc72-140">For example, if your benefit period is 15 months, the system divides the total number of flex credits by 15 to calculate the number of flex credits employees receive per month.</span></span></li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]