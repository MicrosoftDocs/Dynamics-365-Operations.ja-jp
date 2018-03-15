--- 
title: "ロイヤルティ報酬ポイントの定義"
description: "この手順では、ロイヤルティ報酬ポイントを定義する方法を説明します。"
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 26b5615df427fb01cc4a1764507fbaa11bf0d7a0
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---
# <a name="define-loyalty-reward-points"></a>ロイヤルティ報酬ポイントの定義

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、ロイヤルティ報酬ポイントを定義する方法を説明します。 ロイヤルティ プログラムを設定する前に、ロイヤルティ報酬ポイントを設定する必要があります。 この手順では、デモ データの会社 USRT を使用します。

1. [小売りとコマース] > [顧客] > [ロイヤルティ] > [ロイヤルティ報酬ポイント] に移動します。
2. [新規] をクリックします。
3. [報酬ポイント ID] フィールドで、値を入力します。
4. [説明] フィールドに値を入力します。
5. [報酬ポイント タイプ] フィールドでオプションを選択します。
    * 報酬ポイントに最も近い整数に四捨五入する場合は、[数量] を選択します。 通貨の丸めに関するルールに従って報酬ポイントが端数処理される場合は、[金額] を選択します。 [数量] を選択した場合、この手順の次のステップは省略されます。  
6. [通貨] フィールドに値を入力します。
    * [金額のタイプ] の報酬ポイントの場合、発行されたすべてのポイントは選択した通貨となります。 [数量タイプ] の報酬ポイントの場合、このフィールドは適用されません。この手順はスキップされます。  
7. [引換可能] チェック ボックスをオンまたはオフにします。
8. [引換ランキング] フィールドに数値を入力します。
    * 製品の支払に複数の償還可能な報酬ポイントが使用できる場合、引換ランキングが使用されます。 二つの報酬ポイントの引換ランキングが同じ場合、より小さなポイント数を必要とするものが使用されます。  
9. [有効期限の時刻] フィールドに数値を入力します。
    * 報酬ポイントは、指定された日数、月数、または年数、ポイントが発行された後、有効になります。 「0」という値は、ロイヤルティ報酬ポイントに有効期限がないことを意味します。  
10. [有効期限の単位] フィールドで、オプションを選択します。
11. [保存] をクリックします。


