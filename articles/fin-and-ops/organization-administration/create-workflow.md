---
title: ワークフローの作成
description: このトピックでは、ワークフローの作成方法を説明します。
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 7d4a3c5e12b226a7d801d8db9abcbd15738c1ce0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "353359"
---
# <a name="create-workflows"></a>ワークフローの作成

[!include [banner](../includes/banner.md)]

このトピックでは、ワークフローの作成方法を説明します。

## <a name="open-the-workflow-editor"></a>ワークフロー エディターを開く

作成可能なワークフローのタイプは、使用している Microsoft Dynamics 365 for Finance and Operations モジュールによって決まります。 次の手順に従って、作成するワークフローのタイプを選択し、ワークフロー エディターを開きます。

1. 新しいワークフローを作成するモジュールを開きます。 たとえば、購買要求ワークフローを作成するには、**調達**をクリックします。
2. **設定** &gt; **\[モジュール名\] ワークフロー** の順にクリックします。
3. アクション ウィンドウのリスト ページで、**新規**をクリックします。
4. **ワークフローの作成**ページで、作成するワークフローのタイプを選択し、**ワークフローの作成**をクリックします。 ワークフロー エディターが表示されます。 ワークフローをデザインするには、次の手順を使用できます。

## <a name="drag-workflow-elements-onto-the-canvas"></a>キャンバスへのワークフロー要素のドラッグ

ワークフロー エディターの**ワークフロー要素**領域には、ワークフローに追加できる要素があります。 ワークフローに要素を追加するには、要素をキャンバスにドラッグします。

## <a name="connect-the-elements"></a>要素の接続

あるワークフロー要素と別のワークフロー要素を接続するには、要素の上にポインターを移動して、接続ポイントが表示されるまで保持します。 接続ポイントをクリックし、別の要素にドラッグします。 すべての要素を接続してください。

## <a name="configure-the-properties-of-the-workflow"></a>ワークフローのプロパティのコンフィギュレーション

次の手順に従って、ワークフローのプロパティをコンフィギュレーションします。

1. どのワークフロー要素も選択されていないようにするため、キャンバスをクリックします。
2. **プロパティ**をクリックして、ワークフローの**プロパティ**ページを開きます。
3. [ワークフローのプロパティのコンフィギュレーション](configure-workflow-properties.md) トピックで示されている次の手順に従います。

## <a name="configure-the-elements-of-the-workflow"></a>ワークフローの要素のコンフィギュレーション

キャンバスにドラッグした各要素をコンフィギュレーションします。 各ワークフロー要素をコンフィギュレーションする方法については、次のトピックを参照してください。

- [手動タスクのコンフィギュレーション](configure-manual-task-workflow.md)
- [自動化タスクのコンフィギュレーション](configure-automated-task-workflow.md)
- [承認プロセスのコンフィギュレーション](configure-approval-process-workflow.md)
- [承認ステップのコンフィギュレーション](configure-approval-step-workflow.md)
- [手動決定のコンフィギュレーション](configure-manual-decision-workflow.md)
- [条件付き意思決定のコンフィギュレーション](configure-conditional-decision-workflow.md)
- [並列活動のコンフィギュレーション](configure-parallel-activity-workflow.md)
- [並列分岐のコンフィギュレーション](configure-parallel-branch-workflow.md)
- [行項目ワークフローのコンフィギュレーション](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>エラーまたは警告の解決

ワークフロー エディターの下部にある**エラーおよび警告**ウィンドウには、ワークフローに対して生成されたメッセージが表示されます。 エラーまたは警告が発生した要素を特定するには、エラーまたは警告メッセージをダブルクリックします。 ワークフローを有効にする前に、エラーと警告をすべて解決する必要があります。

## <a name="save-and-activate-the-workflow"></a>ワークフローの保存と有効化

ワークフローを保存して有効化する準備が整ったら、次の手順に従います。

1. **保存して終了**をクリックして、ワークフロー エディターを閉じ、**ワークフローの保存**ページを開きます。
2. ワークフローに加えた変更に関するコメントを入力し、**OK** をクリックします。
3. エラーと警告がすべて解決されると、**ワークフローの有効化**ページが表示されます。 次のいずれかのオプションを選択します。

    - ワークフローのこのバージョンを有効にするには、**新しいバージョンの有効化**をクリックします。 ワークフローが有効な場合は、ユーザーが、処理するドキュメントをワークフローに送信できます。
    - このバージョンを有効にしない場合は、**新しいバージョンを有効にしない**をクリックします。 ワークフローは後で有効にすることができます。
