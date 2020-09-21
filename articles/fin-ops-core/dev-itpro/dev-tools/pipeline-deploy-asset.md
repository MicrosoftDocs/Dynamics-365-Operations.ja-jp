---
title: Azure Pipelines を使用した資産の配置
description: このトピックでは、Microsoft Azure DevOps でパイプラインを使用して、LCS アセット ライブラリから資産を配置する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee92c7cf94d614e51fd2510e2c1742256aa728d6
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765093"
---
# <a name="deploy-assets-by-using-azure-pipelines"></a>Azure Pipelines を使用した資産の配置

Azure DevOps の **Lifecycle Services (LCS) 資産の配置** タスクを使用して、**Lifecycle Services アセット ライブラリ** に保存されている資産を特定の環境に自動的に配置できます。 このタスクには、考慮すべき制限がいくつかあります。

* このタスクは **リリース** パイプラインでのみ使用できます。
* このタスクでは、ソフトウェア配置可能なパッケージを運用環境に展開することを自動化することはできません。
* このタスクでは、ソフトウェア配置可能なパッケージを運用環境にビルドすることを自動化することはできません。
* このタスクでは、ソフトウェアで配置可能なパッケージを、**ローカルビジネスデータ** (LBD) 環境にオンプレミスで配置することはできません。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット配置** のタスク リストを検索します。 ターゲット環境にセルフサービス環境が含まれている場合は、**タスク バージョン** 1.\* またはそれ以降を必ず選択してください。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
| --- | --- | --- |
| LCS 接続 | 有 | Dynamics Lifecycle Services (LCS) へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | 有 | 配置する両方の試算と、ターゲット環境を含む、LCS のプロジェクトを識別するプロジェクト ID を入力します。 プロジェクト ID は、自分のプロジェクトのダッシュボードの URL の末尾に記載できます。 |
| LCS 環境 ID | 有 | ターゲット環境の ID を入力します。 環境 ID は、**環境の詳細** > **環境 ID** の環境の詳細ページにある GUID です 。 |
| LCS ファイル資産 ID | 有 | 配置するソフトウェア配置可能なパッケージの資産 ID を入力します。 資産 ID は、アセット ライブラリで検索できる GUID です。 配置する資産の行を選択し、**追加の詳細** の下に **資産 ID** を検索します。 通常、この ID は、[Dynamics Lifecycle Services (LCS) 資産 アップロード タスク](pipeline-asset-upload.md) などの他のパイプライン ステップから動的に取得されます。 |
| 更新プログラムの名前 | 有 | この名前は、LCS 環境履歴に示される更新プログラムの名前です。 |
| 完了まで待機する | 第        条 | このチェック ボックスをオンにすると、タスクは、資産の検証が成功または失敗するまで待機するようになります。 **いいえ** に設定した場合、タスクは配置のみを開始します。 実行時間の長い配置では、待機するように指示された場合にパイプラインのタイムアウトが発生することがあります。 タイムアウト オプションの詳細については、[パイプラインでのジョブの指定](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=classic&viewFallbackFrom=vsts#timeouts) を参照してください。 |
