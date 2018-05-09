---
title: "生産出荷場所"
description: "このトピックでは、生産出荷場所を識別するために使用される階層について説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ef820db6cdb2ce485ded0dbca9635af5c68403c6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="production-output-location"></a><span data-ttu-id="0f785-103">生産出荷場所</span><span class="sxs-lookup"><span data-stu-id="0f785-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f785-104">このトピックでは、生産出荷場所を識別するために使用される階層について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f785-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="0f785-105">生産出荷場所は、完成品が生産された後に最初に保管される場所です。</span><span class="sxs-lookup"><span data-stu-id="0f785-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="0f785-106">通常、この場所は完成品を生産する生産工程の近くにあります。</span><span class="sxs-lookup"><span data-stu-id="0f785-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="0f785-107">生産出荷場所は、出荷エリア、保管場所、下流生産プロセスの生産入庫場所などに移動する前に、品目の中間保管として使用されます。</span><span class="sxs-lookup"><span data-stu-id="0f785-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="0f785-108">既定の生産出荷場所は、完成品が製造オーダーまたはバッチ オーダーで報告されたときに設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f785-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="0f785-109">次の階層を使用して、この出荷場所を識別します。</span><span class="sxs-lookup"><span data-stu-id="0f785-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="0f785-110">製造オーダーまたはバッチの注文ヘッダーで定義されている出荷場所を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f785-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="0f785-111">そこに場所が見つからない場合は、本番ルートで定義されている最後の操作により使用されているリソースで定義されている出荷場所を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f785-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="0f785-112">そこに場所が見つからない場合は、本番ルートで定義されている最後の操作のリソースにより使用されているリソース グループで定義されている出荷場所を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f785-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="0f785-113">そこに場所が見つからない場合は、製造オーダーに定義されている倉庫で定義されている出荷場所を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f785-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="0f785-114">既定の生産出荷場所は、高度な倉庫プロセスを使用して設定されている製品にのみ設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f785-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="0f785-115">このタイプの品目が完了報告されると、[**商品の保存を完了**] または [**連産品および副産物の保存**] タイプの倉庫作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="0f785-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="0f785-116">このタイプの作業は、ピッキング場所として生産出荷場所を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f785-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="0f785-117">プット アウェイの場所は、場所ディレクティブによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="0f785-117">The put-away location is determined by the location directives.</span></span>

