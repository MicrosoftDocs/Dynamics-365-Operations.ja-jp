---
title: Azure Pipelines を使用した資産のデプロイ
description: この記事では、Azure DevOps のパイプラインを使用して、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリから資産を配置する方法について説明します。
author: gianugo
ms.date: 04/29/2020
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.openlocfilehash: 05a8c116206b321c782b039932d889568020e054
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271063"
---
# <a name="deploy-assets-by-using-azure-pipelines"></a>Azure Pipelines を使用した資産のデプロイ

Microsoft Azure DevOps の **Dynamics Lifecycle Services (LCS) 資産の配置** タスクを使用して、Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリに保存されている資産の配置を特定の環境に自動的に配置できます。 ただし、このタスクには、次のような考慮すべき制限があります。

* このタスクは、**リリース** パイプラインでのみ使用できます。
* ソフトウェア配置可能パッケージの運用環境への配置を自動化することはできません。
* ソフトウェア配置可能パッケージをビルド環境に配置することはできません。
* Commerce Cloud Scale Unit (CSU) 拡張機能パッケージ、および eコマース パッケージは、オンプレミスのローカル ビジネス データ環境には展開できません。

> [!NOTE]
> Commerce Cloud Scale Unit (CSU) 拡張機能または eコマース パッケージは、**Dynamics Lifecycle Services (LCS) アセット配置** を使用して、運用、UAT、またはサンドボックス環境に展開できます

この記事は、[Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識があることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加する前に、Azure DevOps の [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントにインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](/azure/devops/marketplace/install-extension)を参照してください。

## <a name="dynamics-365-for-finance--operations-on-premises-package-deployment"></a>Dynamics 365 for Finance + Operations (on-premises) パッケージ展開

**Dynamics 365 Finance and Operations Tools** 拡張のバージョン 0.2.1239020 から、オンプレミスのローカル ビジネス データ環境にパッケージを展開することが可能になりました。 少なくとも **Dynamics Lifecycle Services (LCS) アセット配置** タスクのバージョン 3.\* を使用する必要があります。 その後、**資産のタイプ** フィールドで **オンプレミス環境のソフトウェア配置可能パッケージ** を選択できます。

> [!NOTE]
> パイプラインの実行全体には 1 時間以上かかるので、Microsoft がホストしている無料のエージェントはタイムアウトになりますので使用すべきではありません。

## <a name="dynamics-365-commerce-cloud-scale-unit-csu-extension-and-e-commerce-package-deployment"></a>Dynamics 365 Commerce Cloud Scale Unit (CSU) 拡張機能および eコマース パッケージの展開

バージョン 3.\* から、**Dynamics Lifecycle Services (LCS) アセット配置** タスクがコマース パッケージの展開に対応しています。 コマース パッケージの配置タイプを選択するために、**資産のタイプ** という新しいフィールド タイプが追加されました。 以下の値は、このフィールドで使用できます:

- **ソフトウェア配置可能パッケージ - 財務と運用の環境配置** (既定値)
- **Commerce Cloud Scale Unit 拡張機能 - CSU 拡張機能パッケージの展開** 
- **eコマース パッケージ - eコマース環境の配置**

**Commerce Cloud Scale Unit 拡張機能n - CSU 拡張機能パッケージ** または **eコマース パッケージ - eコマース環境の配置** オプションのいずれかを選択すると、以前の展開より優先されます。 複数の CSU 拡張機能パッケージがある場合は、すべての CSU パッケージを配置用の 1 つのパッケージとしてマージする必要があります。

## <a name="make-sure-that-msalps-is-installed"></a>MSAL.PS がインストールされていることを確認する

配置タスクのバージョン 2.\* 以降では、MSAL.PS PowerShell ライブラリが使用可能である必要があります。 タスクは、パイプラインの実行中にツールを自動的にインストールするために使用できます。 このタスクは、配置タスクの前にステージの任意の場所に追加できます。 詳細については、[MSAL.PS インストール タスクをパイプラインに追加](pipeline-lcs-connection-update.md#add-the-msalps-install-task-to-a-pipeline) を参照してください。

## <a name="add-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**Dynamics Lifecycle Services (LCS) アセット配置** のタスク リストを検索します。 ターゲット環境にセルフ サービス環境が含まれている場合は、必ずタスク バージョン 1.\* 以降を選択してください。

次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
|---|---|---|
| LCS 接続 | あり | LCS へのサービス接続を選択または作成します。 詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。 |
| LCS プロジェクト ID | あり | 配置する資産およびターゲット環境の両方を含むプロジェクトの ID を LCS に入力します。 プロジェクト ID は、プロジェクトのダッシュボードの URL の末尾に記載できます。 |
| LCS 環境 ID | 有 | ターゲット環境の ID を入力します。 環境 ID はグローバル一意識別子 (GUID) であり、環境詳細ページの **環境詳細**\>**環境 ID** で検索できます。 |
| LCS ファイル資産 ID | 有 | 配置するソフトウェア配置可能なパッケージの資産 ID を入力します。 資産 ID は、資産ライブラリで検索できる GUID です。 配置する資産の行を選択し、**追加の詳細** の下の **資産 ID** フィールドを検索します。 通常、この ID は、[Dynamics Lifecycle Services (LCS) 資産アップロード](pipeline-asset-upload.md) タスクなどの他のパイプライン ステップから動的に取得されます。 |
| 資産 タイプ | 有効 | LCS で環境に展開する資産のタイプを選択する オプションは、**ソフトウェア配置可能パッケージ - 財務と運用環境の配置**、**オンプレミス環境のソフトウェア配置可能パッケージ - Finance + Operations (on-premises) 環境の配置**、**Commerce Cloud Scale Unit 拡張機能 - CSU 拡張パッケージの配置**、および **e コマース パッケージ - e コマース環境の配置** があります。 |
| Commerce Cloud Scale Unit 名 | 無効 | Commerce Cloud Scale Unit 環境の名前を入力すると、**環境機能** \> **コマース** \> **管理** \> **コマース配置 & 設定** \> **Commerce scale units** の下で、環境詳細ページに環境名が表示されます。 パッケージ タイプが **Commerce Cloud Scale Unit 拡張機能** として選択されると、フィールド **Commerce Cloud Scale Unit 名** の値は必須になります。 |
| eコマース環境名 | 無効 | eコマース環境の名前を入力すると、**環境機能** \> **コマース** \> **管理** \> **コマース配置 & 設定** \> **eコマース** の下で、環境詳細ページに環境名が表示されます。 パッケージ タイプが **eコマース パッケージ** として選択されると、フィールド **eコマース環境名** の値は必須になります。 |
| 更新プログラムの名前 | 有効 | LCS の環境履歴に表示される更新プログラムの名前を入力します。 |
| 完了まで待機する | 清算済 (いいえ) | このチェック ボックスをオンにして、資産の配置が成功または失敗するまで待機するようタスクに指示します。 清算済 (**いいえ**) の場合、タスクは配置のみを開始します。 タスクが待機するように指示されている場合、実行時間の長い配置中にパイプラインのタイムアウトが発生することがあります。 タイムアウト オプションの詳細については、[タイムアウト](/azure/devops/pipelines/process/phases#timeouts) を参照してください。 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

