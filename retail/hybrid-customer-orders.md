---
title: Hybrid customer orders
description: "ハイブリッド顧客注文が顧客によって店舗の実行できると製品が製品を含む単一実行するか、または後で出荷される注文。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hybrid customer orders

ハイブリッド顧客注文が顧客によって店舗の実行できると製品が製品を含む単一実行するか、または後で出荷される注文。

、Microsoft Dynamics 365で[小売し、実行するか、すべての製品の値を実行する顧客注文の選択した製品を選択できます。 注文を作成したら実行されるように自動的に請求するマークされた製品ラインはには、この注文が作成された後ピックアップ順序に対して同じです。 ハイブリッド順序で未払金額が実行の行の総額のピッキングおよび出荷の製品ラインの預金残高の割合の追加によって決まります。 ハイブリッド注文の場合は、顧客注文のモードで現金払モードの間で次のように切替えます:

-   買い物カゴのすべての製品が**配送を実行します。**設定され、注文は現金払トランザクションとして処理されます。
-   買い物カゴのいずれかまたはすべての行を選択または** ** **出荷の配送**設定され、注文は顧客注文トランザクションとして処理されます。

その配送方法の特定の買い物カゴの行のみが設定されますが、買い物カゴの行が、選択した**選択**オンの場合、**出荷は、選択した**、または**選択したCarry out **選択されます。 この場合、工程の下流の流れは通常どおりに従います。 ただし、**選択は、選択した**、**出荷は、選択した**、または**選択したCarry out **すべての買い物カゴ品目のリスト。選択した買い物カゴの行がない場合、新しいページが開きます。 この画面で、配送方法を設定するには、複数の行を一度に選択できます。 行を選択するには、この方法を使用すると、行に割り当てられた、前の配送方法が上書きされます。

<a name="see-also"></a>参照
--------

[顧客注文の概要] (顧客注文overview.md) 


