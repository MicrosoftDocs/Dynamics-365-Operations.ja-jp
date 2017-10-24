---
title: "バーコードの設定"
description: "この記事では、Microsoft Dynamics 365 for Retail でのバーコードの使用方法について説明します。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fdc56bf468babd4b0b0652d9791114af676c8470
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="87e19-103">バーコードの設定</span><span class="sxs-lookup"><span data-stu-id="87e19-103">Set up bar codes</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="87e19-104">この記事では、Microsoft Dynamics 365 for Retail でのバーコードの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87e19-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="87e19-105">バーコードを使用して、製品の購買および販売、製品バリアントの追跡、および顧客と従業員の設定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="87e19-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="87e19-106">また、バーコードを使用して、クーポン、ギフト カード、およびクレジット メモを発行して裏書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="87e19-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="87e19-107">標準バーコード、カスタム バーコード、社内バーコードを使用するように、小売製品を設定できます。</span><span class="sxs-lookup"><span data-stu-id="87e19-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="87e19-108">製品では、複数のバーコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="87e19-108">Products can have more than one bar code.</span></span> <span data-ttu-id="87e19-109">たとえば、製品をさまざまな製造業者から仕入れる場合、あるいは製品にサイズ、スタイル、または色に基づいたバリアントがある場合、製品で複数のバーコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="87e19-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="87e19-110">バーコードには、製品の重量や価格を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="87e19-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="87e19-111">バーコード マスクは、バーコードの作成に使用されるテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="87e19-111">Bar code masks are templates that are used to create bar codes.</span></span> <span data-ttu-id="87e19-112">**注記:** バリアントの組み合わせごとに固有のバーコードを割り当てる場合、レジスターで品目のバーコードをスキャンしたときに、製品のどのバリアントが販売されたかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="87e19-112">**Note:** If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="87e19-113">また、バリアント別に販売に関する統計を収集および表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="87e19-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="87e19-114">サイズ、色、およびスタイルの各グループに固有の番号を割り当てて、バーコードで識別できます。</span><span class="sxs-lookup"><span data-stu-id="87e19-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="87e19-115">Dynamics 365 for Retail はバーコード マスクを使用して、バリアントの組み合わせごとに自動的にバーコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="87e19-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="87e19-116">多くのサイズ、色、およびスタイルがある場合は、バリアント コードが追加されるたびに組み合わせが飛躍的に増加するため、この方法を使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="87e19-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="87e19-117">この機能を使用しない場合、製品バリアントを表す組み合わせごとに手動でバーコードを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="87e19-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span> <span data-ttu-id="87e19-118">バーコードは手動または自動で作成できます。</span><span class="sxs-lookup"><span data-stu-id="87e19-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="87e19-119">バーコードを作成するには、表示されている順序で次のタスクを行います。</span><span class="sxs-lookup"><span data-stu-id="87e19-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1.  <span data-ttu-id="87e19-120">[バーコード マスク文字の設定](set-up-bar-code-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="87e19-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2.  <span data-ttu-id="87e19-121">[バーコード マスクの設定](set-up-bar-code-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="87e19-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3.  <span data-ttu-id="87e19-122">バーコードの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="87e19-122">Configure bar code setups.</span></span>
4.  <span data-ttu-id="87e19-123">製品のバーコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="87e19-123">Create bar codes for products.</span></span>


<a name="see-also"></a><span data-ttu-id="87e19-124">参照</span><span class="sxs-lookup"><span data-stu-id="87e19-124">See also</span></span>
--------

[<span data-ttu-id="87e19-125">バーコード マスクの設定</span><span class="sxs-lookup"><span data-stu-id="87e19-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)




