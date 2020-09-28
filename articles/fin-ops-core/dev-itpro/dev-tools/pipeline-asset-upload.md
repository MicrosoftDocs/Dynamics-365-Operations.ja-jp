---
title: Azure Pipelines を使用した資産のアップロード
description: このトピックでは、Azure Pipelines を使用して、LCS アセット ライブラリへ資産をアップロードする方法について説明します。
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
ms.custom: 26731
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4996bcc8da49f188bbd7bffef66b6c58b6c139e9
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765091"
---
# <a name="upload-assets-by-using-azure-pipelines"></a>Azure Pipelines を使用した資産のアップロード

Azure DevOps の **Lifecycle Services (LCS) 資産のアップロード** タスクを使用して、**Lifecycle Services アセット ライブラリ** へ資産を自動的にアップロードできます。 このタスクは **リリース** パイプラインでのみ使用できます。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) 資産 アップロード** のタスク リストを検索します。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
| --- | --- | --- |
| LCS 接続 | 有 | Dynamics Lifecycle Services (LCS) へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | 有 | 配置する両方の試算と、ターゲット環境を含む、LCS のプロジェクトを識別するプロジェクト ID を入力します。 プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。 |
| 資産 タイプ | 有 | アップロードする資産のタイプを選択します。 |
| アップロードするファイル | 有 | LCS **アセット ライブラリ** にアップロードするファイルへのパスを入力します。 |
| LCS 資産の名前 | 第        条 | **アセット ライブラリ** に表示する、資産の名前を入力します。 名前が指定されていない場合は、ファイル名が使用されます。 |
| LCS の説明 | 第        条 | アセット の詳細に表示する、資産の説明を入力します。 |
| 検証を待機する | 第        条 | 検証が必要な資産タイプの場合、このチェック ボックスをオンにすると、タスクは、資産の検証が成功または失敗するまで待機するようになります。 |
