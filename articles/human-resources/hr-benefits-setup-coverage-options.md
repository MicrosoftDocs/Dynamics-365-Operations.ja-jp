---
title: 補充オプションの作成
description: Microsoft Dynamics 365 Human Resources の補償オプションは、医療プランの場合は従業員のみ、生命保険プランの場合は 2 倍の給与など、計画またはプログラムでの参加者が選択する補償のレベルです。
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
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092709"
---
# <a name="create-coverage-options"></a><span data-ttu-id="21467-103">補充オプションの作成</span><span class="sxs-lookup"><span data-stu-id="21467-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="21467-104">Microsoft Dynamics 365 Human Resources の補償オプションは、医療プランの場合は従業員のみ、生命保険プランの場合は 2 倍の給与など、計画またはプログラムでの参加者が選択する補償のレベルです。</span><span class="sxs-lookup"><span data-stu-id="21467-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="21467-105">これを定義すると、給付金オプションは再利用可能になり、オプションを 1 つ以上のプランに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="21467-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="21467-106">補償オプションを定義したら、補償オプションを給付金計画タイプに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="21467-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="21467-107">そして計画タイプは、給付金計画またはプログラムに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="21467-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="21467-108">計画タイプに関連付けられた補償オプションは、その計画タイプで作成されたすべての計画で使用できます。</span><span class="sxs-lookup"><span data-stu-id="21467-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="21467-109">**給付金管理**ワーク スペースの**設定**で、**補償オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="21467-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="21467-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="21467-110">Select **New**.</span></span>

3. <span data-ttu-id="21467-111">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="21467-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="21467-112">フィールド</span><span class="sxs-lookup"><span data-stu-id="21467-112">Field</span></span> | <span data-ttu-id="21467-113">説明</span><span class="sxs-lookup"><span data-stu-id="21467-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="21467-114">**補償オプション**</span><span class="sxs-lookup"><span data-stu-id="21467-114">**Coverage option**</span></span> | <span data-ttu-id="21467-115">固有の補償オプション名。</span><span class="sxs-lookup"><span data-stu-id="21467-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="21467-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="21467-116">**Description**</span></span> | <span data-ttu-id="21467-117">補償オプションの説明。</span><span class="sxs-lookup"><span data-stu-id="21467-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="21467-118">**補償コード**</span><span class="sxs-lookup"><span data-stu-id="21467-118">**Coverage code**</span></span> | <span data-ttu-id="21467-119">補償コードは、対象となる各対象者タイプの最小額と最大額を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="21467-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="21467-120">補償コードは、補償対象者または計画タイプに許可される補償量を示します。</span><span class="sxs-lookup"><span data-stu-id="21467-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="21467-121">補償額は、金額またはパーセンテージで表すことができます。</span><span class="sxs-lookup"><span data-stu-id="21467-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="21467-122">例:</span><span class="sxs-lookup"><span data-stu-id="21467-122">For example:</span></span></br></br><span data-ttu-id="21467-123">- **Emp +** は資格を取得するために、従業員は 1 人の被扶養者を選択する必要があります (複数選択した場合、資格を失います)。</span><span class="sxs-lookup"><span data-stu-id="21467-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="21467-124">- **Emp + family** が資格を得るには、従業員が少なくとも 2 人の被扶養者を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="21467-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="21467-125">**最大数**</span><span class="sxs-lookup"><span data-stu-id="21467-125">**Maximum number**</span></span> | <span data-ttu-id="21467-126">被扶養者の最大数。</span><span class="sxs-lookup"><span data-stu-id="21467-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="21467-127">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="21467-127">**Status**</span></span> | <span data-ttu-id="21467-128">補償オプションのステータス。</span><span class="sxs-lookup"><span data-stu-id="21467-128">The status of the coverage option.</span></span> <span data-ttu-id="21467-129">補償オプションのステータスが無効に設定されている場合、計画タイプで補償オプションを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="21467-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="21467-130">**パーセンテージ**</span><span class="sxs-lookup"><span data-stu-id="21467-130">**Percent**</span></span> | <span data-ttu-id="21467-131">パーセント量。</span><span class="sxs-lookup"><span data-stu-id="21467-131">The percent amount.</span></span> <span data-ttu-id="21467-132">このフィールドは、補償コード フィールドで % x 給与が選択された場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="21467-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="21467-133">**除数**</span><span class="sxs-lookup"><span data-stu-id="21467-133">**Divisor**</span></span> | <span data-ttu-id="21467-134">補償コード % x 給与を選択するときに計算で使用する除数。</span><span class="sxs-lookup"><span data-stu-id="21467-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="21467-135">**最小パーセント**</span><span class="sxs-lookup"><span data-stu-id="21467-135">**Percent minimum**</span></span> | <span data-ttu-id="21467-136">パーセンテージ補償コードを選択した場合の最小パーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="21467-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="21467-137">**最大パーセント**</span><span class="sxs-lookup"><span data-stu-id="21467-137">**Percent maximum**</span></span> | <span data-ttu-id="21467-138">パーセンテージ補償コードを選択した場合の最大パーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="21467-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="21467-139">**個人担当者の適格性オプション**では、各補償オプションに適切な個人担当者の適格性オプションを付けます。</span><span class="sxs-lookup"><span data-stu-id="21467-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="21467-140">**セルフサービス**で、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="21467-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="21467-141">フィールド</span><span class="sxs-lookup"><span data-stu-id="21467-141">Field</span></span> | <span data-ttu-id="21467-142">説明</span><span class="sxs-lookup"><span data-stu-id="21467-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="21467-143">**従業員負担額の許可**</span><span class="sxs-lookup"><span data-stu-id="21467-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="21467-144">従業員が給付金を選択したときに、給付金セルフサービスの拠出額を変更できるようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="21467-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="21467-145">このチェック ボックスをオンにすると、システムは従業員が給付金サービスで入力した拠出額に基づいて給付金計画パラメータを計算します。</span><span class="sxs-lookup"><span data-stu-id="21467-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="21467-146">**従業員補償額の許可**</span><span class="sxs-lookup"><span data-stu-id="21467-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="21467-147">従業員が給付金を選択したときに、給付金セルフ サービスの補償額を変更できるようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="21467-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="21467-148">このチェック ボックスをオンにすると、システムは従業員が従業員セルフ サービスで入力した補償額に基づいて給付金計画パラメータを計算します。</span><span class="sxs-lookup"><span data-stu-id="21467-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="21467-149">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="21467-149">Select **Save**.</span></span> 
