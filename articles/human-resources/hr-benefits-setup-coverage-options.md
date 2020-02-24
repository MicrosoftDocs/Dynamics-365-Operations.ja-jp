---
title: 補償オプションを作成する
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009620"
---
# <a name="create-coverage-options"></a><span data-ttu-id="a76a2-102">補償オプションを作成する</span><span class="sxs-lookup"><span data-stu-id="a76a2-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a76a2-103">Microsoft Dynamics 365 Human Resources の補償オプションは、医療プランの場合は従業員のみ、生命保険プランの場合は 2 倍の給与など、計画またはプログラムでの参加者が選択する補償のレベルです。</span><span class="sxs-lookup"><span data-stu-id="a76a2-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="a76a2-104">これを定義すると、給付金オプションは再利用可能になり、オプションを 1 つ以上のプランに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="a76a2-105">補償オプションを定義したら、補償オプションを給付金計画タイプに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="a76a2-106">そして計画タイプは、給付金計画またはプログラムに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="a76a2-107">計画タイプに関連付けられた補償オプションは、その計画タイプで作成されたすべての計画で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="a76a2-108">**給付金管理**ワーク スペースの**設定**で、**補償オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="a76a2-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-109">Select **New**.</span></span>

3. <span data-ttu-id="a76a2-110">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="a76a2-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="a76a2-111">Field</span></span> | <span data-ttu-id="a76a2-112">説明</span><span class="sxs-lookup"><span data-stu-id="a76a2-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a76a2-113">**補償オプション**</span><span class="sxs-lookup"><span data-stu-id="a76a2-113">**Coverage option**</span></span> | <span data-ttu-id="a76a2-114">固有の補償オプション名。</span><span class="sxs-lookup"><span data-stu-id="a76a2-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="a76a2-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="a76a2-115">**Description**</span></span> | <span data-ttu-id="a76a2-116">補償オプションの説明。</span><span class="sxs-lookup"><span data-stu-id="a76a2-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="a76a2-117">**補償コード**</span><span class="sxs-lookup"><span data-stu-id="a76a2-117">**Coverage code**</span></span> | <span data-ttu-id="a76a2-118">補償コードは、対象となる各対象者タイプの最小額と最大額を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="a76a2-119">補償コードは、補償対象者または計画タイプに許可される補償量を示します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="a76a2-120">補償額は、金額またはパーセンテージで表すことができます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="a76a2-121">例:</span><span class="sxs-lookup"><span data-stu-id="a76a2-121">For example:</span></span></br></br><span data-ttu-id="a76a2-122">- **Emp +** は資格を取得するために、従業員は 1 人の被扶養者を選択する必要があります (複数選択した場合、資格を失います)。</span><span class="sxs-lookup"><span data-stu-id="a76a2-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="a76a2-123">- **Emp + family** が資格を得るには、従業員が少なくとも 2 人の被扶養者を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a76a2-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="a76a2-124">**最大数**</span><span class="sxs-lookup"><span data-stu-id="a76a2-124">**Maximum number**</span></span> | <span data-ttu-id="a76a2-125">被扶養者の最大数。</span><span class="sxs-lookup"><span data-stu-id="a76a2-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="a76a2-126">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="a76a2-126">**Status**</span></span> | <span data-ttu-id="a76a2-127">補償オプションのステータス。</span><span class="sxs-lookup"><span data-stu-id="a76a2-127">The status of the coverage option.</span></span> <span data-ttu-id="a76a2-128">補償オプションのステータスが無効に設定されている場合、計画タイプで補償オプションを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="a76a2-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="a76a2-129">**パーセンテージ**</span><span class="sxs-lookup"><span data-stu-id="a76a2-129">**Percent**</span></span> | <span data-ttu-id="a76a2-130">パーセント量。</span><span class="sxs-lookup"><span data-stu-id="a76a2-130">The percent amount.</span></span> <span data-ttu-id="a76a2-131">このフィールドは、補償コード フィールドで % x 給与が選択された場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="a76a2-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="a76a2-132">**除数**</span><span class="sxs-lookup"><span data-stu-id="a76a2-132">**Divisor**</span></span> | <span data-ttu-id="a76a2-133">補償コード % x 給与を選択するときに計算で使用する除数。</span><span class="sxs-lookup"><span data-stu-id="a76a2-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="a76a2-134">**最小パーセント**</span><span class="sxs-lookup"><span data-stu-id="a76a2-134">**Percent minimum**</span></span> | <span data-ttu-id="a76a2-135">パーセンテージ補償コードを選択した場合の最小パーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="a76a2-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="a76a2-136">**最大パーセント**</span><span class="sxs-lookup"><span data-stu-id="a76a2-136">**Percent maximum**</span></span> | <span data-ttu-id="a76a2-137">パーセンテージ補償コードを選択した場合の最大パーセンテージ。</span><span class="sxs-lookup"><span data-stu-id="a76a2-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="a76a2-138">**個人担当者の適格性オプション**では、各補償オプションに適切な個人担当者の適格性オプションを付けます。</span><span class="sxs-lookup"><span data-stu-id="a76a2-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="a76a2-139">**セルフサービス**で、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="a76a2-140">フィールド</span><span class="sxs-lookup"><span data-stu-id="a76a2-140">Field</span></span> | <span data-ttu-id="a76a2-141">説明</span><span class="sxs-lookup"><span data-stu-id="a76a2-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a76a2-142">**従業員負担額の許可**</span><span class="sxs-lookup"><span data-stu-id="a76a2-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="a76a2-143">従業員が給付金を選択したときに、給付金セルフサービスの拠出額を変更できるようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="a76a2-144">このチェック ボックスをオンにすると、システムは従業員が給付金サービスで入力した拠出額に基づいて給付金計画パラメータを計算します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="a76a2-145">**従業員補償額の許可**</span><span class="sxs-lookup"><span data-stu-id="a76a2-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="a76a2-146">従業員が給付金を選択したときに、給付金セルフ サービスの補償額を変更できるようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="a76a2-147">このチェック ボックスをオンにすると、システムは従業員が従業員セルフ サービスで入力した補償額に基づいて給付金計画パラメータを計算します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="a76a2-148">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a76a2-148">Select **Save**.</span></span> 
