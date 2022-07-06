---
title: オンプレミス環境でのネットワーク プリンター デバイスのインストール
description: この記事では、Microsoft Dynamics 365 Finance + Operations (on-premises) のオンプレミス展開を既存のネットワーク プリンタ デバイスに接続する方法について説明します。
author: RichdiMSFT
ms.date: 04/07/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1ac4cce3eebb425bdc3706d05839115c2649ea58
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847357"
---
# <a name="install-network-printer-devices-in-on-premises-environments"></a>オンプレミス環境でのネットワーク プリンター デバイスのインストール

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Finance + Operations (on-premises) のオンプレミス展開を既存のネットワーク プリンタ デバイスに接続する方法について説明します。 オンプレミス アプリケーションでのネットワーク印刷は、Microsoft Windows Server 2016 の「[印刷およびドキュメント サービス](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831468(v=ws.11))」機能でサポートされます。 この機能を使用すると、プリンター管理に関連するタスクを集中管理できます。 印刷およびドキュメント サービスをインストールして構成するには、Application Object Server (AOS) のプライマリー インスタンスをホストするサーバーへの管理アクセス権が必要です。

ネットワーク印刷サービスの構成には、次の 2 つの役割があります。

- **サービス管理者** – この役割を持つ担当者は、インストールやプラットフォーム インフラストラクチャのコンポーネントのコンフィギュレーションを担当します。 従来、この役割は昇格したドメイン権限を持った Active Directory アカウントです。 Microsoft Windows Server のコンポーネントのインストールに必要な権限があります。
- **組織の管理者** – このロールを持つユーザーはアプリケーション セキュリティ権限を管理します。 この Active Directory アカウントは、**システム管理者** ロールに割り当てられています。

組織の管理者がネットワーク プリンターの追加を開始する前に、サービス管理者はプライマリ AOS インスタンスをホストするサーバーに印刷およびドキュメント サービスをインストールして構成する必要があります。 組織の管理者は、組み込みツールを使用してネットワーク プリンター デバイスの設定を開始できます。

## <a name="install-and-configure-print-and-document-services"></a>印刷およびドキュメント サービスのインストールと構成

環境管理者は、このセクションの情報を使用してネットワーク印刷サービスを有効にします。

1. [印刷およびドキュメント サービスのインストール](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134159(v=ws.11))の手順に従って印刷およびドキュメント サービスをインストールします。
2. 次の手順に従って印刷およびドキュメント サービスをコンフィギュレーションします [印刷およびドキュメント サービスのコンフィギュレーション](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj134163(v=ws.11))。
3. AXService アプリケーションをホストするために使用する各サーバーに対して、これらの手順に従います。
    1. ローカル サーバーで、**ローカル ユーザーとグループ** マネージャーを開始します。
    2. **グループ** ノードを選択します。
    3. **出力演算子** を右クリックし、**グループへの追加** を選択します。
    4. グループに AXService アプリケーションを実行するために使用されるネットワーク Active Directory アカウントを追加します。

> [!NOTE]
> インフラストラクチャ スクリプトのバージョン 2.9.0 移行、アカウントは自動的に適切なグループに追加されます。

### <a name="install-printers-on-nodes-where-axservice-is-executing-under-a-domain-account"></a>AXService がドメイン アカウントで実行されているノードにプリンターをインストール
AXService がドメイン アカウントで実行されているノードにプリンターをインストールするには、次の手順に従います。

1. AXService ユーザー アカウントを使用してネットワーク プリンターをインストールします。 このステップにより、プリンター ドライバーが AXService ユーザー アカウントで使用できることを確認します。
2. すべての接続が正しく構成されていることを確認するため、インストールされているプリンターのテスト ページを印刷します。
3. ユーザーのプロファイルが正しく読み込まれることを確認し、プリンターを見つけるために、AXService アプリケーションを再起動します。

### <a name="install-printers-on-nodes-where-axservice-is-executing-under-a-group-managed-service-account-gmsa"></a>AXService がグループ管理サービス アカウント (gMSA) で実行されているノードにプリンターをインストール
AXService が gMSA で実行されているノードにプリンターをインストールするには、次の手順に従います。

> [!IMPORTANT]
> このセクションには、少なくともバージョン 2.9.0 のインフラストラクチャ スクリプトが必要です。
> また 、[SysInternals Suite](/sysinternals/downloads/) をダウンロードする必要があります 。

1. AOS が使用可能になる各プリンタのネットワーク上の場所を追加して、Printers.json ファイルを更新します。 例のエントリを必ず削除してください。 
2. インフラストラクチャ スクリプト フォルダから次のコマンドを実行します。

```powershell
# Exports the script files to be executed on each VM into a directory VMs\<VMName>.
.\Export-Scripts.ps1 -ConfigurationFilePath .\ConfigTemplate.xml    
```

3. 各 infrastructure\VMs\<VMName> フォルダーの内容を、対応する VM にコピーします。 (リモート処理スクリプトを使用している場合は、コンテンツが自動的に対象の VM にコピーされます。) 続いて、次のコマンドを管理者として実行します。

> [!NOTE]
> - 次の手順では、複数の VM での実行が必要です。 ただし、プロセスを簡略化するために、提供されるリモート処理スクリプトを使用できます。 これらのスクリプトを使用すると、**.\\Export-Scripts.ps1** コマンドの実行に使用されるのと同じコンピューターなど、単一のコンピューターから必要なスクリプトを実行できます。 リモート処理スクリプトが利用可能な場合、Windows PowerShell セクションの **\# If Remoting** コメントの後に宣言されます。
> - リモート処理では [WinRM](/windows/win32/winrm/portal?redirectedfrom=MSDN) を使用します。 場合によっては、[CredSSP](/windows/win32/secauthn/credential-security-support-provider?redirectedfrom=MSDN) を有効にする必要があります。 リモート処理モジュールでは、実行ごとに CredSSP を有効または無効にします。 使用しない場合は、CredSSP を無効にすることをお勧めします。 そうしないと、資格情報の盗難リスクが伴います。 設定が完了したら、次のコマンドを実行します。
> 
> ```powershell
> .\Disable-CredSSP-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml.
> ```

```powershell
# If Remoting, execute
# .\Install-PrintersOnGmsa-AllVMs.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -SysInternalsFolderLocation \\networkshare\SysInternalsSuite -ForcePushLBDScripts

.\Install-PrintersOnGmsa.ps1 -PrintersJsonFilePath .\Printers.json -SysInternalsFolderLocation \\networkshare\SysInternalsSuite
```

## <a name="manage-network-printers"></a>ネットワーク プリンターの管理

システム管理者は、このセクションの情報を使用してネットワーク プリンターを定義します。

1. **組織管理** \> **設定** \> **ネットワーク プリンター** の順に移動します。
2. **ネットワーク プリンター** ページで、新しいプリンターを追加します。 各プリンターで、名前、説明、パス、およびステータスを指定します。 プリンター パスがインストールされているプリンターのネットワーク パスと一致していることを確認します。

**有効** とマークされている項目は、すぐにアプリケーションのユーザーによって利用できるようになるので、ネットワーク プリンター デバイスで文書スタイル レポートの印刷を開始できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
