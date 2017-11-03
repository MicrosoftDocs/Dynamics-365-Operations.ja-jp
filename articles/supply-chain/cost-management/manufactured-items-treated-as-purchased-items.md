---
title: "生産または調達する製品を設定する"
description: "製品はさまざまな方法で提供できます。製品は生産 (製造) または調達 (購買) できます。 この記事は、複数の調達をサポートするために、製品の構成時に考慮する一般的な点について説明します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5ed8c93c13746249605ad8742549c23bb1e0e10
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="e0f7b-104">生産または調達する製品を設定する</span><span class="sxs-lookup"><span data-stu-id="e0f7b-104">Set up products that can be produced or procured</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e0f7b-105">製品はさまざまな方法で提供できます。製品は生産 (製造) または調達 (購買) できます。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="e0f7b-106">この記事は、複数の調達をサポートするために、製品の構成時に考慮する一般的な点について説明します。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="e0f7b-107">複数の調達は、通常、購買品目がまれにしか製造されない場合や、主として製造されていた品目が変更になり現在の主とした購買品目になった場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="e0f7b-108">最初に、品目は、部品表 (BOM) と工順情報を定義し、品目の製造オーダーをサポートするために、製造品目として指定されます。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="e0f7b-109">生産タイプは **BOM** に設定します (または、製造プロセスの場合、**式** または **連産品**)。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="e0f7b-110">標準原価を使用すると、品目原価レコードは製造品目に対して計算できます。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="e0f7b-111">ただし、品目原価レコードは、購入目標にする標準原価と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="e0f7b-112">その場合、必要な標準原価を手動で入力し、品目原価レコードに対して有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="e0f7b-113">原価計算には、会計年度期間中に製品の供給の組み合わせを示し、差異を経時的に最小限にするような特別な BOM とルーティングの使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="e0f7b-114">さらに、あるサイトの製造品目を別のサイトに転送することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="e0f7b-115">したがって、品目の転送先となるサイトに対して品目の原価を手動で入力して有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="e0f7b-116">製造品目を上位レベルの製品のコンポーネントとして使用する場合、コンポーネントのコストは購入品目として取り扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="e0f7b-117">このガイドラインは、コンポーネントのコストが計算されたか、手動で入力されたかどうかに関係なく当てはまります。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="e0f7b-118">つまり、BOM 計算では、品目のコストを、品目の部品表と工順の情報に基づいて計算するのではなく、購入したコンポーネントとして扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> <span data-ttu-id="e0f7b-119">品目に割り当てられている BOM 計算グループに埋め込まれている**展開の停止**フラグを選択することで、この計算を行わないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="e0f7b-120">マスタ スケジューリング計算が品目を通して要件を展開しないようにするには、品目補充または補充グループの展開フェンスを 0 (ゼロ) 日に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="e0f7b-121">マスター スケジューリングの計算は、品目を購入品目として扱い、それ以上部品表および工順情報に対する計算を行いません。</span><span class="sxs-lookup"><span data-stu-id="e0f7b-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






