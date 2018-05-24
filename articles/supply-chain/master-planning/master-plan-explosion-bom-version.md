---
title: "BOM バージョンの展開"
description: "この記事では、部品表 (BOM) のバージョンの展開を含むマスター プランのシナリオを説明します。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 80c9fa6ec98bd2cdc3edd5329e2a619ef9cc8cb2
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="7b15a-103">BOM バージョンの展開</span><span class="sxs-lookup"><span data-stu-id="7b15a-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b15a-104">この記事では、部品表 (BOM) のバージョンの展開を含むマスター プランのシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="7b15a-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="7b15a-105">BOM バージョンの需要展開は、特定サイト (および場合によっては特定倉庫) における各 BOM 明細行品目に対する需要を作ります。</span><span class="sxs-lookup"><span data-stu-id="7b15a-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="7b15a-106">サイト固有 BOM では、各 BOM 明細行に対して、特定の倉庫が定義される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7b15a-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="7b15a-107">また、各 BOM 明細行に対し、倉庫が必要かどうかが品目の分析コード設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="7b15a-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="7b15a-108">その後、結果としての各 BOM 明細行品目に対する需要は、追加の需要展開の開始点となります。</span><span class="sxs-lookup"><span data-stu-id="7b15a-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="7b15a-109">このマスター計画シナリオの前提条件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="7b15a-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="7b15a-110">サイト分析コードが必須であり、需要トランザクションで入力する必要がある。</span><span class="sxs-lookup"><span data-stu-id="7b15a-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="7b15a-111">サイト分析コードが一貫している。</span><span class="sxs-lookup"><span data-stu-id="7b15a-111">The site dimension is consistent.</span></span> <span data-ttu-id="7b15a-112">したがって、下位レベル需要のサイトは、初期需要トランザクションのサイトと同じである。</span><span class="sxs-lookup"><span data-stu-id="7b15a-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="7b15a-113">次の図は、マスタ プラン需要展開のプロセス方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7b15a-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![BOM バージョンを使用した展開が必要    ](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="7b15a-115">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7b15a-115">Additional resources</span></span>
--------

[<span data-ttu-id="7b15a-116">マスター プラン - BOM バージョンを決定する方法</span><span class="sxs-lookup"><span data-stu-id="7b15a-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="7b15a-117">マスタ プランとマルチサイト機能</span><span class="sxs-lookup"><span data-stu-id="7b15a-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




