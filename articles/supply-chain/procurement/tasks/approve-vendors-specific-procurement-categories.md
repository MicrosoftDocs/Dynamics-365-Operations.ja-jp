---
title: 特定の調達カテゴリに対する仕入先の承認
description: このトピックでは、Dynamics 365 for Finance and Operations の特定の調達カテゴリの仕入先を承認する方法について説明します。
author: mkirknel
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1583a2eedc535f81b84e3094fee1574451f6f209
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867152"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>特定の調達カテゴリに対する仕入先の承認

[!include [task guide banner](../../includes/task-guide-banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations の特定の調達カテゴリの仕入先を承認する方法について説明します。 購買要求が作成されると、承認仕入先または優先仕入先を選択する必要があり、それは購入ポリシーの設定方法によって異なります。 この手順では、特定の調達カテゴリに対して仕入先が承認、または優先されるよう指定する方法を示します。 通常、このタスクを実行するのは、調達担当者です。 デモ データの会社 USMF でこの手順を使用できます。

1. ナビゲーション ウィンドウで、**モジュール > 調達 > 仕入先 > すべての仕入先**の順に移動します。
2. カテゴリで承認仕入先または優先仕入先として設定する仕入先を選択します。
3. アクション ウィンドウで、**一般**を選択します。
4. **カテゴリ**を選択します。
5. **カテゴリの追加**を選択します。
6. **カテゴリ** フィールドで、**オフィスとデスク アクセサリ (OFFICE AND DESK ACCESSORIES)** を選択します。
7. **仕入先カテゴリ ステータス** フィールドで、**優先**を選択します。 カテゴリに複数の優先仕入先を指定することができます。  
8. **保存** を選択します。
9. ナビゲーション ウィンドウで、**モジュール > 調達 > 調達カテゴリ**の順に移動します。
10. ツリーで、**CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES** を選択します。
11. **仕入先**セクションを展開します。 選択した仕入先が、オフィスとデスク アクセサリ カテゴリの優先仕入先として表示されているか確認します。 この手順をタスク ガイドとして実行する場合、仕入先の一覧にスクロールできるように**ロック解除**ボタンを選択する必要があります。  このページに優先仕入先および承認済仕入先を追加することもできます。  
12. ツリーで、**OFFICE AND DESK ACCESSORIES** を展開し、**シザーズ**を選択します。
13. **親カテゴリからの継承仕入先:** フィールドで、**いいえ**を選択します。
14. **親カテゴリからの継承仕入先:** フィールドで、**はい**を選択します。

