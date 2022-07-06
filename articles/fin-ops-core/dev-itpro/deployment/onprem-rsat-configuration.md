---
title: Finance + Operations (on-premises) 環境で RSAT を有効化する
description: このトピックでは、環境を構成および有効化して、Regression Suite Automation Tool で使用するために必要な手順について説明します。
author: faix
ms.date: 03/06/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2022-06-03
ms.openlocfilehash: 7620f101cd9a9582dfc218f1cecf309d7b8c66ee
ms.sourcegitcommit: 1fa1ac1fa25e977e98bc02ed5d9d39bd3a7a28d7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/08/2022
ms.locfileid: "8945858"
---
# <a name="enable-rsat-in-finance--operations-on-premises-environments"></a>Finance + Operations (on-premises) 環境で RSAT を有効化する

Regression Suite Automation Tool (RSAT) を使用すると、Finance + Operations (on-premises) のユーザー受け入れテスト (UAT) の時間と費用を大幅に削減できます。 詳細については、[Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md) を参照してください。

## <a name="generate-and-deploy-the-certificate"></a>証明書を生成して配置する

始める前に、インフラストラクチャ スクリプトの 2.15.0 以降のバージョンが必要です。

1. **インフラストラクチャ** フォルダーが含まれるファイル共有の場所に移動し、**ConfigTemplate.xml** ファイルを開きます。
2. 証明書セクションで、**RSAT** タイプの証明書を検索し、**無効** オプションを **false** に設定します。
3. 次のコマンドを実行して、RSAT 証明書を生成します。

    ```powershell
    .\New-SelfSignedCertificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > ACTIVE Directory Certificate Services (AD&nbsp;CS) の証明書および証明機関 (CA) の証明書は使用できないので、RSAT の証明書は自己署名してある必要があります。

4. 証明書をエクスポートします。

    ```powershell
    .\Export-Certificates.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

5. スクリプトをエクスポートします。

    ```powershell
    .\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

6. 前提条件スクリプトを再実行して、証明書がインストールされていることを確認します。 この手順を管理者として実行します。

    ```powershell
    # If remoting, only execute
    # .\Complete-PreReqs-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ForcePushLBDScripts

    .\Complete-PreReqs.ps1
    ```

## <a name="update-the-local-agent-configuration"></a>ローカル エージェント コンフィギュレーションの更新

開始する前に、ローカル エージェント 3.1.0 以降であることを確認してください。 それ以外の場合は、Microsoft Dynamics Lifecycle Services (LCS) から最新バージョンをダウンロードします。

1. ローカル エージェントが Azure Service Fabric Cluster 内で既にプロビジョニングされている場合は、それを削除します。

    ```powershell
    .\LocalAgentCLI.exe Cleanup <path of localagent-config.json>
    ```

2. **localagent-config.json** ファイルを開きます。
3. **deploymentOptions** で、**rsatEnabled** を **true** に設定します。 また、**rsatCertificateThumbprint** を、生成した RSAT 証明書の拇印に設定する必要があります。 拇印は **ConfigTemplate.xml** ファイルで確認できます。
4. ローカル エージェントをインストールします。

    ```powershell
    .\LocalAgentCLI.exe Install <path of localagent-config.json>
    ```

## <a name="deploy-or-service-your-environment"></a>環境の配置またはサービス

配置されていない新しい環境については、[LCS から Finance + Operations 環境を配置する](.\setup-deploy-on-premises-pu41.md#deploy)から環境の配置方法について参照してください。

既存の環境では、新しいパッケージを配置するか、次の手順に従って環境にサービスを提供して変更を適用します。

1. [LCS](https://lcs.dynamics.com) で、RSAT 構成を適用する環境の **完全な詳細** リンクを選択します。
2. **管理** を選択し、**更新の設定** を選択します。 設定は変更しないでください。
3. **準備** を選択します。

    ダウンロードおよび準備が完了すると、**環境の更新** ボタンが表示されます。

    ![環境の更新ボタン。](media/0a9d43044593450f1a828c0dd7698024.png)

4. **環境の更新** を選択して、環境の更新を開始します。

    更新操作が完了すると、環境は RSAT で動作するように構成されます。
