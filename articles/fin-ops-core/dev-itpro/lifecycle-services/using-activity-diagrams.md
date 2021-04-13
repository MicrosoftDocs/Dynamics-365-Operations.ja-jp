---
title: ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する
description: このトピックでは、BPM ライブラリでアクティビティ図を使用する方法について説明します。
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 24bed4ec28e34e17c2bbf5019cce7f29b5459394
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746035"
---
# <a name="work-with-activity-diagrams-in-business-process-modeler-libraries"></a>ビジネス プロセス モデラー ライブラリの活動ダイアグラムを使用する

[!include [banner](../includes/banner.md)]

活動ダイアグラムを業務プロセスに関連付けることができます。 活動ダイアグラムは、提案されたソフトウェア ソリューションで業務プロセスまたはタスクを完了する方法について記述するために使用されます。

活動ダイアグラムには 2 つの種類があります。

- **タスク記録** – Finance and Operations のタスク記録に関連する業務プロセスには、自動的に生成される活動ダイアグラムおよびプロセスの手順が含まれます。
- **Microsoft Visio** – Visio ファイルを手動でアップロードすることによって、業務プロセスを Visio 図に関連付けることができます。


## <a name="browse-activity-diagrams"></a>活動ダイアグラムの参照
BPM ライブラリ内の **図** 列は、特定の業務プロセスがアクティビティ図に関連付けられているかどうかを示します。 列の番号は、ダイアグラムを含む子プロセスの数を示します。 番号の横にあるシンボルは、現在のノードまたはプロセスがダイアグラムに関連付けられているかどうかを示します。 これらのインジケーターは、Visio ダイアグラムには適用されません。

[![monitoringanddiagnostics01](./media/browse_activity_diagrams.JPG)](./media/browse_activity_diagrams.JPG)

アクティビティ図を表示するには、業務プロセスを選択し、右ウィンドウの **概要** タブで **図** を選択します。 **フローチャート** ページが表示されます。 


## <a name="upload-task-recording"></a>作業記録のアップロード
タスク記録をアップロードするには、アップロードする業務プロセス ライブラリを開きます。 タスクの記録をアップロードするプロセス手順を選択し、**アップロード** をクリックします。

[![activitydiagrams01](./media/activity_diagrams_01.jpg)](./media/activity_diagrams_01.jpg)


右ウィンドウで、**参照** をクリックしてファイルを選択してから **アップロード** をクリックします。

[![activitydiagrams02](./media/activity_diagrams_02.jpg)](./media/activity_diagrams_02.jpg)


## <a name="activity-diagrams-that-are-created-from-task-recordings"></a>タスク記録から作成された活動ダイアグラム

> [!重要] ビジネス プロセス モデラーのフローチャート図は、非推奨になりました。 非推奨の詳細については、[ビジネス プロセス モデラーのフローチャートの図](removed-deprecated-features.md#flowchart-diagrams-in-business-process-modeler) を参照してください。

環境でタスク記録を作成して、Microsoft Dynamics Lifecycle Services (LCS) に直接保存することができます。 この方法で、タスク記録を BPM ライブラリ内の業務プロセスと関連付けることができます。 詳細については、[ヘルプ システムの接続](../../fin-ops/get-started/help-connect.md) および [タスク レコーダーを使用したドキュメントやトレーニングの作成](../user-interface/task-recorder-training-docs.md) を参照してください。

タスク レコーダー ツールを使用すると、配布可能な記録ファイルを作成できます。 記録ファイルは、.axtr ファイル名拡張子を持ちます。 手動で記録ファイルをアップロードすることにより、BPM 内の業務プロセスをタスク記録に関連付けることができます。 

記録ファイルをアップロードするには、業務プロセスを選択し、右ウィンドウの **概要** タブで **アップロード** を選択します。

BPM は作成されたすべてのタスク記録の活動ダイアグラムと詳細なプロセスの手順を自動的に生成します。 次の図は、例を示します。

![活動ダイアグラムおよびタスク記録プロセスの手順の例](./media/NEWBPM_BlogPost17-1024x483.png "活動ダイアグラムおよびタスク記録プロセスの手順の例")


## <a name="visio-files"></a>Visio ファイル
業務プロセスを Visio 図に関連付けることができます。 この機能は通常、タスク記録では表現できない高度なプロセスに使用されます。

> [!Note]
> BPM は .vsd および .vsdx ファイルをサポートしています。 ただし、.vsdm ファイル (マクロ対応の Visio 図面ファイル) はサポートされていません。 .vsd ファイルにマクロが含まれている場合、BPM マクロの実行が無効になります。

Visio ファイルを表示またはアップロードするには、次の手順を実行します。

1. 業務プロセスを選択し、右ウィンドウの **概要** タブで **図** を選択します。
2. **フローチャート** ページで、**Visio** タブを選択します。詳細については、[ビジネス プロセス モデラーのフローチャート (BPM)](flowcharts-business-process-modeler.md) の未接続のフローチャート セクションを参照してください。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]