---
title: ワークフロー システムの概要
description: このトピックでは、ワークフロー システムについて説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660e01618eea66bc611dd51818694d36993ba9ea
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796999"
---
# <a name="workflow-system-overview"></a>ワークフロー システムの概要

[!include [banner](../includes/banner.md)]

このトピックでは、ワークフロー システムについて説明します。

## <a name="what-is-workflow"></a>ワークフローについて

*ワークフロー* という用語は 2 とおりに定義できます。それは、システムとしての定義と、業務プロセスとしての定義です。

### <a name="workflow-is-a-system"></a>システムとしてのワークフロー

ワークフローは、 pplication Object Server (AOS) で実行されるシステムです。 ワークフロー システムによって提供される機能を使用して、個々のワークフローまたは業務プロセスを作成できます。

### <a name="workflow-is-a-business-process"></a>業務プロセスとしてのワークフロー

1 つのワークフローは 1 つの業務プロセスを表します。 ここでは、タスクを完了し、決定を下し、ドキュメントを承認するユーザーを示すことによって、システムにおけるドキュメントの流れ (移動) を定義します。 たとえば、次の図は経費精算書のワークフローを示しています。

![ユーザーに割り当てられた要素を含むワークフロー](./media/workflow_user.gif)

このワークフローをよりよく理解するため、Sam が USD 7,000 の経費精算書を送信したと仮定します。 このシナリオでは、Sam から送られた領収書を Ivan が確認する必要があります。 その後、Frank と Sue が経費精算書を承認する必要があります。 次に、Sam が USD 11,000 の経費精算書を送信したとします。 このシナリオでは、Ivan が領収書を確認する必要があり、Frank、Sue、および Ann が経費精算書を承認する必要があります。

## <a name="benefits-of-using-the-workflow-system"></a>ワークフロー システムを使用する利点

組織でワークフロー システムを使用することにはいくつかの利点があります。

- **一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントをどのように処理するか定義できます。 ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。
- **プロセスの可視性** – ワークフロー インスタンスの状態、履歴およびパフォーマンス測定方法を追跡できます。 これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。
- **集中化された作業一覧** – ユーザーは、集中化された作業一覧を表示して、自分に割り当てられているワークフロー タスクおよび承認を確認できます。


## <a name="workflow-content"></a>ワークフロー コンテンツ

+ [ワークフロー システムのアーキテクチャ](workflow-system-architecture.md)
+ [ワークフロー要素](workflow-elements.md)
+ [ワークフローの承認プロセスでのアクション](workflow-actions.md)
+ [ワークフローの作成の概要](create-workflow.md)
+ [ワークフロー プロパティのコンフィギュレーション](configure-workflow-properties.md)
+ [ワークフローでの手動タスクのコンフィギュレーション](configure-manual-task-workflow.md)
+ [ワークフローでの自動化タスクのコンフィギュレーション](configure-automated-task-workflow.md)
+ [ワークフローでの承認プロセスのコンフィギュレーション](configure-approval-process-workflow.md)
+ [ワークフローでの承認ステップのコンフィギュレーション](configure-approval-step-workflow.md)
+ [ワークフローでの手動決定のコンフィギュレーション](configure-manual-decision-workflow.md)
+ [ワークフローでの条件付き意思決定のコンフィギュレーション](configure-conditional-decision-workflow.md)
+ [ワークフローでの並列活動のコンフィギュレーション](configure-parallel-activity-workflow.md)
+ [ワークフロー内の並列分岐のコンフィギュレーション](configure-parallel-branch-workflow.md)
+ [品目ワークフローのコンフィギュレーション](configure-line-item-workflow.md)
+ [ワークフローに関するよく寄せられる質問](workflow-FAQ.md)
