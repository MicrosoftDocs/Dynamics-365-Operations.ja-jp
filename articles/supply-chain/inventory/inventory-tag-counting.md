---
title: "在庫タグ棚卸"
description: "この記事は、倉庫の実際の内容と手持在庫の比較に使用する、タグ棚卸に関する情報を提供します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1b1281c41e3427148cdbd7bd874f3408056e3df1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="inventory-tag-counting"></a>在庫タグ棚卸

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

この記事は、倉庫の実際の内容と手持在庫の比較に使用する、タグ棚卸に関する情報を提供します。

**タグ棚卸**ページの行を作成することにより、1 から 500 の番号など、各在庫品目にタグ番号を付けます。 カウント中に、対応するタグの品目番号と数量を入力します。 また、このタグは、タグ棚卸仕訳帳で入力する際の基準として使用できます。 タグ棚卸仕訳帳を転記すると、**棚卸** ページに新しい棚卸仕訳帳が作成されます。 新しい仕訳帳は、作成したタグ棚卸仕訳帳明細行に基づきます。 特定の在庫分析コードにより品目をタグ棚卸するには、タグ棚卸仕訳帳を作成したときに表示される **分析コードの表示** ページの分析コードを選択します。 たとえば、特定の倉庫の品目の棚卸では、**倉庫** チェック ボックスをオンにします。 **在庫および倉庫管理パラメーター** ページの **棚卸中に品目をロック** スライダーをオンにすると、棚卸中に品目が現物的に更新できません。 ただし、タグ棚卸仕訳帳の品目は、棚卸中にロックされません。 在庫トランザクションは、タグ棚卸明細行が棚卸仕訳帳に転記および転送されるまで、作成されません。 タグが順不同で入力されている場合に、欠落しているタグを確認するには、**タグ** 列のヘッダーをクリックして、タグで行を並べ替えます。

<a name="additional-resources"></a>その他のリソース
--------

[循環棚卸](../warehousing/cycle-counting.md)

