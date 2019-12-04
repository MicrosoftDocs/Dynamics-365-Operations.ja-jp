---
title: 管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問
description: このトピックでは、管理者アクセスを許可しない仮想マシンに関するよくある質問 (FAQ) への回答を示します。
author: yukonpeegs
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform
ms.custom: ''
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 6284de23e456078a2af8fb57ffc83368ead5fd50
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811947"
---
# <a name="development-and-build-vms-that-dont-allow-admin-access-faq"></a>管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問

[!include [banner](../includes/banner.md)]

このトピックでは、管理者アクセスを許可しない仮想マシン (VM) に関するよくある質問 (FAQ) への回答を示します。 

## <a name="how-can-i-install-a-deployable-package"></a>どのように配置可能パッケージをインストールできますか。
可能な限り、Microsoft Dynamics Lifecyle Services (LCS) を使用して、配置可能なパッケージをインストールします。 **-devinstall** オプションを使用して、展開可能なパッケージをインストールすることができます。 このオプションには手動データベース同期が必要な点に留意してください。

配置可能パッケージをインストールする方法の詳細については、 [コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md)を参照してください。

## <a name="is-the-finance-and-operations-website-accessible-when-visual-studio-isnt-running"></a>Visual Studio が実行されていないときに Finance and Operations の Web サイトはアクセス可能ですか。
はい、Microsoft Visual Studio が実行されていない時に Finance and Operations Web サイトにアクセスできます。 Microsoft Internet Information Services (IIS) Express は、ユーザーとして実行する .exe ファイルです。 ただし、Visual Studio を終了すると、XPPC エージェントが終了する前に通常の IIS (IIS Express ではなく) が起動します。 この動作により、サインアウトした場合やマシンを再起動した場合でも、Application Object Server (AOS) インスタンスと Web サイトにリモートでアクセスできるようになります。 多くのユーザーがこのような開発者用マシンをテスト用マシンとして使用してていること、また彼らが常に AOS インスタンスが実行されていることを期待していることを認識しています。 ただし、IIS Express は、この動作をサポートしていません。

## <a name="what-about-the-other-services"></a>他のサービスはどうなのですか ?
Microsoft SQL Server、SQL Server Reporting Services (SSRS)、SQL Server Integration Services (SSIS)、SQL Server Analysis Services (SSAS)、Batch、Financial reporting (旧 Management Reporter)、および IIS などの Microsoft Windows サービスを再起動することができます。 (IIS の場合は、iisreset.exe を使用できないため、World Wide Web 発行サービスを再起動する必要があります。)

## <a name="can-i-clean-up-the-service-volume-drive"></a>サービス ボリューム ドライブをクリーンアップできますか。
はい、サービス ボリューム ドライブに対する完全なアクセス権があります。 したがって、監視データをクリーンアップすることができます。

## <a name="what-are-the-alternatives-to-vms-that-dont-allow-administrator-access"></a>管理者アクセスを許可しない VM に代わる方法とは
プライベート Azure サブスクリプションの Microsoft Azure 環境とローカル仮想ハード ディスク (VHD) の両方は管理者アクセスを許可します。 ただし、Visual Studio を管理者として実行する必要があります。 管理者は明示的にではなく、**管理者**グループを介してのみこれらの代替手段にアクセスできるため、この要件が適用されます。

## <a name="can-i-run-visual-studio-as-an-administrator"></a>Visual Studio を管理者として実行できますか。
管理者として Visual Studio を実行する必要はありません。 Microsoft 所有の Azure サブスクリプションである VM に対して、リモート デスクトップ プロトコル (RDP) を使用して管理者として接続することはできません。 これらの VM には、サブスクリプションおよび Tier 1 アドオン VM に含まれる Tier 1 VM が含まれます。 ただし、管理者として Microsoft 所有のサブスクリプションの下にはない VM に接続する場合、管理者として引き続き Visual Studio を実行する必要があります。

## <a name="a-get-latest-operation-in-visual-studio-failed-because-files-are-blocked-by-the-aos-instance-how-do-i-start-and-stop-iis"></a>ファイルが AOS インスタンスによってブロックされているため、Visual Studio での「最新の取得」操作が失敗しました。 IIS を開始または停止するにはどうすればよいですか。
IIS Express を使用する必要があります。 詳細については、次のセクションを参照してください。

## <a name="what-are-the-instructions-for-using-iis-express"></a>IIS Express の使用方法は ?
IIS Express が起動されると、通知領域 (時計の近くにある) にアイコンが表示されます。 IIS Express アイコンを右クリックすると、実行中のすべてのサイトが一覧表示されます。 そのメニューから IIS Express を停止することができます。 Visual Studio でのいくつかのアクションによって IIS Express が起動しますが、**Dynamics 365** メニューで **IIS Express の再起動**を選択することで、Visual Studio から明示的に IIS Express を起動することもできます。

IIS Express および Finance and Operations Visual Studio プロジェクトでデバッグが正常に機能することを確実にするため、次のインターネット オプションの設定をお勧めします:

- **コントロール パネル** > **インターネット オプション** > **セキュリティ** タブ >**インターネット** に移動し、**保護モードの有効化** チェック ボックスをオンにします。
- **コントロール パネル** > **インターネット オプション** > **セキュリティ** タブ >**制限付きサイト** に移動し、**保護モードの有効化** チェック ボックスをオンにします。

## <a name="can-i-install-additional-development-tools-such-as-fiddler-and-pepper"></a>追加の開発ツール (Fiddler や Pepper など) をインストールすることはできますか。
いいえ、追加の開発ツールをインストールすることはできません。

## <a name="is-there-a-way-to-run-windows-powershell-and-command-prompt-commands-as-an-administrator"></a>管理者として Windows PowerShell およびコマンド プロンプトのコマンドを実行する方法はありますか。
いいえ、管理者として Windows PowerShell コマンドおよびコマンド プロンプトのコマンドを実行できません。

## <a name="is-the-trace-parser-supported"></a>Trace Parser はサポートされていますか。
現在 Trace Parser を使用するには、ユーザーが管理者であることが必要です。 Microsoft によって管理され、管理者アクセスを許可しない開発 / テスト環境ではサポートされていません。

## <a name="is-the-admin-user-provisioning-tool-supported"></a>管理者ユーザー プロビジョニング ツールはサポートされますか?
**管理者ユーザー プロビジョニング** ツールを使用するには現在、ユーザーが管理者である必要があります。 **管理者ユーザー プロビジョニング** ツールは通常、環境のテナントを変更するために使用され、必要ありません。 管理者ユーザーまたは他のユーザーのデータベースで情報を更新またはサインインすることができます。 この環境または同じテナントの別の環境にアクセスできるユーザーからの SID およびネットワーク エイリアス (電子メール アドレスなど) のみ必要です。 多くの場合、SID とネットワーク エイリアスは当初の環境に付属していたデータベースにあります。 次のコマンドを実行してソース環境から適切な SID とネットワーク エイリアスを取得し、それぞれ対象の環境で更新します。

    -- get value from source env.
    select ID, SID, NETWORKALIAS from USERINFO where ID = 'Admin'

    -- update value in target env.
    update USERINFO set SID = 'new_SID', NETWORKALIAS = 'new_NetworkAlias' where ID = 'Admin'

## <a name="can-the-system-be-put-into-maintenance-mode"></a>システムをメンテナンス モードにすることはできますか。
システムをメンテナンス モードにしてライセンス コンフィギュレーションを変更することができます。 ただし、[メンテナンス モード](maintenance-mode.md) に記載されている手順はサポートされていません。 すべての環境におけるメンテナンス モードのセルフ サービス サポートが将来 LCS に追加されます。 このサポートが LCS で利用可能になるまで、以下の手順に従ってシステムをメンテナンス モードにすることができます。

1. 開発者のマシンに RDP の接続を確立します。
2. 開発者のマシンで、LCS から axdbadmin ユーザーの資格情報を使用して SQL Server にサインインします。 次に、AXDB データベースに切り替えて、次のコマンドを実行します。

    ```
    update SQLSYSTEMVARIABLES SET VALUE = 1 where PARM = 'CONFIGURATIONMODE'
    ```

3. **World Wide Web 公開サービス** を再起動して IIS をリセットします。

    サービスが再起動されると、システムはメンテナンス モードになります。

4. メンテナンス モードの活動を完了したら、ステップ 2 および 3 を繰り返しますが、値はステップ 2 で **0** に設定します。

## <a name="can-i-install-a-license-deployable-package"></a>ライセンス配置可能パッケージをインストールできますか。
### <a name="development-environments"></a>開発環境
LCS を使用して、クラウド開発環境にライセンス配置可能パッケージをインストールします。
### <a name="build-environments"></a>ビルド環境
LCS では、AOT またはライセンス配置可能パッケージをビルド環境にインストールできません。 これを回避するには、VM にリモート接続し、「[配置可能なパッケージのコマンドラインからのインストール](../deployment/install-deployable-package.md)」で説明されているようにコマンド ラインから **-devinstall** オプションを使用してライセンス配置可能パッケージをインストールします。 このコマンド ライン インストールは、プラットフォーム更新 17 で機能します。 プラットフォーム更新プログラム 17 より古いプラットフォーム バージョンを実行しており、ビルド環境への管理者アクセス権を持っていない場合、サポート リクエストを作成し、ライセンス配置可能パッケージのインストールを Microsoft に依頼します。

## <a name="is-licensing-visual-studio-by-entering-a-product-key-supported"></a>プロダクト キーを入力することによってライセンス Visual Studio はサポートされますか。
Visual Studio に直接プロダクト キーを入力することはサポートされていません。 代わりに、Visual Studio 定期売買ライセンスを使用し、ライセンスに関連付けられている電子メール アドレス (ユーザー アカウント) で Visual Studio にサインインします。 Visual Studio ライセンスをユーザー アカウントにリンクするには、MSDN ライセンスをユーザー アカウントに割り当てるか、または https://www.visualstudio.com/subscriptions-administration を使用してユーザー アカウントにライセンスを割り当てます。

## <a name="can-i-upgrade-my-database-to-a-new-application-release"></a>新しいアプリケーションのリリースに、データベースをアップグレードすることはできますか？
Lifecyle Services (LCS) の 2018 年 2 月リリースと同じく、開発環境の LCS 環境ページからデータ アップグレード パッケージを実行できます。 LCS からのデータ アップグレード パッケージの実行では、VM の管理者である必要はありません。

[開発環境またはデモ環境でのデータのアップグレード](../migration-upgrade/upgrade-data-to-latest-update.md) で説明されているプロセスは、コマンド ラインからのデータ アップグレード パッケージを実行します。 これを行うには、VM の管理者である必要があります。

## <a name="what-do-i-need-to-know-if-i-am-developing-for-retail"></a>Retail の開発をしている場合、何を把握する必要がありますか。
Dynamics 365 Retail を開発する場合、コンフィギュレーション手順および他の重要な情報は、[管理者のアクセス権がないクラウド ホストの開発環境で作業している Retail 開発者向けのコンフィギュレーション手順](../../../retail/dev-itpro/cloud-dev-box.md) に記載されています。
