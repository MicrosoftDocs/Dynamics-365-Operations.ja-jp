---
title: 控除のコンフィギュレーション
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009696"
---
# <a name="configure-deductions"></a><span data-ttu-id="c0a2f-102">控除のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c0a2f-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c0a2f-103">Microsoft Dynamics 365 Human Resources の控除を使用して、各給付金について従業員の給与から控除する金額 (必要な場合) を決定します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="c0a2f-104">控除は日付が有効であるため、控除情報の履歴を記録しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="c0a2f-105">**給付金管理**ワーク スペースの**設定**で、**控除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="c0a2f-106">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-106">Select **New**.</span></span>

3. <span data-ttu-id="c0a2f-107">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c0a2f-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="c0a2f-108">Field</span></span> | <span data-ttu-id="c0a2f-109">説明</span><span class="sxs-lookup"><span data-stu-id="c0a2f-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c0a2f-110">控除</span><span class="sxs-lookup"><span data-stu-id="c0a2f-110">Deduction</span></span> | <span data-ttu-id="c0a2f-111">給付金の控除を識別するために使用される固有の ID。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="c0a2f-112">説明</span><span class="sxs-lookup"><span data-stu-id="c0a2f-112">Description</span></span> | <span data-ttu-id="c0a2f-113">控除の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="c0a2f-114">開始</span><span class="sxs-lookup"><span data-stu-id="c0a2f-114">Effective</span></span> | <span data-ttu-id="c0a2f-115">開始日。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-115">The start date.</span></span> <span data-ttu-id="c0a2f-116">既定値は現在のシステム日付です。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="c0a2f-117">有効期限</span><span class="sxs-lookup"><span data-stu-id="c0a2f-117">Expiration</span></span> | <span data-ttu-id="c0a2f-118">終了日。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-118">The end date.</span></span> <span data-ttu-id="c0a2f-119">既定値は 12/31/2154 で、意味がありません。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="c0a2f-120">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c0a2f-120">Heading</span></span> | <span data-ttu-id="c0a2f-121">この控除が給与の給付金を処理するときに控除の従業員部分に使用する給与計算システムの見出しコード。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c0a2f-122">これは、サードパーティの給与計算プロバイダーを使用するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="c0a2f-123">従業員給与控除参照</span><span class="sxs-lookup"><span data-stu-id="c0a2f-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="c0a2f-124">給与計算のために給付金を処理する際に、従業員分の控除に対して、この控除で使用する給与システムの控除コード。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="c0a2f-125">金額の見出し</span><span class="sxs-lookup"><span data-stu-id="c0a2f-125">Amount heading</span></span> | <span data-ttu-id="c0a2f-126">給与の給付金を処理するときに、この控除額が従業員の控除部分に使用する給与計算システムの見出しコード。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="c0a2f-127">これは通常、サードパーティの給与計算プロバイダーを使用するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="c0a2f-128">削除可能</span><span class="sxs-lookup"><span data-stu-id="c0a2f-128">Can delete</span></span> | <span data-ttu-id="c0a2f-129">Dynamics 365 for Finance and Operations からエクスポートされた値が給与計算システムで値を削除できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="c0a2f-130">ペアの列</span><span class="sxs-lookup"><span data-stu-id="c0a2f-130">Paired columns</span></span> | <span data-ttu-id="c0a2f-131">対になった隣接する列の見出しと控除額を給与計算システムにエクスポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="c0a2f-132">変更の有効日</span><span class="sxs-lookup"><span data-stu-id="c0a2f-132">Change effective date</span></span> | <span data-ttu-id="c0a2f-133">給付控除の変更が有効になる日付。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="c0a2f-134">この日付に、システムは自動的に給付控除を変更し、控除変更の更新処理を実行している限り、この控除に関連するすべての給付プランを更新します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="c0a2f-135">控除の変更が完了しています</span><span class="sxs-lookup"><span data-stu-id="c0a2f-135">Deduction change completed</span></span> | <span data-ttu-id="c0a2f-136">控除更新の変更処理によって給付控除の変更が完了すると、控除の変更が完了しましたチェックボックスが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="c0a2f-137">利益率の設定に対する変更を追跡して維持するには、**アクション**を選択し、**バージョンの維持**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="c0a2f-138">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0a2f-138">Select **Save**.</span></span> 
