---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2019 年 1 月 23 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4e492095d5269ec81c0c22145b7af356937c256b
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742519"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="d7a24-103">Dynamics 365 for Talent Core HR の新機能および変更された機能 (2019 年 1 月 23 日)</span><span class="sxs-lookup"><span data-stu-id="d7a24-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d7a24-104">**ビルド 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="d7a24-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="d7a24-105">このトピックでは、Core HR の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7a24-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="d7a24-106">変更</span><span class="sxs-lookup"><span data-stu-id="d7a24-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="d7a24-107">新規固定報酬レコードの作成時に、従業員の固定報酬のインポートは機能しません</span><span class="sxs-lookup"><span data-stu-id="d7a24-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="d7a24-108">インポート時の報酬レベルを取得するために、従業員固定報酬のエンティティに変更が加えられました。</span><span class="sxs-lookup"><span data-stu-id="d7a24-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="d7a24-109">このリリースより前は、レベルが必要であることを示すメッセージが表示されていました。</span><span class="sxs-lookup"><span data-stu-id="d7a24-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="d7a24-110">休暇申請ダイアログ ボックスから最小残高フィールドを削除します</span><span class="sxs-lookup"><span data-stu-id="d7a24-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="d7a24-111">**最小残高**フィールドは、**休暇申請**ダイアログ ボックスから削除されました。</span><span class="sxs-lookup"><span data-stu-id="d7a24-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="d7a24-112">この変更は、休暇要求可能なすべての領域に影響します。</span><span class="sxs-lookup"><span data-stu-id="d7a24-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="d7a24-113">報酬レベルのデータ アップグレードはすべてのシナリオで更新されません</span><span class="sxs-lookup"><span data-stu-id="d7a24-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="d7a24-114">固定報酬プランの報酬レベルを更新するための変更が行われました。</span><span class="sxs-lookup"><span data-stu-id="d7a24-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="d7a24-115">この変更により、従業員に割り当てられたジョブの固定プランに対する報酬レベルが設定されます。</span><span class="sxs-lookup"><span data-stu-id="d7a24-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="d7a24-116">給与情報の変更ページではシステム管理者としてログインする時のみ使用できます</span><span class="sxs-lookup"><span data-stu-id="d7a24-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="d7a24-117">この変更により、給与管理者のロールを持つ従業員は、その職位の**変更のタイムライン > 変更の管理**ページ上の給与情報にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="d7a24-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="d7a24-118">ジョブ フィールドを職位に設定</span><span class="sxs-lookup"><span data-stu-id="d7a24-118">Job fields default to positions</span></span>
<span data-ttu-id="d7a24-119">ある職位でジョブを変更すると、ジョブ フィールドはその職位に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d7a24-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="d7a24-120">既定値をそのまま使用するか、またはそれらのフィールドの既存の値をそのまま使用するかを選択できるよう警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d7a24-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="d7a24-121">猶予期間およびカレンダーは、将来採用される従業員には表示されません。</span><span class="sxs-lookup"><span data-stu-id="d7a24-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="d7a24-122">この変更により、**猶予期間**および**カレンダー** フィールドが**変更の管理**ページに追加され、将来および過去の従業員のデータデータ入力が可能になりました。</span><span class="sxs-lookup"><span data-stu-id="d7a24-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="d7a24-123">プラットフォーム update 23</span><span class="sxs-lookup"><span data-stu-id="d7a24-123">Platform update 23</span></span>
<span data-ttu-id="d7a24-124">マイナーなバグ修正は、プラットフォーム更新プログラム 23 の一部として含まれています。</span><span class="sxs-lookup"><span data-stu-id="d7a24-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="d7a24-125">詳細については、[新機能および変更された機能 Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (1月2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d7a24-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 
