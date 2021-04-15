---
title: 理由コードの設定
description: Dynamics 365 Human Resources は、理由コードを使用して、従業員の給付金が変化する理由を説明します。
author: andreabichsel
ms.date: 01/25/2021
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
ms.openlocfilehash: ee74cb8b11c9b72940448077ee485ade4c0b7a39
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801050"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="6a174-103">理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="6a174-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6a174-104">Dynamics 365 Human Resources は、理由コードを使用して、従業員の給付金が変化する理由を説明します。</span><span class="sxs-lookup"><span data-stu-id="6a174-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="6a174-105">2021 年 1 月時点で、理由コードは、**従業員管理ワーク** スペースに移行されているため、**福利厚生管理** ワークスペースでは　ご利用いただけません。</span><span class="sxs-lookup"><span data-stu-id="6a174-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="6a174-106">詳細については、[従業員管理に理由コードを手動で移行する](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a174-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="6a174-107">理由コードの作成</span><span class="sxs-lookup"><span data-stu-id="6a174-107">Create reason codes</span></span>

1. <span data-ttu-id="6a174-108">**Human Resources** ワークスペース (または理由コードがまだ移行されていない場合は **福利厚生管理** ワークスペース) で、**リンク** を選択し、**理由コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a174-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="6a174-109">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a174-109">Select **New**.</span></span>

3. <span data-ttu-id="6a174-110">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a174-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6a174-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="6a174-111">Field</span></span> | <span data-ttu-id="6a174-112">説明</span><span class="sxs-lookup"><span data-stu-id="6a174-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6a174-113">**理由コード**</span><span class="sxs-lookup"><span data-stu-id="6a174-113">**Reason code**</span></span> | <span data-ttu-id="6a174-114">従業員が給付金プランの登録を変更する理由を識別する一意の名前。</span><span class="sxs-lookup"><span data-stu-id="6a174-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="6a174-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="6a174-115">**Description**</span></span> | <span data-ttu-id="6a174-116">理由コードの説明。</span><span class="sxs-lookup"><span data-stu-id="6a174-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="6a174-117">**該当するシナリオ** で、**福利厚生管理** を **はい** に 設定します。</span><span class="sxs-lookup"><span data-stu-id="6a174-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="6a174-118">(理由コードがまだ **担当者管理** ワークスペースに移行していない場合は、適用されません。)</span><span class="sxs-lookup"><span data-stu-id="6a174-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="6a174-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a174-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="6a174-120">従業員管理に理由コードを手動で移行する</span><span class="sxs-lookup"><span data-stu-id="6a174-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="6a174-121">2021 年 1 月時点で、理由コードは、**従業員管理** ワークスペースに移行されているため、**福利厚生管理** ワークスペースではご利用いただけません。</span><span class="sxs-lookup"><span data-stu-id="6a174-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="6a174-122">ほとんどの理由コード データは、環境内で自動的に移行されます。</span><span class="sxs-lookup"><span data-stu-id="6a174-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="6a174-123">一部の理由コード データは移行されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="6a174-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="6a174-124">たとえば、理由コードの最大文字数が15文字となった場合、15文字を超える理由コードは自動的に移行されません。</span><span class="sxs-lookup"><span data-stu-id="6a174-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="6a174-125">**福利厚生管理** ワークスペースの **リンク** ページにバナーが表示され、移行に関する情報やコードが移行されなかった理由が通知されます。</span><span class="sxs-lookup"><span data-stu-id="6a174-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="6a174-126">移行ステータスに関する詳細を示す **理由コード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a174-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="6a174-127">[![理由コード](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="6a174-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="6a174-128">移行に失敗した理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a174-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="6a174-129">[![理由コードの移行状態](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="6a174-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="6a174-130">**理由コードの移行** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="6a174-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="6a174-131">[![理由コードを移行する](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="6a174-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="6a174-132">**福利厚生理由コード移行** ペインでは、Human Resources の理由コードにマッピングする 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="6a174-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="6a174-133">従業員管理で既存の理由コードを使用するには、**既存の理由コードを使用** から選択します。</span><span class="sxs-lookup"><span data-stu-id="6a174-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="6a174-134">従業員管理で既存の理由コードを使用できるのは、別の福利厚生管理理由コードにまだ移行していない場合のみです。</span><span class="sxs-lookup"><span data-stu-id="6a174-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="6a174-135">従業員管理に新しい理由コードを作成するには、**新しい理由コード** に新たな理由コードを入力し、**新しい説明** に説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a174-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="6a174-136">[![従業員管理の理由コードへのマッピング](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="6a174-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="6a174-137">理由コードが Human Resources に移行した後で、福利厚生管理でそれらを使用するオプションは自動的に **はい** に設定 されます。</span><span class="sxs-lookup"><span data-stu-id="6a174-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="6a174-138">[![福利厚生管理で理由コードを使用する](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="6a174-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]