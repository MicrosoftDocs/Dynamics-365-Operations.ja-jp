---
title: Azure Pipelines に配置可能なパッケージの作成
description: この記事では、Microsoft Azure DevOps でビルドの自動化を実行するときに、ソフトウェア配置可能なパッケージを作成する方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2de9e17002ffb96d609d6addcea41a746f7ab320
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103202"
---
# <a name="create-deployable-packages-in-azure-pipelines"></a>Azure Pipelines に配置可能なパッケージの作成

カスタマイズを環境に配置する場合は、配置可能なパッケージが Microsoft Dynamics Lifecycle Services (LCS) に必要です。 このパッケージは、ビルド プロセスまたはリリース プロセス中に Azure Pipelines を使用して作成できます。

この記事は、[Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加する前に、Azure DevOps の [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントにインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](/azure/devops/marketplace/install-extension)を参照してください。
>
> この Azure DevOps タスクを実行するには、エージェントで X++ コンパイラ ツールを使用できる必要があります。 このタスクをビルド バーチャル マシン (VM) エージェントで実行するか、コンパイラ ツール NuGetパッケージを使用してください。 NuGet パッケージとパイプラインへのインストール方法の詳細については、[Microsoft がホストするエージェントと Azure Pipelines を使用したビルドの自動化](hosted-build-automation.md)を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**配置可能なパッケージの作成** のタスク リストを検索します。 次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
| --- | --- | --- |
| X++ ツール パス | 有 | X++ ツールの場所のパス。 この場所は、ビルド VM 上の **PackagesLocalDirectory\\bin** フォルダーの場所か、コンパイラ ツール NuGet パッケージの抽出された NuGet ファイルの場所です。 |
| パッケージに対する X++ バイナリの場所 | 有 | 配置可能パッケージに含める X++ パッケージ (モジュール) のすべてのバイナリが格納されているフォルダーのパス。 ビルド パイプラインでこのタスクを使用する場合、このフォルダーは通常、コンパイラの出力フォルダーと同じです。 |
| パッケージ化するバイナリの検索パターン | 有 | **パッケージへの X++ バイナリの場所** オプションで指定されているパス内で、X++ パッケージ (モジュール) 名に一致する名前を指定します。 検索パターンの代わりに名前の一覧を指定したり、テスト パッケージが含まれていないように除外フィルターを指定したりすることもできます。 検索パターンは、フォルダーを検索し、X++ アセンブリ で `bin` サブフォルダーが含まれていることを検証します。 詳細については、[ファイルの一致パターン リファレンス](/azure/devops/pipelines/tasks/file-matching-patterns)を参照してください。  |
| 配置可能なパッケージのファイル名とパス | 有 | 配置可能なパッケージのパスとファイル名。 出力ファイルは zip ファイルであり、ファイル名には通常、ファイルを識別しやすいようにするためのバージョン情報が含まれています。 |

## <a name="nuget-dependency"></a>NuGet の依存関係

ビルド VM でこのタスクを実行すると、NuGet が既に使用可能になっており、アクションは必要ありません。 ただし、このタスクをホストされたエージェントまたはその他のプライベート エージェントで実行する場合は、NuGet がインストールされている必要があります。 この場合、Azure DevOps には、パッケージを作成するタスクを実行する前に実行できる [NuGet ツール インストーラー タスク](/azure/devops/pipelines/tasks/tool/nuget)があります。

> [!NOTE]
> NuGet バージョン 3.4 以降のセマンティック バージョニングが導入されたため、バージョン 3.3.0 またはそれ以前のバージョンをインストールする必要があります。

## <a name="search-for-binaries-to-package"></a>パッケージ化するバイナリの検索

ビルド仮想マシンのレガシー パッケージングと比較して、パッケージング タスクでは、パッケージするモジュールとその場所を指定する必要があります。 標準のパイプラインでは、コンパイル中の X ++ モジュールが Azure DevOps エージェントのバイナリ フォルダーに出力されます。 既定では、パッケージング タスクは X++ バイナリのフォルダーを検索します。 フォルダー名を検索します。 X++ アセンブリを含む `/bin/` サブフォルダーがある場合は、このフォルダー内でタスクが確認されます。

> [!NOTE]
> ソース管理リポジトリに ISV モジュールなどのサード パーティ バイナリが含まれている場合、パッケージ ステップには特にそれらのバイナリが含まれています。 この記事の例のセクションを参照してください。

## <a name="examples-of-search-patterns"></a>検索パターンの例

次の例では、**パッケージへの X ++ バイナリの場所** プロパティが既定値の `$(Build.BinariesDirectory)` に設定されていると想定しています。これは、X ++ コンパイラがバイナリを生成する場所です。

| 検索パターン | 説明 |
| --- | --- |
| `*` | `$(Build.BinariesDirectory)` 内のすべての X++ バイナリを検索する。 これが既定値です。 |
| `*`<br/>`!*Tests` | すべての X++ バイナリを検索し、`Tests` で終了するモジュール名は除外します。 |
| `MyPackage` | `$(Build.BinariesDirectory)` フォルダーで `MyPackage` という名前のモジュールを検索します。 |
| `*`<br/>`$(Build.SourcesDirectory)\Metadata\MyBinaryPackage` | すべての X ++ バイナリを `$(Build.BinariesDirectory)` に含め、 `MyBinaryPackage` という名前のモジュールを `Metadata` フォルダー内のソース ディレクトリ (マップされたソース管理リポジトリ フォルダー) に含めます。 |
| `*`<br/>`!*Tests`<br/>`$(Build.SourcesDirectory)\Metadata\MyISV1`<br/>`$(Build.SourcesDirectory)\Metadata\MyISV2` | すべての X++ バイナリを `$(Build.BinariesDirectory)` に含め、名前が `Tests` で終わるモジュールを除外し、`MyISV1` と `MyISV2` という名前の 2 つのモジュールを `Metadata` フォルダー内のソース ディレクトリ (マップされたソース管理リポジトリ フォルダー) に含めます。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
