---
title: 固定資産の一括更新
description: 帳簿を使用した場合、同じ減価償却簿の一部である資産グループの減価償却方法を変更できます。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30b9aaaabcac09c9147c350422924a23f785c0ce
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178638"
---
# <a name="fixed-asset-mass-update"></a><span data-ttu-id="b27a9-103">固定資産の一括更新</span><span class="sxs-lookup"><span data-stu-id="b27a9-103">Fixed asset mass update</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b27a9-104">帳簿を使用した場合、同じ減価償却簿の一部である資産グループの減価償却方法を変更できます。</span><span class="sxs-lookup"><span data-stu-id="b27a9-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="b27a9-105">たとえば、米国でその年の第 4 四半期に供用された資産が 40% を超える場合、四半期の期中の減価償却方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27a9-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="b27a9-106">一括更新プロセスを使用して、新しい減価償却方法が必要な資産すべてを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b27a9-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="b27a9-107">資産の減価償却方法を更新した場合、これらの資産に存在するすべての減価償却トランザクションは削除されます。</span><span class="sxs-lookup"><span data-stu-id="b27a9-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="b27a9-108">また、これらの資産の減価償却調整トランザクション、特別償却トランザクション、および特別減価償却トランザクションもすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="b27a9-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="b27a9-109">既に処理された資産の減価償却方法を更新するには、既存の処分トランザクションを最初に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27a9-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="b27a9-110">また、処分プロセスにより生成されたすべてのトランザクションも削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b27a9-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="b27a9-111">資産の減価償却方法を更新した後、資産ごとに減価償却および特別減価償却の処理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="b27a9-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="b27a9-112">調整が必要な場合は、手動で減価償却調整を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="b27a9-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>




