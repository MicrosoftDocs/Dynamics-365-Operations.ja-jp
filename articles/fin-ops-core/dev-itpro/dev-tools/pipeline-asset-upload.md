---
title: Azure Pipelines を使用した資産のアップロード
description: このトピックでは、Azure Pipelines を使用して、Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリにアップロードする方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 26731
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a5eaeeedd967e2e435e06be3cef1d2439b4f935
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883478"
---
# <a name="upload-assets-by-using-azure-pipelines"></a>Azure Pipelines を使用した資産のアップロード

Azure DevOps の **Dynamics Lifecycle Services (LCS) 資産のアップロード** タスクを使用して、 Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリに自動的にアップロードできます。 このタスク **リリース** パイプラインでのみ使用可能です。

このトピックは、[Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](/azure/devops/marketplace/install-extension)を参照してください。

## <a name="make-sure-that-msalps-is-installed"></a>MSAL.PS がインストールされていることを確認する

アップロード タスクのバージョン 1.\* 以降では、MSAL.PS PowerShell ライブラリが使用可能である必要があります。 タスクは、パイプラインの実行中にツールを自動的にインストールするために使用できます。 このタスクは、アップロード タスクの前にステージの任意の場所に追加できます。 詳細については、[MSAL.PS インストール タスクをパイプラインに追加](pipeline-lcs-connection-update.md#add-the-msalps-install-task-to-a-pipeline) を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) 資産 アップロード** のタスク リストを検索します。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
|---|---|---|
| LCS 接続 | あり | LCS へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | あり | 配置する資産およびターゲット環境の両方を含むプロジェクトの ID を LCS に入力します。 プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。 |
| 資産 タイプ | あり | アップロードする資産のタイプを選択します。 |
| アップロードするファイル | あり | LCS アセット ライブラリにアップロードしたいファイルへのパスを入力します。 |
| LCS 資産の名前 | なし | アセット ライブラリに表示する、資産の名前を入力します。 ここで名前を入力しない場合は、ファイル名が使用されます。 |
| LCS の説明 | なし | 資産の詳細に資産を表示する説明を入力します。 |
| 検証を待機する | なし | 検証が必要な資産タイプの場合、このチェック ボックスを使用して、アセットの検証が成功または失敗するまで待機するようにタスクに指示します。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
