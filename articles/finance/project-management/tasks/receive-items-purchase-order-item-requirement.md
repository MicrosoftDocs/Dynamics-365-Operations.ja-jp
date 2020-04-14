---
title: 在庫品目要求からの発注品目の入庫
description: このトピックでは、在庫品目要求から発注書の品目を受け取る方法について説明します。
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f288a47f952a30d98a4a5b96409dc53f880d41d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139063"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>在庫品目要求からの発注品目の入庫

[!include [banner](../../includes/banner.md)]

このトピックでは、在庫品目要求から発注書の品目を受け取る方法について説明します。

品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。 

このタスクでは、USSI データ セットを使用します。

1. ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > プロジェクト > すべてのプロジェクト**の順に移動します。
2. 一覧で、目的の行のリンクを選択します。
3. アクション ウィンドウで、**計画**を選択します。
4. **在庫品目要求**を選択します。
5. **新規** を選択します。
6. 新しい行で、**品目番号**フィールドに値を入力または選択します。
7. **数量**フィールドに、数値を入力します。
8. **保存** を選択します。
9. アクション ウィンドウで、**管理**を選択します。
10. **機能**を選択します。
11. **発注書の作成**を選択します。
12. **すべてを含む**のチェック ボックスをオンにします。
13. **仕入先**フィールドで、値を入力または選択します。
14. **OK** を選択します。
15. ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > すべての発注書**に移動します。
16. 一覧で、目的の行のリンクを選択します。
17. アクション ウィンドウで、**購買**を選択します。
18. **確認**を選択します。
19. アクション ウィンドウで、**入庫**を選択します。
20. **製品受領書**を選択します。
21. **製品受領書**フィールドに値を入力します。
22. **OK** を選択します。

