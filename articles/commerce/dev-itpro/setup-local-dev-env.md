---
title: ローカル開発環境の設定
description: この記事では、Microsoft Dynamics 365 Commerce Cloud Scale Unit (CSU) および販売時点管理 (POS) 機能のローカル開発環境の設定方法について説明します。
author: mugunthanm
ms.date: 09/16/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 09-16-2021
ms.dyn365.ops.version: AX 10.0.22
ms.openlocfilehash: 3b8df31f52ea90483355659e4642b71632b0e555
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069008"
---
# <a name="set-up-a-local-development-environment"></a>ローカル開発環境の設定

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Cloud Scale Unit (CSU) および販売時点管理 (POS) 機能のローカル開発環境の設定方法について説明します。 Dynamics 365 Commerce アプリケーション バージョン 10.0.22 以降に適用されます。

> [!IMPORTANT]
> この記事で説明されている環境設定は、拡張機能開発にのみ使用できます。 テスト、ユーザー受け入れテスト (UAT)、または運用には使用できません。

## <a name="supported-development-environment-types"></a>サポートされる開発環境タイプ

Commerce は、クラウドベース環境とローカル環境の両方をサポートします。

+ **クラウドベース:** [Microsoft Dynamics Lifecycle Service (LCS)](../../fin-ops-core/dev-itpro/dev-tools/access-instances.md) を使用して、クラウドベースの開発環境を展開します。
+ **ローカル:** 自分のコンピューターで開発環境を設定するには、次の 2 つのオプションがあります:

    - **自己ホスト CSU** – この環境タイプは、CSU をローカルに展開します (実行可能ファイルとしての自己ホスト)。 リアルタイムの呼び出しに対応するインターネット インフォメーション サービス (IIS)、Commerce データ同期、または Commerce Headquarters 接続はありません。 このオプションを使用した場合、Commerce Headquarters と CSU チャネルのデータベース間でデータの同期は行われません。 チャネル データベースには、開発目的で使用される既定のデモ データが入力されています。 ギフト カードを発行するための呼び出しなど、Commerce Headquarters へのすべての要求および呼び出しは、ローカル CSU によって阻止されます。
    - **IIS ホスト CSU:** – この環境タイプは、IIS に CSU を展開し、Commerce Headquarters と CSU チャネル データベースの間でデータを同期する Async Client を設定します。 また、Commerce Headquarters とのリアルタイム接続のサポートも設定します。 この設定には、追加のコンフィギュレーションがいくつか必要です。 たとえば、Azure Active Directory (Azure AD) アプリを設定し、証明書を展開する必要があります。 IIS ホスト CSU をインストールする方法の詳細については、[IIS ホストされた Commerce Scale Unit ドキュメントの構成およびインストール](retail-store-scale-unit-configuration-installation.md#configure-a-new-commerce-scale-unit)を参照してください。

## <a name="hardware-requirements"></a>ハードウェア要件

16 GB の RAM と少なくとも 2 つの CPU コアを持つ Windows コンピューターを使用することをお勧めします。 財務と運用アプリ、Retail Server、eコマース開発、その他の同時プロセスを実行している場合は、24 GB のRAM と 4 つの CPU コアをお勧めします。

## <a name="local-self-hosted-csu"></a>ローカルの自己ホスト CSU

このバージョンの Scale Unit は、非常に軽量です。 他のシステムおよびサービスへの最小限または全く依存関係を必要としない、さまざまな Commerce runtime (CRT)/RTS 拡張機能を開発する迅速な方法を提供します。

**メリット:**

- Commerce Headquarters は必須ではありません。
- IIS は必須ではありません。 Retail Server はコンソール アプリでホストされます。
- トランスポート層セキュリティ (TLS) のコンフィギュレーションは必須ではありません。
- リアルタイム サービス (RTS) 通信は、一連のデモ モード CRT ハンドラーによって阻止されます。
- Async Client は必須ではありません。 チャネル データベースには自動的にデモ データが入力されます。
- Scale Unit の展開を開始するのに必要なパラメーターは少ししかありません。 したがって、展開の前提条件は最小限に抑えられています。 たとえば、証明書を明示的に作成してインストーラーに提供する必要はありません。
- このバージョンでは、CRT/Retail Server の開発およびランタイム機能を非常に迅速かつ簡単に紹介しています。

**デメリット:**

- Cloud POS (CPOS)、Async Client、HTTPS は存在せず、RTS 呼び出しがないため、このバージョンは実際の運用環境で使用されるトポロジとは一致しません。
- リアルタイム操作を完全にテストすることはできません。 阻止されるためです。

## <a name="local-iis-hosted-csu"></a>ローカルの IIS ホスト CSU

IIS モードは完全なオンプレミスの Scale Unit であり、すべてのコンポーネントが実際の稼働展開と一致し、何も阻止されません。

**メリット:**

- このバージョンは、IIS で Retail Server をホストするオンプレミスの Scale Unit として十分な機能を備えています。
- これは、Commerce Headquarters との実際の (阻止されない) RTS 対話を使用します。
- これには、通常の Scale Unit と同様に、Commerce Headquarters データベースのデータに基づいて、チャネル データベースを埋める Async Client が含まれます。 したがって、デモ データは関係ありません。

**デメリット:**

- 証明書および Azure AD 登録を作成し、Commerce Headquarters からコンフィギュレーション ファイルをダウンロードするには、追加の手順が必要です。

## <a name="prerequisites-for-setting-up-the-local-development-environment"></a>ローカル開発環境を設定するための前提条件

自己ホスト環境または IIS ホスト環境を設定する前に、次の前提条件をこの順序で完了します:

1. Windows x64 用 .NET Core SDK 3.1 を [.NET Core 3.1 をダウンロードする](https://dotnet.microsoft.com/download/dotnet/3.1)からインストールします。
2. [SQL Server](/sql/database-engine/install-windows/install-sql-server) の任意のエディションをインストールし、全文検索を有効にします。 詳細については、[SQL Server (セットアップ) のインスタンスへの追加機能](/sql/database-engine/install-windows/add-features-to-an-instance-of-sql-server-setup)を参照してください。 サポートされる最小バージョンは、13.0.5026.0 SqlServer 2016 SP2 です。

    + 複合の (SQL + Windows/Integrated) 認証を有効にします。
    + SQL Server の既定のインスタンスがインストールされていない場合、CSU の展開は失敗します。 エラー メッセージは、インスタンスが見つからなかったことを示します。 代わりに名前付きインスタンスを使用する場合は、行 78 の後に次の行を挿入して **Install.ps1** ファイルを編集します。 (このスクリプトは、**Dynamics365Commerce.ScaleUnit/src/ScaleUnitSample/Scripts** フォルダーで検索できます。)

        ```powershell
        $installerArgs += $("--sqlservername", "PutYourSqlServerSeenInSSMSHere")
        ```

        (この行を挿入する場合は、**PutYourSqlServerSeenInSSMSHere** を SQL Server 名に置き換えます。)

3. [利用可能な NuGet 配分バージョン](https://www.nuget.org/downloads)から NuGet.exe をインストールします。 ある場所にコピーしてから、**PATH** 環境変数を追加更新して、その場所を指すようにします。
4. MSBuild をインストールしていない場合は、[Visual Studio ツールをダウンロードする](https://visualstudio.microsoft.com/downloads/)から Visual Studio ツールをインストールします。 **Visual Studio 用ツール** セクションを展開し、**Visual Studio 用ビルド ツール** をダウンロードして実行します。 どのコンポーネントも指定しないでください。 **インストール** を選択して、既定のインストールを行います。

    + Visual Studio ツールをインストールしたら、コマンド プロンプト ウィンドウを開き、コマンド `where msbuild` を実行します。 msbuild.exe が見つからない場合は、Visual Studio 開発者コマンド プロンプトからコマンドを実行します。
    + msbuild.exe を見つけた後、**PATH** 環境変数が、パスの先頭に "msbuild" を含むフォルダーを指していることを確認します。 パスには、少なくともバージョン 15 の msbuild.exe のバージョンが含まれている必要があります。 バージョン番号を確認するには、コマンド `msbuild /version` を実行します。
    + **PATH** 変数が正しく設定されていることを確認するには、通常のコマンド プロンプトからコマンド `msbuild/version` を実行します。 開発者コマンド プロンプトは使用しないでください。 コマンドでは、少なくとも 15 のバージョン番号を出力する必要があります。 MSBuild の設定が完了したら、Visual Studio Code を再起動します。

5. 以前にダウンロードした Visual Studio ツールを使用して Microsoft.NET.Sdk をインストールします。 **個々のコンポーネント** に移動し、**.NET SDK** を入力し、.NET SDK のチェック ボックスをオンにしてから、**インストール** を選択します。
6. [Node をダウンロードしてインストールする](https://nodejs.org/en/download/) から、Node.JS の 64-ビット バージョンをインストールします。 **PATH** 環境変数がその場所を指していることを確認します。 メッセージが表示されたら、**必要なツールの自動インストール** チェック ボックスをオンにします。
7. Windows 用 Visual Studio Code の 64-ビット バージョンを [Visual Studio Code をダウンロードする](https://code.visualstudio.com/download)からインストールします。
8. [拡張機能マーケットプレース](https://code.visualstudio.com/docs/editor/extension-marketplace)の手順に従って、Visual Studio Code の  Visual Studio Code 用 C# (OmniSharp を利用) 拡張機能をインストールします。
9. [Scale Unit GitHub リポジトリ (リポジトリ)](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit) を複製またはダウンロードします。
10. LCS で、[共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)に移動し、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、**Commerce Scale Unit (SEALED)** で終わるファイルを検索します。 必要なリリースのバージョン (バージョン 10.0.22 または 10.0.23 など) を選択してください。 ファイルをダウンロードし、前の手順で複製またはダウンロードした Scale Unit GitHub リポジトリで、**ダウンロード** フォルダーに保存します (**Dynamics365Commerce.ScaleUnit/src/ScaleUnitSample/Download/**)。

## <a name="additional-prerequisites-for-iis-hosted-csu"></a>IIS ホスト CSU におけるその他の前提条件

+ IIS が必須であり、複数の機能を有効にする必要があります。 インストーラーは必要な任意の機能を報告しますが、その機能はまだ有効になっていません。
+ システムで、TLS 1.2 を有効にする必要があります。 (TLS 1.0 または 1.1 は使用しないでください。) この前提条件に関してはインストーラーに確認させます。 コンピューターで TSL 1.2 の変更が必要な場合、インストーラーには操作可能な指示が表示されます。
+ **.vscode/tasks.json** ファイルで次の変更を加えることにより、TLS の強力な暗号化を積極的に設定できます:

    - **baseProduct\_Port** – 既定のポート (446) を保持するか、または変更したい任意の値に変更できます。 指定したポートが別のアプリケーションで使用される場合は、基本インストーラー展開で、別のポートを指定するように求めるメッセージが表示されます。
    - **baseProduct\_SslCertFullPath** – このパスは、CSU Web サイトが HTTPS 通信に使用する Secure Sockets Layer (SSL) 証明書を指す必要があります。 この非実稼働設定の場合、証明書は自己署名ができます。 この証明書は **LocalMachine/Personal** 証明書ストアに格納される必要があります。 証明書を生成するには、次の手順に従います:

        1. IIS を開き、コンピュータ名のアイコンをダブルタップ (またはダブルクリック) します。
        2. **サーバー証明書** をダブルタップ (またはダブルクリック) します。
        3. 右側で、**自己署名証明書を作成する** を選択します。
        4. 証明書のフレンドリ名を指定するようにメッセージが表示されたら、コンピューターの完全修飾ドメイン名 (FQDN) を指定します。 コンピューターがドメインと結合している場合、FQDN にはそのコンピューター名自体とドメインが含まれます。 Windows PowerShell コマンド `[System.Net.Dns]::GetHostEntry("")` を実行して、FQDN を検索できます。 Windows の **システム** コントロール パネルの項目で、**フル コンピューター名** フィールドから FQDN を取得することもできます。
        5. 証明書ストア (**個人**) の規定値をそのまま使用します。
        6. **OK** を選択します。
        7. 新しい証明書を一覧で検索し、ダブルタップ (またはダブルクリック) します。
        8. **詳細** タブで、**拇印** の値を検索します。
        9. 拇印をテキスト エディターにコピーして貼り付け、すべての文字を大文字に変換します。 次に、**baseProduct\_SslCertFullPath** オプションの定義済テンプレートの末尾に変換された値を追加して、テンプレートが `store:///My/LocalMachine?FindByThumbprint=YourThumbprintGoesHere` に類似するようにします。

        > [!NOTE]
        > 基本インストーラーには、さらに 2 つの証明書が必要で、合計 3 つの証明書が必要となります。 セキュリティ上の理由から、すべての実稼働展開に対して、3 つの異なる証明書を作成する必要があります。 ただし、この展開設定では、この方法がポリシーに違反しない限り、3 つのコンフィギュレーション オプションすべてで同じ証明書を使用することで時間を節約できます。 この場合、次の 2 つのパラメーターに対して同じ拇印を指定できます。

    - **baseProduct\_RetailServerCertFullPath** – 作成した証明書の拇印を使用して、このパラメーターを更新します。 この証明書は、Retail Server の ID を表します。 CSU が POS シナリオのセキュリティ トークンを発行する場合などに、ID が使用されます。 この証明書を作成するには、SSL 証明書に使用したのと同じ手順に従いますが、指定したい任意のフレンドリ名 (たとえば、**RsTestIdentity**) を指定します。 この証明書は、後で Azure AD アプリケーションを設定するときに必要になります。
    - **baseProduct\_AsyncClientCertFullPath** – Async Clientは、Commerce Headquarters による通信用 Azure AD からセキュリティ トークンを取得するときにこの証明書を使用します。 この証明書を作成するには、SSL 証明書に使用したのと同じ手順に従いますが、指定したい任意のフレンドリ名 (たとえば、**AsyncClientTestIdentity**) を指定します。
    - **baseProduct\_RetailServerAadClientId** – 値は、Retail Server の ID を表す Azure AD アプリケーション クライアント ID です。 CSU が POS シナリオのセキュリティ トークンを発行する場合などに使用されます。 アプリケーションを作成し、そのアプリケーション (クライアント) IDを取得するには、[独自の Azure AD アプリケーションを使用する CPOS の構成方法](https://community.dynamics.com/ax/b/axforretail/posts/how-to-point-cpos-to-use-your-own-azure-ad-application)の手順 3 に従います。
    - **baseProduct\_RetailServerAadResourceId** – 値は登録済 Azure AD アプリケーションのリソース ID です。 [独自の Azure AD アプリケーションを使用する CPOS の構成方法](https://community.dynamics.com/ax/b/axforretail/posts/how-to-point-cpos-to-use-your-own-azure-ad-application)の手順 3c で "アプリケーション ID URI" と説明されている値を使用します。
    - **baseProduct\_CposAadClientId** – 値は CPOS を表す Azure AD アプリケーション クライアント ID です。 アプリケーションを作成し、そのアプリケーション (クライアント) IDを取得するには、[独自の Azure AD アプリケーションを使用する CPOS の構成方法](https://community.dynamics.com/ax/b/axforretail/posts/how-to-point-cpos-to-use-your-own-azure-ad-application)の手順 4 に従います。 この手順で、Azure AD での CSU/CPOS の設定を完了します。 Commerce Headquarters で必要な設定を完了するには、[独自の Azure AD アプリケーションを使用する CPOS の構成方法](https://community.dynamics.com/ax/b/axforretail/posts/how-to-point-cpos-to-use-your-own-azure-ad-application)の手順 6 に従います。
    - **baseProduct\_AsyncClientAadClientId** – 値は、Commerce Headquarters での認証が必要な場合に Async Client が使用する Azure AD アプリケーション クライアント ID です。 このアプリケーションを作成し、もう 1 つの Azure AD アプリケーションを登録するには、[独自の Azure AD アプリケーションを使用する CPOS の構成方法](https://community.dynamics.com/ax/b/axforretail/posts/how-to-point-cpos-to-use-your-own-azure-ad-application)の手順 3a から 3b に従います。 Commerce Headquarters を使用して作成済アプリケーションのみを登録するには、[AX7 のサービスからサービスへの認証](https://community.dynamics.com/ax/b/axforretail/posts/service-to-service-authentication-in-ax7)の手順 2 に従います。
    - **baseProduct\_Config** – [CSU インストーラーのダウンロード](retail-store-scale-unit-configuration-installation.md#download-the-commerce-scale-unit-installer)の手順 4 で説明されているように、Commerce Headquarters からダウンロードできるチャネル データベース コンフィギュレーションに対応するファイル名のみを指定し、完全なパスは指定しません。 Commerce Headquarters からファイルをダウンロードした後、[ダウンロード](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-ScaleUnit?path=/src/ScaleUnitSample/Download&version=GC0acfab2d3d7cbd734ea5b19f2b2ac6713d7391ef) フォルダーに保存します。
    - **baseProduct\_UseSelfHost** – この値を **false** に設定します。

## <a name="debug-an-extension-by-using-the-self-hosted-csu"></a>自己ホスト CSU を使用した拡張機能のデバッグ

1. Visual Studio Code を管理者として開きます。
2. 以前に複製またはダウンロードした Scale Unit GitHub レポジトリで、**src\\ScaleUnitSample** フォルダーを開きます。
2. **.vscode/tasks.json** ファイルを開き、**baseProduct\_UseSelfHost** を **true** に設定します。
3. **ターミナル** メニューで、**タスクの実行** を選択し、**ビルド拡張機能** を入力します。

    このシステムで実行スクリプトが無効になっているというエラー メッセージが表示された場合は、管理者としてコマンド プロンプト ウィンドウを開き、`powershell Set-ExecutionPolicy RemoteSigned` を実行します。 次に、Visual Studio Code を閉じて再度開きます。 セキュリティ ポリシーを変更する影響を理解していない限り、実稼働機械の実行ポリシーを変更しないでください。

4. 拡張メソッドにブレーク ポイントを配置し、**F5** キーを選択して拡張機能をデバッグします。

**F5** を選択すると、次のアクションが自動的に実行されます。 (これらのアクションは、Visual Studio Code のみでサポートされます。)

- Scale Unit のサンプル コードがコンパイルされます。 コンパイルにより、シールドされた CSU 拡張機能インストーラーを含むパッケージが生成されます。
- 基本シールドされた Scale Unit インストーラーは、まだ展開されていない場合に展開されます。
- デモ データを含むパッケージは、SDK のフィードからダウンロードされ、チャネル データベースに適用されます。
- シールドされた Scale Unit 拡張機能インストーラーが展開されます。
- CSU の正常性チェック エンドポイントへの呼び出しの結果を示す Web ブラウザー ウィンドウが開きます。
- デバッガーは CSU をホストするプロセスに関連付けられ、CSU は URL `http://localhost:12345` で受信要求を処理する準備ができています。

ローカル Scale Unit が要求に対応している間は、デバッグ コンソールを使用して Scale Unit の内部診断のログをリアルタイムで監視します。 ログは、デバッグしているときにに役立ちます。

## <a name="debug-an-extension-by-using-the-iis-hosted-csu"></a>IIS ホスト CSU を使用した拡張機能のデバッグ

1. Visual Studio Code で、 **実行とデバッグ** を選択 (または **Ctrl+Shift+D** を選択) します。 上部ナビゲーション バーの下に、緑の矢印でドロップダウン メニューが表示されます。 **IIS を使用したデバッグ** を選択します。
2. **F5** キーを選択します。 自己ホスト CSU モードでデバッグする場合と同様に、基本インストーラーが最初に展開されます。 次に、拡張機能インストーラーが展開されます。
3. 基本インストーラーは前提条件チェックを実行し、必要なアクションを報告します。 前提条件には、SQL Server、IIS、TLS、および .Net Core ホスト バンドルが含まれます。
4. 基本パッケージと拡張機能パッケージが展開された後、Visual Studio Code が、正常性チェックへの呼び出しの結果を示す Web ブラウザー ウィンドウを開きます。 Visual Studio Code により、デバッガーを関連付けるよう求めるダイアログ ボックスも開きます。 この手順はオプションです。 デバッガーを関連付ける場合は、プロセスの一覧に **w3wp** と入力し、**RssuCore** を含む行を選択します。 RssuCore は、CSU Web サイトの実行に使用される IIS アプリケーション プールの名前です。

これで、次の要素を含む、完全に機能するオンプレミスの展開済 Scale Unit となりました:

- チャネル データベース
- Async Client
- RTS 経由で Commerce Headquarters と対話できる ASP.NET Core 3.1 ベースの Retail Server
- CPOS

今展開した CPOS と CSU に対応する URL を検索するには、基本インストーラーのログを確認します。 URL はログの最後の方に表示され、CSU と CPOS の正常性チェックが行われます。 Commerce Headquarters からのデータを使用してチャネル データベースに入力するには、[新しい Commerce Scale Unitを構成する](retail-store-scale-unit-configuration-installation.md#configure-a-new-commerce-scale-unit)の手順 28 に従います。 (ドキュメントの前の手順は既に完了している必要があります。)

## <a name="switching-from-iis-mode-to-self-hosted-mode"></a>IIS モードから自己ホスト モードへの切り替え

IIS と自己ホスト モード間を切り替える場合は、次の手順に従ってください。 (これが最初の実行である場合は、ここで説明されている値は既定値なので、これらの手順を省略できます。)

- Visual Studio Code で、 **実行とデバッグ** を選択 (または **Ctrl+Shift+D** を選択) します。 上部ナビゲーション バーの下に、緑の矢印でドロップダウン メニューが表示されます。 **自己ホストを使用したデバッグ** を選択します。
- **.vscode/tasks.json** ファイルを開き、**baseProduct\_UseSelfHost** が **false** に設定されるよう確認します。

**F5** を選択すると、次のアクションが自動的に実行されます。 (これらのアクションは、Visual Studio Code のみでサポートされます。)

- Scale Unit のサンプル コードがコンパイルされます。 コンパイルにより、シールドされた CSU 拡張機能インストーラーを含むパッケージが生成されます。
- 基本シールドされた Scale Unit インストーラーは、まだ展開されていない場合に展開されます。
- デモ データを含むパッケージは、SDK のフィードからダウンロードされ、チャネル データベースに適用されます。
- シールドされた Scale Unit 拡張機能インストーラーが展開されます。
- CSU の正常性チェック エンドポイントへの呼び出しの結果を示す Web ブラウザー ウィンドウが開きます。
- デバッガーは CSU をホストするプロセスに関連付けられ、CSU は URL `http://localhost:12345` で受信要求を処理する準備ができています。

ローカル Scale Unit が要求に対応している間は、デバッグ コンソールを使用して Scale Unit の内部診断のログをリアルタイムで監視します。 ログは、デバッグしているときにに役立ちます。

## <a name="deploy-the-extension-package-to-production"></a>拡張パッケージを実稼働に展開する

ビルドがエラーなく完了した場合、出力を使用して拡張機能を展開できます:

- **Cloud Scale Unit拡張機能パッケージ** – このパッケージは、**ScaleUnit\\bin\\Debug\\netstandard2.0** フォルダーにあり、クラウド展開用に使用されます。
- **Scale Unit 拡張機能インストーラー** – このインストーラーは、**Installer\\bin\\Debug\\net461** フォルダーにあり、オンプレミスの (店舗内) インストールに使用されます。

ビルド パイプラインを設定してパッケージを生成してから、それを展開する必要があります。 詳細については、[独立したパッケージ SDK のビルド パイプラインの設定](build-pipeline.md)および[パッケージを CSU に展開する](retail-sdk/retail-sdk-packaging.md#deploy-the-package-to-csu)を参照してください。

### <a name="troubleshooting"></a>トラブルシューティング

展開問題のトラブルシューティングについては、Visual Studio Code の **ターミナル** タブで、一連の詳細ログおよび関連するメッセージを確認して下さい。 ご自身で問題点を特定できない場合は、Microsoft にお問い合わせください。 Microsoft にお問い合わせの際は、次のデータを提供してください:

- 実行したアクションの詳細な説明
- 基本の Scale Units の展開プロセスの出力の最初と最後に参照されるログ ファイル
- Visual Studio Code ターミナルの出力 (警告やエラーを含む)

Retail Server と Async Client (IIS ホストの場合) に対応するランタイム ログは、イベント ビューアーの **Windows ログ \> アプリケーション** に表示されます。 ログをフィルター処理するには、次のソースを使用します:

- Microsoft Dynamics - Async Client サービス
- Microsoft Dynamics - Retail Server

自己ホスト CSU は、ランタイム ログを Visual Studio Code ターミナルにも直接出力します。

## <a name="out-of-box-tasks-in-visual-studio-code"></a>Visual Studio Code での既成のタスク

Visual Studio Code の **ターミナル** メニューで **タスクの実行** コマンドを選択すると、次の一連のタスクが利用可能になります:

- **ビルド拡張機能** – 拡張機能を構築します。
- **check-msbuild** – Visual Studio Code に使用できる MSBuild のバージョンを表示します。
- **check-ps-bitness** – Visual Studio Code に使用できる Windows PowerShell のバージョンが、必要な 64-ビット バージョンであるかどうかを確認します。
- **clean-extension** – 拡張機能の構築中に生成されたビルド出力を取り除きます。
- **インストール** – 展開時のすべての前提条件を確認してから、選択したモード (自己ホストまたは IIS) に対して必要なすべてのアクションを実行します。 このタスクには、基本の Scale Unit および拡張機能インストーラーのインストールが含まれます。
- **アンインストール** – 拡張機能と基本の Scale Unit をアンインストールします。
- **uninstall-base-product** – 基本の Scale Unit をアンインストールします。 インストールされた拡張機能が検出された場合、このタスクは失敗します。
- **uninstall-extension** – 拡張機能をアンインストールします。

### <a name="support"></a>サポート

セットアップが期待通りに機能しない、またはヘルプが必要な場合は、次のリンクを使用してサポートを利用してください:

+ [microsoft/Dynamics365Commerce.ScaleUnit](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit/issues)
+ [Dynamics 365 Commerce フォーラム](https://community.dynamics.com/365/commerce/f/dynamics-365-commerce-forum)
+ [Retail 利益団体](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=1585934)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

