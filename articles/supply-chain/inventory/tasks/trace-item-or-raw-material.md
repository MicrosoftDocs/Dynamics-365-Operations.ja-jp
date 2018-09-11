--- 
title: "品目または原材料の追跡"
description: "この手順は、品目の追跡を使用して、品目または原材料が使用された場所または使用されている場所を識別する方法を示します。"
author: pjacobse
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d7eb282ddf9597385d6660a3fc0ef73f403ab898
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="trace-an-item-or-raw-material"></a>品目または原材料の追跡

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、品目の追跡を使用して、品目または原材料が使用された場所または使用されている場所を識別する方法を示します。 この手順を使用すると、品目を識別し、ソースまで過去方向に追跡してから、完成品の生産と販売まで将来方向に追跡できます。 このプロセスは、影響を受ける顧客、販売注文などの調査に使用できます。 この手順では、デモ データの会社 USP2 を使用します。


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a>既知のバッチ番号を使用して品目を過去方向に追跡
1. [在庫管理] > [照会およびレポート] > [追跡用分析コード] > [品目の追跡] の順に選択します。
2. [品目番号] フィールドで [P9100] を選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [次方向または前方向] のフィールドで [前] を選択します。
5. [バッチ番号] フィールドで、[as-12-344-01] を選択します。
6. 一覧で、選択された行のリンクをクリックします。
7. [OK] をクリックします。

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a>品目を識別し、将来方向に追跡し、分析を行う
    * ツリーのトップ ノードは、選択された品目とバッチの手持数量を表します。 後方向追跡を実行する必要がある品目を検索するには、ツリーのノードを展開する必要があります。   
1. ツリーで、[以下に説明されたノード、次に最後のノードを選択する] を展開します。
    * 「P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101」 を展開し、次にそのノードを選択します。     
2. ツリーで、[以下に説明されたノード、次にそのノードを選択する] を展開します。
    * 先ほど選択したノードから開始します。「M9103 ● 生産ライン B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01」を展開し、次にそのノードを選択します。  
3. [ノードから追跡] をクリックします。
4. [次] をクリックします。
5. [アクション] ウィンドウで、[追跡] をクリックします。
    * 追跡する品目により影響を受ける顧客に関する情報、および出荷済み品目と未出荷品目に関連する販売品目に関する情報を提供する複数の追跡オプションがあります。   
6. [顧客] をクリックします。
7. ページを閉じます。
8. [アクション] ウィンドウで、[追跡] をクリックします。
9. [未出荷の販売注文] をクリックします。
10. ページを閉じます。


