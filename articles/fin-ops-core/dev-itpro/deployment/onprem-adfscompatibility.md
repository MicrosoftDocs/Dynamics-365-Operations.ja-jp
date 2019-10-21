---
title: AD FS Office 365の互換性
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft Office 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。
author: faix
manager: AnnBe
ms.date: 09/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: dc858034cfa5e6929966eb211c3c7372dc8ee0cf
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249316"
---
# <a name="ad-fs-office-365-compatibility"></a>AD FS Office 365 の互換性

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> 現在、この機能は財務報告と互換性がありません。 

> ローカル エージェント 2.2.0 またはそれ以降がインストールされていて、プラットフォーム更新プログラム 28 またはそれ以降でサービスを行う必要があります。

このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft Office 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。

## <a name="existing-deployments"></a>既存の配置

1. Microsoft Dynamics Lifecycle Services (LCS) から新しいローカル エージェント バージョンをダウンロードします。 バージョン 2.2.0 またはそれ以降である必要があります。
2. この機能に必要な追加の構成が含まれているので、ローカル エージェント構成ファイルの新しいバージョンをダウンロードします。
3. 新しいローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。
4. 次のコマンドを実行して、古いローカル エージェント バージョンをクラスターからアンインストールします。

    ```powershell
    .\LocalAgentCLI.exe Cleanup '<path of localagent-config.json>'
    ```

5. 次のコマンドを実行して、新しいローカル エージェント バージョンをインストールします。

    ```powershell
    .\LocalAgentCLI.exe Install '<path of localagent-config.json>'
    ```

6. 新しい構成を使用できるようにするには、プラットフォーム更新プログラム 28 またはそれ以降を使用したサービス操作を実行します。
7. サービス操作が完了したら、次のスクリプトを実行します。

    ```powershell
    .\Reset-DatabaseUsers.ps1 -DatabaseServer '<FQDN of the SQL server>' -DatabaseName '<AX database name>'
    ```

    > [!IMPORTANT]
    > このステップを省略すると、プライマリ管理者ユーザーはサインインできなくなります。

8. Service Fabric Explorer を使用して、[Application Object Server (AOS) ノードを再起動](troubleshoot-on-prem.md#restartapplications)します。
9. USERINFO テーブルで SQL クエリを実行して **NETWORKDOMAIN** フィールドを変更します。 古い構成が `https://ax.contoso.com/adfs` だった場合は、すべてのユーザー エントリを `http://ax.contoso.com/adfs/services/trust` に変更する必要があります。

## <a name="new-deployments"></a>新しい配置

1. [オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って、ローカル エージェントをインストールします。 ただし、ローカル エージェントを実際にインストールする前に、この手順のステップ 2 を完了してください。
2. ローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。
3. [オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って作業を続行し、プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンを配置します。 プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンがない場合は、使用可能な最新の基準バージョンを配置します。 次に、プラットフォーム更新プログラム 28 が最上位に配置されるようにサービスを処理します。
