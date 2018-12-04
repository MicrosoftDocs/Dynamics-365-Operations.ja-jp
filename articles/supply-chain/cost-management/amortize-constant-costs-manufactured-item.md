---
title: "製造品目の固定費の償却"
description: "製造品目の固定費は、工程の段取り時間と、数量または仕損金額が一定のコンポーネントを反映します。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 75c0f5bcff0aae63aa8c7dae9b0767f8c7e6a81c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a>製造品目の固定費の償却

[!include [banner](../includes/banner.md)]

製造品目の固定費は、工程の段取り時間と、数量または仕損金額が一定のコンポーネントを反映します。 

製造品目の算出原価の中でこれらの固定費を償却するために、原価ロット サイズという概念が使用されます。 この概念には複数の同義語があり、その 1 つが会計ロット サイズです。 固定費の償却という概念にもさまざまな同義語があり、その 1 つが比例固定費です。

製造品目の原価ロット サイズ数量は、部品表 (BOM) 計算で使用されます。 この数量は、次に説明するように、BOM 計算を開始および実行する方法によって異なります:

-   品目の BOM 計算における既定の計算量 − 在庫用の品目の標準注文数量は、原価ロット サイズとして機能しますが、この既定値は、品目の注文数量の倍数を反映する大きな数量になる場合があります。 品目の標準注文数量と倍数は、既定の注文設定またはサイト固有の注文設定の中に定義できます。
-   品目の BOM 計算における指定された計算量 : 指定された計算量は、品目の原価ロット サイズとして機能します。 計算量は、最初は、品目の標準注文数量が使用されますが、手動で上書きできます。 指定された計算量は、指定した品目と、生産の BOM 明細行タイプがある製造コンポーネントの原価ロット サイズを表します。 これは、コンポーネントが正確な数量で生産されることが前提となっているためです。 品目が BOM 明細行タイプであるその他の製造コンポーネントの原価ロット サイズは、それぞれの標準注文数量を反映します。
-   品目の BOM 計算における指定された受注生産計算量 : 指定された計算量は、BOM 計算で受注生産展開モードが使用される場合の品目と製造コンポーネントの原価ロット サイズとして機能します。 製造コンポーネントは、生産が BOM 明細行タイプの製造コンポーネントと同じように、正確な数量で生産されるということが前提になっています。
-   注文固有の BOM 計算における指定された計算量 : 注文固有の BOM 計算は、販売注文、販売見積、またはサービス注文の品目に対して実行できます。 指定された計算量では元の明細行品目の数量が使用されますが、この既定の数量は上書きできます。 注文固有の BOM 計算では、受注生産とマルチレベル展開モードのどちらを使用するかを選択できます。

製造品目の償却される固定費の計算金額は雑費と呼ばれます。






