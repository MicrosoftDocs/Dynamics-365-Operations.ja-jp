---
title: 元帳カレンダーの変更または再割り当て
description: このトピックでは、元帳に現在割り当てられているカレンダーを変更する方法と、新しいカレンダーを元帳に割り当てる方法について説明します。
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039953"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="cf173-103">元帳カレンダーの変更または再割り当て</span><span class="sxs-lookup"><span data-stu-id="cf173-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf173-104">このトピックでは、元帳に現在割り当てられているカレンダーを変更する方法と、新しいカレンダーを元帳に割り当てる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf173-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="cf173-105">問題</span><span class="sxs-lookup"><span data-stu-id="cf173-105">Issue</span></span>

<span data-ttu-id="cf173-106">会社は、元帳に割り当てられている既存のカレンダーを変更するか、新しいカレンダーを割り当てる必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="cf173-107">解決策</span><span class="sxs-lookup"><span data-stu-id="cf173-107">Resolution</span></span>

<span data-ttu-id="cf173-108">元帳カレンダーの変更または再割り当てには、2 つのシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="cf173-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="cf173-109">最初のシナリオでは、元帳に既に割り当てられている既存のカレンダーを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="cf173-110">2 つ目のシナリオでは、新しいカレンダーを作成して元帳に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="cf173-111">どちらの変更も、トランザクションが元帳に転記された後でも、いつでも実行できます。</span><span class="sxs-lookup"><span data-stu-id="cf173-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="cf173-112">既存の会計カレンダーの変更</span><span class="sxs-lookup"><span data-stu-id="cf173-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="cf173-113">元帳に割り当てられている既存のカレンダーを変更するには、**一般会計 \> 元帳の設定 \> 元帳** に移動し、会計カレンダーのリンクを選択して **元帳カレンダー** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="cf173-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="cf173-114">カレンダーに対して行える変更には制限があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="cf173-115">たとえば、年の *期間* の開始日と終了日を変更できますが、カレンダーの *年* の開始日と終了日変更できます。</span><span class="sxs-lookup"><span data-stu-id="cf173-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="cf173-116">年の期間を変更するには、適切なカレンダーと年を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf173-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="cf173-117">最初に、**期間の削除** ボタンを使用して、既存の決算期間の一部またはすべてを削除します。</span><span class="sxs-lookup"><span data-stu-id="cf173-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="cf173-118">1 つ目以外のすべての決算期間は削除できます。</span><span class="sxs-lookup"><span data-stu-id="cf173-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="cf173-119">次に、**期間の分割** ボタンを使用し、次の期間の適切な開始日を入力して残りの期間または期間を新しい期間に分割します。</span><span class="sxs-lookup"><span data-stu-id="cf173-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="cf173-120">カレンダーの期間を変更した後、カレンダーが割り当てられているすべての法人 (会社) で **元帳期間の再計算** プロセスを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="cf173-121">警告メッセージでこの手順を完了するように通知されませんが、一般会計の転記済の各トランザクションに割り当てられている期間を更新するには、再計算プロセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="cf173-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="cf173-122">再計算プロセスを実行するには、各会社の **元帳の設定** ページで **元帳期間の再計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf173-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="cf173-123">再計算プロセスを実行しない場合、試算表または財務諸表のトランザクション残高が誤って期間に含まれる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="cf173-124">この場合は、再計算プロセスを実行していつでも残高を修正できます。</span><span class="sxs-lookup"><span data-stu-id="cf173-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="cf173-125">新しい会計カレンダーの割り当て</span><span class="sxs-lookup"><span data-stu-id="cf173-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="cf173-126">新しい会計カレンダーを割り当てるには、**一般会計 \> 元帳の設定 \> 元帳** に移動し、**編集** を選択して **元帳** ページを編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="cf173-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="cf173-127">次に、**会計カレンダー** で新しい会計カレンダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf173-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="cf173-128">元帳の会計カレンダーを変更した後に、**元帳期間の再計算** を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="cf173-129">元帳に新しい会計カレンダーを割り当てると、この手順を完了するように通知するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf173-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="cf173-130">このメッセージで再計算プロセスがオプションであると示していると思われる場合でも、オプションではありません。</span><span class="sxs-lookup"><span data-stu-id="cf173-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="cf173-131">一般会計の転記済の各トランザクションに割り当てられている期間を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="cf173-132">再計算プロセスを実行するには、**元帳の設定** ページで **元帳期間の再計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf173-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="cf173-133">再計算プロセスを実行しない場合、試算表または財務諸表のトランザクション残高が誤って期間に含まれる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="cf173-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="cf173-134">この場合は、再計算プロセスを実行していつでも残高を修正できます。</span><span class="sxs-lookup"><span data-stu-id="cf173-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
