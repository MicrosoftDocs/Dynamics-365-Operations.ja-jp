---
title: Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加
description: このトピックでは、Microsoft Azure DevOps でビルドの自動化を実行するときに、既存のソフトウェア配置可能なパッケージにライセンス ファイルを追加する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26731
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-03-05
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 169fd55df3c3d737456dfc22f2a8e52102275108
ms.sourcegitcommit: 2186155e4662ae5010a190c0ede458ef6cf91f24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2020
ms.locfileid: "4409510"
---
# <a name="add-license-files-to-a-deployable-package-in-azure-pipelines"></a>Azure Pipelines にある配置可能なパッケージへのライセンス ファイルの追加

[!include [banner](../includes/banner.md)]

配置可能パッケージを使用して環境を更新する場合は、独立系ソフトウェアベンダー (ISV) またはパートナー X++ のソリューションに対してライセンスが必要になることがあります。 ISV は、リリースまたはビルド パイプラインのライセンスを自動的に追加するパイプラインを作成できます。 ユーザーは、独自のパイプラインを作成して、ISV 配置可能なパッケージとライセンス ファイルを結合することができます。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。

## <a name="adding-the-task-to-a-pipeline"></a>パイプラインへのタスクの追加

YML または Classic パイプラインのビルドにタスクを追加するには、**配置可能なパッケージへのライセンスの追加** のタスク リストを検索します。 次のテーブルに、このタスクで使用可能なオプションを示します。

| 入力名 | 必須 | 説明 |
| --- | --- | --- |
| パッケージに追加するライセンス ファイルの検索パターン | 有 | ビルド エージェントのライセンス ファイルの一覧、またはビルド エージェントのファイルの検索パターン。 ライセンス ファイルをビルド エージェントで使用できるようにするには、それらをソース管理に追加します。 また、パイプラインの前の手順でダウンロードまたは生成することもできます。 詳細については、[ファイルの一致パターン リファレンス](https://docs.microsoft.com/azure/devops/pipelines/tasks/file-matching-patterns)を参照してください。 |
| 更新する配置可能なパッケージのファイル名とパス | 有 | ライセンス ファイルを追加する既存の配置可能パッケージ zip ファイルのパスおよびファイル名。 |
