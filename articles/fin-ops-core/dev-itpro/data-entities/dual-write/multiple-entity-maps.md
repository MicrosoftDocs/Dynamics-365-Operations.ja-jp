---
title: 複数のテーブル マップの管理
description: このトピックでは、テーブル マップの選択、依存テーブル マップの一覧表示、テーブル マップとそれに関連するすべてのテーブルの有効化、および既存のデータをコピーする方法について説明します。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f52294e0a59d8b69f5dd32bb78ba96afd9733ca2
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128373"
---
# <a name="manage-multiple-table-maps"></a><span data-ttu-id="7b0a1-103">複数のテーブル マップの管理</span><span class="sxs-lookup"><span data-stu-id="7b0a1-103">Manage multiple table maps</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="7b0a1-104">この記事では、複数のテーブル マップを選択し、依存テーブル マップの一覧を表示し、テーブル マップとそれに関連するすべてのテーブルを有効にし、さらに既存のデータをコピーする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-104">This article describes how to select multiple table maps, view a list of dependent table maps, enable the table maps and all of its related tables, and copy pre-existing data.</span></span>

<span data-ttu-id="7b0a1-105">日常業務の一部として、テーブル マップを一括処理する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-105">As part of day to day operations, there may be a need to bulk handle table maps.</span></span> <span data-ttu-id="7b0a1-106">たとえば、一連のテーブル マップを同時に有効化または一時停止することができます。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-106">For example, you may want to simultaneously enable or pause a set of table maps.</span></span> <span data-ttu-id="7b0a1-107">これを 1 つずつ行うのは煩雑で時間がかかるので、代わりに、二重書き込みリスト ページで複数のテーブル マップを同時に有効化、一時停止、再開、または停止することができます。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-107">Instead of doing this one by one, which is cumbersome and time consuming, you can now enable, pause, resume, or stop more than one table map at the same time in the dual-write list page.</span></span>

![複数のテーブル マップの選択](media/select-multiple-entity-maps.png)
 
<span data-ttu-id="7b0a1-109">複数のテーブル マップを有効にすると共に、**関連テーブル マップの表示** を選択することによって、すべての依存テーブル マップの一覧を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-109">As part of enabling multiple table maps, you also get to view the list of all the dependent table maps by selecting **Show related table map(s)**.</span></span>

![関連するテーブル マップの表示](media/show-related-entity-map.png)
 
<span data-ttu-id="7b0a1-111">選択したテーブル マップとそれに関連するすべてのテーブルを有効にするには、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-111">To enable the selected table map and all its related tables, select **Run**.</span></span> <span data-ttu-id="7b0a1-112">選択したテーブル マップまたはその依存に対応する既存のデータをコピーする場合は、**初期同期** に対応するチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-112">If you want to copy the pre-existing data for the selected table maps or its dependents, select the corresponding **Initial sync** check box.</span></span> <span data-ttu-id="7b0a1-113">または、チェック ボックスをオフにして、1 つ以上の関連テーブルの選択を削除します。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-113">Alternatively, remove one or more of the related tables by clearing the corresponding check box.</span></span> <span data-ttu-id="7b0a1-114">テーブル マップをドラッグ アンド ドロップして、同期されるマップの順序を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="7b0a1-114">You can also drag and drop the table maps to change the order in which the maps will be synced.</span></span>
