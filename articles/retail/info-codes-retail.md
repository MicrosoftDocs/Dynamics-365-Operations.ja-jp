---
title: 情報コードおよび情報コード グループ
description: この記事は、情報コード、情報コード グループとその使用方法に関する概要を示します。
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6939ed56944ecafb29c1cadd2744b5746b19cb46
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023367"
---
# <a name="info-codes-and-info-code-groups"></a><span data-ttu-id="5ccd0-103">情報コードおよび情報コード グループ</span><span class="sxs-lookup"><span data-stu-id="5ccd0-103">Info codes and info code groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ccd0-104">この記事は、情報コード、情報コード グループとその使用方法に関する概要を示します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-104">This article provides an overview about info codes, info code groups, and how to use them.</span></span>

<span data-ttu-id="5ccd0-105">情報コードは、販売時点管理 (POS) レジスタでデータを取得する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-105">Info codes provide a way for you to capture data at a point-of-sale (POS) register.</span></span> <span data-ttu-id="5ccd0-106">品目の販売、品目の返品、または顧客の選択などの、POS でのさまざまなアクションの間に情報の入力をレジ担当者に求めるために、情報コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-106">You can use info codes to prompt the cashier to enter information during various actions at the POS, such as item sales, item returns, or selecting customers.</span></span> <span data-ttu-id="5ccd0-107">レジ担当者は一覧から入力を選択したり、それをコード、数値、日付、またはテキストとして入力できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-107">Cashiers can select input from a list or enter it as a code, number, date, or text.</span></span> <span data-ttu-id="5ccd0-108">情報コードは、定義済みの店舗アクション、小売品目、支払方法、顧客、または特定の販売時点管理活動に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-108">You can assign info codes to predefined store actions, retail items, payment methods, customers, or specific point-of-sale activities.</span></span> <span data-ttu-id="5ccd0-109">情報コードを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-109">You can use info codes to do the following:</span></span>

- <span data-ttu-id="5ccd0-110">フライト番号や返品の理由などの追加情報をトランザクション時に取得します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-110">Capture additional information at transaction time, such as a flight number or the reason for a return.</span></span>
- <span data-ttu-id="5ccd0-111">レジ担当者に特定の製品の価格の一覧から選択するように要求します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-111">Prompt the register cashier to select from a list of prices for specific products.</span></span>
- <span data-ttu-id="5ccd0-112">レジ担当者に特定の活動の実行時に入力を求める情報コードにサブコードを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-112">Link a subcode to an info code to prompt the cashier for input when performing a specific activity.</span></span> <span data-ttu-id="5ccd0-113">たとえば、顧客が製品を返品するとき、製品が返品される理由をレジ担当者が確認するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-113">For example, when a customer returns a product, you can prompt the cashier to ask why the product is being returned.</span></span> <span data-ttu-id="5ccd0-114">その後、サブコードを使用して、レジ担当者が選択できる理由の一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-114">Then you can use subcodes to display a list of reasons that the cashier can choose from.</span></span>
- <span data-ttu-id="5ccd0-115">通常の販売、割引販売、または無料製品として製品を販売します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-115">Sell a product as a regular sale, discounted sale, or free product.</span></span>
- <span data-ttu-id="5ccd0-116">販売操作を行なわずにレジスタのドロワーを開くと、キャッシャーは値を入力またはサブコードの一覧から選択するように促されます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-116">Prompt the cashier to enter a value or select from a list of subcodes when the register drawer is opened without performing a sales operation.</span></span>

## <a name="info-codes-group"></a><span data-ttu-id="5ccd0-117">情報コード グループ</span><span class="sxs-lookup"><span data-stu-id="5ccd0-117">Info codes group</span></span>

<span data-ttu-id="5ccd0-118">Retail で、情報コード グループを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-118">In Retail, you can create groups of info codes.</span></span> <span data-ttu-id="5ccd0-119">情報コード グループは、少ない情報コードを定義してより多目的な方法で情報コードを使用できるようにすることによって、柔軟性を増加させます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-119">Info code groups add flexibility by enabling you to define fewer info codes and then use them in more versatile ways.</span></span> <span data-ttu-id="5ccd0-120">情報コード グループは次の方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-120">You can use info code groups in the following ways:</span></span>

- <span data-ttu-id="5ccd0-121">少ない情報コードを定義して、簡単に再利用します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-121">Define fewer info codes and easily re-use them.</span></span> <span data-ttu-id="5ccd0-122">情報コード グループに含まれる情報コードは、他の情報コードとは定義済みの依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-122">Info codes that are included in info code groups have no predefined dependencies on other info codes.</span></span> <span data-ttu-id="5ccd0-123">同じ情報コードを複数の情報コード グループに含め、次に優先順位を使用してどの特定の状態でも意味の通る順序で同じ情報コードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-123">You can include the same info code in multiple info code groups and then use prioritization to present the same info codes in the order that makes sense in any particular situation.</span></span>
- <span data-ttu-id="5ccd0-124">情報コードをそのほかの情報コードまたは情報コード グループに関連付けて、シナリオごとに個別の情報コードまたはリンク情報コードを定義することなく必要とする方法で、製品またはトランザクションに関する情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-124">Link info codes to other info codes or info code groups to gather information about a product or transaction without having to define a separate info code or linked info code for each scenario.</span></span>

## <a name="info-code-examples"></a><span data-ttu-id="5ccd0-125">情報コードの例</span><span class="sxs-lookup"><span data-stu-id="5ccd0-125">Info code examples</span></span>

<span data-ttu-id="5ccd0-126">**例 1: 用情報コードの再利**</span><span class="sxs-lookup"><span data-stu-id="5ccd0-126">**Example 1: Reuse info codes**</span></span>

<span data-ttu-id="5ccd0-127">1 つの情報コードがトリガーされると別の情報コードがその直後にトリガーされるように、情報コードをリンクできます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-127">You can link info codes so that when one info code is triggered, another info code is triggered immediately after it.</span></span> <span data-ttu-id="5ccd0-128">たとえば、特定の製品を販売するとき、顧客が電池と製品の保証の購入を必要とするかどうかをレジ担当者に確認するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-128">For example, when you sell certain products, you can prompt the cashier to ask the customer if they want to purchase batteries and a product warranty.</span></span> <span data-ttu-id="5ccd0-129">他の製品の場合には、顧客が電池の購入を必要とするかどうかを確認するように、また顧客の郵便番号を収集するようにレジ担当者に要求できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-129">For other products, you can prompt the cashier to ask the customer if they want to purchase batteries and collect their postal code.</span></span> <span data-ttu-id="5ccd0-130">これらのシナリオに対してリンクされた情報コードを作成する場合、適切な情報を要求するようにレジ担当者に求めるために、情報コードのすべてのバリエーションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-130">If you create linked info codes for these scenarios, you must set up every variation of the info code so that the cashier is prompted to ask for the right information.</span></span> <span data-ttu-id="5ccd0-131">情報コード グループを使用する場合、電池が必要かどうかを確認するなどの共通の情報コードは一度設定すると、複数の情報コード グループで再利用できます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-131">If you use info code groups, common info codes, such as asking for batteries, can be set up once and then reused in multiple info code groups.</span></span> <span data-ttu-id="5ccd0-132">また、情報コード グループで優先順位を使用して、プロンプトが表示される順序を識別することもできます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-132">You can also use prioritization in the info code groups to identify the order in which the prompts are displayed.</span></span>

<span data-ttu-id="5ccd0-133">**例 2: 情報コードと情報コード グループの関連付け**</span><span class="sxs-lookup"><span data-stu-id="5ccd0-133">**Example 2: Link info codes to info code groups**</span></span>

<span data-ttu-id="5ccd0-134">モバイル デバイスなどの特定の製品を販売するとき、電話番号、携帯機器識別番号 (MEID)、およびシリアル番号などの一連の特定の情報を収集する必要が常にあります。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-134">When you sell certain products, for example mobile devices, you always want to collect a specific set of information, such as telephone number, mobile equipment identifier (MEID), and serial number.</span></span> <span data-ttu-id="5ccd0-135">ただし、タブレットと携帯電話を対比したさまざまな情報も収集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-135">However, you also want to collect different information for a tablet versus a mobile phone.</span></span> <span data-ttu-id="5ccd0-136">電話番号、MEID、およびシリアル番号に対するプロンプトを含む情報コード グループを設定し、情報コード グループを個別の情報コードに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-136">You can set up an info code group that includes prompts for the telephone number, MEID, and the serial number, and then link the info code group to an individual info code.</span></span> <span data-ttu-id="5ccd0-137">製品固有の情報コードがトリガーされると、次に情報コード グループがトリガーされ、各デバイスについてリンクされた複数のセットの情報コードを定義しなくても、共通データを収集できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5ccd0-137">When the product-specific info code is triggered, the info code group can be triggered next to enable you to collect the common data without having to define multiple sets of linked info codes for each device.</span></span>
