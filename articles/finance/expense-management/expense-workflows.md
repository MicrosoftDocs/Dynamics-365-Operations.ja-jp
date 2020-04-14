---
title: 経費管理ワークフローの設定
description: 旅費経費のドキュメントを確認および承認するために使用されるワークフロー プロセスを設定できます。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153997"
---
# <a name="set-up-workflows-for-expense-management"></a>経費管理ワークフローの設定

[!include [banner](../includes/banner.md)]

旅費経費のドキュメントを確認および承認するために使用されるワークフロー プロセスを設定できます。 ワークフローを定義できるドキュメントには、経費レポート、出張費要求、および現金前貸し要求が含まれます。

1 つのワークフローは 1 つの業務プロセスを表します。 ここでは、ドキュメントの処理および承認に携わるべきユーザーを示すことによって、システムにおけるドキュメントの流れを定義します。 組織でワークフロー システムを使用することにはいくつかの利点があります。

-   **一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントの承認プロセスを定義できます。 ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。

-   プロセスの可視性 - 特定のワークフロー インスタンスのステータス、履歴およびパフォーマンス測定方法を追跡できます。 これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。

-   集中化された作業一覧 - ユーザーは、集中化された作業一覧を表示して、自分に割り当てられているワークフローのタスクおよび承認を確認できます。 

**ワークフローのタイプを作成することができる**

次の表に、**経費**で作成できるワークフローのタイプの一覧を示します。


|              <strong>タイプ</strong>              |                   <strong>このタイプは次の目的で使用します。</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>経費精算書</strong>         |            経費レポートの承認ワークフローを作成します。             |
|  <strong>経費精算書の自動転記</strong>   |        経費レポートの自動転記のワークフローを作成します。        |
|       <strong>経費明細行品目</strong>        |     経費レポートの行項目の承認ワークフローを作成します。      |
| <strong>経費明細行品目の自動転記</strong> | 経費レポートの行項目の自動転記のワークフローを作成します。 |
|       <strong>出張費要求</strong>       |          旅費要求の承認ワークフローを作成します。           |
|      <strong>現金前貸し要求</strong>      |         現金前貸し要求の承認ワークフローを作成します。          |
|        <strong>VAT 過誤納税の還付</strong>        | 付加価値税 (VAT) の還付の承認ワークフローを作成します。  |

