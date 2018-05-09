---
title: "標準原価の原価計算バージョンの制限"
description: "このトピックでは、標準原価の原価計算バージョンに適用する制限について説明します。"
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: adc77f632fecebc39e818fa38f78071842ec8de4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="1975e-103">標準原価の原価計算バージョンの制限</span><span class="sxs-lookup"><span data-stu-id="1975e-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1975e-104">このトピックでは、標準原価の原価計算バージョンに適用する制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="1975e-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="1975e-105">次の制限は、標準原価原則への保証の順守に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1975e-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="1975e-106">品目の原価には、費用が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1975e-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="1975e-107">製造品目の費用は、部品表 (BOM) および工順情報内の償却済固定費を表します。</span><span class="sxs-lookup"><span data-stu-id="1975e-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="1975e-108">したがって、これらの費用を単位原価に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1975e-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="1975e-109">購買品目の費用も品目の単位原価に含まれます。</span><span class="sxs-lookup"><span data-stu-id="1975e-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="1975e-110">製造品目の標準原価の計算は、標準原価の原価バージョン内の原価レコードに基づく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1975e-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="1975e-111">原価データの代わりのソースは、購入品目の購入価格売買契約などのように、予定原価の原価バージョンのみで使用できます。</span><span class="sxs-lookup"><span data-stu-id="1975e-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="1975e-112">原価データの代わりのソースは、BOM 計算グループによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="1975e-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="1975e-113">BOM の計算は、単一レベル展開モードで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1975e-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="1975e-114">標準原価の品目原価データは、標準原価または予定原価を含む別の原価バージョンにコピーできます。</span><span class="sxs-lookup"><span data-stu-id="1975e-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="1975e-115">ただし、このトピックで先に示した制限は予定原価には適用されないので、予定原価に対する品目原価データは、標準原価を含む原価バージョンにはコピーできません。</span><span class="sxs-lookup"><span data-stu-id="1975e-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="1975e-116">関連トピック</span><span class="sxs-lookup"><span data-stu-id="1975e-116">Related topics</span></span>
--------

[<span data-ttu-id="1975e-117">原価バージョン</span><span class="sxs-lookup"><span data-stu-id="1975e-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="1975e-118">非製造環境での標準原価を更新</span><span class="sxs-lookup"><span data-stu-id="1975e-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="1975e-119">製造品目の標準原価を管理するための準備</span><span class="sxs-lookup"><span data-stu-id="1975e-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


