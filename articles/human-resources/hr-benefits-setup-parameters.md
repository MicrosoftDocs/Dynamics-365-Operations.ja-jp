---
title: 給付金管理パラメーターの設定
description: Microsoft Dynamics 365 Human Resources で給付金管理に対するパラメーターをコンフィギュレーションします。
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009683"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="d8985-103">給付金管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="d8985-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d8985-104">Microsoft Dynamics 365 Human Resources で休暇計画を設定する前に、給付金管理パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8985-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="d8985-105">これらのパラメーターは既定値、理由コード、およびその他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="d8985-106">一般パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d8985-106">Configure general parameters</span></span>

1. <span data-ttu-id="d8985-107">**設定**の**給付金管理**ワーク スペースで、**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8985-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="d8985-108">**一般**タブで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="d8985-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="d8985-109">Field</span></span> | <span data-ttu-id="d8985-110">説明</span><span class="sxs-lookup"><span data-stu-id="d8985-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d8985-111">**国/地域**</span><span class="sxs-lookup"><span data-stu-id="d8985-111">**Country/region**</span></span> | <span data-ttu-id="d8985-112">**国/地域**フィールドでは郵便番号/状態の表示順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="d8985-113">選択した国がドロップダウン リストの最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8985-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="d8985-114">**登録理由コード**</span><span class="sxs-lookup"><span data-stu-id="d8985-114">**Enrollment reason code**</span></span> | <span data-ttu-id="d8985-115">従業員計画がオープン登録の処理中に作成された場合、既定の理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8985-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="d8985-116">**キャンセルの理由コード**</span><span class="sxs-lookup"><span data-stu-id="d8985-116">**Cancellation reason code**</span></span> | <span data-ttu-id="d8985-117">従業員の給付金計画がキャンセルされた場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="d8985-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="d8985-118">キャンセル プロセス中、ダイアログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8985-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="d8985-119">ユーザーは必要に応じて**キャンセルの理由コード**を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d8985-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="d8985-120">**再オープン理由コード**</span><span class="sxs-lookup"><span data-stu-id="d8985-120">**Reopen reason code**</span></span> | <span data-ttu-id="d8985-121">従業員の給付金計画が再開された場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="d8985-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="d8985-122">キャンセル プロセス中、ダイアログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8985-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="d8985-123">ユーザーは必要に応じて**再開の理由コード**を変更できます。</span><span class="sxs-lookup"><span data-stu-id="d8985-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="d8985-124">**ライフ イベント理由コード**</span><span class="sxs-lookup"><span data-stu-id="d8985-124">**Life event reason code**</span></span> | <span data-ttu-id="d8985-125">ライフイベントが発生した場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="d8985-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="d8985-126">**レート変更理由コード**</span><span class="sxs-lookup"><span data-stu-id="d8985-126">**Rate change reason code**</span></span> | <span data-ttu-id="d8985-127">レート変更の更新処理中に従業員の給付金計画がキャンセルまたは再開された場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="d8985-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="d8985-128">これはレート変更の更新処理によって変更されたレコードを示します。</span><span class="sxs-lookup"><span data-stu-id="d8985-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="d8985-129">**適格な新規採用者**</span><span class="sxs-lookup"><span data-stu-id="d8985-129">**New hire eligible**</span></span> | <span data-ttu-id="d8985-130">新規採用が適格かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="d8985-131">**新規採用要録期間**</span><span class="sxs-lookup"><span data-stu-id="d8985-131">**New hire enrollment period**</span></span> | <span data-ttu-id="d8985-132">新規採用登録が許可される期間。</span><span class="sxs-lookup"><span data-stu-id="d8985-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="d8985-133">**注記**: この設定は、計画適格ルールで設定されたすべての新規採用登録を上書きします。</span><span class="sxs-lookup"><span data-stu-id="d8985-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="d8985-134">**年次給与の拡張設定**</span><span class="sxs-lookup"><span data-stu-id="d8985-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="d8985-135">**従業員の給付金の詳細**で**年間給付金給与**金額を自動的に計算するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="d8985-136">これは従業員の**固定報酬支払レード**、**平均時間**、および**支払頻度**に基づいています。</span><span class="sxs-lookup"><span data-stu-id="d8985-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="d8985-137">**平均時間** x **固定報酬支払** x **支払頻度** (# 支払期間中での) = **年間給付金給与**</span><span class="sxs-lookup"><span data-stu-id="d8985-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="d8985-138">**平均時間**、**固定報酬支払レート**、または**支払頻度**フィールドのいずれかの値が変更された場合、システムは変更値に基づいて従業員の**年間給付金給与**金額を自動的に再計算します。</span><span class="sxs-lookup"><span data-stu-id="d8985-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="d8985-139">システムによって、変更が発生した正確な日時を識別するための**有効日**レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d8985-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="d8985-140">必要に応じて**年間給付金給与**金額を手動で編集することができます。</span><span class="sxs-lookup"><span data-stu-id="d8985-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="d8985-141">**ライフ イベントが有効になりました**</span><span class="sxs-lookup"><span data-stu-id="d8985-141">**Life events enabled**</span></span> | <span data-ttu-id="d8985-142">ライフ イベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d8985-142">Enables life events.</span></span> |
   | <span data-ttu-id="d8985-143">**レガシ給付金フォームの非表示**</span><span class="sxs-lookup"><span data-stu-id="d8985-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="d8985-144">レガシ給付金フォームの非表示を許可できます。</span><span class="sxs-lookup"><span data-stu-id="d8985-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="d8985-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8985-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="d8985-146">従業員のセルフ サービス パラメーターをコンフィグレーションする</span><span class="sxs-lookup"><span data-stu-id="d8985-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="d8985-147">**設定**の**給付金管理**ワーク スペースで、**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8985-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="d8985-148">**従業員のセルフ サービス**タブで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="d8985-149">フィールド</span><span class="sxs-lookup"><span data-stu-id="d8985-149">Field</span></span> | <span data-ttu-id="d8985-150">説明</span><span class="sxs-lookup"><span data-stu-id="d8985-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d8985-151">**給付金の検証**</span><span class="sxs-lookup"><span data-stu-id="d8985-151">**Benefit verification**</span></span> | <span data-ttu-id="d8985-152">セルフサービス給与金のチェックアウト中に使用する検証テキスト。</span><span class="sxs-lookup"><span data-stu-id="d8985-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="d8985-153">**被指名人の自動選択**</span><span class="sxs-lookup"><span data-stu-id="d8985-153">**Auto select designees**</span></span> | <span data-ttu-id="d8985-154">計画オプションに対する適格性に基づいて被扶養者と受益者を自動的に選択するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8985-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="d8985-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8985-155">Select **Save**.</span></span>
