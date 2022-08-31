---
title: Azure Pipelines での LCS 接続認証タスクの MSAL への更新
description: この記事では、認証に Microsoft 認証ライブラリ (MSAL) を使用するように Azure Pipelines を更新する方法について説明します。
author: gianugo
ms.date: 11/30/2021
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.openlocfilehash: 84679f8e8fefd7a69e897db70ce06d4d0df79665
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271059"
---
# <a name="update-lcs-connection-authentication-tasks-to-msal-in-azure-pipelines"></a>Azure Pipelines での LCS 接続認証タスクの MSAL への更新

既定では、Dynamics 365 の Microsoft Azure DevOps タスクの新しいバージョンは、[Microsoft Authentication Library (MSAL)](/azure/active-directory/develop/msal-overview#languages-and-frameworks) をサポートし、認証用の既定で使用します。 これらの新しいバージョンをサポートするには、タスクを実行するすべてのエージェントに MSAL PowerShell ライブラリ (MSAL.PS) をインストールする必要があります。 自己ホストされているエージェントの場合は MSAL.PS ライブラリを [PowerShell ギャラリーから手動でインストール](https://github.com/AzureAD/MSAL.PS/#msalps) できます。 Azure DevOps でホストされているエージェントを含むすべてのエージェントに対して、Microsoft は、パイプラインが実行されるたびに MSAL.PS ライブラリをインストールするタスクを提供します。

## <a name="update-existing-service-connections"></a>既存のサービス接続の更新

既存のサービス接続の場合、**認証エンドポイント** 設定は `https://login.microsoftonline.com/organizations` に更新する必要があります。 国内クラウドを使用している場合は、[国内クラウド](/azure/active-directory/develop/authentication-national-cloud) を参照して、関連するエンドポイントを検索します。 新しいサービス接続を作成すると、既定で正しい認証エンドポイントが設定されます。 この設定は、国内クラウドについてのみ更新する必要があります。

接続の設定方法の詳細については、[Azure Pipelines での LCS 接続の作成](pipeline-lcs-connection.md) を参照してください。

## <a name="add-the-msalps-install-task-to-a-pipeline"></a>MSAL.PS インストール タスクをパイプラインに追加する

YML または Classic パイプラインのビルドに MSAL.PS インストール タスクを追加するには、**MSAL.PS をインストールし、認証を有効にする** のタスク リストを検索します。 このタスクにはオプションや設定はありません。 Microsoft Dynamics Lifecycle Services (LCS) による認証が必要なタスクを実行する前に、このインストールタスクがすべてのエージェントで実行されていることを確認してください。

> [!NOTE]
> MSAL.PS ライブラリは、LCS による認証を必要とするタスクを実行するすべてのエージェントにインストールする必要があります。 パイプラインが複数のステージで構成されている場合、各ステージは異なるエージェントで実行される場合があります。 したがって、各ステージでライブラリを確実にインストールする必要があります。

## <a name="update-existing-tasks"></a>既存のタスクの更新

新しい MSAL 認証を使用するように既存のタスクを更新するには、タスクのバージョンを更新する必要があります。 タスク バージョンの更新方法についての詳細は、[タスク タイプ & 使用](/azure/devops/pipelines/process/tasks?view=azure-devops&tabs=classic#task-versions) を参照してください。 次の表に、認証を使用するタスクを表示します。 また、MSAL を使用する各タスクの最も近いバージョンも表示されます。

| タスク名 | MSAL を使用する最小バージョン |
| --- | --- |
| [Dynamics Lifecycle Services (LCS) アセット ダウンロード](pipeline-asset-download.md) | 2.\* 以降 |
| [Dynamics Lifecycle Services (LCS) アセット アップロード](pipeline-asset-upload.md) | 1.\* 以降 |
| [Dynamics Lifecycle Services (LCS) アセット配置](pipeline-deploy-asset.md) | 1.\* 以降 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
