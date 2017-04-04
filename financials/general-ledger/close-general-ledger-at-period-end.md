---
title: "期末に一般会計を決算"
description: "このトピックでは、完了したタスクについて説明します決算総勘定元帳の期間を実行する場合。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a7b72dfa98758b14d303d09890bd46729b1cdbe9
ms.lasthandoff: 03/31/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>期末に一般会計を決算

このトピックでは、完了したタスクについて説明します決算総勘定元帳の期間を実行する場合。 

一般会計では、期または年度で決算手続きを完了できます。 決算プロセスでは、新しい期間のためのシステムを準備します。 [年間システムを準備するには、年度の決算プロセスを実行する必要があります。 各コンフィギュレーションする期間の決算の実行できるように、プロセスおよび手順があります。 期間の最後の一部のオプションの手順を次に示します。:

-   売掛金勘定、買掛金勘定、在庫などの、他のすべてのモジュールのためのすべてのタスクを完了します。
-   すべての仕訳帳が転記されていることを確認します。
-   未実現利益または損失金額を生成するために外貨再評価を実行します。
-   各勘定科目のトランザクションの決済
-   配賦要求を処理します。
-   手動で期末調整を転記します。
-   トランザクションを仕訳し、**元帳仕訳帳**レポートを確認します。
-   連結会社または財務報告を使用して連結を実行します。
-   財務報告を使用して期末財務諸表を生成します。
-   他の転記が発生しないように、元帳期間を [**保留中**] に設定します。 期末の活動の実行中に、使いやすさのため、期を特定のユーザー グループに制限できます。 これは決済済期間を再開できないため、期間を**完全に処理**設定するための概念ではありません。

組織している場合でも、財務期間の最後の作業スペースを使用でき、さまざまな期間に対して必要なタスクを追跡するためのプロセスを終了します。 [財務期間の決算ワークスペース] (財務期間終了workspace.md) と期末決算[] (詳細については年末close.md) トピックを参照してください。 




