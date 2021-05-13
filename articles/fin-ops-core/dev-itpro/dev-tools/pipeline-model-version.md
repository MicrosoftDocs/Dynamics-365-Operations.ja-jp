---
title: Azure Pipelines で、X++ モデルのバージョン管理
description: このトピックでは、Microsoft Azure DevOps でビルドの自動化を実行するときにバージョン X++ のモデルを自動的に作成する方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59a23ba0bfae452371c33cbf5cc6a66202f6f2ce
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923411"
---
# <a name="x-model-versioning-in-azure-pipelines"></a>Azure Pipelines で、X++ モデルのバージョン管理

ビルドの自動化時に、X++ モデル バージョンを更新して、パイプラインのビルド番号に一致またはリンクするようにすることができます。 これらの更新プログラムを使用すると、ユーザーは実行中の X++ パッケージのバージョンを容易に識別できるようになります。 また、開発者がバージョンを追跡して、ビルド パイプラインやソース コード ファイルのバージョンに戻すこともできます。

このトピックは、[Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](/azure/devops/marketplace/install-extension)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**モデル バージョンの更新** のタスク リストを検索します。 次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
| --- | --- | --- |
| X++ のソースの場所 | 有 | X++ ソース コードを含む親フォルダーのパス。 **記述子の検索パターン** オプションは、このパスとサブフォルダーで実行されます。 既定値 **$(Build.SourcesDirectory)** は、ソース コード リポジトリのルートをポイントします。 |
| 記述子検索パターン | 有 | **X++ のソースの場所** オプションで指定されたパス内の記述子ファイルを検索するファイルに一致するパターンを指定します。 また、検索パターンではなく、記述子ファイルの完全パスの一覧を指定することもできます。 詳細については、[ファイルの一致パターン リファレンス](/azure/devops/pipelines/tasks/file-matching-patterns)を参照してください。 |
| 更新する最下位のレイヤー | 有 | 検索パターンを使用している場合、このタスクによって、ソース管理の ISV またはパートナー コードの記述子が検出される場合があります。 これらの記述子のバージョンは、更新されない可能性があります。 このオプションを使用すると、タスクによって更新される最も低いレイヤーを定義する追加のフィルタを定義できます。 |
| 更新するバージョン番号 (形式 #.#.#.#) | 有 | 記述子に書き込むバージョン番号。 この形式は、ピリオド (.) で区切られた 4 桁の数字で構成されている必要があることに注意してください。 ビルド ID またはビルド番号を使用すると、追跡可能になります。 既定のビルド番号は正しい形式ではないことに注意してください。 形式は、**オプション** \> **ビルド番号の形式** の下にあるクラシック エディターで変更できます。 また、YML ファイルの先頭に `name:` タグを追加することによって変更することもできます。 年、月、日、およびビルド数リビジョン番号を使用する有効なビルド番号の例として、`$(Date:yy.MM.dd)$(Rev:.r)` があります。 詳細については、[実行番号またはビルド番号の構成](/azure/devops/pipelines/process/run-number)を参照してください。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]