---
title: "請求書の合計価格の照合における差異を解決"
description: 
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8773773d9686bf5061958fbe414ed1fef7288f81
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>請求書の合計価格の照合における差異を解決

[!include[banner](../includes/banner.md)]




請求書照合の検証の一つのタイプは、請求合計の照合です。 システムが請求合計の照合をするよう指定するには、[**買掛金勘定パラメータ**] ページの [**請求書の検証**] タブで [**請求合計の照合**] オプションを [**はい**] に設定します。 

合計請求書の照合により、合計請求書金額が、許容差を超えて予測金額から逸脱していないことを確認できます。 6 つの合計が [**請求合計照合の詳細**] ページで比較されます。 合計のいずれかが、対応する発注書の合計予想金額から逸脱すると、照合不一致にフラグが立ちます。 

合計の照合不一致のある請求書を確認するには、[**仕入先請求書の入力**] ワークスペースで [**保留中の請求書**] のタイルをクリックします。 その後、アクション ペインの [**確認**] タブで [**照合の詳細**] をクリックします。 照合不一致が検出された場合に、警告アイコンが請求金額の横に表示されます。 請求合計照合の詳細を表示して合計に関する詳細を表示できます。 

不一致を識別した後で、請求書の情報が間違っていると思う場合には、仕入先に連絡する必要があるかもしれません。 その結果の仕入先との合意に応じて、次のいずれかのアクションを実行できます。

-   価格差異を受け入れ、照合不一致のある請求書を転記する。 照合不一致がある場合、転記する前に承認を要求するようにシステムが設定されている場合があります。 この場合、照合不一致を承認し、必要に応じて承認コメントを入力できます。 その後、請求書を転記する選択ができます。
-   請求書金額を想定される金額に改訂し、請求書を転記する。
-   仕入先にフル クレジットと訂正した新しい請求書を要求する。





