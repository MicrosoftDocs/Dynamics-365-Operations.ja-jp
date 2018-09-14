--- 
title: "固定資産への追加物の入力"
description: "この手順では、既存の固定資産への追加物を追加する方法を示します。"
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3579148033023f648e1a78a3dd009018f153fdad
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a>固定資産への追加物の入力

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、既存の固定資産への追加物を追加する方法を示します。 固定資産の付属品の目的は、品目の追加、メンテナンス、改善を追跡することであり、情報提供のみを目的としています。 固定資産価値または耐用年数の変更はすべて、個別に行う必要があります。   



この手順では USMF の法人に対して経理担当ロールとデモ データを使用します。

1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、付属品に関連する固定資産を見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [アクション] ウィンドウで、[固定資産] をクリックします。
5. [固定資産の追加物] をクリックします。
6. [新規] をクリックします。
7. [名前] フィールドに値を入力します。
8. 追加の購買またはサービスの日付を設定します。
9. 資産に関する品目、保守、またはその他の改良の原価を入力します。
10. [数量] フィールドに数値を入力します。
    * 原価合計は、固定資産の値に影響せず、追跡および情報目的でのみ使用されます。 原価が資本化される場合、評価増調整トランザクションは個別に転記する必要があります。  
11. [一般] タブをクリックします。
    * 追加物によって固定資産の耐用年数が増加する場合は、耐用年数の増加を設定します。  
    * これは情報提供のみを目的としたフィールドです。 耐用年数を増加させるには、資産の価値モデルまたは減価償却簿の耐用年数を変更します。  


