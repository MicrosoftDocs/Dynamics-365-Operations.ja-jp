---
title: 給付金管理パラメーターの設定
description: Microsoft Dynamics 365 Human Resources で給付金管理に対するパラメーターをコンフィギュレーションします。
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
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229766"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="441f6-103">福利厚生管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="441f6-103">Set Benefits management parameters</span></span>

<span data-ttu-id="441f6-104">Microsoft Dynamics 365 Human Resources で休暇計画を設定する前に、給付金管理パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="441f6-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="441f6-105">これらのパラメーターは既定値、理由コード、およびその他のオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="441f6-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="441f6-106">一般パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="441f6-106">Configure general parameters</span></span>

1. <span data-ttu-id="441f6-107">**設定**の**給付金管理**ワーク スペースで、**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="441f6-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="441f6-108">**一般**タブで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="441f6-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="441f6-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="441f6-109">Field</span></span> | <span data-ttu-id="441f6-110">説明</span><span class="sxs-lookup"><span data-stu-id="441f6-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="441f6-111">**国/地域**</span><span class="sxs-lookup"><span data-stu-id="441f6-111">**Country/region**</span></span> | <span data-ttu-id="441f6-112">**国/地域**フィールドでは郵便番号/状態の表示順序を決定します。</span><span class="sxs-lookup"><span data-stu-id="441f6-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="441f6-113">選択した国がドロップダウン リストの最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="441f6-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="441f6-114">**登録理由コード**</span><span class="sxs-lookup"><span data-stu-id="441f6-114">**Enrollment reason code**</span></span> | <span data-ttu-id="441f6-115">従業員計画がオープン登録の処理中に作成された場合、既定の理由コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="441f6-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="441f6-116">**キャンセルの理由コード**</span><span class="sxs-lookup"><span data-stu-id="441f6-116">**Cancellation reason code**</span></span> | <span data-ttu-id="441f6-117">従業員の給付金計画がキャンセルされた場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="441f6-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="441f6-118">キャンセル プロセス中、ダイアログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="441f6-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="441f6-119">ユーザーは必要に応じて**キャンセルの理由コード**を変更できます。</span><span class="sxs-lookup"><span data-stu-id="441f6-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="441f6-120">**再オープン理由コード**</span><span class="sxs-lookup"><span data-stu-id="441f6-120">**Reopen reason code**</span></span> | <span data-ttu-id="441f6-121">従業員の給付金計画が再開された場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="441f6-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="441f6-122">キャンセル プロセス中、ダイアログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="441f6-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="441f6-123">ユーザーは必要に応じて**再開の理由コード**を変更できます。</span><span class="sxs-lookup"><span data-stu-id="441f6-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="441f6-124">**ライフ イベント理由コード**</span><span class="sxs-lookup"><span data-stu-id="441f6-124">**Life event reason code**</span></span> | <span data-ttu-id="441f6-125">ライフイベントが発生した場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="441f6-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="441f6-126">**レート変更理由コード**</span><span class="sxs-lookup"><span data-stu-id="441f6-126">**Rate change reason code**</span></span> | <span data-ttu-id="441f6-127">レート変更の更新処理中に従業員の給付金計画がキャンセルまたは再開された場合に使用する理由コード。</span><span class="sxs-lookup"><span data-stu-id="441f6-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="441f6-128">これはレート変更の更新処理によって変更されたレコードを示します。</span><span class="sxs-lookup"><span data-stu-id="441f6-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="441f6-129">**適格な新規採用者**</span><span class="sxs-lookup"><span data-stu-id="441f6-129">**New hire eligible**</span></span> | <span data-ttu-id="441f6-130">新規採用が適格かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="441f6-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="441f6-131">**新規採用要録期間**</span><span class="sxs-lookup"><span data-stu-id="441f6-131">**New hire enrollment period**</span></span> | <span data-ttu-id="441f6-132">新規採用登録が許可される期間。</span><span class="sxs-lookup"><span data-stu-id="441f6-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="441f6-133">**注記**: この設定は、計画適格ルールで設定されたすべての新規採用登録を上書きします。</span><span class="sxs-lookup"><span data-stu-id="441f6-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="441f6-134">**ライフ イベントが有効になりました**</span><span class="sxs-lookup"><span data-stu-id="441f6-134">**Life events enabled**</span></span> | <span data-ttu-id="441f6-135">ライフ イベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="441f6-135">Enables life events.</span></span> |
   | <span data-ttu-id="441f6-136">**レガシ給付金フォームの非表示**</span><span class="sxs-lookup"><span data-stu-id="441f6-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="441f6-137">レガシ給付金フォームの非表示を許可できます。</span><span class="sxs-lookup"><span data-stu-id="441f6-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="441f6-138">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="441f6-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="441f6-139">従業員のセルフ サービス パラメーターをコンフィグレーションする</span><span class="sxs-lookup"><span data-stu-id="441f6-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="441f6-140">**設定**の**給付金管理**ワーク スペースで、**パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="441f6-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="441f6-141">**従業員のセルフ サービス**タブで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="441f6-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="441f6-142">フィールド</span><span class="sxs-lookup"><span data-stu-id="441f6-142">Field</span></span> | <span data-ttu-id="441f6-143">説明</span><span class="sxs-lookup"><span data-stu-id="441f6-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="441f6-144">**給付金の検証**</span><span class="sxs-lookup"><span data-stu-id="441f6-144">**Benefit verification**</span></span> | <span data-ttu-id="441f6-145">セルフサービス給与金のチェックアウト中に使用する検証テキスト。</span><span class="sxs-lookup"><span data-stu-id="441f6-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="441f6-146">**被指名人の自動選択**</span><span class="sxs-lookup"><span data-stu-id="441f6-146">**Auto select designees**</span></span> | <span data-ttu-id="441f6-147">計画オプションに対する適格性に基づいて被扶養者と受益者を自動的に選択するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="441f6-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="441f6-148">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="441f6-148">Select **Save**.</span></span>
