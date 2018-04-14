---
title: "分析コード メンバーの共通セットに対する原価要素分析コード メンバーのマップ"
description: "異なる原価要素分析コード メンバーに、原価要素分析コード メンバーの共通セットをマッピングすると、分析に使用する共通の形式でデータをマージします。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1c867e1b5f908772d721e349ea148b7e5fc7d9fc
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="f2f98-103">分析コード メンバーの共通セットに対する原価要素分析コード メンバーのマップ</span><span class="sxs-lookup"><span data-stu-id="f2f98-103">Map cost element dimension members to a common set of dimension members</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f2f98-104">異なる原価要素分析コード メンバーに、原価要素分析コード メンバーの共通セットをマッピングすると、分析に使用する共通の形式でデータをマージします。</span><span class="sxs-lookup"><span data-stu-id="f2f98-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="f2f98-105">グローバル会社で、法律の会計要件に準拠している場合は、複数の勘定科目表を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2f98-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="f2f98-106">さまざまな勘定科目表から原価要素分析コード メンバーをインポートすると、勘定の組み合わせが発生します。</span><span class="sxs-lookup"><span data-stu-id="f2f98-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="f2f98-107">ただし、これらの勘定は、実際に同じ性質を持ち、共通の形式を使用して原価を分析および割り当てる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f2f98-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="f2f98-108">原価要素分析コード メンバーに共通の形式をマップします</span><span class="sxs-lookup"><span data-stu-id="f2f98-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="f2f98-109">次の例では、原価コントローラーとして、原価要素分析コード メンバーを米国の勘定科目表の構造やフランスの勘定科目表の構造から原価要素分析コード メンバーの共通のセットにマッピングする原価計算で、新しい原価要素分析コードを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f2f98-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="f2f98-110">その後、原価要素分析コード メンバーの共通セットを使用して、原価会計元帳の 2 つの法人から原価データを分析することができます。</span><span class="sxs-lookup"><span data-stu-id="f2f98-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="f2f98-111">ソース: 米国の勘定科目表</span><span class="sxs-lookup"><span data-stu-id="f2f98-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="f2f98-112">ソース: フランスの勘定科目表</span><span class="sxs-lookup"><span data-stu-id="f2f98-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="f2f98-113">原価要素分析コード メンバーの新しい共通セット</span><span class="sxs-lookup"><span data-stu-id="f2f98-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="f2f98-114">米国の勘定科目表からインポートされた原価要素分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="f2f98-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="f2f98-115">フランスの勘定科目表からインポートされた原価要素分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="f2f98-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="f2f98-116">米国とフランスの原価要素分析コード メンバーの共通セットへのマッピング</span><span class="sxs-lookup"><span data-stu-id="f2f98-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="f2f98-117">5001: 販売</span><span class="sxs-lookup"><span data-stu-id="f2f98-117">5001: Sales</span></span>                                                           | <span data-ttu-id="f2f98-118">5001: 販売と広告</span><span class="sxs-lookup"><span data-stu-id="f2f98-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="f2f98-119">5000: 販売と広告</span><span class="sxs-lookup"><span data-stu-id="f2f98-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="f2f98-120">5030: 広告</span><span class="sxs-lookup"><span data-stu-id="f2f98-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="f2f98-121">6390: 在庫発注\*</span><span class="sxs-lookup"><span data-stu-id="f2f98-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="f2f98-122">7000: クリーニング費用</span><span class="sxs-lookup"><span data-stu-id="f2f98-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="f2f98-123">7001: クリーニング費用</span><span class="sxs-lookup"><span data-stu-id="f2f98-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="f2f98-124">7001: 旅費交通費</span><span class="sxs-lookup"><span data-stu-id="f2f98-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="f2f98-125">7001: 旅費交通費</span><span class="sxs-lookup"><span data-stu-id="f2f98-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="f2f98-126">\*在庫発注のフランスの原価要素分析コード メンバーは、マッピングされません。</span><span class="sxs-lookup"><span data-stu-id="f2f98-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="f2f98-127">通貨の換算</span><span class="sxs-lookup"><span data-stu-id="f2f98-127">Currency conversion</span></span>
<span data-ttu-id="f2f98-128">使用するさまざまな勘定科目表は、異なる通貨を使用するように設定されたかもしれません。</span><span class="sxs-lookup"><span data-stu-id="f2f98-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="f2f98-129">この場合に、必ず通貨換算を指定してください、原価データは、原価要素分析コード メンバーが使用した原価会計元帳で正しい通貨を使用して処理されます。</span><span class="sxs-lookup"><span data-stu-id="f2f98-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="f2f98-130">前の例では、原価会計元帳で米ドル (USD) が使用された場合、マップされた原価要素分析コード メンバーのトランザクションを処理するために USD からユーロ (EUR) の通貨換算を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2f98-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="f2f98-131">いつでもマッピングを更新</span><span class="sxs-lookup"><span data-stu-id="f2f98-131">Update mappings at any time</span></span>
<span data-ttu-id="f2f98-132">いつでも原価要素分析コードのためのマッピングの定義を更新できます。</span><span class="sxs-lookup"><span data-stu-id="f2f98-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="f2f98-133">マッピングは、日付が有効ではないので、変更は次回原価トランザクションを処理、または原価計算を実行の時に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f2f98-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




