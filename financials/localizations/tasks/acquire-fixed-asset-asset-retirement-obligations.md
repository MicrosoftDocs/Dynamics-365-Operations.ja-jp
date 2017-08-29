--- 
title: "資産除去責務がある固定資産の取得 (日本)"
description: "日本では、資産除去責務 (ARO) は現在の値に割引され、固定資産の取得原価に追加されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbcc4f5b65e89a02685f17e789ce22959d7be6c0
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="acquire-a-fixed-asset-with-asset-retirement-obligations-japan"></a>資産除去責務がある固定資産の取得 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

日本では、資産除去責務 (ARO) は現在の値に割引され、固定資産の取得原価に追加されます。 



このタスクでは、ARO を持つ固定資産の取得方法について説明します。 



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。

1. [固定資産] > [資産除去責務] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [日付] フィールドに日付を入力します。
7. [勘定] フィールドで、任意の値を指定します。
8. [帳簿] フィールドに値を入力します。
9. [借方] フィールドに数値を入力します。
10. [機能] をクリックします。
11. [資産除去責務トランザクションの生成] をクリックします。
    * [機能] > [資産除去責務トランザクションの生成] のメニューは、固定資産が同じ仕訳帳にある場合に使用します。     また、すでに取得済の固定資産については、[提案] > [除去費用の資産計上] のメニューも使用することができます。  
    * [ドキュメント タイプ] が [資産除去責務] である新しいレコードが作成されていることを確認します。  
12. 一覧で、選択された行をマークします。
    * 提案金額は現在の値に割引されます。  
13. [転記] をクリックします。


