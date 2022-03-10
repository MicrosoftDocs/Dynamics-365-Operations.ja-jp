---
title: ネットワーク印刷を有効にするためにドキュメント回覧エージェントをインストールする
description: このトピックでは、Microsoft Dynamics 365 Finance の配置用にドキュメント回覧エージェントをインストールして構成する方法について説明します。
author: RichdiMSFT
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.custom: 98663
ms.assetid: cd017bfd-2eba-4e8a-ab9b-a0ce393c2108
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e28fbd4fe0be7b031c3f777d6d39a20c5691746c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345675"
---
# <a name="install-the-document-routing-agent-to-enable-network-printing"></a>ネットワーク印刷を有効にするためにドキュメント回覧エージェントをインストールする

[!include [banner](../includes/banner.md)]

このトピックでは、ドキュメント回覧エージェント (DRA) をインストールして構成する方法について説明します。  DRA は、ネットワーク印刷シナリオを有効にするのに使用できる、ダウンロード可能なアプリケーションを提供します。 クライアント内管理ページを使用して、特定の会社のためにネットワーク プリンターを有効にすることができます。

## <a name="preparing-to-install-the-document-routing-agent"></a>ドキュメント回覧エージェントのインストールを準備

- Windows 8.1、Windows 10、Microsoft Windows Server 2012 R2、または Microsoft Windows Server 2016 でサポートされています。
- ネットワーク印刷リソースへのアクセスには、Active Directory Domain Services (AD DS) 認証が必要です。
- DRA をインストールする場合は、管理者ユーザーとしてログインしていることを確認してください。
- DRA を構成するために使用される Microsoft Azure Active Directory (Azure AD) アカウントには、Azure テナントと同じドメインを共有する必要があります。
- DRA には、クライアント上に .NET 4.62 以降と Adobe Acrobat Reader が必要です。
- ドキュメントの拡大縮小を防止するために、Adobe クライアントの印刷設定をコンフィギュレーションします。

アプリケーションに登録されているネットワーク プリンターは、環境で定義されているすべての法人 (会社とも呼ばれます) で使用できます。 ネットワーク プリンター設定は会社固有です。 したがって、管理者はユーザーのアクティブな会社に基づいてアクセスを制限できます。 たとえば、有効な会社内のユーザーは、ドキュメント回覧エージェントによって登録されるすべてのネットワーク プリンターへアクセスできる可能性があります。 ただし、別の会社内のユーザーは、アクセスがその会社に対して明示的に有効になるまで、それらのプリンターへアクセスできません。

## <a name="key-concepts"></a>重要な概念
このトピックは、次の作業に役立ちます。

- アプリケーションでネットワーク印刷のサポートに関連する主要なコンポーネントを識別します。
- ドキュメント回覧エージェントの機能について説明します。
- 既存のアプリケーションに対して機能するようにドキュメント回覧エージェントをコンフィギュレーションします。
- 管理ページを使用して、ネットワーク プリンタへのアクセスを管理します。

## <a name="install-the-document-routing-agent"></a>ドキュメント回覧エージェントのインストール
アプリケーションは、ドキュメント回覧エージェントを使用して、ネットワーク プリンター デバイスへのドキュメントのスプーリングを管理します。 Web アプリケーションに埋め込まれている直接リンクを使用して、クライアントを取得することができるようになりました。 アプリケーションをローカル コンピューターにダウンロードするには、次の手順を使用します。 次に、コンピューターに接続されているローカル プリンターとネットワーク プリンターの両方に、単一配置からアクセスできます。

1. **ネットワーク プリンターの管理** ページを開きます。(**組織管理** &gt; **設定** &gt; **ネットワーク プリンター**)
2. **オプション** タブの、**アプリケーション** グループで、**ドキュメント回覧エージェント インストーラーのダウンロード** をクリックします。

    [![download-document-routing-agent-installer.](./media/download-document-routing-agent-installer.png)](./media/download-document-routing-agent-installer.png)

3. インストール プロセスを開始するためにダウンロードしたファイルを実行します。
4. 設定プロセスを完了します。

アプリケーションをインストールした後、アプリケーションのネットワーク プリンターとしてローカル プリンターの登録を開始できます。

## <a name="configure-the-document-routing-agent"></a>ドキュメント回覧エージェントのコンフィギュレーション
処理中のドキュメントをホストする Azure サービスと通信できるように、クライアント アプリケーションを構成するには、次の手順を使用します。

1. アプリケーションを実行しているすべてのブラウザー インスタンスを閉じます。 これにより、ローカル Azure 認証トークンがリセットされます。
2. デスクトップで、ドキュメント回覧エージェントを実行します。
3. ツール バーで、**設定** をクリックします。

    [![the-document-routing-agent-window.](./media/the-document-routing-agent-window.png)](./media/the-document-routing-agent-window.png)

4. 次の設定を追加します。

    - **アプリケーション ID** - アプリケーション固有の ID で、自動的に入力されます。
    - **Finance and Operations URL** – アプリケーションのベース URL。
    - **Azure AD テナント** – Azure AD のドメイン名。

5. **OK** をクリックします。
6. **サインイン** をクリックしてアカウントにサインインします。

    > [!NOTE]
    > アカウントは、アプリケーションに関連付けられている Azure AD と同じドメインを共有する必要があります。 ドキュメント回覧エージェントで、ドキュメントを処理する準備が整いました。

正常にサインインした後、**プリンター** ボタンがツールバーに表示されます。

## <a name="register-network-printers"></a>ネットワーク プリンターの登録
この手順を実行する前に、ローカル ホスト コンピューターのすべてのネットワーク プリンターをインストールしていることを確認してください。 サービス登録にインストールされているすべてのプリンター デバイスは利用可能です。 アプリケーションで公開するプリンターのみを選択してください。

1. ツール バーで、**プリンター** をクリックします。
2. アプリケーションで使用できるようにするプリンターを選択します。

    [![printers-to-add.](./media/printers-to-add.png)](./media/printers-to-add.png)

3. プリンターの既定の名前を指定します。
4. **OK** をクリックします。

この手順を完了した後、選択したプリンター デバイスはアプリケーションのネットワーク プリンター カタログに登録されます。 システム管理者は、アプリケーション内からプリンターへのアクセスを有効にできるようになりました。

## <a name="administer-network-printers"></a>ネットワーク プリンターの管理
クライアントのページを使用して、1 つ以上のドキュメント回覧エージェントによって登録されているネットワーク プリンターへのアクセスを管理します。 ネットワーク プリンターは、パスで一意に識別されます。 したがって、複数のドキュメント回覧エージェントによって登録されている場合でも、プリンターは一度に一覧表示されます。 Application Object Server (AOS) のネットワーク プリンターを有効にするには、次の手順を使用します。

1. **ネットワーク プリンターの管理** ページを開きます。(**組織管理** &gt; **設定** &gt; **ネットワーク プリンター**)

    [![manage-network-printers-page.](./media/manage-network-printers-page.png)](./media/manage-network-printers-page.png)

2. 各ネットワーク プリンターにマップされている既存のエントリを編集します。 変更の一環として、接続パスを編集します。
3. **印刷先** フィールドにプリンタをオプションとして含めるには、**有効** フィールドを **はい** に設定します。

ネットワーク プリンターは、アプリケーションで使用できるようになりました。

## <a name="frequently-asked-questions"></a>よく寄せられる質問
### <a name="does-the-document-routing-agent-have-to-be-installed-on-each-computer-where-a-user-connects-by-using-a-browser"></a>ドキュメント回覧エージェントは、ユーザーがブラウザーを使い接続する各コンピューターにインストールする必要がありますか。

一連番号 ドキュメント回覧エージェントのクライアント インストールは、プロビジョニングされた環境にアクセスする個人が共有できます。 1 つまたは複数のプリント サーバーに、またはネットワーク プリンターへのアクセス権を持つドメインによってホストされている他のクライアントに、エージェントをインストールすることをお勧めします。

### <a name="if-the-document-routing-agent-belongs-on-a-network-print-server-why-doesnt-the-client-run-as-a-service"></a>ドキュメント回覧エージェントがネットワーク プリント サーバーに属している場合は、クライアントがサービスとして実行しないのはなぜですか?

ドキュメント回覧エージェントは現在、サービスとしてのバックグラウンドでの実行をサポートしています。 クライアントの最新版をダウンロードしたことを確認する必要があります。 詳細については、[Windows サービスとしてドキュメント回覧エージェントを実行](run-document-routing-agent-as-windows-service.md) を参照してください。

### <a name="do-i-need-to-update-credentials-or-refresh-azure-authentication-tokens-on-a-recurring-basis"></a>定期的に資格情報を更新するか、Azure 認証トークンを更新する必要がありますか。

はい。 Azure Active Directory トークンは 90 日おきに更新する必要があります。 更新しなかった場合、DRA は認証できなくなり、印刷する指示のアプリケーションを取得できなくなります。

### <a name="is-the-document-routing-agent-supported-on-microsoft-windows-server-2019"></a>ドキュメント回覧エージェントは Microsoft Windows Server 2019 でサポートされていますか?

はい。 ドキュメント回覧エージェントは Microsoft Windows Server 2019 でサポートされています。

> [!NOTE]
> サーバーがバックグラウンド サービスを回避するよう構成されている場合、ドキュメント回覧エージェントのクライアントはサービスとして実行できません。 詳細については、[Windows サービスとしてドキュメント回覧エージェントを実行](run-document-routing-agent-as-windows-service.md) を参照してください。

### <a name="will-microsoft-add-support-for-microsoft-windows-server-2008-servers"></a>Microsoft は Microsoft Windows Server 2008 サーバーのサポートを追加しますか?

いいえ、この時点ではありません。 Azure の機能には、Microsoft Windows Server 2012 R2 および Microsoft Windows Server 2016 でのみ使用可能ないくつかの依存関係があります。

### <a name="does-the-user-who-installs-the-document-routing-agent-have-to-be-part-of-a-finance-and-operations-apps-security-group"></a>ドキュメント回覧エージェントをインストールするユーザーは、Finance and Operations アプリ セキュリティ グループの一部である必要がありますか?

はい。 エージェントのインストール リンクにアクセスするには、ユーザーは **ドキュメント ルート指定クライアント** のセキュリティ ロールの一部でなければなりません。

### <a name="how-many-network-printers-can-the-document-routing-agent-support"></a>ドキュメント回覧エージェントはいくつのネットワーク プリンターをサポートできますか。

サポートされているネットワーク プリンターの数は、法人の数と配置されたネットワーク プリンターの数によって異なります。 50 台のプリンタと 1 つの法人組織がある場合は、単一のドキュメント ルーティング エージェントが負荷を処理できます (高可用性を確保するために複数のドキュメント ルーティング エージェントが必要になります)。 プリンタおよび法人の数が多い場合は、必要となるドキュメント回覧エージェントの数を決定するいくつかのパフォーマンス テストを実行することをお勧めします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]