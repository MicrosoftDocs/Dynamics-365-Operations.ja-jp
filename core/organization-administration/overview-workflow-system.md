---
title: "ワークフロー システムの概要"
description: "この記事では、Microsoft Dynamics 365のワークフロー システムについて説明します。"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 08c36f02f88fef7508730b6c01a1c99a0f77fb0c
ms.lasthandoff: 03/31/2017


---

# <a name="workflow-system-overview"></a>ワークフロー システムの概要

この記事では、Microsoft Dynamics 365のワークフロー システムについて説明します。

<a name="what-is-workflow"></a>ワークフローについて
-----------------

*ワークフロー*という用語は 2 とおりに定義できます。それは、システムとしての定義と、業務プロセスとしての定義です。
### <a name="workflow-is-a-system"></a>システムとしてのワークフロー

現在の作業がインストールされているDynamics 365 for OperationsとApplication Object Server (AOS)を実行し、システムです。 ワークフロー システムによって提供される機能を使用して、個々のワークフローまたは業務プロセスを作成できます。

### <a name="workflow-is-a-business-process"></a>業務プロセスとしてのワークフロー

1 つのワークフローは 1 つの業務プロセスを表します。 ここでは、タスクを完了し、決定を下し、ドキュメントを承認するユーザーを示すことによって、システムにおけるドキュメントの流れ (移動) を定義します。 たとえば、次の図は経費精算書のワークフローを示しています。 ![ユーザーに割り当てられた要素を含むワークフロー](./media/workflow_user.gif) このワークフローをわかりやすくするため、Sam が 7,000 USD の経費精算書を送信したと仮定します。 このシナリオでは、Sam から送られた領収書を Ivan が確認する必要があります。 その後、Frank と Sue が経費精算書を承認する必要があります。 次に、Sam が USD 11,000 の経費精算書を送信したとします。 このシナリオでは、Ivan が領収書を確認する必要があり、Frank、Sue、および Ann が経費精算書を承認する必要があります。
ワークフロー システムを使用する利点
-------------------------------------

組織でワークフロー システムを使用することにはいくつかの利点があります。
-   **一貫したプロセス** - 購買要求や経費報告書などの特定のドキュメントをどのように処理するか定義できます。 ワークフロー システムを使用することで、ドキュメントが一貫した方法で効率的に処理および承認されます。
-   **プロセスの可視性** – ワークフロー インスタンスの状態、履歴およびパフォーマンス測定方法を追跡できます。 これは、効率を向上させるためにワークフローに変更するかどうかを決定するのに役立ちます。
-   **集中化された作業一覧** – ユーザーは、集中化された作業一覧を表示して、自分に割り当てられているワークフロー タスクおよび承認を確認できます。




