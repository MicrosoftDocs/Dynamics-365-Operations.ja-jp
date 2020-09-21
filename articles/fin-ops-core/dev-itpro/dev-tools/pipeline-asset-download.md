---
title: Azure パイプラインを使用した資産のダウンロード
description: このトピックでは、Azure パイプラインを使用して、LCS アセット ライブラリから資産をダウンロードする方法について説明します。
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
ms.openlocfilehash: 2d974d546188ef26e736ed28b711884b7135cbc2
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765090"
---
# <a name="download-assets-by-using-azure-pipelines"></a>Azure パイプラインを使用した資産のダウンロード

Azure DevOps の **Lifecycle Services (LCS) 資産のダウンロード** タスクを使用して、**Lifecycle Services アセット ライブラリ** から資産をダウンロードできます。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット ダウンロード** のタスク リストを検索します。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
| --- | --- | --- |
| LCS 接続 | 有 | Dynamics Lifecycle Services (LCS) へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | 有 | 配置する両方の試算と、ターゲット環境を含む、LCS のプロジェクトを識別するプロジェクト ID を入力します。 プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。 |
| ダウンロード先のパス | 有 | 資産のダウンロード先のパスを入力します。 |
| 検索パターン | 有 | **アセット ライブラリ** で資産を検索する方法を選択します。 |

選択した **検索パターン** のタイプに応じて、次のオプションを使用できます。

* **資産 ID (GUID)** を選択する場合は、**LCS ファイル資産 ID**  フィールドに GUID を入力するか、資産 ID の GUID またはセミコロンで区切られた一覧を指定します。
* **名前** を選択する場合は、**LCS ファイル資産タイプ** ドロップダウン リストから資産タイプを選択し、**LCS ファイル資産名** フィールドで検索する名前を選択します。 **MyPackage\*** など、アスタリスク (\*) 記号を使用して名前にワイルドカードを使用することができます。

ダウンロードが正常に行われた後、ファイルパスの一覧を出力変数と共に取得できます。 複数のファイルが存在する場合は、セミコロンで区切られたファイルパスの一覧が出力変数に割り当てられます。 **Azure DevOps** の出力変数の詳細については、[タスクからの出力変数を使用する](https://docs.microsoft.com/azure/devops/pipelines/process/variables?view=azure-devops&tabs=yaml%2Cbatch#use-output-variables-from-tasks) を参照してください
