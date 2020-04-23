---
title: 計画タイプの作成
description: Microsoft Dynamics 365 Human Resources のプラン タイプは、給付金の特定のタイプを高レベルにグループ化したものです。 各プラン タイプには、そのプラン タイプのルールを決定するプラン タイプ コードがあります。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 06a36f9f3fef54e7e06d616c9179374db4ce7115
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229697"
---
# <a name="create-plan-types"></a><span data-ttu-id="9cccf-104">計画タイプの作成</span><span class="sxs-lookup"><span data-stu-id="9cccf-104">Create plan types</span></span>

<span data-ttu-id="9cccf-105">Microsoft Dynamics 365 Human Resources のプラン タイプは、給付金の特定のタイプを高レベルにグループ化したものです。</span><span class="sxs-lookup"><span data-stu-id="9cccf-105">A plan type in Microsoft Dynamics 365 Human Resources is a high-level grouping of specific types of benefits.</span></span> <span data-ttu-id="9cccf-106">各プラン タイプには、そのプラン タイプのルールを決定するプラン タイプ コードがあります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-106">Each plan type has a plan type code that determines rules for the plan type.</span></span> <span data-ttu-id="9cccf-107">たとえば、プラン タイプ基本ライフには、一種の生命保険プランなのでライフ プラン タイプ コード用に確立されたルールに準拠する必要があるため、プラン タイプ コード ライフがあります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-107">For example, the plan type Basic life would have the plan type code Life because it’s a kind of life insurance plan and must conform to rules established for the Life plan type code.</span></span> <span data-ttu-id="9cccf-108">別のプラン タイプは、同じくプラン タイプ コード ライフの補助ライフになります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-108">Another plan type might be Supplemental life, also with plan type code Life.</span></span>

<span data-ttu-id="9cccf-109">各プラン タイプは、従業員がそのタイプの 1 つまたは複数のプランに登録できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-109">Each plan type indicates whether an employee can enroll in one plan of its type or multiple.</span></span> <span data-ttu-id="9cccf-110">たとえば、従業員はプラン タイプ ライフの基本ライフおよび補助ライフ ポリシーの両方に登録できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-110">For example, an employee would likely be able to enroll in both the Basic life and the Supplemental life policies of plan type Life.</span></span> <span data-ttu-id="9cccf-111">従業員は、医療タイプのポリシーを 1 つのみに登録することが許可される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-111">An employee would likely be allowed to enroll in only one policy of type Medical.</span></span>

<span data-ttu-id="9cccf-112">プラン タイプに連絡先が含まれている場合、そのプラン タイプは、連絡先が受益者または扶養家族であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-112">If a plan type involves contacts, the plan type indicates whether contacts are beneficiaries or dependents.</span></span> <span data-ttu-id="9cccf-113">たとえば、基本ライフ プラン タイプには受益者が入っていますが、基本の医療プラン タイプに被扶養者が入っています。</span><span class="sxs-lookup"><span data-stu-id="9cccf-113">For example, a Basic life plan type would have beneficiaries, while a Basic medical plan type would have dependents.</span></span> <span data-ttu-id="9cccf-114">場合によっては、プランに個人の連絡先が含まれていないことがあります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-114">In some cases, a plan may not have any personal contacts.</span></span> <span data-ttu-id="9cccf-115">たとえば、Flexible Spending Account または駐車許可などです。</span><span class="sxs-lookup"><span data-stu-id="9cccf-115">For example, a Flexible Spending Account or Parking allowance.</span></span>

<span data-ttu-id="9cccf-116">あるプラン タイプは、補償オプションを定義するかもしれません。</span><span class="sxs-lookup"><span data-stu-id="9cccf-116">A plan type may define coverage options.</span></span> <span data-ttu-id="9cccf-117">補償オプションは、補償オプション フォームで定義されます。</span><span class="sxs-lookup"><span data-stu-id="9cccf-117">The coverage options are defined in the Coverage option form.</span></span> <span data-ttu-id="9cccf-118">補償オプションでは、給付金額またはプラン タイプに適格な連絡先を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9cccf-118">A coverage option can specify the amount of the benefit or the contacts who are eligible for the plan type.</span></span> <span data-ttu-id="9cccf-119">たとえば、連絡先タイプが受益者である場合、補償オプションで、給付金の利用時に受益者が受け取る資格の条件を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-119">For example, if the contact type is Beneficiary, the coverage option should define the terms of what the beneficiary is eligible to receive when the benefit is utilized.</span></span> <span data-ttu-id="9cccf-120">連絡先タイプが扶養家族である場合、補償オプションで、その扶養家族と従業員の関係を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-120">If the contact type is Dependent, the coverage option should define the relationship between the dependent and employee.</span></span> 

1. <span data-ttu-id="9cccf-121">**給付金管理**ワーク スペースの**設定**で、 **プラン タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-121">In the **Benefits management** workspace, under **Setup**, select **Plan types**.</span></span>

2. <span data-ttu-id="9cccf-122">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-122">Select **New**.</span></span>

3. <span data-ttu-id="9cccf-123">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-123">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9cccf-124">フィールド</span><span class="sxs-lookup"><span data-stu-id="9cccf-124">Field</span></span> | <span data-ttu-id="9cccf-125">説明</span><span class="sxs-lookup"><span data-stu-id="9cccf-125">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9cccf-126">**計画タイプ**</span><span class="sxs-lookup"><span data-stu-id="9cccf-126">**Plan type**</span></span> | <span data-ttu-id="9cccf-127">プラン タイプを識別する一意の名前。</span><span class="sxs-lookup"><span data-stu-id="9cccf-127">A unique name that identifies the plan type.</span></span> |
   | <span data-ttu-id="9cccf-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="9cccf-128">**Description**</span></span> | <span data-ttu-id="9cccf-129">プラン タイプの説明。</span><span class="sxs-lookup"><span data-stu-id="9cccf-129">A description of the plan type.</span></span> |
   | <span data-ttu-id="9cccf-130">**計画タイプ コード**</span><span class="sxs-lookup"><span data-stu-id="9cccf-130">**Plan type code**</span></span> | <span data-ttu-id="9cccf-131">値のドロップ ダウン リストからプラン タイプ コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-131">Select a plan type code from the drop-down list of values.</span></span> <span data-ttu-id="9cccf-132">プラン タイプ コード リストには、現在のバージョンでサポートされているすべてのプラン タイプが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9cccf-132">The plan type code list displays all the plan types that are supported in the current version.</span></span> |
   | <span data-ttu-id="9cccf-133">**同時登録**</span><span class="sxs-lookup"><span data-stu-id="9cccf-133">**Concurrent enrollment**</span></span> | <span data-ttu-id="9cccf-134">従業員が同じプラン タイプの複数の給付金プランに登録できるか、またはプラン タイプごとに 1 つの給付金プランのみに登録できるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-134">Specifies whether an employee can enroll in multiple benefit plans of the same plan type or only one benefit plan per plan type.</span></span> |
   | <span data-ttu-id="9cccf-135">**連絡先タイプ**</span><span class="sxs-lookup"><span data-stu-id="9cccf-135">**Contact type**</span></span> | <span data-ttu-id="9cccf-136">個人の連絡先の役割を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-136">Specifies the role of the personal contact.</span></span> <span data-ttu-id="9cccf-137">値には、空白、被扶養者、および受益者があります。</span><span class="sxs-lookup"><span data-stu-id="9cccf-137">The values are blank, Dependent, and Beneficiary.</span></span> <span data-ttu-id="9cccf-138">補償オプションに基づいてプラン タイプが被扶養者または受益者を必要としない場合、**連絡先タイプ** を空白のままにすることができます。</span><span class="sxs-lookup"><span data-stu-id="9cccf-138">You can leave **Contact type** blank if their plan type does not require a dependent or beneficiary based on the coverage option.</span></span> |

4. <span data-ttu-id="9cccf-139">ライフ イベント オプションを構成するには、**アクション**を選択してから、**ライフ イベント オプション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-139">To configure life event options, select **Actions**, and then select **Life event options**.</span></span> <span data-ttu-id="9cccf-140">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-140">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9cccf-141">フィールド</span><span class="sxs-lookup"><span data-stu-id="9cccf-141">Field</span></span> | <span data-ttu-id="9cccf-142">説明</span><span class="sxs-lookup"><span data-stu-id="9cccf-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9cccf-143">**計画タイプ**</span><span class="sxs-lookup"><span data-stu-id="9cccf-143">**Plan type**</span></span> | <span data-ttu-id="9cccf-144">ライフ イベント オプションを構成するプラン タイプ。</span><span class="sxs-lookup"><span data-stu-id="9cccf-144">The plan type to configure life event options for.</span></span> |
   | <span data-ttu-id="9cccf-145">**ライフ イベント タイプ ID**</span><span class="sxs-lookup"><span data-stu-id="9cccf-145">**Life event type ID**</span></span> | <span data-ttu-id="9cccf-146">ライフ イベント タイプの ID。</span><span class="sxs-lookup"><span data-stu-id="9cccf-146">The ID of the life event type.</span></span> |
   | <span data-ttu-id="9cccf-147">**キャンセルの許可**</span><span class="sxs-lookup"><span data-stu-id="9cccf-147">**Allow cancellation**</span></span> | <span data-ttu-id="9cccf-148">従業員がライフ イベント中に給付金プランをキャンセルできるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-148">Specifies whether an employee can cancel a benefits plan during the life event.</span></span> |
   | <span data-ttu-id="9cccf-149">**補償オプションの変更**</span><span class="sxs-lookup"><span data-stu-id="9cccf-149">**Change coverage option**</span></span> | <span data-ttu-id="9cccf-150">従業員がライフ イベント中に補償オプションを変更できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-150">Specifies whether an employee can change coverage options during the life event.</span></span> |
   | <span data-ttu-id="9cccf-151">**新しい計画に変更**</span><span class="sxs-lookup"><span data-stu-id="9cccf-151">**Change to a new plan**</span></span> | <span data-ttu-id="9cccf-152">従業員がライフ イベント中にプランを変更できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-152">Specifies whether an employee can change plans during the life event.</span></span> |
   | <span data-ttu-id="9cccf-153">**計画の自動キャンセル**</span><span class="sxs-lookup"><span data-stu-id="9cccf-153">**Auto cancel plan**</span></span> | <span data-ttu-id="9cccf-154">ライフ イベント中にプランを自動的にキャンセルするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-154">Specifies whether to automatically cancel the plan during the life event.</span></span> |
   | <span data-ttu-id="9cccf-155">**適格性検索の自動再オープン**</span><span class="sxs-lookup"><span data-stu-id="9cccf-155">**Auto reopen eligibility check**</span></span> | <span data-ttu-id="9cccf-156">ライフ イベント中に給付金登録の適格性検索を自動的に再オープンするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-156">Specifies whether to automatically reopen the benefits enrollment eligibility check during the life event.</span></span> |
   | <span data-ttu-id="9cccf-157">**レポート ウィンドウ**</span><span class="sxs-lookup"><span data-stu-id="9cccf-157">**Reporting window**</span></span> | <span data-ttu-id="9cccf-158">ライフ イベントのレポート ウィンドウを日単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-158">Specifies the reporting window, in days, of the life event.</span></span> <span data-ttu-id="9cccf-159">**注記**: 金額を入力しない場合、システムはレポート ウィンドウはゼロとみなし、ライフ イベントは処理されません。</span><span class="sxs-lookup"><span data-stu-id="9cccf-159">**Note**: If you don't enter an amount, the system assumes the reporting window to be zero and won't process the life event.</span></span> |

5. <span data-ttu-id="9cccf-160">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cccf-160">Select **Save**.</span></span> 
