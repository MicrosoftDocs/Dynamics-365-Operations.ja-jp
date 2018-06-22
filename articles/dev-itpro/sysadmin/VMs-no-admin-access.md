---
title: "管理者のアクセスを許可しない仮想マシンに関するよく寄せられる質問"
description: "このトピックでは、管理者アクセスを許可しない仮想マシンに関するよくある質問 (FAQ) への回答を示します。"
author: yukonpeegs
manager: AnnBe
ms.date: 03/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform
ms.custom: 
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8124081c061b11fe391811be1979567cf2012206
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="virtual-machines-that-dont-allow-administrator-access-faq"></a>管理者のアクセスを許可しない仮想マシンに関するよく寄せられる質問

[!INCLUDE [banner](../includes/banner.md)]

このトピックでは、管理者アクセスを許可しない仮想マシン (VM) に関するよくある質問 (FAQ) への回答を示します。 具体的には、このトピックの情報は、Platform update 12 以降を実行する Tier 1 VM に適用されます。

## <a name="how-can-i-install-a-deployable-package"></a>どのように配置可能パッケージをインストールできますか。
可能な限り、Microsoft Dynamics Lifecyle Services (LCS) を使用して、配置可能なパッケージをインストールします。 **-devinstall** オプションを使用して、展開可能なパッケージをインストールすることができます。 このオプションには手動データベース同期が必要な点に留意してください。

配置可能パッケージをインストールする方法の詳細については、[配置可能パッケージのインストール](../deployment/install-deployable-package.md) を参照してください。

## <a name="is-the-finance-and-operations-website-accessible-when-visual-studio-isnt-running"></a>Visual Studio が実行されていないときに Finance and Operations の Web サイトはアクセス可能ですか。
はい、Microsoft Visual Studio が実行されていない場合、Microsoft Dynamics 365 for Finance and Operations Web サイトにアクセスすることができます。 Microsoft Internet Information Services (IIS) Express は、ユーザーとして実行する .exe ファイルです。 ただし、Visual Studio を終了すると、XPPC エージェントが終了する前に通常の IIS (IIS Express ではなく) が起動します。 この動作により、サインアウトした場合やマシンを再起動した場合でも、Application Object Server (AOS) インスタンスとFinance and Operations Web サイトにリモートでアクセスできるようになります。 多くのユーザーがこのような開発者用マシンをテスト用マシンとして使用してていること、また彼らが常に AOS インスタンスが実行されていることを期待していることを認識しています。 ただし、IIS Express は、この動作をサポートしていません。

## <a name="what-about-the-other-services"></a>他のサービスはどうなのですか ?
Microsoft SQL Server、SQL Server Reporting Services (SSRS)、SQL Server Integration Services (SSIS)、SQL Server Analysis Services (SSAS)、Batch、Financial reporting (旧 Management Reporter)、および IIS などの Microsoft Windows サービスを再起動することができます。 (IIS の場合は、iisreset.exe を使用できないため、World Wide Web 発行サービスを再起動する必要があります。)

## <a name="can-i-clean-up-the-service-volume-drive"></a>サービス ボリューム ドライブをクリーンアップできますか。
はい、サービス ボリューム ドライブに対する完全なアクセス権があります。 したがって、監視データをクリーンアップすることができます。

## <a name="what-are-the-alternatives-to-vms-that-dont-allow-administrator-access"></a>管理者アクセスを許可しない VM に代わる方法とは
プライベート Azure サブスクリプションの Microsoft Azure VM とローカル仮想ハード ディスク (VHD) の両方は管理者アクセスを許可します。 ただし、Visual Studio を管理者として実行する必要があります。 管理者は明示的にではなく、**管理者**グループを介してのみこれらの代替手段にアクセスできるため、この要件が適用されます。

## <a name="can-i-run-visual-studio-as-an-administrator"></a>Visual Studio を管理者として実行できますか。
Platform update 12 以降、Visual Studio を管理者として実行する必要がなくなりました。 Microsoft 所有の Azure サブスクリプションである VM に対して、リモート デスクトップ プロトコル (RDP) を使用して管理者として接続することはできなくなりました。 これらの VM には、サブスクリプションおよび Tier 1 アドオン VM に含まれる Tier 1 VM が含まれます。 ただし、管理者として Microsoft 所有のサブスクリプションの下にはない VM に接続する場合、管理者として引き続き Visual Studio を実行する必要があります。

## <a name="a-get-latest-operation-in-visual-studio-failed-because-files-are-blocked-by-the-aos-instance-how-do-i-start-and-stop-iis"></a>ファイルが AOS インスタンスによってブロックされているため、Visual Studio での「最新の取得」操作が失敗しました。 IIS を開始または停止するにはどうすればよいですか。
IIS Express を使用する必要があります。 詳細については、次のセクションを参照してください。

## <a name="what-are-the-instructions-for-using-iis-express"></a>IIS Express の使用方法は ?
IIS Express が起動されると、通知領域 (時計の近くにある) にアイコンが表示されます。 IIS Express アイコンを右クリックすると、実行中のすべてのサイトが一覧表示されます。 そのメニューから IIS Express を停止することができます。 Visual Studio でのいくつかのアクションによって IIS Express が起動しますが、**Dynamics 365** メニューで **IIS Express の再起動** を選択することで、Visual Studio から明示的に IIS Express を起動することもできます。

## <a name="how-can-i-apply-a-partner-visual-studio-license-that-isnt-linked-to-the-visual-studio-sign-in-account-that-is-likely-to-be-used-in-the-customer-azure-ad-or-domain"></a>顧客の Azure AD またはドメインで使用される可能性のある、Visual Studio サインイン アカウントにリンクされていない、パートナーの Visual Studio ライセンスはどのように適用できますか。
この機能はサポートされていません。 パートナーの Visual Studio ライセンスは、顧客の Azure Active Directory (Azure AD) またはドメインで使用されている Visual Studio サインイン アカウントにリンクされない限り、適用することはできません。

## <a name="can-i-install-additional-development-tools-such-as-fiddler-and-pepper"></a>追加の開発ツール (Fiddler や Pepper など) をインストールすることはできますか。
いいえ、追加の開発ツールをインストールすることはできません。

## <a name="is-there-a-way-to-run-windows-powershell-and-command-prompt-commands-as-an-administrator"></a>管理者として Windows PowerShell およびコマンド プロンプトのコマンドを実行する方法はありますか。
いいえ、管理者として Windows PowerShell コマンドおよびコマンド プロンプトのコマンドを実行できません。

## <a name="is-the-trace-parser-supported"></a>Trace Parser はサポートされていますか。
Trace Parser は現在サポートされていませんが、間もなく再度そのサポートを追加する予定です。

## <a name="can-the-system-be-put-into-maintenance-mode"></a>システムをメンテナンス モードにすることはできますか。
システムをメンテナンス モードにしてライセンス コンフィギュレーションを変更することができます。 ただし、[メンテナンス モード](maintenance-mode.md) に記載されている手順はサポートされていません。 すべての環境におけるメンテナンス モードのセルフ サービス サポートが将来 LCS に追加されます。 このサポートが LCS で利用可能になるまで、以下の手順に従ってシステムをメンテナンス モードにすることができます。

1. 開発者のマシンに RDP の接続を確立します。
2. 開発者のマシンで、LCS から axdbadmin ユーザーの資格情報を使用して SQL Server にサインインします。 次に、AXDB データベースに切り替えて、次のコマンドを実行します。

    ```
    update SQLSYSTEMVARIABLES SET VALUE = 1 where PARM = 'CONFIGURATIONMODE'
    ```

3. **World Wide Web 公開サービス** サービスを再起動して IIS をリセットします。

    サービスが再起動されると、システムはメンテナンス モードになります。

4. メンテナンス モードの活動を完了したら、ステップ 2 および 3 を繰り返しますが、値はステップ 2 で **0** に設定します。

## <a name="can-i-install-a-license-deployable-package"></a>ライセンス配置可能パッケージをインストールできますか。
**- devinstall** オプションを使用して、ライセンスが配置可能なパッケージをインストールできる必要があります。 ただし、このシナリオで問題が検出されました。 問題の解決に取り組んでいます。

