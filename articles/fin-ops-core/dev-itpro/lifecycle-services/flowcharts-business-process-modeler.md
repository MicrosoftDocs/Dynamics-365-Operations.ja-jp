---
title: ビジネス プロセス モデラー (BPM) のフローチャート
description: このトピックでは、接続フローチャートを変更し、タスク レコーダーからのフローチャートを作成してアップロードし、ビジネス プロセス モデルのフローチャートをインポートする方法について説明します。
author: AngelMarshall
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 11453
ms.assetid: c1735f54-e020-45c6-97d1-d6da2382881b
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 7
ms.openlocfilehash: 825a65c128b2754795e5ad112c9807ebc84de5fc
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547965"
---
# <a name="flowcharts-in-business-process-modeler-bpm"></a>ビジネス プロセス モデラー (BPM) のフローチャート

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> ビジネス プロセス モデラーのフローチャート図は、非推奨になりました。 非推奨の詳細については、[ビジネス プロセス モデラーのフローチャートの図](/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features#flowchart-diagrams-in-business-process-modeler) を参照してください。

Microsoft Dynamics Lifecycle Services (LCS) でビジネス プロセス モデラーを使用して、組織のためにビジネス プロセス フローチャートを定義および格納することができます。 このトピックでは、既定の接続フローチャートを表示する方法、接続したフローチャートを Visio ファイルの形式でエクスポートする方法、および未接続のフローチャートをアップロードして表示する方法について説明します。

-   接続フローチャートは、タスクレコーダーに記録され、ビジネス プロセス シミュレーターにアップロードされたデータに基づいて自動的に生成されるフローチャートです。これには、タスク記録のプロセス ステップも含まれます。 
-   接続されていないフローチャートは、Visio から直接アップロードされます。

<!---
## Connected flowcharts
This section explains how to view a connected flowchart, how to modify it, how to export the flowchart to Visio, how to generate a gap analysis, and how to export the gap analysis to a comma-separated file that you can manually import into Microsoft Visual Studio Team Foundation Server as work items. For information about how to upload recordings of custom business processes, see [Upload custom business processes to Business process modeler (BPM)](upload-business-processes-bpm-task-recorder.md). 

Activities that can appear in flowcharts are described in the following table.

| Activity                  | Description                                                                                                                                                      |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Script                    | Action performed by a script.                                                                                                                                    |
| Loop                      | Action performed repetitively.                                                                                                                                   |
| Service                   | Action performed by a service.                                                                                                                                   |
| Manual                    | Step performed outside of a Finance and Operations app.                                                                                                                               |
| Receive                   | Information received from outside of a Finance and Operations app without using a service or script.                                                                                  |
| Send                      | Information sent outside of a Finance and Operations app without using a service or script.                                                                                           |
| User                      | Action performed by a user.                                                                                                                                      |
| Collapsed                 | A sub-process that is not shown in the diagram. Collapsed processes cannot be expanded.                                                                          |
| Arrow                     | Indicates direction of flow between process steps.                                                                                                               |
| Validation                | Decision point at which a process either proceeds or loops.                                                                                                      |
| Process start (circle)    | The beginning of the process.                                                                                                                                    |
| Process end (bold circle) | The end of the process.                                                                                                                                          |
| Roles                     | Role swimlane. Add roles when a process requires actions by multiple roles to complete. Swimlanes list the default roles that can perform the action. |

### 
--->

### <a name="view-a-connected-flowchart"></a>接続中のフローチャートの表示

既定の接続されたフローチャートは、業界標準ライブラリの多くのノードで使用できます。 ニーズを満たしているかどうかを判断するために接続されているフローチャートを表示することができます。 

接続されたフローチャートを表示するには、次の手順を実行します。

1.  Lifecycle Services にサインインしてプロジェクトを開き、**ビジネス プロセス モデラー** をクリックします。
2.  **プロジェクト ライブラリ** セクションで、表示するライブラリを選択します。 
3.  業務プロセス ライブラリを展開し、関連付けられたフローチャート アイコンを持つライブラリ ノードをクリックします: [![フローチャート BPM トピック 1。](./media/flowchart-bpm-topic1.jpg)](./media/flowchart-bpm-topic1.jpg)

    フローチャートが表示されます。 プロセスの各活動は、図の形によって表されます。 プロセス ステップが右のウィンドウに表示されます。 

<!---
### Modify a connected flowchart

You can modify an existing connected flowchart to match your company's business process.

> [!NOTE]
> Any time you modify a flowchart, a gap is automatically created.

To modify a connected flowchart, follow these steps:
1.  Sign in to Lifecycle Services, open a project, and then click **Business process modeler**.
2.  In the **My libraries** section, select a library to display it.
3.  Open a library node with a flowchart icon.
4.  Make changes to the flowchart.
    -   To change an existing flowchart activity, right-click the activity to display the app bar, and then click **Edit**. Make changes, and then click **Save**.
    -   To add a flowchart activity, drag an activity from the **Activities** list to the flowchart. Right-click the new activity and then click **Edit** to change the name and other information for the activity. Make changes and then click **Save**.
    -   To delete a flowchart activity, right-click the activity, and then click **Delete**.

### Import a business process model flowchart from another library

You can import a business process model flowchart from an existing business process library into a bottom level task.
1.  Select an existing task that does not have an associated flowchart, right-click it to display the app bar, and then click **Import**.
2.  On the **Import business process model** page, select a library to import from, and then select the appropriate business process. Only business processes with existing model flowcharts appear in the list.
3.  When the **Do you want to copy** message appears, click **Yes**. When the import is complete, the flowchart will be associated with the original task. Gap information and the version history are also copied.
--->

### <a name="export-a-flowchart-as-a-visio-file"></a>Visio ファイルとしてフローチャートをエクスポート

業務プロセス モデルのフローチャートは Visio ファイルにエクスポートすることができます。
1.  Lifecycle Services にサインインしてプロジェクトを開き、**ビジネス プロセス モデラー** をクリックします。
2.  **プロジェクト ライブラリ** セクションで、表示するライブラリを選択します。
3.  ライブラリを展開し、関連付けられたフローチャートのアイコンを持つ全てのライブラリ ノードを選択します。
4.  **概要** ウィンドウで、**ダイアグラム** を選択してフローチャートを表示します。   
5.  フローチャート タブで、**エクスポート** をクリックし てVisio 形式のファイルで保存します。 

<!--
### Mark a change to not be a gap
Please note that gap functionality has been deprecated in LCS. To learn more about how to use Azure DevOps Synchronization, see [Synchronize BPM libraries with Azure DevOps](synchronize-bpm-vsts.md).

Any time you modify a flowchart, a gap is automatically created. You can modify any change to no longer be considered a gap. 

To modify a change, follow these steps:

1.  Select the object that you added, and then right-click it.
2.  On the app bar, click **Not a gap**.

### Generate a gap analysis and export it to use with Azure DevOps

You can generate a gap analysis list for the project that you are working with. You can export the gap analysis list to a comma-separated file. You can then import that file to Visual Studio Team Foundation Server to create work items. 

To generate a gap analysis and export it, follow these steps:

1.  Sign in to Lifecycle Services, open a project, and then click **Business process modeler**.
2.  In the **My libraries** section, select a library to display it.
3.  Expand the library and then click any library node that has a flowchart icon associated with it. The flowchart is displayed.
4.  Right-click the flowchart to display the app bar, and then click **Gap list**. The **Gap analysis** page is displayed. The page includes all modifications for the project that you are working with. It includes changes to the standard library and to all default flowcharts for the project.
5.  Optional: To export the gap analysis to a comma-separated file, right-click to display the app bar, and then click **Export**. A .csv file is created. You can import the file into Visual Studio Team Foundation Server to create work items that represent the work that is required to fill in the gaps.
-->

## <a name="unconnected-flowcharts"></a>未接続のフローチャート
Visio ダイアグラムなどの未接続のフローチャートは、財務と運用アプリの外部で実行される高度な業務プロセスの記述に非常に役立ちます。

### <a name="upload-an-unconnected-flowchart"></a>未接続のフローチャートをアップロード

1.  **プロジェクト ライブラリ** セクションで、表示するライブラリを選択します。
2.  ライブラリを展開し、関連付けられたフローチャート・アイコンを持つ全てのライブラリ・ノードをクリックします。
3.  **概要** ウィンドウで、**ダイアグラム** を選択し ます。   
5.  **Visio** タブで、 **アップロード** をクリックしてvisioファイルをアップロードします。

> [!Note] 
> 間違ったファイルをアップロードした場合は、既存のファイルを削除し、新たなファイルをアップロードして置き換えてください。

<!--
### View an unconnected flowchart

A business process with an unconnected Visio flowchart associated with it will have a document icon on its title bar: [![Flowchart BPM topic2.](./media/flowchart-bpm-topic2.jpg)](./media/flowchart-bpm-topic2.jpg)
-   Click the document icon to view the flowchart.
-   Click **Download** on the Visio page to download the flowchart.
--->


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]