---
title: バリアント重量を使用した発注書へのバリアント製品の追加
description: この手順では、自動事前設定の購買注文明細行に製品のバリアントごとに異なる重量を使用するための手順を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cd4ca3652c1ce7422e8f80426a7b11545e09861
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242568"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>バリアント重量を使用した発注書へのバリアント製品の追加

[!include [banner](../../includes/banner.md)]

この手順では、自動事前設定の購買注文明細行に製品のバリアントごとに異なる重量を使用するための手順を説明します。 自分が購買する製品の数量を選択すると、製品バリアントの重量コンフィギュレーションに基づく推奨数量のすべての製品のバリアントに、購買注文明細行が作成されます。 この手順には、製品分析コードおよび製品バリアントの重量値を設定する手順は含まれていません。 この手順では、デモ データの会社 USRT を使用します。

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]