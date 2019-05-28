---
title: 受入倉庫から店舗までのクロスドッキング製品
description: この手順は、発注書の入荷場所から、一つまたは複数の店舗に製品を配分するクロスドッキングを作成および処理する手順を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c8e25007cc4a204aeaf73a2e819c129fa8fa29d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563392"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>受入倉庫から店舗までのクロスドッキング製品

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、発注書の入荷場所から、一つまたは複数の店舗に製品を配分するクロスドッキングを作成および処理する手順を説明します。 ユーザーは、複数のコンフィギュレーションを定義したり、製品の配分方法を提案するシステムを使用できます。あるいは製品をどこに、どの程度各店舗に配分するか手動で入力することもできます。 手順には、補充ルール、組織階層と店舗の重量などのクロスドッキングに使用できるデータの設定は含まれません。 この手順では、USRT というデモ会社を使用します。

1. [すべての発注書] に移動します。
2. 一覧から購買注文ポリシーを選択し、リンクをクリックして注文を開きます。
3. アクション ウィンドウで、[小売] をクリックします。
4. [クロスドッキング] をクリックします。
5. [編集] をクリックします。
    * [明細] セクションの品目をフィルタ処理するためにカテゴリを使用できます。  
6. 一覧で、目的のレコードを見つけ、選択します。
7. [クロスドッキング数量] フィールドで、配分する必要がある選択した製品の購買数量の数量を指定するための値を入力します。
8. [追加のクロスドッキング数量] フィールドに購入できる製品に対して配分する数量を指定するための値を入力します。
9. [配送] フィールドで、[場所の重量] を入力します。
    * 配送のために、さまざまなルールを使用する他のタイプを選択できます。  
10. [補充階層] フィールドで値を選択します。
11. [品揃えの考慮] フィールドで、[はい] を選択します。
12. [数量の計算] をクリックします。
13. [注文の作成] をクリックします。
14. [はい] をクリックします。
15. 一覧で、製品を受け入れる倉庫を見つけ、選択します。
16. 選択した倉庫に対して作成された注文を表示するには、[注文] をクリックします。

