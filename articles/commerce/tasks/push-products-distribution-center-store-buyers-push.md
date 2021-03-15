---
title: 集中的購買を使用した物流センターから店舗への製品の配送
description: この手順は、一つの場所から、一つまたは複数の店舗に製品を配分する集中的購買を作成および処理する手順を説明します。
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3720945823cf127f776a9ea6a6ad75a72ceec00c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012344"
---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a>集中的購買を使用した物流センターから店舗への製品の配送

[!include [banner](../includes/banner.md)]

この手順は、一つの場所から、一つまたは複数の店舗に製品を配分する集中的購買を作成および処理する手順を説明します。 ユーザーは、複数のコンフィギュレーションを定義したり、製品の配分方法を提案するシステムを使用できます。あるいは製品をどこに、どの程度各店舗に配分するか手動で入力することもできます。 この手順には、補充ルール、組織階層と店舗の重量などの集中的購買に使用できるデータの設定は含まれません。 この手順では、USMF というデモ会社を使用します。

1. [集中的購買] に移動します。
2. [新規] をクリックします。
3. [説明] フィールドに値を入力します。
4. [サイト] フィールドで値を入力または選択します。
5. [倉庫] フィールドで、手持在庫数量の製品のある倉庫を入力、または選択します。
6. [追加] をクリックします。
7. 一覧で、選択された行をマークします。
8. [品目番号] フィールドで、製品を入力または選択します。
9. [追加] をクリックします。
10. 一覧で、選択された行をマークします。
11. [品目番号] フィールドで、バリアント製品を入力または選択します。
    * バリアント製品を入力すると、明細行がバリアントごとに作成されます。  
12. 一覧で行をマーキングします。
13. [プッシュ数量] フィールドに、配布する選択された製品の数量を入力します。
14. [プッシュする追加数量] フィールドで、配送先の有効数量がある製品の数量を入力します。
15. [配送] フィールドで、[場所の重量] を入力します。
    * 配送のために、他のルールを使用する他のタイプを選択できます。  
16. [補充階層] フィールドで値を選択します。
17. [品揃えの考慮] フィールドで、[はい] を選択します。
18. [数量の計算] クリックし、[倉庫] セクションの行に追加される数量を確認します。
19. [注文の作成] をクリックします。
20. [はい] をクリックします。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]