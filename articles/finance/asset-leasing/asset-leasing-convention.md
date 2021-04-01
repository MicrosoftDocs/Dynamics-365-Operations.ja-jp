---
title: 資産リース規則
description: このトピックは、リース資産の規則について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237519"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="25702-103">資産リース規則</span><span class="sxs-lookup"><span data-stu-id="25702-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="25702-104">このトピックは、リース資産の規則について説明します。</span><span class="sxs-lookup"><span data-stu-id="25702-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="25702-105">リース規則は、リース帳簿の開始日を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="25702-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="25702-106">リース規則が **なし** に設定されている場合、開始日はリースの開始日と同じになります (**リース開始日** フィールドの値)。</span><span class="sxs-lookup"><span data-stu-id="25702-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="25702-107">リース規則が **満 1 か月** 設定されている場合、開始日はリースを開始した月の最初の日になります。</span><span class="sxs-lookup"><span data-stu-id="25702-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="25702-108">その開始日によって、負債償却および資産減価償却スケジュールの期間の開始日が決まります。</span><span class="sxs-lookup"><span data-stu-id="25702-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="25702-109">支払利息と減価償却費は、関連するスケジュールの期間終了日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="25702-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="25702-110">初期認識および調整仕訳入力は、開始日に転記されます。</span><span class="sxs-lookup"><span data-stu-id="25702-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="25702-111">リース規則機能は、機能管理でオンにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25702-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="25702-112">**管理機能** ワークスペースで、**資産リースのリース規則** 機能を探して選択し、**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25702-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="25702-113">リース規則は、リース資産帳簿の設定に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="25702-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="25702-114">リース規則を表示または割り当てるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="25702-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="25702-115">**資産リース \> 設定 \> リース帳簿** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="25702-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="25702-116">**リース規則** フィールドで、次のいずれかの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="25702-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="25702-117">リース規則</span><span class="sxs-lookup"><span data-stu-id="25702-117">Leasing convention</span></span> | <span data-ttu-id="25702-118">説明</span><span class="sxs-lookup"><span data-stu-id="25702-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="25702-119">None</span><span class="sxs-lookup"><span data-stu-id="25702-119">None</span></span>               | <span data-ttu-id="25702-120">開始日はリースの開始日と同じ日付なので、負債償却スケジュールと資産減価償却スケジュールの初日はリースの開始日です。</span><span class="sxs-lookup"><span data-stu-id="25702-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="25702-121">終了日は 1 か月後です。</span><span class="sxs-lookup"><span data-stu-id="25702-121">The end date is one month later.</span></span> <span data-ttu-id="25702-122">リース規則は、利息が毎月の最終日に転記されることを保証しません。</span><span class="sxs-lookup"><span data-stu-id="25702-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="25702-123">全月</span><span class="sxs-lookup"><span data-stu-id="25702-123">Full month</span></span>         | <span data-ttu-id="25702-124">開始日をその月のどの日付でも設定できるリースの場合、負債償却スケジュールおよび資産減価償却スケジュールでは、その月の初日に経費が発生します。</span><span class="sxs-lookup"><span data-stu-id="25702-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="25702-125">このリース規則により、その月全体の利息が各月の最終日に発生します。</span><span class="sxs-lookup"><span data-stu-id="25702-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="25702-126">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25702-126">Select **Save**.</span></span>

<span data-ttu-id="25702-127">リースが作成されると、リース用に入力された開始日と、帳簿に対して指定されているリース規則に基づいて、各帳簿の開始日が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="25702-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]