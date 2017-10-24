--- 
title: "範囲のある利息コードの作成"
description: "利息コードは値の範囲によって異なる利息金額を計算するように設定できます。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 05ca41dd5d660e9f0ef72ee5bd49d800645081a5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-interest-code-with-a-range"></a>範囲のある利息コードの作成

[!include[task guide banner](../../includes/task-guide-banner.md)]

利息コードは値の範囲によって異なる利息金額を計算するように設定できます。 この手順は、利息コードを追加し、その範囲を追加する方法を示します。

1. [貸方転記および取立] > [利息] > [利息コードの設定] の順に移動します。
2. [新規] をクリックします。
3. [利息コード] フィールドで、利息コードの名前を入力します。
4. [説明] フィールドに、利息コードの説明を入力します。
5. [月] を選択します。
6. [所得] セクションを展開します。
7. [通貨別受取利息] セクションを展開します。
8. [元帳転記勘定] フィールドで、任意の値を指定します。
9. [範囲別の利息] フィールドで「月」を選択します。
10. [追加] をクリックします。
11. [説明] フィールドに、この通貨と範囲の説明を入力します。
12. [保存] をクリックします。
13. [範囲] をクリックします。
14. [新規] をクリックします。
15. [開始値] に 0 を入力し、利息を計算するのに使用される月ごとの利率を入力します。 この例の場合、1.5 です。
16. [新規] をクリックします。
17. 次の [開始値] に 4 を入力します。これは新しい利息金額の計算をする最初の月です。
18. 4 の月からの利息の計算に使う、月ごとの利率を入力します。 この例の場合、2.0 です。
19. [新規] をクリックします。
20. 次の [開始値] に 7 を入力します。これは新しい利息金額の計算をする次の月です。
21. 7 の月からの利息の計算に使う、月ごとの利率を入力します。 この例の場合、2.5 です。
22. 設定を完了するには、[終了] をクリックしてください。


