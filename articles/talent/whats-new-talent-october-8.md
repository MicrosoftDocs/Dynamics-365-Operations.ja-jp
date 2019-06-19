---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 8 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 34216e2181915cf615e6e77fa2a10d06a4e9db85
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617275"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-8-2018"></a><span data-ttu-id="615d9-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 8 日)</span><span class="sxs-lookup"><span data-stu-id="615d9-103">What's new or changed in Dynamics 365 for Talent Core HR (October 8, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="615d9-104">**ビルド 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="615d9-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="615d9-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="615d9-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="615d9-106">休暇層基準 (休暇管理) で他の日付を使用する許可</span><span class="sxs-lookup"><span data-stu-id="615d9-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="615d9-107">従業員への報奨休暇の場合、報奨層基準によって従業員が見越計上する休暇時間が決定されます。</span><span class="sxs-lookup"><span data-stu-id="615d9-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="615d9-108">現在、これらの層は従業員の開始日および勤続日数に基づいています。</span><span class="sxs-lookup"><span data-stu-id="615d9-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="615d9-109">一部のシナリオにおいて、組織には、これらの層が記念日または元の採用日付などの、他の日付に基づいているようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="615d9-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="615d9-110">これらの日付は、見越計上が発生する時を決定するために休暇計画で既に使用されており、これら同じ日付が従業員が計画に登録される時に使用される機能は、見越計上金額を決定するために追加されています。</span><span class="sxs-lookup"><span data-stu-id="615d9-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="615d9-111">その他の変更</span><span class="sxs-lookup"><span data-stu-id="615d9-111">Other changes</span></span>
<span data-ttu-id="615d9-112">その他の修正プログラムは今回のリリースに含まれています。</span><span class="sxs-lookup"><span data-stu-id="615d9-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="615d9-113">既知の問題</span><span class="sxs-lookup"><span data-stu-id="615d9-113">Known issue</span></span>

<span data-ttu-id="615d9-114">**問題:** 作業者に新しい添付ファイルを追加する場合、**新規**および**編集**ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="615d9-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="615d9-115">**作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="615d9-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="615d9-116">(この問題は次のプラットフォーム更新プログラムで修正されます。)</span><span class="sxs-lookup"><span data-stu-id="615d9-116">(This issue will be fixed in the next platform update.)</span></span>
