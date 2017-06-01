---
title: "期末に一般会計を決算"
description: "このトピックでは、一般会計の期間締めを実行する場合に通常完了するタスクについて説明します"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 81d687cc16ef43442c8c1c166cc6f0d8b171e28f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>期末に一般会計を決算

[!include[banner](../includes/banner.md)]


このトピックでは、一般会計の期間締めを実行する場合に通常完了するタスクについて説明します 

一般会計では、期または年度で決算手続きを完了できます。 決算プロセスでは、新しい期間のためのシステムを準備します。 新しい年度のシステムを準備するには、年度末決算処理を実行する必要があります。 各組織には、期末に実行するさまざまなプロセスやステップがあります。 次に、期末のオプションの手順をいくつか示します。

-   売掛金勘定、買掛金勘定、在庫などの、他のすべてのモジュールのためのすべてのタスクを完了します。
-   すべての仕訳帳が転記されていることを確認します。
-   未実現利益または損失金額を生成するために外貨再評価を実行します。
-   各勘定科目のトランザクションの決済
-   配賦要求を処理します。
-   手動で期末調整を転記します。
-   トランザクションを仕訳し、**元帳仕訳帳**レポートを確認します。
-   連結会社または財務報告を使用して連結を実行します。
-   財務報告を使用して期末財務諸表を生成します。
-   他の転記が発生しないように、元帳期間を [**保留中**] に設定します。 期末の活動の実行中に、使いやすさのため、期を特定のユーザー グループに制限できます。 決算済みの期間を再度開くことはできないため、期間を [**完全に閉じる**] に設定するのは、よい考えではありません。

財務期間終了ワークスペースを使用して、さまざまな期末処理プロセスに必要なタスクを整理して追跡できます。 詳細については、「[財務期間終了ワークスペース](financial-period-close-workspace.md)」および「[年度末決算](Year-end-close.md)」のトピックを参照してください。 






