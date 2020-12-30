---
title: すべての会社に対する給付金の管理と従業員セルフサービス パラメータの設定
description: Microsoft Dynamics 365 Human Resources で給付金の管理と従業員セルフサービスのパラメータを構成する。
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692700"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="4aceb-103">すべての会社に対する給付金の管理と従業員セルフサービス パラメータの設定</span><span class="sxs-lookup"><span data-stu-id="4aceb-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="4aceb-104">Microsoft Dynamics 365 Human Resources で給付金計画を設定する前に、給付金管理パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4aceb-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="4aceb-105">これらのパラメーターは既定値、理由コード、およびその他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="4aceb-106">一般パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4aceb-106">Configure general parameters</span></span>

1. <span data-ttu-id="4aceb-107">**福利厚生管理** ワークスペースの **設定** で、**人事管理共有パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="4aceb-108">**福利厚生の管理** タブで、次のフィールドの値を指定します:</span><span class="sxs-lookup"><span data-stu-id="4aceb-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="4aceb-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="4aceb-109">Field</span></span> | <span data-ttu-id="4aceb-110">説明</span><span class="sxs-lookup"><span data-stu-id="4aceb-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4aceb-111">**国/地域**</span><span class="sxs-lookup"><span data-stu-id="4aceb-111">**Country/region**</span></span> | <span data-ttu-id="4aceb-112">**国/地域** フィールドでは郵便番号/状態の表示順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="4aceb-113">選択した国がドロップダウン リストの最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="4aceb-114">**登録理由コード**</span><span class="sxs-lookup"><span data-stu-id="4aceb-114">**Enrollment reason code**</span></span> | <span data-ttu-id="4aceb-115">従業員計画がオープン登録の処理中に作成された場合、既定の理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="4aceb-116">**キャンセルの理由コード**</span><span class="sxs-lookup"><span data-stu-id="4aceb-116">**Cancellation reason code**</span></span> | <span data-ttu-id="4aceb-117">従業員の給付金計画がキャンセルされた場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="4aceb-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="4aceb-118">キャンセル プロセス中、ダイアログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="4aceb-119">ユーザーは必要に応じて **キャンセルの理由コード** を変更できます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="4aceb-120">**再オープン理由コード**</span><span class="sxs-lookup"><span data-stu-id="4aceb-120">**Reopen reason code**</span></span> | <span data-ttu-id="4aceb-121">従業員の給付金計画が再開された場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="4aceb-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="4aceb-122">キャンセル プロセス中、ダイアログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="4aceb-123">ユーザーは必要に応じて **再開の理由コード** を変更できます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="4aceb-124">**ライフ イベント理由コード**</span><span class="sxs-lookup"><span data-stu-id="4aceb-124">**Life event reason code**</span></span> | <span data-ttu-id="4aceb-125">ライフイベントが発生した場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="4aceb-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="4aceb-126">**レート変更理由コード**</span><span class="sxs-lookup"><span data-stu-id="4aceb-126">**Rate change reason code**</span></span> | <span data-ttu-id="4aceb-127">レート変更の更新処理中に従業員の給付金計画がキャンセルまたは再開された場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="4aceb-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="4aceb-128">これはレート変更の更新処理によって変更されたレコードを示します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="4aceb-129">**年間給付金**</span><span class="sxs-lookup"><span data-stu-id="4aceb-129">**Benefits annual salary**</span></span> | <span data-ttu-id="4aceb-130">従業員の **福利厚生の年間給与** 額を設定できます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="4aceb-131">Human Resources では、補償範囲額を決定する際に、固定報酬の年間金額ではなく、**福利厚生の年間給与** 額を使用します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="4aceb-132">**適格な新規採用者**</span><span class="sxs-lookup"><span data-stu-id="4aceb-132">**New hire eligible**</span></span> | <span data-ttu-id="4aceb-133">新規採用が適格かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="4aceb-134">**新規採用要録期間**</span><span class="sxs-lookup"><span data-stu-id="4aceb-134">**New hire enrollment period**</span></span> | <span data-ttu-id="4aceb-135">新規採用登録が許可される期間。</span><span class="sxs-lookup"><span data-stu-id="4aceb-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="4aceb-136">**注記**: この設定は、計画適格ルールで設定されたすべての新規採用登録を上書きします。</span><span class="sxs-lookup"><span data-stu-id="4aceb-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="4aceb-137">**既定の支払頻度**</span><span class="sxs-lookup"><span data-stu-id="4aceb-137">**Default pay frequency**</span></span> | <span data-ttu-id="4aceb-138">新しい従業員が追加されたときに使用する既定の支払頻度。</span><span class="sxs-lookup"><span data-stu-id="4aceb-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="4aceb-139">**ライフ イベントが有効になりました**</span><span class="sxs-lookup"><span data-stu-id="4aceb-139">**Life events enabled**</span></span> | <span data-ttu-id="4aceb-140">ライフ イベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4aceb-140">Enables life events.</span></span> |
   | <span data-ttu-id="4aceb-141">**レガシ給付金フォームの非表示**</span><span class="sxs-lookup"><span data-stu-id="4aceb-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="4aceb-142">レガシ給付金フォームの非表示を許可できます。</span><span class="sxs-lookup"><span data-stu-id="4aceb-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="4aceb-143">**給付金の検証**</span><span class="sxs-lookup"><span data-stu-id="4aceb-143">**Benefit verification**</span></span> | <span data-ttu-id="4aceb-144">セルフサービス給与金のチェックアウト中に使用する検証テキスト。</span><span class="sxs-lookup"><span data-stu-id="4aceb-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="4aceb-145">**被指名人の自動選択**</span><span class="sxs-lookup"><span data-stu-id="4aceb-145">**Auto select designees**</span></span> | <span data-ttu-id="4aceb-146">計画オプションに対する適格性に基づいて、被扶養者と受益者を自動的に選択するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="4aceb-147">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="4aceb-148">従業員のセルフサービス パラメーターをコンフィグレーションする</span><span class="sxs-lookup"><span data-stu-id="4aceb-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="4aceb-149">**福利厚生管理** ワークスペースの **設定** で、**人事管理パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="4aceb-150">**福利厚生の管理** タブで、次のフィールドの値を指定します:</span><span class="sxs-lookup"><span data-stu-id="4aceb-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="4aceb-151">フィールド</span><span class="sxs-lookup"><span data-stu-id="4aceb-151">Field</span></span> | <span data-ttu-id="4aceb-152">説明</span><span class="sxs-lookup"><span data-stu-id="4aceb-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4aceb-153">**給付金の検証**</span><span class="sxs-lookup"><span data-stu-id="4aceb-153">**Benefit verification**</span></span> | <span data-ttu-id="4aceb-154">セルフサービス給与金のチェックアウト中に使用する検証テキスト。</span><span class="sxs-lookup"><span data-stu-id="4aceb-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="4aceb-155">**被指名人の自動選択**</span><span class="sxs-lookup"><span data-stu-id="4aceb-155">**Auto select designees**</span></span> | <span data-ttu-id="4aceb-156">計画オプションに対する適格性に基づいて被扶養者と受益者を自動的に選択するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="4aceb-157">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4aceb-157">Select **Save**.</span></span>


