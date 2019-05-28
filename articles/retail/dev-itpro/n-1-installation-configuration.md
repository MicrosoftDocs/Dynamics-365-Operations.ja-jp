---
title: 段階的なロールアウト (N-1) インストール、コンフィギュレーション、および切替ガイド
description: このトピックでは、Microsoft Dynamics AX 2012 R3 チャンネル コンポーネントが、Microsoft Dynamics 365 for Retail バックオフィスを使用できるように、段階的なロールアウト (N-1) のコンポーネントを設定する方法について説明します。
author: jashanno
manager: AnnBe
ms.date: 07/31/2018
ms.topic: article
ms.prod: ''
ms.service: Dynamics-365-retail
ms.technology: ''
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail, Core
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: f2dec055788ea60839ef026b18d9847c6e7442b2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537589"
---
# <a name="phased-rollout-n-1-installation-configuration-and-cutover-guide"></a>段階的なロールアウト (N-1) インストール、コンフィギュレーション、および切替ガイド

[!include [banner](../../includes/banner.md)]

ここでは、Microsoft Dynamics AX for Retail Modern Point of Sale (MPOS) および Retail サーバー、または Microsoft Dynamics AX for Retail Enterprise Point of Sale (EPOS) などの Microsoft Dynamics AX 2012 R3 チャンネル コンポーネントが、Microsoft Dynamics 365 for Retail バックオフィスを使用できるように、段階的ロールアウト (N-1) のコンポーネントを設定する方法について説明します。

## <a name="key-terms"></a>重要な用語
| 相談 | 説明 |
|---|---|
| N-1 非同期サーバー コネクタ サービス | 小売用バック オフィスと AX 2012 R3 チャネル コンポーネントの間でデータ パッケージを同期する場合に使用されるコンポーネント。 |
| N-1 リアルタイム サービス | AX 2012 R3 チャネル コンポーネントから小売用バックオフィスへのリアルタイムの呼び出しをサポートするコンポーネント。 |

## <a name="overview"></a>概要
このトピックのセクションでは、N-1 コンポーネントを所持する環境の設定を行う必要がある以下の手順について説明します。 これらの手順では、Retail バック オフィスが既に配置され、AX 2012 R3 環境が現在実行中であることを前提としています。

- **[Azure AD アカウントを設定](#set-up-azure-ad-accounts)** – このセクションでは、小売用バックオフィスに接続するために使用する N-1 コンポーネントの Microsoft Azure Active Directory (Azure AD) アカウントの設定方法について説明します。
- **[N-1コンポーネントを構成する](#configure-n-1-components)** – このセクションでは、小売用バックオフィスで N-1コンポーネントを構成する方法について説明します。
- **[N-1 コンポーネントのインストール](#install-n-1-components)** – このセクションでは既存の AX 2012 R3 環境で N-1 コンポーネントをダウンロードおよびインストールする方法について説明します。
- **[N-1 に切り替えるための切替手順](#cutover-steps-to-switch-to-n-1)** – このセクションでは、既存の AX 2012 R3 環境を AX 2012 R3 バックオフィスから Dynamics 365 小売用バックオフィスに切り替えるために、新しい N-1 コンポーネントを使用する方法について説明します。
- **[トラブルシューティングの手順](#troubleshooting-steps)** – このセクションでは、一般的な問題のトラブルシューティングの手順について説明します。
- **[N-1 に必要な KB](#required-kbs-for-n-1)** – このセクションでは、N-1 環境を設定するために必要な Microsoft サポート技術情報の記事番号 (KB) が一覧で表示されます。

### <a name="high-level-architecture"></a>高レベル アーキテクチャ
次の図は、N-1 手順の高レベル概要を示しています。

![段階的なロールアウト (N-1) アーキテクチャ](media/CDX/N-1/Overview.jpg)

## <a name="verify-that-the-n-1-license-key-is-turned-on"></a>N-1 ライセンス キーが有効であることを確認します。
コンフィギュレーションおよび N-1 コンポーネントのインストールを開始する前に、対応するライセンス キーが有効であることを確認してください。 このライセンス キーは、AX 2012 R3 から Microsoft Dynamics 365 for Retail へのアップグレード中に自動的にオンになります。 ただし、次の手順でこのキーが必要となるため、続行する前にオンになっていることを確認する必要があります。

1. 小売用バックオフィスにサインインし、**システム管理\>設定\>ライセンス コンフィギュレーション**に移動します。
2. **コンフィギュレーション キー** タブで、**小売**キーを展開し、**小売用スケジューラ**キーを展開し、**Retail Data Commerce Exchange 下位互換性**キーのチェック ボックスがオンであることを確認します。

    > [!NOTE]
    > キーがオンになっていない場合は、Microsoft サポートに問い合わせてオンにしてください。

## <a name="set-up-azure-ad-accounts"></a>Azure AD アカウントの設定
> [!IMPORTANT]
> 企業全体で高いレベルのセキュリティを維持するために、このインストールに新しいクライアント ID とシークレットを作成することを強くお勧めします。 このステップでは、新しい Web アプリが必要です。

1. Connector for Microsoft Dynamics AX のクライアント ID とシークレットを作成するために Azure Web App を生成します。 手順については、「[Azure Active Directory アプリケーションを作成する](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-service-principal-portal)」の「Azure Active Directory アプリケーションを作成する」セクションを参照してください。
2. 顧客 ID およびシークレットの作成が終了したら、顧客 ID を Retail で承諾する必要があります。 **システム管理 \> 設定 \> Azure Active Directory アプリケーション**の順に移動します。 クライアント ID を**クライアント ID** 列に入力し、説明のテキストを**名**列に入力、および **RetailServiceAccount** を**ユーザー ID** 列に入力します。

## <a name="configure-n-1-components"></a>N-1コンポーネントの構成
小売用バック オフィスで N-1 コンポーネントを構成するには、このセクションの手順に従います。

### <a name="connector-for-microsoft-dynamics-ax"></a>Connector for Microsoft Dynamics AX
1. 小売用バックオフィスにサインインし、**小売 \> 本社の設定 \> 小売用スケジューラ \> Connector for Microsoft Dynamics AX** に移動します。
2. アクション ウィンドウで、**新規**を選択し、次のフィールドを設定します。

    | 項 | フィールド | 説明 | サンプル値 |
    |---|---|---|---|
    | 表題 | プロファイル | 設定する N-1 プロファイルの固有の名前を入力します。 AX 2012 R3 Real-time Service が現在インストールされている環境/サーバーごとに、1 つのプロファイルを作成する必要があります。 | AXConnect |
    | 表題 | 説明 | プロファイルを識別するための説明テキストを入力します。 | AX2012 のコネクタ |
    | **接続** | サーバー | N-1 リアルタイム サービスがインストールされるサーバーの名前を入力します。 (このサーバーは、AX 2012 R3 Real-time Service が現在インストールされているサーバーと同一です。)。 | sampleserver.local |
    | **接続** | 港 | N-1 リアルタイム サービスが使用するポートを入力します。 | 8017 |
    | **接続** | Web アプリケーション名 | Microsoft インターネット インフォメーション サービス (IIS) の N-1 リアルタイム サービスに使用する名前を入力します。 | Real-timeServiceAX63 |
    | **接続** | プロトコル | AX 2012 R3 のリアルタイム サービスによって使用されているプロトコルを選択します。 | https |
    | **接続** | 共通名 | N-1 リアルタイム サービスが使用する証明書のフレンドリ名を入力します。 | samplecertificate.local |
    | **接続** | パスフレーズ | N-1 リアルタイム サービスで使用するパスフレーズを入力します。 | |
    | **接続** | 言語 | N-1 リアルタイム サービスにマップされているストアに関連付けられている言語を選択します。 | EN-US |

3. 完了したら、**保存** を選択します。

### <a name="retail-shared-parameters"></a>小売共有パラメーター
1. 小売用バックオフィスにサインインし、**小売\>本社の設定\>パラメーター\>小売共有パラメーター**に移動します。
2. **セキュリティ**タブで、次のフィールドを設定します。

    | フィールド | 説明 | サンプル値 |
    |---|---|---|
    | Real-time Service プロファイル | 前のセクションの **Connector for Microsoft Dynamics AX** ページで作成したプロファイルを選択します。 | AXConnect |
    | TS パスワードの暗号化名 | トランザクションのサービスに接続するために使用するアルゴリズムを入力します。 **SHA256** にこのフィールドを設定する必要があります。 | SHA256 | 
    | レガシ デバイス アルゴリズム | AX 2012 R3 デバイス アルゴリズムを入力します。 | AES |

### <a name="retail-scheduler-parameters"></a>小売用スケジューラのパラメーター
1. 小売用バックオフィスにサインインし、**小売\>本社の設定\>パラメーター\>小売用スケジューラのパラメーター**に移動します。
2. **HQ メッセージ データベース**クイック タブで、次のフィールドを設定します。

    | フィールド | 説明 | サンプル値 |
    |---|---|---|
    | SQL Server インスタンス名 | 既存の AX 2012 R3 HQ メッセージ データベースをホストする Microsoft SQL Server インスタンスの名前を入力します。 | sampleinstance |
    | サーバー名 | 既存の AX 2012 R3 HQ メッセージ データベースをホストするサーバーの名前を入力します。 | sampleserver |
    | データベース名 | AX 2012 R3 HQ メッセージ データベースの名前を入力します。 AX 2012 R3 では、既定の名前は **HQMessageDB** でした。 | HQMessageDB |

2. 完了したら、**保存** を選択します。

### <a name="working-folders"></a>作業フォルダー
> [!NOTE]
> ここに記載されているフィールドの値は、AX 2012 R3 から環境をアップグレードする際に、自動的に設定される既定値です。 ただし、それが正しいことを確認する必要があります。 AX 2012 R3 からアップグレードしていない環境で、これらの値を手動で入力する必要があります。

1. 小売用バックオフィスにサインインし、**小売\>本社の設定\>小売用スケジューラ\>作業フォルダー**に移動します。
2. グリッドで、次のフィールドの値が設定されていることを確認してください。

    | フィールド | 説明 | サンプル値 |
    |---|---|---|
    | 氏名 | 作業フォルダーの名前。 | N-1 のファイル ストレージ |
    | 説明 | 作業フォルダーの説明。 | N-1 のファイル ストレージ |
    | ダウンロード パス | AX 2012 R3 Commerce Data Exchange (CDX) ダウンロード パッケージを格納するネットワーク パス。 | \\\\sampleserver\\ダウンロード |
    | アップロード パス | AX 2012 R3 CDX がをアップロード パッケージを格納するネットワーク パス。 | \\\\sampleserver\\アップロード |

3. 完了したら、**保存** を選択します。

### <a name="channel-database-group"></a>チャネル データベース グループ
> [!NOTE]
> ここに記載されているフィールドの値は、AX 2012 R3 から環境をアップグレードする際に、自動的に設定される既定値です。 ただし、それが正しいことを確認する必要があります。 AX 2012 R3 からアップグレードしていない環境で、これらの値を手動で入力する必要があります。

1. 小売用バックオフィスにサインインし、**小売\>本社の設定\>小売用スケジューラ\>チャネル データベース グループ**に移動します。
2. AX 2012 R3 環境の各現物チャネル データベースについては、アクション ペインで**新規**を選択し、以下のフィールドを設定します。

    | 項 | フィールド | 説明 | サンプル値 |
    |---|---|---|---|
    | 表題 | 氏名 | AX 2012 R3 チャネル環境のために使用されるチャネル データベース グループの名前を入力します。 | 既定の\_AX63 |
    | 表題 | 説明 | AX 2012 R3 チャネル環境のために使用されるチャネル データベース グループの説明を入力します。 | AX63 チャネル データベースの既定のグループ |
    | **全般**クイック タブ | 小売チャネル スキーマ | AX 2012 R3 スキーマを選択します。 このフィールドは、**AX2012R3** に設定する必要があります。 | AX2012R3 |
    | **全般**クイック タブ | 作業フォルダー | CDX データ パッケージの同期に使用される作業フォルダー レコードへの参照を選択します。 前のセクションで、この作業フォルダーのレコードを作成しました。 | workingfolder |

3. 完了したら、**保存** を選択します。

### <a name="channel-database"></a>チャネル データベース
> [!NOTE]
> ここに記載されているフィールドの値は、AX 2012 R3 から環境をアップグレードする際に、自動的に設定される既定値です。 ただし、それが正しいことを確認する必要があります。 AX 2012 R3 からアップグレードしていない環境で、これらの値を手動で入力する必要があります。

1. 小売用バックオフィスにサインインし、**小売\>本社の設定\>小売用スケジューラ\>チャネル データベース**に移動します。
2. AX 2012 R3 環境の各現物チャネル データベースについては、アクション ペインで**新規**を選択し、以下のフィールドを設定します。

    | 項 | フィールド | 説明 | サンプル値 |
    |---|---|---|---|
    | 表題 | チャネル データベース ID | 現物の チャネル データベースの固有識別子を入力します。 この値は AX 2012 R3 環境から派生している必要があります。 | 既定の\_AX63\_データベース |
    | 表題 | チャネル データベース グループ | チャネル データベースがマップされているチャネル データベース グループを選択します。 この値は AX 2012 R3 環境から派生している必要があります。 | 既定の\_AX63\_DatabaseGroup |
    | 表題 | 型 | チャネル データベース レコードのタイプを選択します。 このフィールドは、**チャンネル データベース**に設定する必要があります。 | チャネル データベース |
    | 表題 | データ同期間隔 | CDX データの同期を実行する間隔を選択します。 **このフィールドは空白のままにする必要があります。** | |
    | 表題 | ユーザー名 (大文字と小文字を区別) | AX 2012 R3 チャネル データベースへの接続に使用するユーザー名を入力します。 | channeluser |
    | 表題 | パスワード | AX 2012 R3 チャネル データベースへの接続に使用するパスワードを入力します。 | *パスフレーズ* |
    | 表題 | データベース名 | AX 2012 R3 チャンネル データベースの名前を入力します。 | SampleChannelDB |
    | 表題 | サーバー名 | AX 2012 R3 チャネル データベースをホストするサーバーの名前を入力します。 | sampleserver |
    | **小売チャネル** クイック タブ | チャンネル | チャネル データベースにマップされている段階的なロールアウト (N-1) の小売チャネルのリストを追加するには、**追加**を選択します。 値は AX 2012 R3 環境から派生している必要があります。 | ロンドン |

3. 完了したら、**保存** を選択します。

### <a name="channel-profiles"></a>チャネル プロファイル
> [!IMPORTANT]
> このセクションは、既存の AX 2012 R3 環境が、チャンネル データベースとやり取りするために Retail サーバーを使用する場合にのみ適用されます。 AX 2012 R3 MPOS からダイレクト チャネル データベースへのアクセスが有効な場合は、この手順を省略できます。

> [!NOTE]
> ここに記載されているフィールドの値は、AX 2012 R3 から環境をアップグレードする際に、自動的に設定される既定値です。 ただし、それが正しいことを確認する必要があります。 AX 2012 R3 からアップグレードしていない環境で、これらの値を手動で入力する必要があります。

1. 小売用バックオフィスにサインインし、**小売\>チャネル\>小売店舗\>すべての小売店舗**に移動します。
2. N-1 環境でホストされている各 Retail サーバーについては、アクション ペインで**新規**を選択し、以下のフィールドを設定します。

    | 項 | フィールド | 説明 | サンプル値 |
    |---|---|---|---|
    | 表題 | 氏名 | 設定する N-1 チャネル プロファイルの固有の名前を入力します。 AX 2012 R3 Retail サーバーが現在インストールされている環境/サーバーごとに、1 つのプロファイルを作成する必要があります。 AX 2012 R3 Retail サーバーが現在インストールされている環境/サーバーごとに、1 つのプロファイルを作成する必要があります。 | 既定の\_AX63\_プロファイル |
    | **プロファイルのプロパティ** | プロパティ キー | AX 2012 R3 環境で使用される Retail サーバー URL のキーを入力します。 このフィールドは、**Retail サーバー URL** に設定する必要があります。 | Retail サーバー URL |
    | **プロファイルのプロパティ** | プロパティ値 | AX 2012 R3 環境で使用される Retail サーバー URL を入力します。 | `http://localhost"35080/RetailServer/V1` |
    | **プロファイルのプロパティ** | プロパティ キー | AX 2012 R3 環境で使用されるハードウェア ステーション URL のキーを入力します。 | Hardware Station URL |
    | **プロファイルのプロパティ** | プロパティ値 | AX 2012 R3 環境で使用されるハードウェア ステーション URL を入力します。 | ipc://localhost |

3. 完了したら、**保存** を選択します。

### <a name="all-retail-stores"></a>すべての小売店舗
> [!NOTE]
> Retail Headquarters 環境が AX 2012 R3 Headquarters から更新された場合、記載されているフィールド値は設定されます。

1. 小売用バックオフィスにサインインし、**小売\>チャネル\>小売店舗\>すべての小売店舗**に移動します。
2. N-1 環境にマップされている各ストアについては、小売チャネル ID を選択します。 次に、店舗詳細ページの、**一般**クイックタブで、次のフィールドを設定します。

    | フィールド | 説明 | サンプル値 |
    |---|---|---|
    | ライブ チャネル データベース | ストアをマップしたチャネル データベースを選択して、それ以前に設定します。 | 既定の\_AX63\_データベース |
    | チャネル プロファイル | ストアをマップしたチャネル プロファイルを選択し、前のセクションでそれを設定します。 | 既定の\_AX63\_プロファイル |

3. 完了したら、**保存** を選択します。

### <a name="initialize-the-ax-2012-retail-scheduler"></a>AX 2012 小売用スケジューラの初期化
1. 小売用バックオフィスにサインインし、**小売 \> 本社の設定 \> 小売用スケジューラ \> AX 2012 小売用スケジューラの初期化**に移動します。
2. **OK** を選択します。

### <a name="distribution-schedule"></a>配送スケジュール
> [!NOTE]
> Retail Headquarters 環境が AX 2012 R3 Headquarters から更新された場合、記載されているフィールド値は設定されます。

1. 小売用バックオフィスにサインインし、**小売\>小売 IT \>配送スケジュール**に移動します。
2. 左側のウィンドウで、接尾語 **AX63** のある配送スケジュールを選択します。 次に、**チャンネル データベース グループ**クイックタブで、先ほど作成したエントリが配送スケジュールにマップされているかどうかを確認します。

### <a name="workers"></a>作業者
> [!NOTE]
> Retail Headquarters 環境が AX 2012 R3 Headquarters から更新された場合、記載されているフィールド値は設定されます。

1. 小売用バックオフィスにサインインし、**小売\>従業員\>作業者**に移動します。
2. AX 2012 R3 環境にサインインする各作業者の名前を選択します。 次に、作業者の詳細ページの、**Retail** タブの、**Retail** クイックタブで、**パスワード**フィールドを設定します。

## <a name="install-n-1-components"></a>N-1 コンポーネントのインストール
Connector for Microsoft Dynamics AX インストーラーを実行する前に、次の要件が満たされていることを確認します。

- インストーラーでは、Microsoft .NET Framework バージョン 4.5.1 がシステムにインストールされている必要があります。
- インストーラーは、Connector for Microsoft Dynamics AX アプリケーションを次のオペレーティング システムにのみインストールします。 任意のコンポーネントをインストールする前に、オペレーティング システムに使用可能なすべてのサービス パックおよび更新プログラムを更新する必要があります。

    - Windows 7 Professional、Enterprise、または Ultimate エディション (x86 および x64 アーキテクチャの両方)。 Home エディションおよび埋め込みエディションはサポートされていません。
    - Windows 8.1 Update 1 Pro または Enterprise エディション (x86 および x64 アーキテクチャの両方)。 標準エディションはサポートされていません。
    - Windows 10 Pro または Enterprise エディション (x86 および x64 アーキテクチャの両方)。 Home エディションはサポートされていません。
    - Microsoft Windows Server 2012 R2 または Microsoft Windows Server 2016。

### <a name="async-server-connector-service"></a>非同期サーバー コネクタ サービス
インストーラーは、すべての前提条件が満たされていることを検証します。 これらの前提条件には、SQL Server のローカル インストールなどの SQL 前提条件、または SQL Command Line Utilities やその他の必要な SQL 接続インストールなどの別の前提条件が含まれています。

前提条件を満たすためには、接続されている SQL Server で全文検索が必要であり、最低でもトランスポート層セキュリティ (TLS) 1.2 がサポートされている必要があります。 Microsoft SQL Server 2012 では、最低でも、Service Pack 3 がインストールされる必要があります。 Microsoft SQL Server 2014 では、Service Pack 2 がインストールされている必要があります。

システムの再起動が必要な場合、インストーラーでこの要件が表示されます。 再起動することを推奨されていますが、インストーラーを使用せずに続行することができます。

準備ができたら、次の手順に従ってコンポーネントをダウンロードおよびインストールします。

1. 小売用バックオフィスにサインインし、**小売 \> 本社の設定 \> 小売用スケジューラ \> Connector for Microsoft Dynamics AX** に移動します。
2. 作成済みのコネクタを選択します。
3. アクション ウィンドウの**ダウンロード**タブで、**Async Server Connector service** を選択してインストーラー ファイルをダウンロードし、**Async Server Connector service** の下の**構成ファイル**を選択して、対応する構成ファイルをダウンロードします。 構成ファイルがインストーラー ファイルの横に保存されることを確認してください。
4. インストーラーおよび構成ファイルをダウンロード後、インストーラー ファイルをダブルクリックし、次の手順に従います。

    1. Application Object Server (AOS) URL (小売用バック オフィスへのアクセスに使用される URL) を確認し、**次へ** を選択します。
    2. 特定のユーザーが必要な場合は、サービスを実行するために必要なユーザー名とパスワードを入力します。 既定では、インストーラーは自動的に使用するサービス アカウントを生成します。 この方法は、安全性が向上しお勧めしますが、データベースが別のコンピューターにある場合は使用できません。 **次へ** を選択して続行します。
    3. アプリケーション ID (クライアント ID) および Connector for Microsoft Dynamics AX  インストールと関連するシークレットを入力します。
    4. **インストール**を選択します。

    > [!NOTE]
    > - クライアント ID およびシークレットを作成するため Azure Web アプリを正しく生成する方法の詳細については、「[Azure Active Directory アプリケーションを作成する](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-service-principal-portal)」で「Azure AD でアプリケーションを登録するための基本」セクションを参照してください。
    > - Web アプリを作成するとき、最初の URI と URL は特定の値である必要はありません。 作成されるアプリケーション ID (クライアント ID) とシークレットのみ重要です。

5. アプリケーション ID (クライアント ID) とシークレットが作成された後、アプリケーション ID は、小売で受け入れる必要があります。 **Retail \> バック オフィス設定 \> Azure Active Directoryアプリケーション**に移動します。 アプリケーション ID を**クライアント ID** 列に入力し、説明テキストを**名**列に入力、および **RetailServiceAccount** を**ユーザー ID** 列に入力します。
6. 小売用バックオフィスにサインインし、**小売\>本社の設定\>パラメーター\>小売共有パラメーター**に移動します。
7. **ID プロバイダー**タブで、**発行者**値で始まる `HTTPS://sts.windows.net/` プロバイダーを選択します。 選択に基づいて、**依存する関係者**クイックタブの値が自動的に設定されます。
8. **依存する関係者**クイック タブで、**追加**を選択します。 このインストールに作成された アプリケーション ID (クライアント ID) を入力します。 **Type** フィールドを **Public** に、**UserType** フィールドを **Worker** に設定します。 [アクション] ウィンドウで、**保存** を選択します。
9. アクション ウィンドウで、**保存**を選択します。

### <a name="n-1-real-time-service"></a>N-1 リアルタイム サービス
1. 小売用バックオフィスにサインインし、**小売 \> 本社の設定 \> 小売用スケジューラ \> Connector for Microsoft Dynamics AX** に移動します。
2. 作成済みのコネクタを選択します。
3. アクション ウィンドウの**ダウンロード**タブで、**Real-time service for Dynamics AX 2012 R3** を選択してインストーラー ファイルをダウンロードし、**Real-time service for Dynamics AX 2012 R3** の下の**構成ファイル**を選択して、対応する構成ファイルをダウンロードします。 構成ファイルが設定ファイルの横に保存されることを確認してください。
3. インストーラーおよび構成ファイルをダウンロード後、インストーラー ファイルをダブルクリックし、次の手順に従います。

    1. AOS URL (小売用バック オフィスへのアクセスに使用される URL) を確認し、**次へ** を選択します。
    2. HTTPS 通信に使用する有効な SSL 証明書を選択し、**次へ**を選択します。

        証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。 また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。 ローカル コンピューターの個人用証明書格納場所に保存する必要があります。

    3. 特定のユーザーが必要な場合は、アプリケーション プールを実行するために必要なユーザー名とパスワードを入力します。 既定では、インストーラーは自動的に使用するサービス アカウントを生成します。 この方法は、安全性が向上しお勧めしますが、データベースが別のコンピューターにある場合は使用できません。 **次へ** を選択して続行します。
    4. 使用する必要のある HTTPS ポートを確認し、コンピューターのホスト名が正しいことを確認します。 **次へ** を選択して続行します。

        HTTPS ポートは、店舗システムのプロファイルに一覧表示されます。 店舗システム プロファイルにアクセスするには、**小売店舗詳細** ページの **店舗システム** FastTabで、選択した店舗システムのプロファイル ID を選択します。 インストーラーは自動的にホスト名を入力します。 何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更します。 ホスト名はシステムの完全修飾ドメイン名 (FQDN) でなければなりません。また、このトピックの前半にある **Connector for Microsoft Dynamics AX** ページに入力した値と一致する必要があります。

    5. アプリケーション ID (クライアント ID) および Connector for Microsoft Dynamics AX  インストールと関連するシークレットを入力します。 その後、**インストール** を選択します。

        このアプリケーション ID とシークレットは、Async Server Connector service のインストールで使用したのと同じアプリケーション ID とシークレットにできます。 クライアント ID およびシークレットを作成するため Azure Web アプリを正しく生成する方法の詳細については、「[Azure Active Directory アプリケーションを作成する](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-service-principal-portal)」で「Azure AD でアプリケーションを登録するための基本」セクションを参照してください。 Web アプリを作成するとき、最初の URI と URL は特定の値である必要はありません。 作成されるアプリケーション ID (クライアント ID) とシークレットのみ重要です。

## <a name="cutover-steps-to-switch-to-n-1"></a>N-1に切り替えるための切替手順
ここでは、既存の AX 2012 R3 チャンネル環境を AX 2012 R3 バックオフィスから Dynamics 365 Retail バックオフィスに切り替えるための、推奨される詳細な手順を説明します。 これらの手順は一般的なものです。 特定のビジネスまたは技術面の要件に対応するためには、さまざまな実装がこれらの手順から逸脱する必要がある可能性があります。

### <a name="prerequisites"></a>前提条件
切り替えの環境を準備するのにはこれらの手順に従います。

| ステップ | 詳細情報 | タイムライン |
|---|---|---|
| 1. 小売用バックオフィスを配置します。 | 小売用バックオフィスを稼働します。 Microsoft Dynamics 365 for Retail クラウド POS (CPOS) は、環境内の機能を検証するために使用できます。 | 切替前の数週間または数か月 |
| 2. Microsoft Dynamics 365 for Retail アプリケーション (X++) KB をインストールします。 | N-1 に関連するすべての問題が解決されていることを確認するには、[N-1 に必要な KB](#required-kbs-for-n-1) セクションに記載されている KB をインストールします。 | 切替前の数週間または数か月 |
| 3. Azure AD アカウントを設定します。 | [Set up Azure AD アカウントの設定](#set-up-azure-ad-accounts) セクションの指示に従い、N-1 コンポーネントに必要なアカウントを作成し、小売用バックオフィスに対して認証します。 | 切替前の数週間または数か月 |
| 4. 小売用バックオフィスのコンフィギュレーション | [N-1 コンポーネントを構成する](#configure-n-1-components) セクションの指示に従い、N-1 コンポーネントをインストールする前にすべての設定を構成します。 | 切替前の数週間または数か月 |
| 5. N-1 コンポーネントのインストール。 | [N-1 コンポーネントのインストール](#install-n-1-components) セクションの指示に従い、N-1 コンポーネントをインストールします。 N-1 Async Server Connector Service コンポーネントはインストールする必要がありますが、AX 2012 R3 と Dynamics 365 CDX パッケージが混在しないようにするには、すぐに無効にする必要があることに注意してください。 | 切替前の数週間または数か月 |

### <a name="preparation"></a>準備
切り替えがスケジュールされる数日前に、これらの手順に従って準備します。

| ステップ | 詳細情報 | タイムライン | この手順を実行されたことを検証する方法 |
|---|---|---|---|
| 1. AX 2012 R3 のすべてのダウンロード ジョブを停止します。 | AX2012 R3 のバック オフィスですべての AX 2012 R3 ダウンロード ジョブが停止していることを確認してください。 | 切替前に少なくとも数日間 | アップロード ジョブの AX 2012 R3 ネットワーク共有内のすべてのパッケージが処理され、新たに表示されるパッケージはありません。 |
| 2. 小売用バックオフィスですべての **AX63** CDX ダウンロード ジョブを完全に同期させます。 | CXD ダウンロード ジョブを実行してパッケージが生成され、Azure Blob storage の Blob に削除されていることを確認し、N-1 非同期サーバー コネクタ サービスが切替中にそれらを使用できるようにします。 | 切替前に少なくとも数日間 | CDX ダウンロード ジョブは、小売用バックオフィス内の**ダウンロード セッション**にて**利用可能**になります。 |

### <a name="cutover-steps"></a>切替手順
切替プロセスを行うには、これらの手順に従います。

| ステップ | 詳細情報 | タイムライン | この手順を実行されたことを検証する方法 |
|---|---|---|---|
| 1. すべてのシフトを閉じます。 | すべてのシフトがクローズしていることを確認してください。 | ストア終了後 | シフトがクローズしているストアを手動で検証します。 |
| 2. 中断されたトランザクションをすべてクリーンアップします。 | 中断されたすべてのトランザクションがクリーンアップされることを確認してください。 | 前の手順の後 | シフトがクローズしているストアを手動で検証します。 |
| 3. トランザクションのすべてのデータを同期します。 | すべてのトランザクション データが CDX アップロード ジョブによって AX 2012 R3 バックオフィスに同期されていることを確認してください。 | 前の手順の後 | アップロード ジョブの AX 2012 R3 ネットワーク共有内のすべてのパッケージが処理され、新たに表示されるパッケージはありません。 |
| 4. AX 2012 R3 CDX のアップロード ジョブを無効にします。 | すべての AX 2012 R3 アップロード ジョブが無効になっていることを確認して、パッケージがもう集荷されないようにしてください。 | 前の手順の後 | AX 2012 R3 バックオフィスの UI を通じて、CDX アップロード ジョブが無効になっていることを手動で検証します。 |
| 5. AX 2012 R3 のリアルタイム サービスをシャット ダウンします。 | AX 2012 R3 のリアルタイム サービスをホストするサーバーに接続し、IIS を起動し、AX 2012 R3 のリアルタイム サービスを右クリックしてサービスを停止します。 | 前の手順の後 | サービスが停止していることを IIS で手動で検証します。 |
| 6. **メタデータ同期のリセット** コマンドを小売用バックオフィスで実行します。 | Microsoft Dynamics AX では、**Retail \> 本社の設定 \> 小売用スケジューラ \> Connector for Microsoft Dynamics AX** に移動し、**メタデータ同期のリセット**を選択して N-1 の切替のために AX 2012 R3 環境内の **HQMessageDB** データベースをリセットします。 | 前の手順の後 | 該当なし |
| 7. N-1 非同期サーバー コネクタ サービスを有効にします。 | N-1 Async Server Connector Service をホストするサーバーに接続し、Microsoft Windows サービスを有効にします。 | 前の手順の後 | **利用可能**から**適用済**までの Retail バックオフィス変更の**ダウンロード セッション**ページのダウンロード ジョブの状態。 |

次の図は、これらの手順のビジュアル表示です。

![段階的なロールアウト (N-1) アーキテクチャの概要](media/CDX/N-1/Cutover.jpg)

## <a name="troubleshooting-steps"></a>トラブルシューティングの手順
このセクションでは、発生する可能性があるいくつかの一般的な問題と、調査、または回復する手順について説明します。

### <a name="runtime"></a>ランタイム
このセクションでは、アプリケーションの実行時に発生する可能性のあるエラーの、トラブルシューティングの手順について説明します。

#### <a name="metadata-synchronization-fails"></a>メタデータ同期に失敗
| フィールド | 先頭値 |
|---|---|
| イベント ログ | Microsoft-Dynamics-Commerce-AsyncServerConnectorService/操作 |
| サンプル イベント ログのエラー メッセージ | 非同期サーバー コネクタ サービスで、ダウンロード タイマーのティックにエラーが発生しました。 CorrelationId {4c9cd9a0-d4e3-43e5-80da-59ea2eb01acf}; エラーの詳細 : Microsoft.Dynamics.Retail.AsyncServerConnector.Service.Exceptions.SyncMetadataException: メタデータの同期が失敗しました。 ---\> Microsoft.Dynamics.Retail.AsyncServerConnector.Service.Exceptions.MessageDBOperationException: HQ メッセージ DB のメタデータを更新できませんでした。 ---\> System.Data.SqlClient.SqlException: 接続がサーバーで正常に確立されましたが、ログイン プロセス時にエラーが発生しました。 (プロバイダー: SSL プロバイダー、エラー: 0 - 証明書チェーンは信頼されていない機関によって発行されました。)---\>System.ComponentModel.Win32Exception: 証明書チェーンは、信頼されていない機関によって発行されました |
| トラブルシューティングの手順 | これは、Synch サービスの web.config 接続文字列が TrustServerCertificate を false に設定しているために発生した可能性があります。 問題を解決するには、Sync サービスの Web サイトを参照して、web.config を開きます。ConnectionStrings セクションを検索して、TrustServerCertificate が false の場合は、true に更新します。 |

#### <a name="metadata-synchronization-fails"></a>メタデータ同期に失敗
| フィールド | 先頭値 |
|---|---|
| イベント ログ | Microsoft-Dynamics-Commerce-AsyncServerConnectorService/操作 |
| サンプル イベント ログのエラー メッセージ | 非同期サーバー コネクタ サービスで、ダウンロード タイマーのティックにエラーが発生しました。 CorrelationId {73d9d0d3-4d12-42ca-ac65-3f1f947c7840}; エラーの詳細 : Microsoft.Dynamics.Retail.AsyncServerConnector.Service.Exceptions.SyncMetadataException: メタデータの同期が失敗しました。 ---\> Microsoft.Dynamics.Retail.AsyncServerConnector.Service.Exceptions.MessageDBOperationException: HQ メッセージ DB のメタデータを更新できませんでした。 ---\> System.Data.SqlClient.SqlException: ログインによって要求されたデータベース「HQMessageDB」を開くことができません。 ログインに失敗しました。 ユーザー「localhost\\RetailAsUser」のログインが失敗しました。 |
| トラブルシューティングの手順 | これは、非同期サーバー コネクタ サービスを実行するユーザーに HQ メッセージ データ ベースへのアクセス権がないために発生した可能性があります。 問題を解決するには、services.msc を実行して、非同期サーバー コネクタ サービスを実行しているユーザーを確認します。 SQL で HQ メッセージ データベースにこのユーザー アクセスを提供します。 |

#### <a name="metadata-synchronization-fails-or-cdx-jobs-are-successfully-downloaded-but-arent-applied"></a>メタデータの同期が失敗した場合、または、CDX ジョブが正常にダウンロードされたが、適用されない場合
| フィールド | 金額 |
|---|---|
| イベント ログ | Microsoft Dynamics AX Retail : Async Client SynchClientService |
| サンプル イベント ログのエラー メッセージ | サーバーと通信してダウンロードすることができません。 ユーザー名/パスワード、サーバーおよびデータベース接続を確認してください。 エラーの詳細: System.ServiceModel.CommunicationException: `https://localhost:44300/SynchService/DownloadService.svc` への HTTP 要求中にエラーが発生しました。 HTTPS の場合、サーバー証明書が HTTP.SYS で正しくコンフィギュレーションされていない可能性があります。 これは、クライアントとサーバー間のセキュリティ バインドの不一致によっても発生する可能性があります。 ---\> System.Net.WebException: 基礎的な接続が閉じられました: 送信時に予期しないエラーが発生しました。 ---\> System.IO.IOException: リモート側がトランスポート ストリームを閉じたため、認証に失敗しました。 |
| トラブルシューティングの手順 | 次の理由で発生した可能性があります。<br>1) 非同期クライアントで提供するユーザー ID とパスワードが、AX で提供されているチャネル データベースのユーザー ID とパスワードと一致しません。<br>2) 非同期サービスのエンド ポイントに到達できません。 `https://localhost:44300/SynchService/DownloadService.svc`。 この問題を解決するには、1) 非同期クライアントのインストール場所から、非同期のクライアント構成ユーティリティ (AsyncClientConfigurationUtility.exe) を起動します。 `Async Server connection tab -> Authentication information (case sensitive)` の下で -> AX の N-1 チャンネル データベースで提供される値に従って、チャンネル データベース ID、 ユーザー ネームおよびパスワード フィールドをアップデートしてください (`Retail -> Headquarters setup -> Channel database`)。 2) ユーティリティの `Test connection` をクリックします。 接続が成功した場合は、Async Client サービスを再起動します。 接続に失敗した場合は、AX の N-1 チャネル データベース (`Retail -> Headquarters setup -> Channel database`) に移動し、ユーザ名およびパスワードを更新して、保存します。 AX で `Retail scheduler parameters` に移動し、`Reset metadata synchronization` をクリックします。 これにより、新しい値を使用して HQ メッセージ データベースが設定されます。 手順 1 をもう一度繰り返します。 3) 非同期サーバーのエンド ポイント (`https://localhost:44300/SynchService/DownloadService.svc`) に到達できない場合、サービスのバインディングをチェックし、関連する証明書があることを確認してください。 それでも問題が解決しない場合は、`AX2012R3` の 小売チャネル スキーマにリンクされたすべてのチャネル データベース グループに対して `Working folders` が指定されていることを確認してください。 |

#### <a name="cdx-jobs-are-successfully-downloaded-but-arent-applied"></a>CDX ジョブが正常にダウンロードされますが、適用されません。
| フィールド | 金額 |
|---|---|
| イベント ログ | Microsoft Dynamics AX Retail : Async Client SynchClientService |
| サンプル イベント ログのエラー メッセージ | DownloadAgent.Execute 中の例外です。 エラーの詳細: System.IO.FileNotFoundException: ファイルまたはアセンブリ「Microsoft.Dynamics.Retail.StoreConnect.Request.Base, Version=6.3.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35」またはその依存関係のうちのいずれか 1 つを読み込めませんでした。 システムでは、指定したファイルが見つかりません。 ファイル名: 「Microsoft.Dynamics.Retail.StoreConnect.Request.Base, Version=6.3.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35」at Microsoft.Dynamics.Retail.SynchClient.Core.DownloadAgent.ApplySessionFileToClientDatabase(SessionManager sessionMgr, String fileName) at Microsoft.Dynamics.Retail.SynchClient.Core.DownloadAgent.ProcessDownloadSession(DownloadSession session) at Microsoft.Dynamics.Retail.SynchClient.Core.DownloadAgent.Execute() |
| トラブルシューティングの手順 | これは、AX63 ストア接続コンポーネントが環境にインストールされていないために発生した可能性があります。 問題を解決するには、非同期のクライアント コンポーネントを実行している環境で AX63 ストア接続コンポーネントをインストールします。 |

#### <a name="n-1-async-server-connector-service-communication-exception"></a>N-1 非同期サーバー コネクタ サービスの通信例外
| フィールド | 金額 |
|---|---|
| イベント ログ | Microsoft Dynamics AX Retail : Async Client SynchClientService |
| サンプル イベント ログのエラー メッセージ | サーバーと通信してダウンロードすることができません。 ユーザー名/パスワード、サーバーおよびデータベース接続を確認してください。 エラーの詳細: System.ServiceModel.CommunicationException: `https://localhost:44300/SynchService/DownloadService.svc` への HTTP 要求中にエラーが発生しました。 HTTPS の場合、サーバー証明書が HTTP.SYS で正しくコンフィギュレーションされていない可能性があります。 これは、クライアントとサーバー間のセキュリティ バインドの不一致によっても発生する可能性があります。 ---\> System.Net.WebException: 基礎的な接続が閉じられました: 送信時に予期しないエラーが発生しました。 ---\> System.IO.IOException: リモート側がトランスポート ストリームを閉じたため、認証に失敗しました。 |
| トラブルシューティングの手順 | HQ メッセージ DB にデータがあることを確認してください。 接続が成功したことを検証するために、asyncClient コンフィギュレーション ツールを使用します。 |

#### <a name="ax-2012-r3-mpos-activation-fails-with-an-error-on-step-1"></a>AX 2012 R3 MPOS のライセンス認証は、ステップ 1 でエラーで失敗します。
| フィールド | 金額 |
|---|---|
| イベント ログ | Microsoft Dynamics AX Retail : Retail サーバー RetailServer |
| サンプル イベント ログのエラー メッセージ | Microsoft.Dynamics.Commerce.Runtime.UserAuthenticationException: ログオン時にエラーが発生しました。 ---\> Microsoft.Dynamics.Commerce.Runtime.ConfigurationException: ローカル データベースで公開済チャネルが見つかりません。 少なくとも 1 つの小売チャネルが、AX を通じてこの DB に公開されていることを確認してください。 |
| 有効化場面上での MPOS エラー | DA1002: ユーザーがログオンできないサーバー側エラーが発生しました。 サーバー ログで詳細を確認するか、IT サポートにお問い合わせください。 |
| トラブルシューティングの手順 | CDX ダウンロード ジョブが正常に実行され、チャネルのデータベースにデータが含まれていることを確認してください。 |

#### <a name="ax-2012-r3-mpos-activation-fails-with-an-error-on-step-2"></a>AX 2012 R3 MPOS のライセンス認証は、ステップ 2 でエラーで失敗します。
| フィールド | 金額 |
|---|---|
| イベント ログ | Microsoft Dynamics Retail Modern POS |
| サンプル イベント ログのエラー メッセージ | Dynamics- エラー: LoginViewModel ActivateDevice のログオンに失敗しました。 ErrorMessage: ; ErrorCode: Microsoft\_Dynamics\_Commerce\_Runtime\_HeadquarterTransactionServiceMethodCallFailure; |
| 有効化場面上での MPOS エラー | DA2001 |
| トラブルシューティングの手順 | 有効化しようとしているデバイスは、既に有効になっています。 デバイスを無効にして、有効化を試みてください。 |

#### <a name="ax-2012-r3-mpos-activation-fails-with-an-error-on-step-2"></a>AX 2012 R3 MPOS のライセンス認証は、ステップ 2 でエラーで失敗します。
| フィールド | 金額 |
|---|---|
| サンプル イベント ログのエラー メッセージ | 例外が発生しました: [2018/04/19 19 時 26 分 51 秒] Microsoft.Dynamics.Commerce.Runtime.UserAuthenticationException: ログオン時にエラーが発生しました。 ---\> Microsoft.Dynamics.Commerce.Runtime.StorageException: データベースからの読み取りに失敗しました。 詳細については、内部例外を参照してください。 DatabaseErrorCode: 0 ---\> Microsoft.Dynamics.Commerce.Runtime.Data.DatabaseException: 無効なオブジェクト名 'crt.EMPLOYEEPERMISSIONSVIEW' です。 ---\> System.Data.SqlClient.SqlException: 'crt.EMPLOYEEPERMISSIONSVIEW' は無効なオブジェクト名です。 at System.Data.SqlClient.SqlConnection.OnError(SqlException exception, Boolean breakConnection, Action'1 wrapCloseInAction) at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj, Boolean callerHasConnectionLock, Boolean asyncClose) |
| 有効化場面上での MPOS エラー | DZ1001 |
| トラブルシューティングの手順 | 有効化しようとしているデバイスは、既に有効になっています。 デバイスを無効にして、有効化を試みてください。 |

#### <a name="ax-2012-r3-mpos-activation-fails-with-an-error-on-step-9"></a>AX 2012 R3 MPOS のライセンス認証は、ステップ 9 でエラーで失敗します。
| フィールド | 金額 |
|---|---|
| イベント ログ | Microsoft Dynamics Retail Modern POS |
| サンプル イベント ログのエラー メッセージ | Dynamics- エラー: LoginViewModel ActivateDevice のログオンに失敗しました。 ErrorMessage: デバイスでの暗号化に問題が発生しました。 システム管理者に連絡してください。; ErrorCode:MICROSOFT\_DYNAMICS\_POS\_DATAENCRYPTIONERROR; |
| 有効化場面上での MPOS エラー | DA3122: デバイスでの暗号化に問題が発生しました。 システム管理者に連絡してください。 |
| トラブルシューティングの手順 | ストアの CDX 下位互換性セクションで、リアル タイム サービス プロファイル フィールドを確認してください。 これは、N-1 用に作成した RTS プロファイルに設定する必要があります。 |

## <a name="required-kbs-for-n-1"></a>N-1 に必要な KB
次の図では、正常に動作するために N-1 を必要とする全ての KB を表しています。

### <a name="dynamics-365-for-retail--microsoft-dynamics-365-72-headquarters"></a>Dynamics 365 for Retail – Microsoft Dynamics 365 7.2 バック オフィス
| KB 番号 | 肩書き |
|---|---|
| 4095190 | 顧客が 6.3 から D365 にデータを移動するための公式アップグレード プロセスに従わなかった場合に N-1 機能を有効化するのに必要なため、RetailSharedParameters フォームの RetailSharedParameter の TransactionServiceProfileID を公開します。 |
| 4095192 | 顧客が AX6.3 から D365 にデータを移動するための公式アップグレード プロセスに従わなかった場合に N-1 機能を有効化するのに必要なため、RetailSharedParameters フォームの RetailSharedParameter の TSPasswordEncryption フィールドを公開します。 |
| 4095209 | Real-timeServiceAX63 N-1 コンポーネントの Webconfig では、無効な認証タイプ名が含まれています。 これは、コンポーネントがトランザクション サービスを D365 で認証しようとする時に問題の原因になります |
| 4095189 | RetialTransactionServiceProfile テーブルのプロトコル列が、新しいバージョンの D365 AX データベースから古いバージョンのチャネル データベースに同期されていません。 |
| 4095191 | セキュリティ保護された URL のみが許可されるため、ユーザーが Retail サーバー USRL を http ベースの URL に設定する事は許可されていません。 これは、ユーザーが backwardcompatiility モードで実行中に古いバージョン (6.3) の Retail サーバーに接続することを防ぎます。 |
| 4132456 | \[アップグレード \& N-1\]\[デザイナー\] テンキーの高さを拡張する必要があります |
| 4095926 | アップグレード \& N-1: N-1 非アップグレード環境でトランザクションが見つからないため、返品注文は 63MPOS から失敗します。 |
| 4095664 | 新しい顧客を作成するために Microsoft Dynamics AX 2012 クライアントが AX7.2 HQ へ接続することを許可します。 |
| 4132454 | \_AX63 サブジョブによって重複したレコードの例外が原因で N-1 バージョンの 1070 が失敗する |
| 4131243 | D365 を N-1 の下位互換性で実行している場合、ユーザーは AX クライアントを使用して HardwareStationURL を設定できないため、6.3 ハードウェア ステーションを正しく設定できないことがあります。 |
| 4338120 | 非同期サービス コネクタ インストーラは、ユーザーが提供した HQ メッセージ データベース名に関係なく、常に既定の名前を使用する代わりに、提供された HQ メッセージ DB 名を使用する必要があります。 |
| 4337834 | D365 を N-1 の下位互換性で実行している場合、RetailTransactionService でメソッドが見つからないために MPOS から顧客を追加または更新している間に N-1 (6.3) バージョン MPOS が失敗することがあります。 |
| 4337864 | D365 を N-1 の下位互換性で実行している場合、ハードウェア プロファイル支払商社プロパティをロードまたは使用しようとすると、ログインまたは支払中に N-1 (6.3) バージョン MPOS が失敗することがあります。 |
| 4132453 | 6.3 バージョンのチャネル データベースの InventDim テーブルにデータを移動すると、製品ダウンロード ジョブの N-1 バージョン (1040\_AX63) の実行に失敗 |
| 4206905 | POS レポートは、アップグレードされていない N-1 環境で実行するとエラーをスローします。 |
| 4133289 | 製品の N-1 version の実行 - 仕訳帳または既存のトランザクションからの払戻に失敗 |
| 4161086 | CDX テーブル配送は、ルート テーブル ノードに追加された 'FieldValue' リンク タイプを無視するため、テーブルのフィルター処理にその情報を使用せず、提供された条件 (x++ 修正) を使用します。 |
| 4161099 | CDX テーブル配送は、ルート テーブル ノードに追加された 'FieldValue' リンク タイプを無視するため、テーブルのフィルター処理にその情報を使用せず、提供された条件 (バイナリ変更) を使用します。 |
