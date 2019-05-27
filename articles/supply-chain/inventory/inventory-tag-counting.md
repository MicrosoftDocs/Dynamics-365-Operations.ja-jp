---
title: 在庫タグ棚卸
description: この記事は、倉庫の実際の内容と手持在庫の比較に使用する、タグ棚卸に関する情報を提供します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff899d0e6d94287c0f1924fe1787189d79c09f4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570837"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="11c27-103">在庫タグ棚卸</span><span class="sxs-lookup"><span data-stu-id="11c27-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="11c27-104">この記事は、倉庫の実際の内容と手持在庫の比較に使用する、タグ棚卸に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="11c27-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="11c27-105">**タグ棚卸**ページの行を作成することにより、1 から 500 の番号など、各在庫品目にタグ番号を付けます。</span><span class="sxs-lookup"><span data-stu-id="11c27-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="11c27-106">カウント中に、対応するタグの品目番号と数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="11c27-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="11c27-107">また、このタグは、タグ棚卸仕訳帳で入力する際の基準として使用できます。</span><span class="sxs-lookup"><span data-stu-id="11c27-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="11c27-108">タグ棚卸仕訳帳を転記すると、**棚卸** ページに新しい棚卸仕訳帳が作成されます。</span><span class="sxs-lookup"><span data-stu-id="11c27-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="11c27-109">新しい仕訳帳は、作成したタグ棚卸仕訳帳明細行に基づきます。</span><span class="sxs-lookup"><span data-stu-id="11c27-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="11c27-110">特定の在庫分析コードにより品目をタグ棚卸するには、タグ棚卸仕訳帳を作成したときに表示される **分析コードの表示** ページの分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="11c27-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="11c27-111">たとえば、特定の倉庫の品目の棚卸では、**倉庫** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="11c27-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="11c27-112">**在庫および倉庫管理パラメーター** ページの **棚卸中に品目をロック** スライダーをオンにすると、棚卸中に品目が現物的に更新できません。</span><span class="sxs-lookup"><span data-stu-id="11c27-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="11c27-113">ただし、タグ棚卸仕訳帳の品目は、棚卸中にロックされません。</span><span class="sxs-lookup"><span data-stu-id="11c27-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="11c27-114">在庫トランザクションは、タグ棚卸明細行が棚卸仕訳帳に転記および転送されるまで、作成されません。</span><span class="sxs-lookup"><span data-stu-id="11c27-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="11c27-115">タグが順不同で入力されている場合に、欠落しているタグを確認するには、**タグ** 列のヘッダーをクリックして、タグで行を並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="11c27-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="additional-resources"></a><span data-ttu-id="11c27-116">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="11c27-116">Additional resources</span></span>
--------

[<span data-ttu-id="11c27-117">循環棚卸</span><span class="sxs-lookup"><span data-stu-id="11c27-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
