---
title: "固定資産ロール フォワード レポート"
description: "このトピックでは、固定資産ロール フォワード レポートを使用する方法について説明します。"
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 0a78df4ede8fd57afbc3e9a7e5a38b840f479cdf
ms.contentlocale: ja-jp
ms.lasthandoff: 01/25/2018

---
# <a name="fixed-assets-roll-forward-report"></a>固定資産ロール フォワード レポート

[!include[banner](../includes/banner.md)]

**固定資産ロール フォワード** レポートは、分かりやすい Microsoft Excel 形式で、ユーザーが必要とする期間決算、財務諸表、および税レポートの詳細な固定資産データを提供します。 レポートには、期間中の評価移動と共に、固定資産の開始および終了時の残高、および期間中に発生した任意の新しい資産の取得と処分が含まれます。 個々の固定資産ごとにデータが報告され、値は固定資産グループおよび法人に対しても集計されます。

**固定資産ロール フォワード** レポートは、電子申告 (ER) フレームワークを使用します。 レポートを実行する前に、固定資産モデルと固定資産ロール フォワード コンフィギュレーションを Microsoft Dynamics Lifecycle Services (LCS) からインポートする必要があります。 手順については、[Lifecycle Services の電子申告コンフィギュレーションのダウンロード](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)を参照してください。

このレポートは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3、または Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) の修正プログラムとして使用できます。 2017 年 7 月リリースのある環境には、3 つの修正プログラムを適用する必要があります。

- **KB 4041754:** 電子申告 (ER) コンフィギュレーションは、LCS からダウンロードできません。プラットフォーム更新プログラムのパッケージの適用後、現在のアプリケーション バージョンに該当しないためです
- **KB 4056107:** 電子申告 (GER) 累積更新プログラム 5
- **KB 4056353:** 固定資産明細書および注記レポートは、GAAP と IFRS の要件を満たしません

次の表に、レポートで使用できるフィールドを示します。

| フィールド                                       | 説明 |
|---------------------------------------------|-------------|
| 残高: 開始                           | レポートに指定されている「開始」日の時点での固定資産正味簿価額。 |
| 残高: 終了                           | レポートに指定されている「終了」日の時点での固定資産正味簿価額。 |
| 取得: 開始時の値                 | **取得** および **取得原価調整** のすべてのトランザクションの合計は、レポートに指定されている「開始」日まで入力します。 |
| 取得: 期間の取得           | **取得** および **取得原価調整** のすべてのトランザクションの合計は、レポートに記載されていた日付範囲を入力します。 |
| 取得: 期間の処分              | レポートの日付範囲内に処分トランザクションがあったと記載されていた、すべての取得の合計は取り消されます。 |
| 取得: 終了時の値                 | **取得** および **取得原価調整** のすべてのトランザクションの合計は、レポートに指定されている「終了」日まで入力します。 |
| 減価償却: 開始時の値                | **減価償却**、**減価償却調整**、**特別減価償却費**、および **特別減価償却** のすべてのトランザクションの合計は、レポートで指定された「開始」日まで入力します。 |
| 減価償却: 減価償却の期間         | **減価償却**、**減価償却調整**、および **特別減価償却** のすべてのトランザクションの合計は、レポートに記載されていた日付範囲を入力します。 |
| 減価償却: 特別減価償却の期間 | **特別減価償却費** のすべてのトランザクションの合計は、レポートに記載されていた日付範囲を入力します。 |
| 減価償却: 期間の処分             | レポートの日付範囲内に処分トランザクションがあったと記載されていた、すべての減価償却の合計は取り消されます。 |
| 減価償却 - 終了時の値                | **減価償却**、**減価償却調整**、**特別減価償却費**、および **特別減価償却** のすべてのトランザクションの合計は、レポートで指定された「終了」日まで入力します。 |
| 評価増/評価減: 開始時の値        | **評価増調整**、**評価減調整**、および **再評価** のすべてのトランザクションの合計は、レポートに指定されている「開始」日まで入力します。 |
| 評価増/評価減: 評価増の期間     | **評価増調整** のすべてのトランザクションの合計は、レポートに記載されていた日付範囲を入力します。 |
| 評価増/評価減: 評価減の期間   | **評価減調整** のすべてのトランザクションの合計は、レポートに記載されていた日付範囲を入力します。 |
| 評価増/評価減: 再評価の期間  | **再評価** のすべてのトランザクションの合計は、レポートに記載されていた日付範囲を入力します。 |
| 評価増/評価減: 処分の期間     | レポートの日付範囲内に処分トランザクションがあったと記載されていた、すべての評価増、評価減、および再評価の合計は取り消されます。 |
| 評価増/評価減: 終了時の値        | **評価増調整**、**評価減調整**、および **再評価** のすべてのトランザクションの合計は、レポートに指定されている「終了」日まで入力します。 |
| 処分: 処分日                    | 固定資産帳簿の処分日。 |
| 処分: 処分時の正味帳簿価格       | 処分時点での固定資産帳簿の正味帳簿価格。 |
| 処分: 販売額                       | 処分となる固定資産帳簿の販売額 – 販売トランザクション |
| 処分: 仕損額                      | 処分となる固定資産帳簿の仕損額 – 仕損トランザクション |
| 処分: 利益/損失                      | 固定資産帳簿に対する処分トランザクションの一部として計算される利益または損失の値。 |
