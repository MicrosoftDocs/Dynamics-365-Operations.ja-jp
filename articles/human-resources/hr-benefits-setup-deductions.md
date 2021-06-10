---
title: 控除のコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources の控除を使用して、各給付金について従業員の給与から控除する金額 (必要な場合) を決定します。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055559"
---
# <a name="configure-deductions"></a><span data-ttu-id="1faca-103">控除のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1faca-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1faca-104">Microsoft Dynamics 365 Human Resources の控除を使用して、各給付金について従業員の給与から控除する金額 (必要な場合) を決定します。</span><span class="sxs-lookup"><span data-stu-id="1faca-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="1faca-105">控除は日付が有効であるため、控除情報の履歴を記録しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="1faca-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="1faca-106">**給付金管理** ワーク スペースの **設定** で、**控除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1faca-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="1faca-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1faca-107">Select **New**.</span></span>

3. <span data-ttu-id="1faca-108">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1faca-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="1faca-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="1faca-109">Field</span></span> | <span data-ttu-id="1faca-110">説明</span><span class="sxs-lookup"><span data-stu-id="1faca-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="1faca-111">**控除**</span><span class="sxs-lookup"><span data-stu-id="1faca-111">**Deduction**</span></span> | <span data-ttu-id="1faca-112">給付金の控除を識別するために使用される固有の ID。</span><span class="sxs-lookup"><span data-stu-id="1faca-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="1faca-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="1faca-113">**Description**</span></span> | <span data-ttu-id="1faca-114">控除の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1faca-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="1faca-115">**開始**</span><span class="sxs-lookup"><span data-stu-id="1faca-115">**Effective**</span></span> | <span data-ttu-id="1faca-116">開始日。</span><span class="sxs-lookup"><span data-stu-id="1faca-116">The start date.</span></span> <span data-ttu-id="1faca-117">既定値は現在のシステム日付です。</span><span class="sxs-lookup"><span data-stu-id="1faca-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="1faca-118">**有効期限**</span><span class="sxs-lookup"><span data-stu-id="1faca-118">**Expiration**</span></span> | <span data-ttu-id="1faca-119">終了日。</span><span class="sxs-lookup"><span data-stu-id="1faca-119">The end date.</span></span> <span data-ttu-id="1faca-120">既定値は 12/31/2154 で、意味がありません。</span><span class="sxs-lookup"><span data-stu-id="1faca-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="1faca-121">**ヘッダー**</span><span class="sxs-lookup"><span data-stu-id="1faca-121">**Heading**</span></span> | <span data-ttu-id="1faca-122">この控除が給与の給付金を処理するときに控除の従業員部分に使用する給与計算システムの見出しコード。</span><span class="sxs-lookup"><span data-stu-id="1faca-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="1faca-123">これは、サード パーティの給与計算プロバイダーを使用するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1faca-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="1faca-124">**従業員給与控除参照**</span><span class="sxs-lookup"><span data-stu-id="1faca-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="1faca-125">給与計算のために給付金を処理する際に、従業員分の控除に対して、この控除で使用する給与システムの控除コード。</span><span class="sxs-lookup"><span data-stu-id="1faca-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="1faca-126">**金額の見出し**</span><span class="sxs-lookup"><span data-stu-id="1faca-126">**Amount heading**</span></span> | <span data-ttu-id="1faca-127">給与の給付金を処理するときに、この控除額が従業員の控除部分に使用する給与計算システムの見出しコード。</span><span class="sxs-lookup"><span data-stu-id="1faca-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="1faca-128">これは通常、サード パーティの給与計算プロバイダーを使用するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="1faca-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="1faca-129">**削除可能**</span><span class="sxs-lookup"><span data-stu-id="1faca-129">**Can delete**</span></span> | <span data-ttu-id="1faca-130">Dynamics 365 for Finance and Operations からエクスポートされた値が給与計算システムで値を削除できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1faca-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="1faca-131">**ペアの列**</span><span class="sxs-lookup"><span data-stu-id="1faca-131">**Paired columns**</span></span> | <span data-ttu-id="1faca-132">対になった隣接する列の見出しと控除額を給与計算システムにエクスポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1faca-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="1faca-133">**変更の有効日**</span><span class="sxs-lookup"><span data-stu-id="1faca-133">**Change effective date**</span></span> | <span data-ttu-id="1faca-134">給付控除の変更が有効になる日付。</span><span class="sxs-lookup"><span data-stu-id="1faca-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="1faca-135">この日付に、システムは自動的に給付控除を変更し、**控除変更の更新** 処理を実行している限り、この控除に関連するすべての給付プランを更新します。</span><span class="sxs-lookup"><span data-stu-id="1faca-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="1faca-136">**控除の変更が完了しています**</span><span class="sxs-lookup"><span data-stu-id="1faca-136">**Deduction change completed**</span></span> | <span data-ttu-id="1faca-137">控除更新の変更処理によって給付控除の変更が完了すると、**控除の変更が完了しました** チェック ボックスが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="1faca-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="1faca-138">利益率の設定に対する変更を追跡して維持するには、**アクション** を選択し、**バージョンの維持** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1faca-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="1faca-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1faca-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]