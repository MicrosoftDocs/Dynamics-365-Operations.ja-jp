---
title: Azure Pipelines を使用した資産のデプロイ
description: このトピックでは、Azure DevOps のパイプラインを使用して、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリから資産を配置する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b811510ee479f9a7c6a801fb0a9e32d7a5f6c5c1
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2021
ms.locfileid: "4723391"
---
# <a name="deploy-assets-by-using-azure-pipelines"></a>Azure Pipelines を使用した資産のデプロイ

Microsoft Azure DevOps の **Lifecycle Services (LCS) 資産の配置** タスクを使用して、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリに保存されている資産の配置を特定の環境に自動的に配置できます。 ただし、このタスクには、次のような考慮すべき制限があります。

* このタスクは、**リリース** パイプラインでのみ使用できます。
* ソフトウェア配置可能パッケージの運用環境への配置を自動化することはできません。
* ソフトウェア配置可能パッケージをビルド環境に配置することはできません。
* ソフトウェア配置可能パッケージを、ローカル ビジネス データ (LBD) 環境にオンプレミスで配置することはできません。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット配置** のタスク リストを検索します。 ターゲット環境にセルフ サービス環境が含まれている場合は、必ずタスク バージョン 1.\* 以降を選択してください。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
|---|---|---|
| LCS 接続 | あり | LCS へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | あり | 配置する資産およびターゲット環境の両方を含むプロジェクトの ID を LCS に入力します。 プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。 |
| LCS 環境 ID | 有 | ターゲット環境の ID を入力します。 環境 ID はグローバル一意識別子 (GUID) であり、環境詳細ページの **環境詳細**\>**環境 ID** で検索できます。 |
| LCS ファイル資産 ID | 有 | 配置するソフトウェア配置可能なパッケージの資産 ID を入力します。 資産 ID は、資産ライブラリで検索できる GUID です。 配置する資産の行を選択し、**追加の詳細** の下の **資産 ID** フィールドを検索します。 通常、この ID は、[Dynamics Lifecycle Services (LCS) 資産アップロード](pipeline-asset-upload.md) タスクなどの他のパイプライン ステップから動的に取得されます。 |
| 更新プログラムの名前 | あり | LCS の環境履歴に表示される更新プログラムの名前を入力します。 |
| 完了まで待機する | 清算済 (いいえ) | このチェック ボックスをオンにして、資産の配置が成功または失敗するまで待機するようタスクに指示します。 清算済 (**いいえ**) の場合、タスクは配置のみを開始します。 タスクが待機するように指示されている場合、実行時間の長い配置中にパイプラインのタイムアウトが発生することがあります。 タイムアウト オプションの詳細については、[タイムアウト](https://docs.microsoft.com/azure/devops/pipelines/process/phases#timeouts) を参照してください。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]