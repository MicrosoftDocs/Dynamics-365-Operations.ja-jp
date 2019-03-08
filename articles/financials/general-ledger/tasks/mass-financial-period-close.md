---
title: 財務期間一括終了
description: この手順では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "311384"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="9f60e-103">財務期間一括終了</span><span class="sxs-lookup"><span data-stu-id="9f60e-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f60e-104">この手順では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-104">This procedure shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="9f60e-105">またこのタスクは、特定のモジュールに転記されたユーザー グループを制限する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="9f60e-106">[総勘定元帳] > [期間の締め] > [元帳カレンダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-106">Go to General ledger > Period close > Ledger calendars.</span></span>
    * <span data-ttu-id="9f60e-107">表示された法人の一覧は、ページで選択した会計カレンダーに依存することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="9f60e-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="9f60e-108">選択された会計カレンダーを使用する法人のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9f60e-108">Only legal entities using the selected fiscal calendar will display.</span></span>  
2. <span data-ttu-id="9f60e-109">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f60e-109">Click Edit.</span></span>
3. <span data-ttu-id="9f60e-110">状態を変更する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="9f60e-111">状態を更新する法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-111">Select the legal entities for which you want to update the status.</span></span>
    * <span data-ttu-id="9f60e-112">グリッドの左上のチェック マークを選択することにより、すべての法人をすばやく選択できます。</span><span class="sxs-lookup"><span data-stu-id="9f60e-112">You can quickly select all legal entities  by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="9f60e-113">[モジュール アクセスの更新] を選択して、選択されたモジュールへのアクセスの転記を定義します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-113">Select Update module access to define the posting access to a selected module.</span></span>
    * <span data-ttu-id="9f60e-114">モジュールの状態は、グリッドのレコードを編集することにより順番に更新できます。</span><span class="sxs-lookup"><span data-stu-id="9f60e-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="9f60e-115">ボタンは、複数の法人のレコードをすばやく更新する場合に役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="9f60e-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="9f60e-116">[アプリケーション モジュール] フィールドで、状態を更新するモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-116">In the Application module, select the module that you want to update the status.</span></span> <span data-ttu-id="9f60e-117">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f60e-117">Click Select.</span></span>
7. <span data-ttu-id="9f60e-118">[アクセス レベル] で、[すべて]、[なし]、または特定のユーザー グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-118">In the Access level, select All, None, or a specific user group.</span></span> <span data-ttu-id="9f60e-119">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f60e-119">Click Select.</span></span>
    * <span data-ttu-id="9f60e-120">[すべて] は、オープン期間の場合、モジュールの編集アクセス許可を持つすべてのユーザーが転記できることを示します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="9f60e-121">[なし] は、オープン期間の場合、ユーザーがモジュールに転記できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="9f60e-122">[特定のユーザー グループ] は、オープン期間の場合に、このグループのユーザーのみがモジュールに転記できることを示します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="9f60e-123">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f60e-123">Click Update.</span></span>
9. <span data-ttu-id="9f60e-124">状態を更新する別の期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="9f60e-125">状態を更新する法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="9f60e-126">[期間の状態の更新] を選択し、状態を [保留中]、[未処理]、または [完全に終了] に設定します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-126">Select Update period status and set the status of On hold, Open, or Permanently closed.</span></span>
    * <span data-ttu-id="9f60e-127">[オープン] は、ユーザーにアクセス許可がある場合に転記できる期間を示します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-127">Open indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="9f60e-128">[保留中] は、期間は転記できないが、再度開くことができることを意味します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-128">On hold means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="9f60e-129">[完全に閉じる] は、期間が終了され、開くことができないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="9f60e-129">Permanently closed means the period is closed and can never be opened.</span></span> <span data-ttu-id="9f60e-130">調整は転記できません。</span><span class="sxs-lookup"><span data-stu-id="9f60e-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="9f60e-131">すべての調整と監査が完了するまで、期間を [完全に閉じる] と設定しないようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9f60e-131">We do not recommend setting a period to Permanently closed until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="9f60e-132">[更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9f60e-132">Click Update.</span></span>

