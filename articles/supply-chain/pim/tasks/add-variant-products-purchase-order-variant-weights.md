--- 
title: "バリアント重量を使用した発注書へのバリアント製品の追加"
description: "この手順では、自動事前設定の購買注文明細行に製品のバリアントごとに異なる重量を使用するための手順を説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3db13646c82ea6dc6949aaa714a5769f9c5ad2a9
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>バリアント重量を使用した発注書へのバリアント製品の追加

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、自動事前設定の購買注文明細行に製品のバリアントごとに異なる重量を使用するための手順を説明します。 自分が購買する製品の数量を選択すると、製品バリアントの重量コンフィギュレーションに基づく推奨数量のすべての製品のバリアントに、購買注文明細行が作成されます。 この手順には、製品分析コードおよび製品バリアントの重量の値をコンフィギュレーションするステップは含まれません。 この手順では、デモ データの会社 USRT を使用します。

1. [買掛金勘定] > [発注書] > [すべての発注書] に移動します。
2. [新規] をクリックします。
3. [仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
5. [一般] セクションの展開を切り替えます。
6. [サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、選択された行のリンクをクリックします。
8. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、目的のレコードを見つけ、選択します。
10. 一覧で、選択された行のリンクをクリックします。
11. [OK] をクリックします。
12. [明細行の詳細] セクションの展開を切り替えます。
13. [バリアント] タブをクリックします。
14. [行の追加] をクリックします。
15. 一覧で、選択された行をマークします。
16. [品目番号] フィールドで「0140」と入力します。
17. 数量を '1000' に設定します。
18. [保存] をクリックします。


