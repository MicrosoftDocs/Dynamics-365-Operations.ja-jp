---
title: 複数のエンティティ マップの管理
description: この記事では、複数のエンティティ マップを選択し、依存エンティティ マップの一覧を表示し、エンティティ マップとそれに関連するすべてのエンティティを有効にし、さらに既存のデータをコピーする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7ba2adbeeb5deb4abbbe77174691eb8aa22a773
ms.sourcegitcommit: d62e52484dfd9913a75a4561766d5e22fe2f3e8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2020
ms.locfileid: "3689524"
---
# <a name="manage-multiple-entity-maps"></a><span data-ttu-id="6ff43-103">複数のエンティティ マップの管理</span><span class="sxs-lookup"><span data-stu-id="6ff43-103">Manage multiple entity maps</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="6ff43-104">この記事では、複数のエンティティ マップを選択し、依存エンティティ マップの一覧を表示し、エンティティ マップとそれに関連するすべてのエンティティを有効にし、さらに既存のデータをコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ff43-104">This article describes how to select multiple entity maps, view a list of dependent entity maps, enable the entity maps and all of its related entities, and copy pre-existing data.</span></span>

<span data-ttu-id="6ff43-105">日常業務の一部として、エンティティ マップを一括処理する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="6ff43-105">As part of day to day operations, there may be a need to bulk handle entity maps.</span></span> <span data-ttu-id="6ff43-106">たとえば、一連のエンティティ マップを同時に有効化または一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="6ff43-106">For example, you may want to simultaneously enable or pause a set of entity maps.</span></span> <span data-ttu-id="6ff43-107">これを 1 つ行う代わりに、煩雑で時間がかかりますが、二重書き込みリスト ページで複数のエンティティ マップを同時に有効化、一時停止、再開、または停止することができます。</span><span class="sxs-lookup"><span data-stu-id="6ff43-107">Instead of doing this one by one, which is cumbersome and time consuming, you can now enable, pause, resume, or stop more than one entity map at the same time in the dual-write list page.</span></span>

![複数のエンティティ マップを選択](media/select-multiple-entity-maps.png)
 
<span data-ttu-id="6ff43-109">複数のエンティティ マップを有効にすると共に、**関連エンティティ マップの表示**を選択することによって、すべての依存エンティティ マップの一覧を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="6ff43-109">As part of enabling multiple entity maps, you also get to view the list of all the dependent entity maps by selecting **Show related entity map(s)**.</span></span>

![関連するエンティティ マップの表示](media/show-related-entity-map.png)
 
<span data-ttu-id="6ff43-111">選択したエンティティ マップとそれに関連するすべてのエンティティを有効にするには、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6ff43-111">To enable the selected entity map and all its related entities, select **Run**.</span></span> <span data-ttu-id="6ff43-112">選択したエンティティマップまたはその依存に対応する既存のデータをコピーする場合は、**初期同期**に対応するチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="6ff43-112">If you want to copy the pre-existing data for the selected entity maps or its dependents, select the corresponding **Initial sync** check box.</span></span> <span data-ttu-id="6ff43-113">または、チェック ボックスをオフにして、1 つ以上の関連エンティティの選択を解除します。</span><span class="sxs-lookup"><span data-stu-id="6ff43-113">Alternatively, remove one or more of the related entities by clearing the corresponding check box.</span></span> <span data-ttu-id="6ff43-114">エンティティ マップをドラッグ アンド ドロップして、同期されるマップの順序を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="6ff43-114">You can also drag and drop the entity maps to change the order in which the maps will be synced.</span></span>
