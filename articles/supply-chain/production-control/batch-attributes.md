---
title: バッチ属性 (複数)
description: このトピックは、バッチ属性に関する情報を提供します。 バッチ属性は、在庫バッチを構成する原材料および完成製品の特性です。 この記事は、バッチ属性の割り当て方法と、バッチの引当を行うときにそれらを検索する方法も説明します。
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370893e415a79091404f1c4eb0404ba8fd5b9ff2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017531"
---
# <a name="batch-attributes"></a><span data-ttu-id="5df18-105">バッチ属性 (複数)</span><span class="sxs-lookup"><span data-stu-id="5df18-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5df18-106">このトピックは、バッチ属性に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5df18-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="5df18-107">バッチ属性は、在庫バッチを構成する原材料および完成製品の特性です。</span><span class="sxs-lookup"><span data-stu-id="5df18-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="5df18-108">この記事は、バッチ属性の割り当て方法と、バッチの引当を行うときにそれらを検索する方法も説明します。</span><span class="sxs-lookup"><span data-stu-id="5df18-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="5df18-109">バッチ属性は、在庫バッチを構成する原材料および完成製品の特性です。</span><span class="sxs-lookup"><span data-stu-id="5df18-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="5df18-110">バッチ属性は環境条件、バッチの生産に使用される原材料の品質、完成品の結果などの要因によって異なります。</span><span class="sxs-lookup"><span data-stu-id="5df18-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="5df18-111">使用されるバッチ属性の数とタイプは、業界によって大きく異なります。</span><span class="sxs-lookup"><span data-stu-id="5df18-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="5df18-112">以下はバッチ属性の 2 つの使用例です。</span><span class="sxs-lookup"><span data-stu-id="5df18-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="5df18-113">チーズ業界でチーズを生産するための原材料の 1 つとして使用される牛乳は、脂肪分や重量パーセントなどの属性を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="5df18-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="5df18-114">牛乳から生産されたチーズは、水分や年数などの属性を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="5df18-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="5df18-115">鉄鋼業界で生産される鉄は、マグネシウム、銀、および亜鉛の含有比率などの属性を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="5df18-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="5df18-116">属性の数とタイプをより上手に管理するために、バッチ属性グループを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5df18-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="5df18-117">これにより、各属性を個別に追加する必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="5df18-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="5df18-118">バッチ属性の割り当て</span><span class="sxs-lookup"><span data-stu-id="5df18-118">Assign batch attributes</span></span>
<span data-ttu-id="5df18-119">在庫バッチの属性を在庫バッチで扱われる個々の製品に割り当てるか、それらを特定の顧客に関連付けられた製品に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5df18-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="5df18-120">顧客レベルでバッチ属性を割り当てる前に、製品レベルで割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5df18-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="5df18-121">製品は、 追跡用分析コード グループで **有効** に設定されたバッチ分析コードが必要です。</span><span class="sxs-lookup"><span data-stu-id="5df18-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="5df18-122">個々の製品にバッチ属性を割り当てるには、製品固有ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="5df18-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="5df18-123">属性が顧客の製品に固有な場合、顧客固有ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="5df18-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="5df18-124">製品に属性を追加する場合、他のパラメータを定義します。</span><span class="sxs-lookup"><span data-stu-id="5df18-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="5df18-125">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="5df18-125">Here are some examples:</span></span>

-   <span data-ttu-id="5df18-126">**整数** または **小数** タイプ属性の最小値と最大値幅。</span><span class="sxs-lookup"><span data-stu-id="5df18-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="5df18-127">**整数** または **小数** タイプの属性の許容アクション。</span><span class="sxs-lookup"><span data-stu-id="5df18-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="5df18-128">属性の値が最小と最大の範囲外にある場合、アクションは警告メッセージまたはエラー メッセージのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="5df18-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="5df18-129">属性のターゲット値。</span><span class="sxs-lookup"><span data-stu-id="5df18-129">The target value for the attribute.</span></span> <span data-ttu-id="5df18-130">この値は、属性の最適な値であり、すべての属性タイプに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5df18-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="5df18-131">[製品情報管理] の **リリースされた製品** リスト ページで選択する商品についてのページを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5df18-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="5df18-132">製品へのバッチ属性を割り当てた後、 **在庫バッチ属性** ページの属性に特定の値を追加できます。</span><span class="sxs-lookup"><span data-stu-id="5df18-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="5df18-133">バッチ引当</span><span class="sxs-lookup"><span data-stu-id="5df18-133">Reserve batches</span></span>
<span data-ttu-id="5df18-134">顧客の注文を満たすための販売注文のバッチの引当を行うときや、製造オーダーでバッチのピッキングや引当を行うとき、バッチ属性で検索できます。</span><span class="sxs-lookup"><span data-stu-id="5df18-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="5df18-135">検索では、必要なバッチ属性を持つ製品を含む在庫バッチを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5df18-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="5df18-136">バッチを見つけた後、元の在庫トランザクション明細行に製品を引当できます。</span><span class="sxs-lookup"><span data-stu-id="5df18-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



