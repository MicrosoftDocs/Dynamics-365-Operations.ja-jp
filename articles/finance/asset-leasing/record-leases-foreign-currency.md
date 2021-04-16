---
title: 外貨でのリースの記録
description: このトピックでは、会計またはレポート通貨以外の通貨でのリースの記録方法について説明します。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7f1f9153d627eba4c3c79a764cffec6a2f008818
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819749"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="a2225-103">外貨でのリースの記録</span><span class="sxs-lookup"><span data-stu-id="a2225-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2225-104">会計通貨、またはレポート通貨以外の通貨でのリースの資産リース会計は、**元帳の設定** ページで設定されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="a2225-105">すべてのリースは、トランザクション通貨で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2225-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="a2225-106">つまり、リース契約で指定された通貨で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2225-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="a2225-107">このトピックでは、会計またはレポート通貨以外の通貨でのリースの記録方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2225-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="a2225-108">外貨でリースを入力すると、使用権 (ROU) 資産が会計通貨とレポート通貨の両方で償却されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="a2225-109">これらの通貨は、**元帳の設定** ページでコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="a2225-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="a2225-110">この動作は、固定資産でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="a2225-111">外貨でリースを作成する場合は、**通貨** フィールドでトランザクション通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2225-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="a2225-112">会計通貨の為替レートは、**会計通貨の為替レート** フィールドの既定値になります。</span><span class="sxs-lookup"><span data-stu-id="a2225-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="a2225-113">レポート通貨の為替レートは、**レポート通貨の為替レート** フィールドの既定値になります。</span><span class="sxs-lookup"><span data-stu-id="a2225-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="a2225-114">これらの為替レートは、リースの開始日に有効になりました。</span><span class="sxs-lookup"><span data-stu-id="a2225-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="a2225-115">**会計通貨の為替** レートと **レポート通貨の為替レート** フィールドは、**リースの詳細** ページの **財務情報とレポート交換情報** クイックタブにあります。</span><span class="sxs-lookup"><span data-stu-id="a2225-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="a2225-116">**固定レート** チェックボックスをオンにして、自動的に入力された為替レートを上書きし、新しいレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="a2225-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="a2225-117">その他のフィールドで、リースに必要な情報を入力し、**スケジュールの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2225-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="a2225-118">新しい **リースの詳細** ページで、**帳簿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2225-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="a2225-119">**リース帳簿** ページの **財務と報告の情報** タブで、**会計通貨の最初の使用権資産** フィールドと **レポート通貨の最初の使用権資産** フィールドを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2225-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="a2225-120">これらの各フィールドには、対応する通貨での換算済使用権資産残高が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="a2225-121">財務情報を変更するたびに、これらのフィールドが更新されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="a2225-122">支払スケジュールを確認する前に **スケジュールを作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2225-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="a2225-123">最初の認識仕訳入力には、リースに一覧表示されている通貨為替レートを使用する使用権資産が記録されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="a2225-124">また、仕訳入力には、**会計通貨の最初の追加の資産** フィールドと、**レポート通貨の最初の使用権資産** フィールドの値も含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2225-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="a2225-125">外貨リースの後続測定</span><span class="sxs-lookup"><span data-stu-id="a2225-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="a2225-126">減価償却スケジュールには、レポート通貨、会計通貨、およびトランザクション通貨で予想される減価償却経費金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="a2225-127">使用権資産残高および減価償却額をレポート通貨または会計通貨のいずれかで表示するには、**資産の償却スケジュール** ページを開き、**会計通貨金額の表示** チェックボックスまたは **通貨金額のレポート** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a2225-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="a2225-128">外貨で換算されたリースに対して減価償却経費仕訳入力を作成すると、この入力には、リースに一覧表示された為替レートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="a2225-129">また、仕訳入力には、**会計通貨の最初の使用権資産** フィールドと、**レポート通貨の最初の使用権資産** フィールドの値も含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2225-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="a2225-130">減価償却経費の最終金額は、わずかに異なる為替レートを使用して計算することができるため、会計通貨とレポート通貨の両方で使用権資産が完全に償却されます。</span><span class="sxs-lookup"><span data-stu-id="a2225-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="a2225-131">リースが **繰延賃料** として再分類されている場合、会計上およびレポート通貨の為替レートが既に定義されている場合、システムによって自動的にその為替レートがクリアされます。</span><span class="sxs-lookup"><span data-stu-id="a2225-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]