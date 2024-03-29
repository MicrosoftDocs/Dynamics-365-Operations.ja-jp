---
title: 元帳決済の照会
description: この記事では、元帳決済の照会ウィンドウについて説明します
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853140"
---
# <a name="ledger-settlement-inquiry"></a>元帳決済の照会

[!include [banner](../includes/banner.md)]

この記事では、会計年度期間の決済済み、未決済、または決済済みと未決済の元帳トランザクションの両方を表示するために使用できる **元帳決済の照会** ウィンドウについて説明します。

## <a name="view-ledger-settlement-transactions"></a>元帳決済のトランザクションの表示
1.  **一般会計 > 照会およびレポート > 元帳決算照会** の順に移動します。
2.  日付範囲 を指定するには、**開始日** フィールドと **終了日** フィールドまたは **日付間隔** フィールドを使用します。 試金に関して、日付の範囲は単一の会計年度内にある必要があります。
3.  **主要勘定** フィールド で、1 つ以上の主要勘定を選択して、元帳トランザクションを表示します。 ドロップダウン リストには、**総勘定元帳パラメータ** ページに、元帳決済用に設定されている主要勘定のみ表示されます。
4.  **財務分析コード セット** フィールドを使用して、財務分析コードをグリッドに表示します。 主要勘定が必要なので、主勘定が含まれるのを含わない財務分析コード セットを選択した場合でも、常に **主要勘定** フィールドの値が最初の列として表示されます。
5.  **状態** フィールドで次を選択します:
-   決済済トランザクションと未決済トランザクションの両方を表示するための **すべて**
-   決済済トランザクションのみを表示するための **未決済** 
-   決済済トランザクションのみを表示するための **決済済み**
6.  **トランザクション表示** を選択します。 入力した基準に基づいて元帳トランザクションがグリッドに表示されます。 詳細な分析のために照会の結果を Microsoft Excel にエクスポートできます。 グリッドで選択して保持 (または右クリック) します。

### <a name="column-details"></a>列の詳細
**元帳決済照会** ページの グリッドには 、次の列が表示されます。
-   **主要勘定** – このフィールドは必須で、常に表示されます。
-   **財務分析コード** – 選択した財務分析コード セットに基づいて財務分析コードが表示されます。
-   **トランザクションの日付** – 元帳トランザクションの転記日付。
-   **元のトランザクションの日付** – 年度末の決算が実行され、元帳決済がメイン勘定の詳細を保持する目的で設定されている場合、未決済のトランザクションは期首残高として詳細に引き渡されます。 元帳トランザクションの元の転記日付は、**元のトランザクション日付** フィールドで管理されます。
-   **トランザクション期間** – すべての決済済トランザクションの値は 0 (ゼロ) です。 未決済トランザクションの場合、この値は、元のトランザクション日付またはトランザクション日付から照会が実行された日付までを日数で計算します。
たとえば、元帳トランザクションのトランザクションの日付が 2022 年 1 月 1 日 (1/1/2022) で、元のトランザクション日付が 2021 年 12 月 30 日 (12/30/2021) とします。 2022 年 1 月 2 日 (1/2/2022) に照会を実行した場合、**トランザクション期日経過日数** の値は 4 になります。 この値は、元のトランザクション日付 (2021 年 12 月 30 日) から 2022 年 1 月 2 日の間の日数として計算されます。

元のトランザクション日付がない場合は、トランザクションの日付が代わりに使用されます。
-   **(その他のトランザクション情報)** – 追加の列には、伝票番号、説明、借方金額と貸方額などの情報が、3 つの通貨 (トランザクション、会計、レポート) すべてで表示されます。
-   **状態** – この値は、**決済済** または **未決済** になります。
-   **決済 ID** – 決済済トランザクションに割り当てられている ID。

[![元帳決済の照会ページ](./media/Inquiry1.png)](./media/Inquiry1.png)

 
合計はグリッドの下に表示できます。
1.  グリッドの右側の省略記号 (...) を選択し、**フッターの表示** を選択します。
2.  各金額の列で選択して保持 (または右クリック) して、**この列でグループ化** を選択して合計を表示します。 合計がフッターに表示されます。 照会がフィルタ処理され、未決済のトランザクションだけが表示された場合は、合計を使用して試算表と一緒に金額を調整できます。







