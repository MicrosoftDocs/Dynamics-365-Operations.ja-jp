---
title: ローカル エージェントの配置前スクリプトおよび配置後スクリプト
description: このトピックでは、ローカル エージェントの配置前スクリプトおよび配置後スクリプトに関する情報を提供します。
author: faix
manager: AnnBe
ms.date: 08/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: f501f44f4c717dbfe0f4fdb50cbfbfb00e376a4a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687897"
---
# <a name="local-agent-pre-deployment-and-post-deployment-scripts"></a>ローカル エージェントの配置前スクリプトおよび配置後スクリプト

[!include [banner](../includes/banner.md)]

ローカル エージェント 2.3.0 は、配置前スクリプトおよび配置後スクリプトの実行をサポートしています。 したがって、環境配置の前後に実行される Microsoft Windows PowerShell スクリプトを設定できるようになりました。 この機能は、配置と再配置に適用されるほか、サービス操作にも適用されます。

この機能を使用できるようにするには、エージェント ファイル共有にスクリプト フォルダーを作成する必要があります。 配置前スクリプトを実行するには、スクリプト フォルダーに **PreDeployment.ps1** ファイルを作成します。 配置後スクリプトを実行するには、**PostDeployment.ps1** ファイルを作成します。 次の例は、フォルダー構造を示しています。

- \\\\\\fileserver\\agent\\scripts\\PreDeployment.ps1
- \\\\\\fileserver\\agent\\scripts\\PostDeployment.ps1

これらのファイルが存在しない場合、配置は通常どおりに続行されます。 次の例は、新しい配置フローを示しています。

**配置または再配置**:

1. 異常なモジュールを取得します。 このステップでは、既存のサービスの健全性を取得して、問題を見つけます。 このステップは再配置シナリオにのみ適用されます。
2. モジュールをクリーンアップします。 このステップでは、サービスが取り除かれ、**wp** フォルダの内容が削除されます。 このステップは再配置シナリオにのみ適用されます。
3. ダウンロード コンポーネントをリンクします。 このステップでは、Microsoft Dynamics Lifecycle Services (LCS) からのコンポーネントのダウンロード、抽出、処理が行われます。
4. 配置前スクリプト。 このステップでは **PreDeployment.ps1** スクリプト (存在する場合) が実行されます。
5. モジュールを設定します。 このステップでは、新しいサービスが配置されます。
6. 配置後スクリプト。 このステップでは **PostDeployment.ps1** スクリプト (存在する場合) が実行されます。

**サービス:**

1. サービスの準備を行います。 このステップでは、LCS でパッケージを準備し、環境にダウンロードします。
2. モジュールをクリーンアップします。 このステップでは、サービスが取り除かれ、**wp** フォルダの内容が削除されます。
3. ダウンロード コンポーネントをリンクします。 このステップでは、LCS から以前にダウンロードしたコンポーネントの抽出および処理が行われます。
4. 配置前スクリプト。 このステップでは **PreDeployment.ps1** スクリプト (存在する場合) が実行されます。
5. モジュールを設定します。 このステップでは、新しいサービスが配置されます。
6. 配置後スクリプト。 このステップでは **PostDeployment.ps1** スクリプト (存在する場合) が実行されます。

> [!NOTE]
> 配置前スクリプトと配置後スクリプトには、任意のものを含めることができます。 スクリプトによって実行されるコードは、顧客の責任を負うものです。 ローカル エージェントはスクリプトを起動するだけです。

## <a name="customizations"></a>カスタマイズ

スクリプト実行の既定のタイムアウトは 30 分です。 この値を変更するには、localagent-config.json ファイルを変更し、その変更したファイルを使用してローカル エージェントを再インストールします。 次の属性は、タイムアウト値を定義するもので、ここで示すように設定する必要があります。 (ここに示すコードは、ファイル内の **LocalAgent** コンポーネントに含まれています。)

```json
"powershellScriptRunner": {
    "timeoutMinutes": {
        "value": "30"
        }
    }
```

## <a name="logging"></a>ログ記録

スクリプトからの出力およびエラー メッセージは、.log ファイルや .err ファイルとして、スクリプト フォルダーのログ フォルダーに書き込まれます。 スクリプトがタイムアウトした場合は、エラー メッセージのみがログに記録されます。 このエラー メッセージには、タイムアウトのメッセージが含まれます。 この場合、他の出力は記録されません。

スクリプトの実行は、Event Tracing for Windows (ETW) イベントとしてもログに記録されます。 これらのイベントはイベント ビューアーで表示できます。 スクリプトでエラーが発生すると、エラー イベントがログに記録されますが、配置は通常どおり続行されます。

