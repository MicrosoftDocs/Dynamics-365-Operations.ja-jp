---
title: Azure Pipelines を使用した資産のダウンロード
description: このトピックでは、Azure Pipelines を使用して、Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリからダウンロードする方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2e4873119be870d3c0793d73b94520498f50529
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781767"
---
# <a name="download-assets-by-using-azure-pipelines"></a>Azure Pipelines を使用した資産のダウンロード

Azure DevOps の **Lifecycle Services (LCS) 資産のダウンロード** タスクを使用して、Microsoft Dynamics Lifecycle Services (LCS) で資産をアセット ライブラリから自動的にダウンロードできます。

このトピックは、[Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](/azure/devops/marketplace/install-extension)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット ダウンロード** のタスク リストを検索します。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
|---|---|---|
| LCS 接続 | あり | LCS へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | あり | 配置する資産およびターゲット環境の両方を含むプロジェクトの ID を LCS に入力します。 プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。 |
| ダウンロード先のパス | あり | 資産のダウンロード先のパスを入力します。 |
| 検索パターン | あり | LCS の資産ライブラリで資産を検索するために使用する検索パターンのタイプを選択します。 選択した値に応じて、次のオプションを使用できます。<ul><li>**資産 ID (guid)** – この値を選択する場合は、**LCS ファイル資産 ID** フィールドに、資産 ID を入力するか、またはセミコロンで区切られた資産 ID の一覧を入力します。 資産 ID は、グローバル一意識別子 (GUID) です。</li><li>**名前** – この値を選択した場合は、**LCS ファイル資産タイプ** フィールドで資産タイプを選択します。 次に、**LCS ファイル資産名** フィールドで、検索する名前を指定します。 アスタリスク (\*) を名前でワイルドカード文字として使用できます。 たとえば、**MyPackage\*** と入力します。</li></ul> |

ダウンロードが正常に行われた後、ファイル パスの一覧を出力変数と共に取得できます。 複数のファイルが存在する場合は、セミコロンで区切られたファイル パスの一覧が出力変数に割り当てられます。 Azure DevOps の出力変数の詳細については、[タスクからの出力変数を使用する を参照してください](/azure/devops/pipelines/process/variables#use-output-variables-from-tasks) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]