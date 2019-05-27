---
title: 経費管理 Power BI コンテンツ
description: このトピックでは、経費管理 Power BI コンテンツ パックの内容について説明します。
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a07d9ed7e4c57c2444d1c2a017109509c153aad4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1503130"
---
# <a name="expense-management-power-bi-content"></a>経費管理 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

このトピックでは、経費管理 Power BI コンテンツの内容について説明します。 

## <a name="overview"></a>概要
バージョン 8.1 以降では、2 つの Power BI コンテンツ パックを経費管理で使用できます。 
- 経費精算書を送信する従業員用に設計された個人用ダッシュボードがあります。 

  ダッシュボードは、未送信および送信済の金額、履歴、および経費トランザクションの履歴分析に関する重要な情報を個人に提供するように調整されています。 個人用ダッシュボードは、ユーザーにとって最も重要な情報を含む単一ページです。

- 買掛金勘定の担当者およびマネージャー用に設計された、管理者ダッシュボードがあります。 ダッシュボードは、従業員経費全体の追跡および報告のために調整されています。 未送信の経費、マイレージおよび経費報告の平均金額などの主要経費指標が表示されます。 トランザクション データを使用し、すべての会社の経費管理の集計ビューを提供します。 また、財務分析コードのデータを追加するオプションを使用して、従業員ごとの内訳も表示されます。 管理者経費分析の内容は次のとおりです。 
  - 経費金額に関する主要な指標とドラフト、処理中の経費、および完了した経費報告に関する分析を含む概要ページ。 
  - 時間、原価タイプ、統計グループ別に従業員に関する個々の詳細を確認するための従業員統計ページ。 
  - 経時的に複数の従業員を比較するための従業員比較ページ。 

金額はすべて会社通貨で表示されます。 すべての会社のデータが表示されますが、必要に応じて会社のフィルターを追加できます。 

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
Expense Admin Dashboard.pbix および Expense Personal Dashboard.pbix Power BI コンテンツは、Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリにあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、[Microsoft およびパートナーからの LCS での Power BI コンテンツ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/) を参照してください。
コンテンツは、経費管理ワークスペースから埋め込み Power Bi コンテンツとして入手できます。 経費の所有者は、誰でも自分の経費にアクセスすることができますが、すべてのユーザーの経費データに関しては、買掛金担当者と管理者のみが管理者コンテンツにアクセスすることができます。

## <a name="refreshing-the-power-bi-content"></a>Power BI コンテンツの更新
経費管理 Power BI コンテンツは、TrvBiExpenseMeasurement メジャーおよび BudgetActivityMeasure をエンティティ格納から更新する必要があります。 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるメトリックス
コンテンツには、レポートのページ一式が含まれます。 各ページは、グラフ、タイル、テーブルとして視覚化される一連のメトリックスで構成されています。 次の表は、Power BI コンテンツの視覚化の概要を示しています。

**個人経費分析**

| レポート ページ | 視覚化                             |
|-------------|-------------------------------------------|
| 自分の経費 | マイレージの量                         |
|             | 処理中の経費精算書                |
|             | 一連番号 未送信経費の               |
|             | 支払対象の個人経費              |
|             | 未送信金額                        |
|             | 送信済金額                          |
|             | 払い戻し処理中の金額             |
|             | 金額とステータスを含む経費精算書   |
|             | 送信されたが未承認の経費清算書  |
|             | 原価タイプ別経費                     |
|             | 商社別経費                      |
|             | 処理済経費別経費            |
|             | プロジェクト別経費                       |
|             | 時間経過に伴うトランザクション合計金額        |

**管理者経費分析**

| レポート ページ         | 視覚化                           |           
|---------------------|-----------------------------------------|
| 経費の概要    | ドラフト経費金額                   |
|                     | ドラフト経費の行の数           |
|                     | ドラフト経費行                     |
|                     | 経費精算書のポリシー違反        |
|                     | 未払い金額                      |
|                     | 送信されたが未承認の経費       |
|                     | 承認済経費                       |
|                     | 経費合計金額                    |
|                     | 経費精算書の概要                |
|                     | 原価タイプ別経費                   |
|                     | 商社別経費                    |
|                     | 従業員別経費                   |
|                     | プロジェクト対経費                     |
| 従業員比較 | 経費金額                         |
|                     | 時間経過に伴う従業員ごとの経費金額   |
| 従業員統計 | 原価タイプ別経費清算書            |
|                     | 個人経費                       |
|                     | 統計グループ別経費精算書     |
