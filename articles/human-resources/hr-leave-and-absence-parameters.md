---
title: 休暇パラメーターのコンフィギュレーション
description: Dynamics 365 Human Resources で休暇のための人事管理パラメーターを定義します。
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
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009657"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="50018-103">休暇パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="50018-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="50018-104">Dynamics 365 Human Resources で休暇計画を設定する前に、下記を含むすべての関連する人事管理パラメーターの設定を確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="50018-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="50018-105">休暇申請の番号順序</span><span class="sxs-lookup"><span data-stu-id="50018-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="50018-106">育児介護休業法 (FMLA) 設定</span><span class="sxs-lookup"><span data-stu-id="50018-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="50018-107">休暇申請のための従業員セルフ サービス設定</span><span class="sxs-lookup"><span data-stu-id="50018-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="50018-108">休暇および欠勤パラメーター</span><span class="sxs-lookup"><span data-stu-id="50018-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="50018-109">人事管理パラメーターの表示および変更</span><span class="sxs-lookup"><span data-stu-id="50018-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="50018-110">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="50018-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="50018-111">**設定**で、**人事管理パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="50018-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="50018-112">**番号順序**タブで、**休暇申請 ID** のための**番号順序コード**を確認し、必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="50018-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="50018-113">この設定により、休暇申請に自動的に ID を割り当てるために使用される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="50018-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="50018-114">**FMLA** タブで、FMLA の設定を確認し必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="50018-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="50018-115">**従業員セルフ サービス** タブで、マネージャーが従業員に代わって休暇申請を入力できるようにするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="50018-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="50018-116">**休暇**タブで設定を確認し、必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="50018-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="50018-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50018-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="50018-118">カレンダー パラメーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="50018-118">Configure calendar parameters</span></span>

<span data-ttu-id="50018-119">休暇カレンダー プレビュー機能を有効にした場合、追加のパラメータをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50018-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="50018-120">2020 年 2 月 3 日のプレビュー リリースでは、**保留中の休暇申請**のみ有効になっています。</span><span class="sxs-lookup"><span data-stu-id="50018-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="50018-121">**休暇および欠勤**のページで、**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="50018-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="50018-122">**設定**で、**人事管理パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="50018-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="50018-123">**カレンダー** タブで、カレンダーの設定を必要に応じて変更します。</span><span class="sxs-lookup"><span data-stu-id="50018-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="50018-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50018-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="50018-125">参照</span><span class="sxs-lookup"><span data-stu-id="50018-125">See also</span></span>

- [<span data-ttu-id="50018-126">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="50018-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
