---
title: ワークフローの作成の概要
description: このトピックでは、ワークフローの作成方法を説明します。
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "195583"
- intro-internal
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 877587601c780a2724517afe88f046ff11caf7d2
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335550"
---
# <a name="create-workflows-overview"></a>ワークフローの作成の概要

[!include [banner](../includes/banner.md)]

このトピックでは、ワークフローの作成方法を説明します。

## <a name="open-the-workflow-editor"></a>ワークフロー エディターを開く

作成可能なワークフローのタイプは、使用しているモジュールによって決まります。 次の手順に従って、作成するワークフローのタイプを選択し、ワークフロー エディターを開きます。

1. 新しいワークフローを作成するモジュールを開きます。 たとえば、購買要求ワークフローを作成するには、**調達** をクリックします。
2. **設定** &gt; **\[モジュール名\] ワークフロー** の順にクリックします。
3. アクション ウィンドウのリスト ページで、**新規** をクリックします。
4. **ワークフローの作成** ページで、作成するワークフローのタイプを選択し、**ワークフローの作成** をクリックします。 ワークフロー エディターが表示されます。 ワークフローをデザインするには、次の手順を使用できます。

## <a name="drag-workflow-elements-onto-the-canvas"></a>キャンバスへのワークフロー要素のドラッグ

ワークフロー エディターの **ワークフロー要素** 領域には、ワークフローに追加できる要素があります。 ワークフローに要素を追加するには、要素をキャンバスにドラッグします。

## <a name="connect-the-elements"></a>要素の接続

あるワークフロー要素と別のワークフロー要素を接続するには、要素の上にポインターを移動して、接続ポイントが表示されるまで保持します。 接続ポイントをクリックし、別の要素にドラッグします。 すべての要素を接続してください。

## <a name="configure-the-properties-of-the-workflow"></a>ワークフローのプロパティのコンフィギュレーション

次の手順に従って、ワークフローのプロパティをコンフィギュレーションします。

1. どのワークフロー要素も選択されていないようにするため、キャンバスをクリックします。
2. **プロパティ** をクリックして、ワークフローの **プロパティ** ページを開きます。
3. [ワークフロー プロパティのコンフィギュレーション](configure-workflow-properties.md) トピックで示されている次の手順に従います。

## <a name="configure-the-elements-of-the-workflow"></a>ワークフローの要素のコンフィギュレーション

キャンバスにドラッグした各要素をコンフィギュレーションします。 各ワークフロー要素をコンフィギュレーションする方法については、次のトピックを参照してください。

- [ワークフローでの手動タスクのコンフィギュレーション](configure-manual-task-workflow.md)
- [ワークフローでの自動化タスクのコンフィギュレーション](configure-automated-task-workflow.md)
- [ワークフローでの承認プロセスのコンフィギュレーション](configure-approval-process-workflow.md)
- [ワークフローでの承認ステップのコンフィギュレーション](configure-approval-step-workflow.md)
- [ワークフローでの手動決定のコンフィギュレーション](configure-manual-decision-workflow.md)
- [ワークフローでの条件付き意思決定のコンフィギュレーション](configure-conditional-decision-workflow.md)
- [ワークフロー内の並列分岐のコンフィギュレーション](configure-parallel-activity-workflow.md)
- [並列分岐のコンフィギュレーション](configure-parallel-branch-workflow.md)
- [品目ワークフローのコンフィギュレーション](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>エラーまたは警告の解決

ワークフロー エディターの下部にある **エラーおよび警告** ウィンドウには、ワークフローに対して生成されたメッセージが表示されます。 エラーまたは警告が発生した要素を特定するには、エラーまたは警告メッセージをダブルクリックします。 ワークフローを有効にする前に、エラーと警告をすべて解決する必要があります。

## <a name="save-and-activate-the-workflow"></a>ワークフローの保存と有効化

ワークフローを保存して有効化する準備が整ったら、次の手順に従います。

1. **保存して終了** をクリックして、ワークフロー エディターを閉じ、**ワークフローの保存** ページを開きます。
2. ワークフローに加えた変更に関するコメントを入力し、**OK** をクリックします。
3. エラーと警告がすべて解決されると、**ワークフローの有効化** ページが表示されます。 次のいずれかのオプションを選択します。

    - ワークフローのこのバージョンを有効にするには、**新しいバージョンの有効化** をクリックします。 ワークフローが有効な場合は、ユーザーが、処理するドキュメントをワークフローに送信できます。
    - このバージョンを有効にしない場合は、**新しいバージョンを有効にしない** をクリックします。 ワークフローは後で有効にすることができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]