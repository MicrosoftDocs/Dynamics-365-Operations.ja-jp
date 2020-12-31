---
title: リース帳簿の設定
description: このトピックでは、リース帳簿で管理される情報について説明します。 リース帳簿には、システム内でのリースの計上方法を決定する会計ポリシーが含まれています。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445385"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="d9b82-104">リース帳簿の設定</span><span class="sxs-lookup"><span data-stu-id="d9b82-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9b82-105">リース帳簿には、システム内でのリースの計上方法を決定する会計ポリシーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9b82-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="d9b82-106">現金主義会計に加えて、資産リースは次の基準をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d9b82-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="d9b82-107">米国の一般会計原則 (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="d9b82-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="d9b82-108">Accounting Standards Codification Topic 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="d9b82-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="d9b82-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="d9b82-109">ASC 840</span></span>
- <span data-ttu-id="d9b82-110">国際財務報告標準 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="d9b82-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="d9b82-111">国際会計標準 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="d9b82-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="d9b82-112">リース帳簿を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d9b82-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="d9b82-113">**資産リース \> 設定 \> リース帳簿** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="d9b82-114">**新規** を選択して帳簿を追加します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="d9b82-115">次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-115">Set the following fields.</span></span>

    | <span data-ttu-id="d9b82-116">氏名</span><span class="sxs-lookup"><span data-stu-id="d9b82-116">Name</span></span>                                     | <span data-ttu-id="d9b82-117">説明</span><span class="sxs-lookup"><span data-stu-id="d9b82-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="d9b82-118">転記階層</span><span class="sxs-lookup"><span data-stu-id="d9b82-118">Posting layer</span></span>                            | <span data-ttu-id="d9b82-119">使用する転記階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-119">Select the posting layer to use.</span></span> <span data-ttu-id="d9b82-120">リースに関連付けられている各帳簿は、特定の転記階層に対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="d9b82-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="d9b82-121">各転記階層には、さまざまな転記目的があります。</span><span class="sxs-lookup"><span data-stu-id="d9b82-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="d9b82-122">リース タイプ</span><span class="sxs-lookup"><span data-stu-id="d9b82-122">Lease type</span></span>                               | <span data-ttu-id="d9b82-123">リースを自動的に分類するか、またはファイナンスおよびオペレーティング リースのどちらとして定義するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="d9b82-124">会計フレームワーク</span><span class="sxs-lookup"><span data-stu-id="d9b82-124">Accounting framework</span></span>                     | <span data-ttu-id="d9b82-125">帳簿に関連付けられているフレームワークを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="d9b82-126">リース期間/耐用年数の設定</span><span class="sxs-lookup"><span data-stu-id="d9b82-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="d9b82-127">リースの種類が **自動** に設定されている場合、および資産の耐用年数におけるリース期間がこのフィールドに入力された割合以上である場合、システムはリースをファイナンス リースとして分類します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="d9b82-128">現在の価値/資産の公正価値の設定</span><span class="sxs-lookup"><span data-stu-id="d9b82-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="d9b82-129">リースのタイプを決定するしきい値を定義するには、整数を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="d9b82-130">将来の最小リース支払の現在の値が、帳簿の設定で定義されたユーザー定義の値よりも大きく、かつ、その帳簿のリース分類が自動に設定されている場合は、リースがファイナンス リースとして分類されます。</span><span class="sxs-lookup"><span data-stu-id="d9b82-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="d9b82-131">短期的しきい値</span><span class="sxs-lookup"><span data-stu-id="d9b82-131">Short-term threshold</span></span>                     | <span data-ttu-id="d9b82-132">短期リースのしきい値として使用する月数を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="d9b82-133">リース期間がここで入力した月数以下である場合は、システムによってリースが短期リースとして分類され、繰延賃貸処置が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9b82-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="d9b82-134">少額しきい値</span><span class="sxs-lookup"><span data-stu-id="d9b82-134">Low value threshold</span></span>                      | <span data-ttu-id="d9b82-135">少額リースのしきい値として使用する金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b82-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="d9b82-136">資産の公平価値がここで入力した値以下である場合、またはその値である場合は、システムによってリースが少額リースとして分類され、繰延賃貸処置が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9b82-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="d9b82-137">仕入先に支払う</span><span class="sxs-lookup"><span data-stu-id="d9b82-137">Pay to vendor</span></span>                            | <span data-ttu-id="d9b82-138">このオプションを **はい** に設定すると、各リースで指定された仕入先勘定に対して、請求書としてリース支払を転記できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d9b82-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="d9b82-139">リース支払を転記すると、仕入先勘定の貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d9b82-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="d9b82-140">このオプションを **いいえ** に設定した場合は、**リース転記パラメーター** ページの **リース支払** 転記タイプに指定された勘定が代わりに貸方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="d9b82-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
