---
title: AD FS Microsoft 365 の互換性
description: このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。
author: faix
manager: AnnBe
ms.date: 01/13/2020
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
ms.openlocfilehash: f253e18e1a2bb4ada232e3eaa04372e57ffa41c0
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893381"
---
# <a name="ad-fs-microsoft-365-compatibility"></a>AD FS Microsoft 365 の互換性

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> この機能は、アプリケーション更新プログラム 10.0.8、プラットフォーム更新プログラム 32、および LocalAgent 2.2.0 でのみ完全にサポートされます。 詳細については、[部分的サポート](#partialsupport) を参照してください。 

このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) 環境と Microsoft 365 で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。

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

8. Service Fabric Explorer を使用して、[アプリケーション (AOS など) を再起動](troubleshoot-on-prem.md#restartapplications) します。
9. 配置中に指定されたシステム管理者ユーザーで製品にサインインできることを検証します。 
10. LCS 共有アセット ライブラリから、インフラストラクチャ スクリプトの最新バージョンをダウンロードします。
11. ダウンロードしたインフラストラクチャ スクリプト フォルダーからの Reset-SID.ps1 スクリプトを AOS コンピューターにコピーします。
12. Reset-Sid.ps1 スクリプトを実行します。
    
    ```powershell
    .\Reset-SID.ps1 -AxsfCodePath 'C:\ProgramData\SF\AOS_13\Fabric\work\Applications\AXSFType_App184\AXSF.Code.1.0.20190902'
    ```

## <a name="new-deployments"></a>新しい配置

1. [オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って、ローカル エージェントをインストールします。 ただし、ローカル エージェントを実際にインストールする前に、この手順のステップ 2 を完了してください。
2. ローカル エージェント構成ファイルを変更して、**office365AdfsCompatibility** 値を **True** に設定します。
3. [オンプレミス環境の設定と配置](setup-deploy-on-premises-pu12.md#configureconnector)の「コネクタを構成し、オンプレミスのローカル エージェントをインストールする」の手順に従って作業を続行し、プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンを配置します。 プラットフォーム更新プログラム 28 またはそれ以降を実行する基準バージョンがない場合は、使用可能な最新の基準バージョンを配置します。 次に、プラットフォーム更新プログラム 28 が最上位に配置されるようにサービスを処理します。

## <a name="partial-support"></a><a name="partialsupport"></a> 部分的サポート

部分的サポートとして、ローカル エージェント 2.2.0 またはそれ以降がインストールされていて、プラットフォーム更新プログラム 28 またはそれ以降でサービスを更新する必要があります。

部分的サポートでは、Financial Reporting サービスに対する認証はサポートされていません。  
