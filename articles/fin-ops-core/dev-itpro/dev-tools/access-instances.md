---
title: 開発環境の配置とアクセス
description: この記事では、開発インスタンスへのアクセス、ローカル開発 VM の構成、および開発者と管理者のための構成設定を見つける方法について説明します。
author: laneswenka
ms.date: 05/24/2022
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 10031
ms.assetid: 4be8b7a1-9632-4368-af41-6811cd100a37
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 3d21292acfd3629512e879cbac766269a0865ebd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867114"
---
# <a name="deploy-and-access-development-environments"></a>開発環境の配置とアクセス

[!include [banner](../includes/banner.md)]

この記事では、開発インスタンスへのアクセス、ローカル開発仮想マシン (VM) の構成、および開発者と管理者にとって重要な構成設定を見つける方法について説明します。

> [!NOTE]
> - Microsoft サポートでは、レベル 1 の開発環境でのトラブルシューティングが制限される場合があります。
> - 特定の状況では、問題を解決するために、Microsoft サポートからレベル 1 環境の新規展開が要求される場合があります。
> - 開発環境にはビジネス クリティカルなデータを含めるべきではなく、破棄可能と見なされます。
> - 120 の環境だけがテナントごとのサポートです。 特定のテナント下のクラウド ホスト環境数を制限して、サンドボックスおよび運用環境を配置できる十分なキャパシティを許可することをお勧めします。
 

## <a name="definitions"></a>定義

| 相談      | 定義                             |
|-----------|----------------------------------------|
| エンド ユーザー  | Web クライアントを使用してインスタンスにアクセスするユーザー。 エンド ユーザーは、インスタンスにアクセスするには Microsoft Azure Active Directory (Azure AD) の資格情報が必要で、そのインスタンスのユーザーとしてプロビジョニングまたは追加する必要があります。 |
| 開発者 | Microsoft Visual Studio 環境でコードを開発するユーザー。 開発者は、開発環境 (VM) へのリモート デスクトップ アクセスが必要です。 開発者アカウントは、VM の管理者である必要があります。 |


## <a name="deploying-cloud-development-environments"></a>クラウド開発環境の配置

LCS プロジェクトにクラウドの開発環境を配置する:

1. LCS プロジェクトと Azure サブスクリプションの間に接続を作成します。 Azure サブスクリプション ID が必要であり、サブスクリプションの使用を承認します。
2. 配置する **環境** の下で **+** を選択します。

    ![LCS Onboard の方法。](media/access-instances-5.jpeg)

3. アプリケーションとプラットフォーム バージョンを選択します。
4. 環境のトポロジを選択します。 詳細については、[プレビュー サブスクリプションのサインアップ](sign-up-preview-subscription.md) を参照してください。
5. クラウドでホストされている環境を選択した場合は、使用する Azure コネクタを選択します。 **配置** を選択します。

    ![環境を配置します。](media/access-instances-3.jpeg)

![クラウド ホスト インスタンス。](media/CloudHostedPicture.jpg)

## <a name="cloud-environment-that-is-provisioned-through-lcs"></a>LCS を通じてプロビジョニングされるクラウド環境

クラウド環境が LCS を通じてプロビジョニングされると、次の操作が行われます。
+ クラウド環境を要求するユーザーは、その環境内の管理者としてプロビジョニングされます。
+ ユーザー アカウントは開発用 VM にプロビジョニングされ、リモート デスクトップを使用して環境へのアクセスを許可します。これらの資格情報は LCS の環境ページからアクセスできます。

### <a name="accessing-an-instance-through-a-url"></a>URL を試用したインスタンスへのアクセス

エンド ユーザーはシステムにアクセスできます。 管理者は、インスタンスの **ユーザー** ページを使用して、このシステムにユーザーを追加することができます。 これらの追加のユーザーは LCS 内のユーザーである必要はないことに注意してください。 LCS プロジェクト サイトからは、クラウド環境のベース URL を取得します。

1. LCS プロジェクトのナビゲーション メニューに移動し、**クラウドホスト環境** を選択します。
2. 環境リスト、配置された環境を選択します。
3. 環境ページが開くと、右上隅で、**ログイン** &gt; **Finance and Operations にログオン** をクリックして、アプリケーションにアクセスできます。
4. 有効なエンド ユーザー資格情報を使用して、アプリケーションにサインインします。 現在の LCS ユーザーが最初に環境を展開したユーザーである場合は、そのユーザーは有効な終了ユーザーおよびアプリケーションの管理者である可能性があります。
5. ブラウザーで、サインインした後にベース URL を記録します。 たとえば、ベース URL は、`https://dynamicsAx7aosContoso.cloud.dynamics.com` である可能性があります。

### <a name="accessing-the-cloud-instance-through-remote-desktop"></a>リモート デスクトップを使用したクラウド インスタンスへのアクセス

クラウド環境は、エンド ユーザーおよび開発者の両方としてアクセスできます。 開発者は、リモート デスクトップの資格情報を使用してシステムにアクセスできます。 リモート デスクトップの資格情報は、LCS プロジェクト サイトの環境ページから取得されます (この記事の前の図を参照してください)。

![制限された管理者アクセス。](media/restricted-admin.png)

配置された **プラットフォーム更新プログラム 12 以前** の環境の対象:
1. VM 名をクリックします。
2. 表示されているローカル管理者のユーザー名とパスワードを使用して、リモート デスクトップ経由でクラウド VM に接続します。 パスワードの表示アイコンを選択してパスワードを表示することができます。

配置された **プラットフォーム更新プログラム 12 以降** の任意の環境については、特徴的アカウント、開発者アカウントおよび管理者アカウントがあります。 

リモート デスクトップを通じて環境にサインインした後、ブラウザーからローカル アプリケーションにアクセスできるようにする場合、リモート コンピューターからアプリケーションにアクセスするために使用するのと同じベース URL を使用します。 上記のセクションは、このベース URL を LCS から取得する方法について説明します。

### <a name="deleting-cloud-hosted-developer-environments"></a>クラウド ホスト開発環境の削除

開発者環境の利用が終わった場合、またはインフラストラクチャ問題のトラブルシューティングに時間がかかる場合は、いつでも LCS から環境を削除し、後から新しい環境を作成できます。  クラウド ホスト環境を LCS から削除するには、次の手順に従います:

1. LCS プロジェクトのナビゲーション メニューに移動し、**クラウドホスト環境** を選択します。
2. 削除する環境を強調表示し、**割り当て解除** を選択します。  これにより、Azure サブスクリプションのマシンがシャット ダウンします。
3. 割り当て解除が正常に行われた後、環境は *割り当て解除済* の状態になります。  **削除** ボタンを使用して削除プロセスを開始できるようになります。

クラウド ホスト環境で作成された仮想ネットワーク (VNET) が他のクラウド ホスト環境でも使用されている場合は、クラウド ホスト環境を削除できません。  これは一般的ではありませんが、お客様の中には、開発環境間でより簡単にファイルを共有するため、開発環境はすべて既存の VNET を再利用してほしいというケースもあります。  このような場合、元の VNET を作成した基本環境を削除する前に、他の環境も削除する必要があります。

削除操作が失敗した場合、次のいずれかが発生した可能性を確認します:

- Azure コネクタの管理証明書が期限切れです。
- Azure サブスクリプションが、元のテナントから別のテナントに移動されました。
- Azure サブスクリプションが無効になっています。
- サブスクリプションには Azure ポリシーがあり、環境のリソース グループ内の 1 つ以上のリソースを削除できないようになっています。

LCS で削除操作を正常に完了できなかった場合、その操作は *未完了* とマークされます。 **LCS メタデータの削除** ボタンを使用して、LCS バックエンド システムからこの環境のメタデータをクリーンアップします。 

> [!NOTE]
> この操作では、Azure サブスクリプション内のリソースの削除を試みません。 環境のリソース グループがまだ存在する場合は、お客様の責任で手動で削除してください。 

環境のリソース グループは、LCS の環境と同じ名前で、Azure サブスクリプションで容易に識別できます。

## <a name="vm-that-is-running-locally"></a>ローカルで実行されている VM
仮想ハード ディスク (VHD) は LCS からダウンロードができるようになり、ローカル コンピューター上に設定可能です。 このシステムは、開発者によるアクセスを目的としており、Finance and Operations アプリの事前構成済みワンボックス開発環境です。 VHD は、資産タイプの **ダウンロード可能な VHD** の下で、LCS の共有アセットライブラリで使用可能です。

1. LCS のメイン ページに移動して **共有アセット ライブラリ** を選択するか、または [共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) に移動します。 
2. 資産タイプの **ダウンロード可能な VHD** を選択します。
3. 目的の Finance and Operations バージョンに基づいて、探している VHD を検索します。 VHD は、ダウンロードする必要がある複数のファイル パーツに分割されています。 たとえば、 "VHD - 10.0.5" で始まる資産ファイルは、バージョン 10.0.5 をインストールするために必要な別のファイルです。
4. 目的の VHD に関連付けられているすべてのファイル (パーツ) をローカル フォルダーにダウンロードします。
5. ダウンロードが完了したら、ダウンロードした実行可能ファイルを実行して、ソフトウェア使用許諾契約に同意し、VHD を抽出するファイル パスを選択します。
6. これにより、ローカルの仮想マシンを実行するのに使用できるローカル VHD ファイルが作成されます。

### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

コマースもコンフィギュレーションしている場合は、このセクションの手順に従います。

ダウンロード可能な VHD を POS のカスタマイズに使用するには、次の手順も実行する必要があります。

- ホスト コンピューターで、入れ子になった VM サポートを有効にします。 詳細については、[入れ子仮想化の仮想マシンで Hyper-v を実行](/virtualization/hyper-v-on-windows/user-guide/nested-virtualization) を参照してください。

### <a name="running-the-virtual-machine-locally"></a>仮想マシンをローカルで実行

Hyper-V マネージャーから VM を実行するには、これらの手順に従います。

1. VM を起動するには、**開始** を選択します。
2. ウィンドウで VM を開くには、**接続** を選択します。
3. ツール バーで **Ctrl + Alt + Delete** ボタンを選択してください。 VM は、ほとんどのキーボード コマンドを受け取りますが、その中に Ctrl + Alt + Del は含まれていません。 したがって、ボタンまたはメニュー コマンドを使用する必要があります。
4. 次の資格情報を使用して VM にログインします。

    - ユーザー名: **管理者**
    - パスワード: <strong>pass@word1</strong>

    > [!TIP]
    > 画面解像度を変更することにより、VM ウィンドウのサイズを変更することができます。 VM でデスクトップを右クリックし、**画面の解像度** をクリックします。 ディスプレイに適した解像度を選択します。

5. 管理者ユーザーを準備します。 詳細については、次のセクションを参照してください。
6. バッチ マネージャー サービスを起動します。 このステップは、バッチ ジョブまたはワークフローを実行している場合に必要です。

    1. 管理者として **コマンド プロンプト** ウィンドウを開きます。
    2. **net start DynamicsAxBatch** と入力し、Enter キーを押します。

   また、サービスを **サービス** ウィンドウから開始することができます。

7. 必要に応じて [更新プログラムを適用](../migration-upgrade/upgrade-latest-platform-update.md#apply-a-platform-update-to-environments-that-are-not-connected-to-lcs) します。

#### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

POS カスタマイズで、ゲスト VM でもこれらの手順に従う必要があります。

1. [Microsoft Emulator for Windows 10 Mobile Anniversary Update](https://www.microsoft.com/download/details.aspx?id=53424) をダウンロードしてインストールします。
2. Hyper-V ホスト サービスを起動します。 詳細については、[Hyper-V: Hyper-V 仮想マシン管理サービスを実行している必要があります](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee956894(v=ws.10)) を参照してください。 起動中にエラーが発生した場合は、ゲスト VM で Hyper-V ロールをアンインストールし、再インストールすることもできます。

### <a name="provisioning-the-administrator-user"></a>管理者ユーザーを準備

開発者がアクセスするには、インスタンスで管理者である必要があります。 LCS を介して提供される環境については、適切なユーザーを配置してください。 詳細については、[よく寄せられる質問](access-instances.md#frequently-asked-questions) を参照してください。 ローカル LCS で管理者として資格情報をプロビジョニングするには、管理者ユーザー プロビジョニング ツールを実行します。 ローカル VM では、デスクトップに提供されているリンクがあります。

1. 管理者として管理者ユーザーのプロビジョニング ツールを実行します (アイコンを右クリックし、**管理者として実行** をクリックします)。
2. 電子メール アドレスを入力し、**送信** を選択します。

> [!NOTE]
> 管理者ユーザー プロビジョニング ツールは、LCS を通じて提供される環境ではサポートされていません。 ローカル VM でのみ使用する必要があります。

> [!NOTE]
> バージョン 10.0.24 以降ににリリースされた仮想ハード ドライブ (VHD) を使用するローカル VM については、代わりに[最初に使用する際にダウンロードできる VHD を設定する](vhd-setup.md)の手順を使用する必要があります。

### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

コマースもコンフィギュレーションしている場合は、このセクションの手順に従います。

### <a name="base-url-of-the-local-application"></a>ローカル アプリケーションの基本 URL

ユーザーが管理者としてプロビジョニングされた後、ユーザーは次のベース URL に移動してコンピュータ上のインスタンスにアクセスできます: `https://usnconeboxax1aos.cloud.onebox.dynamics.com`。 バージョン管理を使用しており、複数の開発 VMs を同じ Azure DevOps プロジェクトに接続する予定がある場合は、ローカル VM 名を変更してください。 手順については、[ローカル開発 (VHD) 環境の名前変更](../migration-upgrade/vso-machine-renaming.md) を参照してください。

#### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

POS アプリケーションの URL は `https://usnconeboxax1pos.cloud.onebox.dynamics.com/`です。　 

クラウド POS アプリケーションの URL は `https://usnconeboxax1pos.cloud.onebox.dynamics.com` です。　 構成手順を完了すると、この VM には Azure AD テナントがプロビジョニングされます。 Azure AD 管理者アカウントは、デモ データ内のレジ担当者アカウントにマップされます。 この環境の POS デバイスを簡単にアクティブにするには、このレジ担当者アカウントを使用できます。

- 出納係ユーザー ID: **000160**
- 出納係パスワード: **123**
- 出納係 LE: **USRT**
- 出納係ストア: **ヒューストン**

## <a name="location-of-packages-source-code-and-other-aos-configurations"></a>パッケージ、ソース コード、およびその他の AOS コンフィギュレーションの場所
VM で、AOSWebApplication の web.config file を開くことによって、ほとんどのアプリケーション コンフィギュレーションが表示されます。

1. IIS を起動します。
2. **サイト** &gt; **AOSWebApplication** に移動します。
3. 右クリックしてから、**エクスプローラー** をクリックしてエクスプローラーを開きます。
4. メモ帳や他のテキスト エディターで web.config ファイルを開きます。 多くの開発者や管理者にとって、次のキーが重要です。

    - **Aos.MetadataDirectory** - このキーは、プラットフォームとアプリケーションのバイナリを含むパッケージ フォルダの場所、およびソースコードをポイントします。 (ソース コードは、開発環境でのみ使用できます。) 一般的な値は、c:\packages、c:\AosServicePackagesLocalDirectory、および J:AosServicePackagesLocalDirectory です。
    - **DataAccess.Database** - このキーは、データベースの名前を保持します。
    - **Aos.AppRoot** - このキーは、Application Object Server (AOS) Web アプリケーションのルート フォルダーをポイントします。

### <a name="commerce-configuration"></a>コマースのコンフィギュレーション

ソフトウェア開発キット (SDK) は、C:\RetailSDK にあります。 アプリケーションの使用およびカスタマイズ方法の詳細については、次のトピックを参照してください。
- [Retail ソフトウェア開発キット (SDK) アーキテクチャ](../../../commerce/dev-itpro/retail-sdk/retail-sdk-overview.md)
- [販売時点管理 (POS) デバイスのライセンス認証](../../../commerce/dev-itpro/retail-device-activation.md)

## <a name="redeploying-or-restarting-the-runtime-on-the-vm"></a>VM でのランタイムの再配置または再起動
ローカルのランタイムを再起動して、すべてのパッケージを再配置するには、次の手順を実行します。

1. ファイル エクスプローラーを開き、C:\CustomerServiceUnit に移動します。
2. **AOSDeploy.cmd** を右クリックして **管理者として実行** をクリックします。

このプロセス時間がかかる場合があります。 cmd.exe ウィンドウが終了すると、プロセスが完了します。 ランタイムを再配置せずに AOS を再起動するのみの場合は、管理者の **Command Prompt** ウィンドウから **iisreset** を実行するか、IIS から AOSWebApplication を再起動します。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="can-we-join-cloud-hosted-environments-to-our-azure-ad-domain-as-it-is-currently-deployed-in-a-workgroup"></a>現在、ワークグループで展開している Azure AD ドメインに、クラウドホスト環境を参加させることは可能ですか?
これらの環境は自己完結型でテストは行われていません。Azure を介して展開すると Azure AD ドメインに参加した場合にもサポートされていません。  

### <a name="is-there-a-way-to-hide-the-local-account-passwords-in-lcs"></a>LCS でローカルアカウントのパスワードを非表示にする方法はありますか?
これは、プロジェクトにおけるユーザーのセキュリティ ロールを *プロジェクト チーム メンバー* ロールに下げた場合のみ可能であり、*環境マネージャー*、または *プロジェクト所有者* ロールのローカル アカウント パスワードを非表示にすることはできません。

### <a name="are-cloud-hosted-environments-supported-with-azure-bastion"></a>クラウド ホスト環境は Azure Bastion でサポートされていますか?
これらの環境はテストされておらず、Azure Bastion でサポートされてもいません。  

### <a name="environment-is-in-a-failed-state-with-the-error-message-updated-aad-tenant-is-missing-reply-url-configuration-how-do-i-resolve-this"></a>環境に、「更新された AAD テナントに、返信 URL コンフィギュレーションがありません」というエラー メッセージが表示され、失敗の状態です。 これをどのように解決しますか。
このメッセージは、レベル 1/顧客管理環境が、配置時に使用するテナントとは異なる Azure AD テナントを使用して構成されていることを示します。 この問題の解決に役立つさまざまなオプションがあります:
1. (推奨) 環境を削除し、環境が使用されるテナントで再配置します。 
2. 設定を配置時に使用したテナント のコンフィギュレーションに戻します。
3. [環境の状態が失敗した場合、またはサイン イン エラーが発生している場合に、既存の環境を修正する方法](access-instances.md#how-can-i-fix-my-existing-environment-when-my-environment-is-in-a-failed-state-or-i-am-getting-sign-in-errors) の手順に従い、ターゲット テナントの返信 URL を更新します。  

### <a name="as-a-partnerisv-how-can-i-facilitate-cloud-hosted-deployments-for-customers-that-i-work-with"></a>パートナーまたは ISV として、作業する顧客向けクラウド ホスト型の配置を円滑化するにはどのようにしますか?
特定の環境に対して、すべてのコンフィギュレーションおよび統合が正しく準備されるように、レベル 1 または顧客管理環境を顧客の Azure AD テナントの下に配置する必要があります。 テナントと環境の関連付けは、環境を配置したユーザーに基づいて決定されます。

クラウド ホスト型の配置を円滑にするために、パートナー企業は、この手順に従って顧客固有のクラウド ホスト環境を作成することをお勧めします。 これにより、配置が正しいテナント下で確実に登録されます。

- 環境が使用されるテナントからユーザーを通じて環境を配置します。 管理者ユーザーのプロビジョニング ツールを使用して、レベル 1 または顧客管理またはクラウド ホスト環境のテナントを変更する必要があります。

> [!NOTE]
> Azure サブスクリプションに関連付けられている Azure AD テナントは、環境コンフィギュレーションでは一切の役割を果たします。 Azure サブスクリプションおよび対応するコネクタ コンフィギュレーションは、Azure リソースの配置にのみ使用されます。

### <a name="i-have-run-the-admin-user-provisioning-tool-on-my-development-environment-and-now-i-receive-the-following-sign-in-error-error-aadsts50011-the-reply-url-specified-in-the-request-does-not-match-the-reply-urls-configured-for-the-application"></a>自分の開発環境で管理者ユーザー プロビジョニング ツールを実行したところ、次のサインイン エラーが発生しました: 「エラー: AADSTS50011: リクエストで指定された返信 URL がアプリケーションに対して構成されている返信 URL と一致しません」
上記の説明のように、正しい Azure AD テナント下に Finance and Operations 環境を配置することが非常に重要です。 LCS を使用してレベル 1 または顧客管理環境において、Azure AD テナント設定の変更は配置後にはサポートされません。

### <a name="how-can-i-fix-my-existing-environment-when-my-environment-is-in-a-failed-state-or-i-am-getting-sign-in-errors"></a>環境が失敗した状態の場合、またはサインイン エラーが発生している場合に、既存の環境をどのように修正しますか?

以前に、管理者ユーザーのプロビジョニング ツールを使用してテナントの設定を更新した環境がある場合は、それらの環境を削除した後、正しい Azure AD テナント下に再配置することをお勧めします。

既存の環境を削除して再配置できない場合は、URL を構成済 Azure AD テナントに追加する必要があります。 テナント管理者は、次のコマンドを実行できます。 

> [!Note]
> URL は手動で追加されるので、環境を削除する場合は URL のクリーンアップも手動で行う必要があります。

1. web.config ファイルから次の値を取得します。

    ```powershell
    $AADTenant = <Value of Aad.TenantDomainGUID from web.config>
    $EnvironmentUrl = <Value of Infrastructure.HostUrl from web.config>

    # For example, if value is spn:fd663e81-110e-4c18-8995-ddf534bcf5e1 then take only fd663e81-110e-4c18-8995-ddf534bcf5e1
    $AADRealm = <Value of Aad.Realm from web.config without spn: prefix. >
    ```

2. **web.config ファイル内のテナントの Azure AD テナント管理者アカウントを介して**、次のコマンドを実行します。

    ```powershell
    # Using tenant admin account under this tenant login to via AzureAD PowerShell cmdlet.
    Connect-AzureAD

    # Get Service Principal details
    $SP = Get-AzureADServicePrincipal -Filter "AppId eq '$AADRealm'"

    #Add Reply URLs
    $SP.ReplyUrls.Add("$EnvironmentUrl")
    $SP.ReplyUrls.Add("$EnvironmentUrl/oauth")

    #Set/Update Reply URL
    Set-AzureADServicePrincipal -ObjectId $SP.ObjectId -ReplyUrls $SP.ReplyUrls
    ```

### <a name="i-have-fixed-my-environment-but-it-is-still-in-a-failed-state-how-do-i-resolve-this"></a>環境は修正されましたが、まだエラー状態です。 これをどのように解決しますか。
環境に対して最初に **停止** から **開始** 操作を実行し、URL から環境を再起動します。 環境コンフィギュレーションが正しいと検出された場合、環境 URL は自動的に **開始** 操作の **2 時間以内** に再起動します。

### <a name="while-running-the-admin-user-provisioning-tool-on-my-local-development-environment-i-get-the-error-the-values-length-for-key-password-exceeds-its-limit-of-128"></a>ローカル開発環境で管理者ユーザー プロビジョニング ツールを実行中に、「キーのパスワードの値の長さが '128' の上限を超えています」というエラーが表示されます。
バージョン 10.0.24 以降にリリースされた仮想ハード ドライブ (VHD) を使用している場合は、管理者ユーザー プロビジョニング ツールの前に自己署名証明書生成ツールを実行する必要があります。 詳細情報については、[最初に使用する際にダウンロードできる VHD を設定する](vhd-setup.md)を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
