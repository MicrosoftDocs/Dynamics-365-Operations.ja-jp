---
title: "Microsoft Dynamics 365 for Retail で使用する N-1 コンポーネントをインストールする"
description: "このトピックでは、セルフ サービスを使用して、Microsoft Dynamics 365 for Retail headquarters で Connector for Microsoft Dynamics AX を構成し、ダウンロードして、 Microsoft Dynamics AX 2012 R3 環境のドメイン コンピューターにインストールし、以前に展開され実行されている店舗でも使用できるようにします。"
author: jashanno
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics-365-retail
ms.technology: 
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail, Core
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: ebcfccd6dadf05e0fb6ac86d33a4464d9bead4bb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="install-n-1-components-for-use-with-microsoft-dynamics-365-for-retail"></a>Microsoft Dynamics 365 for Retail で使用する N-1 コンポーネントをインストールする

[!include [banner](../../includes/banner.md)]

このトピックでは、セルフ サービスを使用して、Microsoft Dynamics 365 for Retail headquarters で Connector for Microsoft Dynamics AX (以前は **N-1**) を構成し、ダウンロードして、 Microsoft Dynamics AX 2012 R3 環境のドメイン コンピューターにインストールし、以前に展開され実行されている店舗でも使用できるようにします。 Connector for Microsoft Dynamics AX は、2 つの独立したインストーラーで構成されています。 1 つのインストーラーは、Retail Async ServerRetail Connector サービス用で、もう 1 つのインストーラーは AX 2012 R3 用のリアルタイム サービス用です。 インストールが完了したら、Microsoft Dynamics 365 for Retail 環境が、POS AX 2012 R3 からの Enterprise POS と Retail Modern POS を含む、現在インストール済みの機能している店舗のバックエンド インフラストラクチャとして使用されます。 このトピックは、これらのインストールのアンインストールとトラブルシューティングの方法についても説明します。

## <a name="before-you-begin"></a>準備

> [!IMPORTANT]
> 企業全体で高いレベルのセキュリティを維持するために、このインストールに新しいクライアント ID とシークレットを作成することを強くお勧めします。 このステップでは、新しい Web アプリが必要です。

1. クライアント ID とシークレットを作成するには、Microsoft Azure Web アプリを生成します。 手順については、[Azure Active Directory アプリケーションを作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application) で「Azure AD でアプリケーションを登録するための基本」セクションを参照してください。
2. クライアント ID とシークレット Connector for Microsoft Dynamics AX を作成した後、Retail でクライアント ID を承諾する必要があります。 **システム管理** &gt; **セットアップ** &gt; **Azure Active Directory アプリケーション**の順に移動します。 クライアント ID を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力および **RetailServiceAccount** を**ユーザー ID** 列に入力します。

## <a name="configure-connector-for-microsoft-dynamics-ax"></a>Connector for Microsoft Dynamics AX のコンフィギュレーション
Connector for Microsoft Dynamics AX を構成するには、[Connector for Microsoft Dynamics AX インストーラの実行] の手順に従って、このトピックのすべてのセクションの手順を実行します。

1. Azure Active Directory (Azure AD) 証明書を使用して、小売用バックオフィスまたは Retail 評価版にサインインします。
2. **ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **Connector for Microsoft Dynamics AX** に移動します。
3. アクション ウィンドウで、**新規**を選択します。
4. **プロファイル** フィールドに、固有値を入力します。
5. **リアルタイム サービスの場所** の **サーバー** フィールドに、2012 R3 のリアルタイム サービスがインストールされるサーバーの URL を入力します。

    > [!NOTE]
    > 現在のリアルタイム サービスを最初にインストールしたのと同じ場所を使用するか、新しい場所を指定することができます。

6. **ポート** フィールドに、AX 2012 R3 の新しいリアルタイム サービスが使用するポートを入力します。
7. **Web アプリケーション名**フィールドで、Internet Information Services (IIS) で使用する必要がある Web アプリケーション名を入力します。 既定では、**RetailCDXRealTimeService** が選択されています。
8. **プロトコル** フィールドで、元のリアルタイム サービスによって使用されているプロトコルを選択します。

    > [!NOTE]
    > HTTPS の使用をお勧めしますが、**net.tcp** は以前のインストール シナリオのより良いサポートのためのリストに表示されます。 

9. **接続情報** の **共通名** フィールドに、AX 2012 R3 のリアルタイム サービスで使用する証明書のフレンドリ名を入力します。 この値と **パスフレーズ** フィールドの値をあわせて、AX 2012 R3 の元のリアルタイム サービスと新しいリアルタイム サービスとの接続が可能になります。
10. **言語**フィールドで、関連付けられている店舗が使用する言語を選択します。
11. アクション ウィンドウで、**保存**を選択します。
12. アクション ウィンドウで、**小売用スケジューラのパラメーター**を選択します。 Async Server Connector service に詳細を入力できるようになりました。
13. **HQ メッセージ データベース**の **SQL Server インスタンス名** フィールドに、使用する Microsoft SQL Server のインスタンス名を入力します。
14. **サーバー名**フィールドに、SQL Server が使用されているコンピューターの完全修飾ドメイン名 (FQDN) を入力します。

    > [!NOTE]
    > データベースが Async Server Connector service と同じコンピューター上にある場合は、**localhost** を入力します。

15. **データベース名**フィールドに、HQ メッセージ データベースの名前を入力します。

    > [!NOTE]
    > AX 2012 R3 では、既定値は **HQMessageDB** でした。

16. アクション ウィンドウで、**保存**を選択します。
17. **小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **チャンネル データ グループ**の順に移動します。
18. **既定** データ グループ、前のインストール セットのチャネルに関連付けられているデータ グループを選択します (AX 2012 R3 から Enterprise POS および Modern POS を使用していた N-1 チャネル)。
19. アクション ウィンドウで、**完全データ同期**を選択します。**配送スケジュールの選択**のフィールドで、ジョブ **9999** を選択し、**OK** を選択します。 表示されるダイアログ ボックスで、**OK** を選択して完全同期を確認します。 チャンネル データベース内のすべてのデータはダウンロードの準備をします。

### <a name="download-the-connector-for-microsoft-dynamics-ax-installers"></a>Microsoft Dynamics AX インストーラーのコネクタをダウンロード

1. Azure AD 証明書を使用して、Microsoft Dynamics 小売用バックオフィスまたは Retail 評価版にサインインします。
2. **ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **本社の設定** &gt; **小売用スケジューラ** &gt; **Connector for Microsoft Dynamics AX** に移動します。
3. 左のコネクタの一覧で、このインストールに対して以前に作成したコネクタを選択します。
4. アクション ウィンドウで、**ダウンロード**を選択します。
5. ドロップダウン メニューの、**Async Server Connector service** で、**コンフィギュレーション ファイル**を選択します。

    > [!NOTE]
    > Connector for Microsoft Dynamics AX インストーラーが構成ファイル (XML ファイル) を正しく使用するためには、構成ファイルをインストーラーと同じ場所に保存する必要があります。

6. Internet Explorer ウィンドウの下部に表示される通知バーで、**保存**を選択します。 (通知バーは、他のブラウザでは別の場所に表示される場合があります。)

    > [!NOTE]
    > ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。 **1 回許可** または **このサイトのオプション** &gt; **常に許可** を選択します。 その後、再度 **ダウンロード** を選択します。

7. アクション ウィンドウで、**ダウンロード**を選択します。
8. ドロップダウン メニューで、**Async Server Connector service** を選択します。
9. Internet Explorer ウィンドウの下部に表示される通知バーで、**保存**を選択します。 (通知バーは、他のブラウザでは別の場所に表示される場合があります。)

    > [!NOTE]
    > 選択したチャネル データベースの Connector for Microsoft Dynamics AX パッケージに基づいて、適切なパッケージがダウンロード用に自動的に選択されます。

10. セットアップ インストーラが保存されたら、通知バーの、**実行**を選択します。 (この手順はブラウザの種類によって異なる場合があります。)
11. **Real-time service for Dynamics AX 2012 R3** に対して手順 4 ～ 10 を繰り返します。

### <a name="running-the-connector-for-microsoft-dynamics-ax-installers"></a>Microsoft Dynamics AX インストーラーのコネクタを実行中

> [!NOTE]
> Connector for Microsoft Dynamics AX インストーラーを実行する前に、次の要件が満たされていることを確認します。
> - インストーラーでは、Microsoft .NET Framework バージョン 4.5.1 がシステムにインストールされている必要があります。
> - インストーラーは、Connector for Microsoft Dynamics AX アプリケーションを次のオペレーティング システムにのみインストールします。 任意のコンポーネントをインストールする前に、オペレーティング システムに使用可能なすべてのサービス パックおよび更新プログラムを更新する必要があります。
>     - Windows 7 Professional、Enterprise、または Ultimate エディション (x86 および x64 アーキテクチャの両方)。 Home エディションおよび埋め込みエディションはサポートされていません。
>     - Windows 8.1 Update 1 Pro または Enterprise エディション (x86 および x64 アーキテクチャの両方)。 標準エディションはサポートされていません。
>     - Windows 10 Pro または Enterprise エディション (x86 および x64 アーキテクチャの両方)。 Home エディションはサポートされていません。
>     - Windows Server 2012 R2 または Windows Server 2016。

Microsoft Dynamics AX インストーラーのコネクタは、まず関連付けられているファイルを抽出し、インストールを開始します。

#### <a name="async-server-connector-service"></a>Async Server Connector service

1. インストーラーは、すべての前提条件が満たされていることを検証します。 これらの前提条件には、SQL Server のローカル インストールなどの SQL 前提条件、または SQL Command Line Utilities やその他の必要な SQL 接続インストールなどの別の前提条件が含まれています。

    > [!NOTE]
    > - 前提条件を満たすためには、接続されている SQL Server で全文検索が必要であり、最低でもトランスポート層セキュリティ (TLS) 1.2 がサポートされている必要があります。 Microsoft SQL Server 2012 では、最低でも、Service Pack 3 がインストールされる必要があります。 Microsoft SQL Server 2014 では、Service Pack 2 がインストールされる必要があります。
    > - システムの再起動が必要な場合、インストーラーでこの要件が表示されます。 再起動することを推奨されていますが、インストーラーを使用せずに続行することができます。

2. Application Object Server (AOS) URL (小売用バック オフィスへのアクセスに使用される URL) を確認し、**次へ** を選択します。

    > [!NOTE]
    > この URL は、構成ファイルから自動的に入力されます。

3. HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。 **次へ** を選択して続行します。

    > [!NOTE]
    > 証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。 また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。 ローカル コンピューターの個人用証明書格納場所に保存する必要があります。

4. 特定のユーザーが必要な場合は、サービスを実行するために必要なユーザー名とパスワードを入力します。 既定では、インストーラーは自動的に使用するサービス アカウントを生成します。 この方法は、安全性が向上しお勧めしますが、データベースが別のコンピューターにある場合は使用できません。 **次へ** を選択して続行します。
5. 使用する必要のある HTTPS ポートを確認し、コンピューターのホスト名が正しいことを確認します。 **次へ** を選択して続行します。

    > [!NOTE]
    > - HTTPS ポートは、店舗システムのプロファイルに一覧表示されます。 店舗システム プロファイルにアクセスするには、**小売店舗詳細** ページの **店舗システム** FastTabで、選択した店舗システムのプロファイル ID を選択します。
    > - インストーラーは自動的にホスト名を入力します。 何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更します。 ホスト名はシステムの FQDN でなければなりません。また、このトピックの前半のセクションにある **Connector for Microsoft Dynamics AX** ページに入力した値と一致する必要があります。

6. アプリケーション ID (クライアント ID) および Connector for Microsoft Dynamics AX installation インストールと関連するシークレットを入力します。 また、コンフィギュレーション ファイルから自動的に入力されるチャネル データベース ID を確認します。 その後、**インストール** を選択します。

    > [!NOTE]
    > - クライアント ID およびシークレットを作成するため Azure Web アプリを正しく生成する方法の詳細については、[Azure Active Directory アプリケーションを作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application) で「Azure AD でアプリケーションを登録するための基本」セクションを参照してください。
    > - Web アプリを作成するとき、最初の URI と URL は特定の値である必要はありません。 作成されるアプリケーション ID (クライアント ID) とシークレットのみ重要です。

7. インストールが完了すると、最終正常性ページが表示されます。 このページには、インストールが成功したかどうかが表示されます。 また、基本的な接続テストに基づいた各コンポーネントの正常性と、このトピックの場所について示します。 インストールに失敗した場合は、ページにログ ファイルの場所が表示されます。
8. アプリケーション ID (クライアント ID) とシークレットが作成された後、アプリケーション ID は、小売で受け入れる必要があります。 **システム管理** &gt; **セットアップ** &gt; **Azure Active Directory アプリケーション**の順に移動します。 クライアント ID を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力および **RetailServiceAccount** を**ユーザー ID** 列に入力します。
9. 小売の**小売共有パラメーター** ページにクライアント ID を追加します。

    1. Retail で、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。
    2. **ID プロバイダー** を選択します。
    3. **ID プロバイダー**クイック タブで、**HTTPS://sts.windows.net/** で始まるプロバイダーを選択します。 選択に基づいて、**依存する関係者** FastTab の値が設定されます。
    4. **依存する関係者**クイック タブで、**+ 追加**を選択します。 このインストールに作成されたクライアント ID を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。 [アクション] ウィンドウで、**保存** を選択します。
    5. アクション ウィンドウで、**保存**を選択します。

10. 完了したら、アプリケーション インストーラーに戻り、**完了** を選択します。

    > [!NOTE]
    > インストーラーがコンポーネントのチェック マークを表示しない場合は、10 分待って、キャッシュされた値をクラウドで更新できるようにします。 再び確認します。 それでもインストーラーが完全に成功しない場合は、このインストールを使用する配送スケジュールで完全同期を実行します。

#### <a name="real-time-service-for-ax-2012-r3"></a>AX 2012 R3 のリアルタイム サービス

1. インストーラーは、すべての前提条件が満たされていることを検証します。

    > [!NOTE]
    > システムの再起動が必要な場合、インストーラーでこの要件が表示されます。 再起動することを推奨されていますが、インストーラーを使用せずに続行することができます。

2. AOS URL (小売用バック オフィスへのアクセスに使用される URL) を確認し、**次へ** を選択します。

    > [!NOTE]
    > この URL は、構成ファイルから自動的に入力されます。

3. HTTPS 通信に使用する、有効な SSL 証明書を選択します。 **次へ** を選択して続行します。

    > [!NOTE]
    > 証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。 また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。 ローカル コンピューターの個人用証明書格納場所に保存する必要があります。

4. 特定のユーザーが必要な場合は、アプリケーション プールを実行するために必要なユーザー名とパスワードを入力します。 既定では、インストーラーは自動的に使用するサービス アカウントを生成します。 この方法は、安全性が向上しお勧めしますが、データベースが別のコンピューターにある場合は使用できません。 **次へ** を選択して続行します。
5. 使用する必要のある HTTPS ポートを確認し、コンピューターのホスト名が正しいことを確認します。 **次へ** を選択して続行します。

    > [!NOTE]
    > - HTTPS ポートは、店舗システムのプロファイルに一覧表示されます。 店舗システム プロファイルにアクセスするには、**小売店舗詳細** ページの **店舗システム** FastTabで、選択した店舗システムのプロファイル ID を選択します。
    > - インストーラーは自動的にホスト名を入力します。 何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更します。 ホスト名はシステムの FQDN でなければなりません。また、このトピックの前半にある **Connector for Microsoft Dynamics AX** ページに入力した値と一致する必要があります。

6. アプリケーション ID (クライアント ID) および Connector for Microsoft Dynamics AX installation インストールと関連するシークレットを入力します。 その後、**インストール** を選択します。

    > [!NOTE]
    > - このアプリケーション ID とシークレットは、Async Server Connector サービスのインストールで使用したのと同じアプリケーション ID とシークレットにできます。 クライアント ID およびシークレットを作成するため Azure Web アプリを正しく生成する方法の詳細については、[Azure Active Directory アプリケーションを作成する](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application) で「Azure AD でアプリケーションを登録するための基本」セクションを参照してください。
    > - Web アプリを作成するとき、最初の URI と URL は特定の値である必要はありません。 作成されるアプリケーション ID (クライアント ID) とシークレットのみ重要です。

7. インストールが完了すると、最終正常性ページが表示されます。 このページには、インストールが成功したかどうかが表示されます。 また、基本的な接続テストに基づいたコンポーネントの正常性と、このトピックの場所について示します。 インストールに失敗した場合は、ページにログ ファイルの場所が表示されます。
8. アプリケーション ID と秘密が非同期サーバー コネクタ サービスで使用した同じアプリケーション ID と秘密である場合、小売業ではアプリケーション ID を受け入れる必要があります。 **システム管理** &gt; **セットアップ** &gt; **Azure Active Directory アプリケーション**の順に移動します。 クライアント ID を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力および **RetailServiceAccount** を**ユーザー ID** 列に入力します。
9. アプリケーション ID とシークレットが、Async Server Connector サービスに使用したアプリケーション ID とシークレットと同じでない場合は、このインストール用に作成されたアプリケーション ID (クライアント ID) を **Retail 共有パラメーター**に追加する必要があります。

    1. Retail で、**Retail** &gt; **本社の設定** &gt; **パラメーター** &gt; **小売共有パラメーター**に移動します。
    2. **ID プロバイダー** を選択します。
    3. **ID プロバイダー**クイック タブで、**HTTPS://sts.windows.net/** で始まるプロバイダーを選択します。 選択に基づいて、**依存する関係者** FastTab の値が設定されます。
    4. **依存する関係者**クイック タブで、**+ 追加**を選択します。 このインストールに作成されたクライアント ID を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。 [アクション] ウィンドウで、**保存** を選択します。
    5. アクション ウィンドウで、**保存**を選択します。

10. 完了したら、アプリケーション インストーラーに戻り、**完了** を選択します。

    > [!NOTE]
    > インストーラーがコンポーネントのチェック マークを表示しない場合は、10 分待って、キャッシュされた値をクラウドで更新できるようにします。 再び確認します。 それでもインストーラーが完全に成功しない場合は、このインストールを使用する配送スケジュールで完全同期を実行します。

### <a name="help-secure-the-connector-for-dynamics-ax-applications"></a>Dynamics AX アプリケーションのコネクタのセキュリティを強化する

現在の Payment Card Industry (PCI) のセキュリティ基準によると、実稼動環境で次のオプションを設定する必要があります。

- コンピューターの SSL (v2およびv3) を完全に無効にする必要があります。
- TLS バージョン 1.2 (または、現時点で最も新しいバージョン) のみを有効にし、使用する必要があります。

    > [!NOTE]
    > - 既定では、インストーラーはこれらの設定を変更しません。 (この点で、これらのインストーラは他のセルフサービス インストーラとは異なります)。 これらの設定を編集または有効にするには、次の手順を実行します。
    >     1. Windows ロゴキーと R キーを同時に押して、**実行**ウィンドウを開きます。
    >     2. **開く**フィールドに、**Regedit** と入力してから **OK** を選択します。
    >     3. **ユーザー アカウント制御**ウィンドウで、**はい** (この手順が必要である場合) を選択してから、新しい**レジストリ エディター** ウィンドウで **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols** に移動します。
    >         次のキーは自動的に入力され、TLS 1.2 のみが有効になりました。
    >         - TLS 1.2\\Server:Enabled=1
    >         - TLS 1.2\\Server:DisabledByDefault=0
    >         - TLS 1.2\\Client:Enabled=1
    >         - TLS 1.2\\Client:DisabledByDefault=0
    >         - TLS 1.1\\Server:Enabled=0
    >         - TLS 1.1\\Client:Enabled=0
    >         - TLS 1.0\\Server:Enabled=0
    >         - TLS 1.0\\Client:Enabled=0
    >         - SSL 3.0\\Server:Enabled=0
    >         - SSL 3.0\\Client:Enabled=0
    >         - SSL 2.0\\Server:Enabled=0
    >         - SSL 2.0\\Client:Enabled=0
    > - この構成は、AX 2012 R3 ストア (エンタープライズの POS と最新の POS) とこのトピックにインストールされている本社のコンポーネント間の通信に大きな影響を与えます。 したがって、現在通信がどのように機能しているかを注意深く検討する必要があります。

- 知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。
- クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。
- こうしたアプリケーションがインストールされたコンピューターで使用する証明書の取得には、信頼された証明機関のみを活用してください。

> [!IMPORTANT]
> IIS と PCI の要件向けのセキュリティ ガイドラインを確認することが重要です。

### <a name="troubleshoot-the-connector-for-microsoft-dynamics-ax-applications"></a>Microsoft Dynamics AX アプリケーションのコネクタのトラブルシューティング

このセクションでは、今後さらに詳細に扱います。 現時点では、これが確認する項目のチェックリストです。

1. Retail の**小売共有パラメーター** ページで、適切なクライアント ID が**依存する関係者**クイック タブに追加されていることを確認します。 
2. Retail で、作成されたすべてのクライアント ID が **Azure Active Directory アプリケーション** ページに存在することを確認します。

### <a name="uninstall-the-connector-for-microsoft-dynamics-ax-applications"></a>Microsoft Dynamics AX アプリケーションのコネクタのアンインストール

Microsoft Windows でコントロール パネルを使用して Retail Store システムをアンインストールします。

1. Windows ロゴ キーを押し、検索ボックスに**コントロール パネル**と入力します。 検索結果で、**コントロール パネル**を選択します。
2. コントロール パネルで、**プログラム** &gt; **プログラムのアンインストール**を選択します。
3. **プログラムと機能**ウィンドウで、**Microsoft Dynamics 365 for Retail ストア システム**を選択してから、プログラムの一覧で**アンインストール**を選択します。
4. アンインストールがプログラムの削除を完了するまで待ちます。

