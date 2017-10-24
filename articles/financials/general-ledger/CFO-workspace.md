---
title: "CFO ワークスペースへの財務分析コードの追加"
description: "このトピックでは、CFO ワークスペースに財務分析コードを追加し、それにより元帳および予算のレポートを使用できるようにする方法を説明します。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9e674948f642ab7525f96092a9a1f3adaae66974
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>CFO ワークスペースへの財務分析コードの追加

[!include[banner](../includes/banner.md)]

このトピックでは、最高財務責任者 (CFO) ワークスペースに財務分析コードを追加し、それにより元帳および予算のレポートを使用できるようにする方法を説明します。 CFO ワークスペースには、[**概要**] タブと [**財務**] タブがあります。これら 2 つのタブ上のレポートは、LedgerActivityMeasure および BudgetActivityMeasure という 2 つの措置によってサポートされています。 Microsoft Dynamics 365 for Finance and Operations、Enterprise edition (2017 年 7 月) では、それら 2 つの措置と DimensionCombinationEntity エンティティの間にリレーションがあります。 したがって、分析コードを選択できます。

1. Finance and Operations の **エンティティ格納** ページで、**LedgerActivityMeasure** および **BudgetActivityMeasure** 措置を更新します。
2. Microsoft Visual Studioで、アプリケーション エクスプ ローラーを開き、**LedgerCFO**を検索します。
3. **リソース**で、**LedgerCFOWorkspacePBIX**を開きます。
4. Microsoft Power BI Desktop でリソースを開く場合、**データの取得**を選択し、**SQL Server データベース**を選択し、次に **接続**を選択します。
5. サーバー名を入力し、**AxDW** をデータベースとして入力します。 **DirectQuery**を選択し **OK**を選択します。
6. **LedgerActivityMeasure\_DimensionCombination**を検索して選択し、**読み込み**を選択します。

    > [!TIP]
    > **フィールド** 一覧で、**財務分析コード**の表の名前を変更し、簡単に識別できるようにします。

7. **関係の管理**を選択し、**新規**を選択します。
8. 最初のフィールドで、**総勘定元帳活動**を選択し、次に **LedgerDimension**を選択します。
9. 2 番目のフィールドで、**LedgerActivityMeasure\_DimensionCombination** (または表の名前を変更した場合、**財務分析コード**) を選択します。 **DimensionCombinationRECID** ヘッダーを選択します。
10. **基数** フィールドで、**多対一**を選択します。
11. **クロス フィルター方向** 値を **単一**に変更します。
12. **この関係を有効にする** および **参照整合性を仮定する**の両方を選択し、**OK**を選択し、次に **閉じる**を選択します。

    [![リレーションシップを作成](./media/Create-relationship.png)](./media/Create-relationship.png)

13. **フィールド** 一覧で、表および使用可能な財務分析コードが表示されるべきです。 レポート レベルのフィルターに、使用する財務分析コードをドラッグします。
14. 変更を保存します。
15. アプリケーション オブジェクト ツリー (AOT) で、プロジェクトを右クリックし、**同期**を選択します。
16. プロジェクトを構築して、結果を表示するアプリケーションを開きます。

    [![完了済ワークスペース](./media/workspace.png)](./media/workspace.png)

