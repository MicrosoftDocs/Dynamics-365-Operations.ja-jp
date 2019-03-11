---
title: 在庫品目要求からの発注書の品目の入庫
description: この手順は、在庫品目要求から発注書の品目を受け取る方法を示します。
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26572a49426719fba520338a5eccd7e0af78890e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "344182"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>在庫品目要求からの発注書の品目の入庫

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、在庫品目要求から発注書の品目を受け取る方法を示します。

品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。 

このタスクでは、USSI データ セットを使用します。

1. [プロジェクト管理および会計] > [プロジェクト] > [すべてのプロジェクト] の順に選択します。
2. 一覧で、選択された行のリンクをクリックします。
3. アクション ウィンドウで、[計画] をクリックします。
4. [在庫品目要求] をクリックします。
5. [新規] をクリックします。
6. 一覧で、選択された行をマークします。
7. [品目番号] フィールドで、値を入力または選択します。
8. [数量] フィールドに数値を入力します。
9. [保存] をクリックします。
10. [アクション] ウィンドウで、[管理] をクリックします。
11. [機能] をクリックします。
12. [発注書の作成] をクリックします。
13. [含む] チェック ボックスをオンにします。
14. [仕入先] フィールドで、値を入力または選択します。
15. [OK] をクリックします。
16. [買掛金勘定] > [発注書] > [すべての発注書] に移動します。
17. 一覧で、選択された行のリンクをクリックします。
18. アクション ウィンドウで、[購買] をクリックします。
19. [確認] をクリックします。
20. アクション ウィンドウで、[入庫] をクリックします。
21. [製品受領書] をクリックします。
22. 一覧で、選択された行をマークします。
23. [製品受領書] フィールドで、値を入力します。
24. [OK] をクリックします。

