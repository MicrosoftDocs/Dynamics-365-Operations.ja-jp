---
title: "連結バッチ オーダー (複数)"
description: "この記事は、連結バッチ注文の概念について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 49c2df19168855e6e6ab9ff061bcdce698947b20
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="97c4e-103">連結バッチ オーダー (複数)</span><span class="sxs-lookup"><span data-stu-id="97c4e-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97c4e-104">この記事は、連結バッチ注文の概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="97c4e-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="97c4e-105">生産されたバルク品目は親品目とみなされますが、梱包済み品目は子品目とみなされます。</span><span class="sxs-lookup"><span data-stu-id="97c4e-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="97c4e-106">バルク品目と梱包済み品目の関係は、バルク品変換に示されます。</span><span class="sxs-lookup"><span data-stu-id="97c4e-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="97c4e-107">このバルク品変換はバルク品目自体に定義されます。</span><span class="sxs-lookup"><span data-stu-id="97c4e-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="97c4e-108">梱包済み品目は、単一サイズのコンテナーに梱包することも、1 つの単位と見なされる複数サイズのコンテナーに梱包することもできます。</span><span class="sxs-lookup"><span data-stu-id="97c4e-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="97c4e-109">バルク品目の注文を連結することで関連するすべてのバッチ オーダーを 1 つのビューで表示できるため、未完了の作業を特定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="97c4e-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="97c4e-110">連結バッチ オーダーは次の注文の組み合わせを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="97c4e-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="97c4e-111">1 つのバルク オーダーと複数の梱包オーダー</span><span class="sxs-lookup"><span data-stu-id="97c4e-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="97c4e-112">複数のバルク オーダーと複数の梱包オーダー</span><span class="sxs-lookup"><span data-stu-id="97c4e-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="97c4e-113">複数のバルク オーダーと 1 つの梱包オーダー</span><span class="sxs-lookup"><span data-stu-id="97c4e-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="97c4e-114">梱包オーダーのみ</span><span class="sxs-lookup"><span data-stu-id="97c4e-114">Only packed orders</span></span>





