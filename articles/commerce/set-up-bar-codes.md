---
title: バーコードの設定
description: この記事は、Dynamics 365 Commerce でのバーコードの使用方法について説明します。
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 74a08fc168dd3c41fa501ca8110af899a181e333
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023188"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="83c78-103">バーコードの設定</span><span class="sxs-lookup"><span data-stu-id="83c78-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83c78-104">この記事は、Dynamics 365 Commerce でのバーコードの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83c78-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="83c78-105">バーコードを使用して、製品の購買および販売、製品バリアントの追跡、および顧客と従業員の設定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="83c78-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="83c78-106">また、バーコードを使用して、クーポン、ギフト カード、およびクレジット メモを発行して裏書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="83c78-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="83c78-107">標準バーコード、カスタム バーコード、社内バーコードを使用するように、小売製品を設定できます。</span><span class="sxs-lookup"><span data-stu-id="83c78-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="83c78-108">製品では、複数のバーコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="83c78-108">Products can have more than one bar code.</span></span> <span data-ttu-id="83c78-109">たとえば、製品をさまざまな製造業者から仕入れる場合、あるいは製品にサイズ、スタイル、または色に基づいたバリアントがある場合、製品で複数のバーコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="83c78-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="83c78-110">バーコードには、製品の重量や価格を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="83c78-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="83c78-111">バーコード マスクは、バーコードの作成に使用されるテンプレートです。</span><span class="sxs-lookup"><span data-stu-id="83c78-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="83c78-112">バリアントの組み合わせごとに固有のバーコードを割り当てる場合、レジスターで品目のバーコードをスキャンしたときに、製品のどのバリアントが販売されたかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="83c78-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="83c78-113">また、バリアント別に販売に関する統計を収集および表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="83c78-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="83c78-114">サイズ、色、およびスタイルの各グループに固有の番号を割り当てて、バーコードで識別できます。</span><span class="sxs-lookup"><span data-stu-id="83c78-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="83c78-115">Retail はバーコード マスクを使用して、バリアントの組み合わせごとに自動的にバーコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="83c78-115">Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="83c78-116">多くのサイズ、色、およびスタイルがある場合は、バリアント コードが追加されるたびに組み合わせが飛躍的に増加するため、この方法を使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="83c78-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="83c78-117">この機能を使用しない場合、製品バリアントを表す組み合わせごとに手動でバーコードを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="83c78-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="83c78-118">バーコードは手動または自動で作成できます。</span><span class="sxs-lookup"><span data-stu-id="83c78-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="83c78-119">バーコードを作成するには、表示されている順序で次のタスクを行います。</span><span class="sxs-lookup"><span data-stu-id="83c78-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="83c78-120">[バーコード マスク文字の設定](set-up-bar-code-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="83c78-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="83c78-121">[バーコード マスクの設定](set-up-bar-code-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="83c78-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="83c78-122">バーコードの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="83c78-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="83c78-123">製品のバーコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="83c78-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83c78-124">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="83c78-124">Additional resources</span></span>

[<span data-ttu-id="83c78-125">バーコード マスクの設定</span><span class="sxs-lookup"><span data-stu-id="83c78-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
