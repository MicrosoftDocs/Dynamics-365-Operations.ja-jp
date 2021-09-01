---
title: AX 2009 の移行 － データ移行ツールのインストール
description: このトピックでは、Microsoft Dynamics AX 2009 からデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。
author: kfend
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 2de55922a17058aae8f2bcc9e4774affc45a66d2eb22dca8b01e979b99aca476
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775256"
---
# <a name="ax-2009-migration--install-the-data-migration-tool"></a>AX 2009 の移行 – データ移行ツールのインストール

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2009 から Finance and Operations にデータを移行できるように、データ移行ツール (DMT) を設定する方法について説明します。 

> [!IMPORTANT]
> 現時点で、DMT はプライベート プレビューです。 関心をお持ちの場合、[プレビュー プログラム](https://microsoft.qualtrics.com/jfe/form/SV_brOLCioQ7mmeykB)にサインアップすることができます。 DMT の公開リリース日は設定されていません。 

## <a name="prerequisites"></a>必要条件

- Microsoft SQL Server 2008/2012/2014/2016。
- Microsoft .NET Framework バージョン 4.5 またはそれ以降。
- Microsoft SQL 2012 Native Client がインストールされている Microsoft SQL Server コンピューター。
- Microsoft SQL Server Integration Services (SSIS) サービスがインストールされ、DMT サービスがインストールされるコンピューターで実行されています。
- SQL Server 認証は、SQL 認証と Microsoft Windows 認証の両方をサポートする必要があります。
- 次の表のバージョン ガイダンスに従っている Microsoft Access データベース エンジン。

    | Office バージョン                    | SQL Server 2008                 | SQL Server 2012 以降 |
    |-----------------------------------|---------------------------------|---------------------------|
    | **VM に Microsoft Office がない** | Access エンジン 32 ビット            | Access エンジン 64 ビット      |
    | **Microsoft Office 32 ビット**       | Access エンジン 32 ビット            | Access エンジン 64 ビット      |
    | **Microsoft Office 64 ビット**       | Access エンジン 32 ビットおよび 64 ビット | Access エンジン 64 ビット      |

- Microsoft Dynamics AX 2009 SP1 5.0.1000.52 以降。
- 前提条件となる修正プログラム (axpatch.exe) がインストールされている。 修正プログラムを見つけるには、ZIP ファイルをダウンロードして抽出した場所から、<pre-requisiteforpatch\>\<application\> に移動します。

## <a name="install-dixf-service"></a>DIXF サービスのインストール

1. ZIP ファイルを展開した場所に移動し、**DIXF msi** フォルダーで **DIXF\_Service\_x64.msi** を右クリックし、**実行** を選択します。
2. ウィザードが開始したら、**次へ** を選択します。
3. ライセンス条項を受け入れ、**次へ** を選択します。
4. サービスのアカウントを選択し、**次へ** を選択します。 アカウントは、管理者権限を持っている必要があります。 **ネットワーク サービス** チェック ボックスをオンにした場合、ネットワーク サービス アカウントに管理者権限があることを確認します。 それ以外の場合、チェック ボックスをオフにし、管理者アカウントのユーザー名とパスワードを入力します。 その後、**次へ** を選択します。
5. SQL Server のバージョンを選択し、**次へ** を選択します。
6. **インストール** を選択し、ウィザードが完了したら **完了** を選択します。

## <a name="copy-binaries"></a>バイナリのコピー
ZIP ファイルを展開した場所に移動し、以下のファイルを **Program Files (x86)\\Microsoft Dynamics AX\\50\\Client\\Bin** フォルダーにコピーします。

- Microsoft.Dynamics.AX.Framework.Tools.DMT.dll
- Interop.Shell32.dll

## <a name="install-dmt-components-for-ax-2009"></a>AX 2009 の DMT コンポーネントのインストール
DMT をインストールする方法は 2 つあります。 結合された XPO ファイルまたはアプリケーション修正プログラムを使用することができます。 Microsoft Dynamics Lifecycle Services (LCS) 実装プロジェクトを使用している場合、アプリケーション修正プログラムを使用します。 インストールには、約 7 時間かかります。

### <a name="combined-xpo-file"></a>結合された XPO ファイル
1. 結合された XPO ファイルを **DMT_V1.0\CombinedXPO** から展開します。
2. AX 2009 に結合された XPO ファイルをインポートします。
3. **DMT_V1.0\Label file** ファイルから  **Program Files\\Microsoft Dynamics AX\\50\\Application\\Appl\\<NameOfYourDeployment\>** フォルダーにラベル ファイルをコピーします。
4. Application Object Server (AOS) インスタンスを再起動します。
5. AX 2009 で、**データ移行** \> **設定** \> **DMT アプリケーションのコンパイルと同期** を選択します。

ユーザーがログインしているレイヤーに結合された XPO ファイルがインポートされることに注意してください。

### <a name="application-hotfix"></a>アプリケーションの修正プログラム
1. **DMT_V1.0\\ApplicationHotfix\\DynamicsAX2009-KB4010403-SP1** に移動し、**setup.exe** を右クリックして **実行** を選択します。
2. AX 2009 のアプリケーション オブジェクト ツリー (AOT) で、**LegalEntityId** フィールドが **DMTCustomerAddressView** ビューと **DMTVendorAddressView** ビューに追加されていることに注目してください。
3. **データ移行** \> **設定** \> **DMT アプリケーションのコンパイルと同期** を選択します。

## <a name="parameter-setup"></a>パラメータの設定
ZIP ファイルを展開した場所に移動し、**defaultvalue.xlsx** を検索します。

> [!NOTE]
> ファイルは .xlsx 形式に保存されます。 拡張機能を変更しないでください。 このファイルを **既定のコンフィギュレーション** パラメーターの入力として入力したら、**すべてのファイル** を選択して .xlsx 形式を選択できるようにします。 この形式を選択しない場合、マッピングの生成を開始するとエラーが発生します。

1. AX 2009 で、**データ移行** \> **設定** \> **既定のマップを構成する** を選択し、次のフィールドに適切な情報を入力します。

    - **既定のコンフィギュレーション**: Microsoft Excel ファイルのパスを入力します。
    - **エクスポート ファイルのパス**: サービスがアクセスできるサーバーのパスを入力します。
    - **SQL Server のユーザー名とパスワード**: AX 2009 データベースの SQL 認証資格情報を入力します。

2. フォームを閉じます。
3. **設定** で、**接続の構成** を選択し、次のフィールドに適切な情報を入力します。

    - **DIXF サービス ホスト**: DIXF サービスのインストールのホスト名を入力します。
    - **テナント URL** – アプリケーション テナントの URL を入力します。 テナントが不明な場合は、Finance and Operations アプリケーションの web.config ファイルを参照してください。

    > [!注意} Azure ポータルでは、Azure Active Directory (AAD) で新しいアプリケーションを作成するときは、2 つのオプションから選択できます。 **Web API** と **ネイティブ**。 このインスタンスでは、**ネイティブ** を選択し、ネイティブ AAD アプリケーションへのアクセス許可を付与します。

## <a name="multi-box-setup"></a>マルチボックスの設定
マルチボックスの設定の場合、次のコンピューターが必要です。

- AX 2009 データベースおよび DIXF サービスがインストールされているコンピューター A
- AX 2009 AOS インスタンスがインストールされているコンピューター B
- AX 2009 クライアントがインストールされているコンピューター C

この 3 コンピューター設定では、コンピューター C はコンピューター B の AOS インスタンスに接続するように構成されています。コンピューター B は、コンピューター A で構成されているデータベースに接続されます。

### <a name="dixf-service-machine-prerequisites-machine-a"></a>DIXF サービス コンピューターの前提条件 (コンピューター A)
コンピューター A の DIXF サービスには、次の前提条件があります。

- SQL Server 2008/2012/2014
- .NET Framework バージョン 4.5
- Access データベース エンジン

    - **SQL Server 2008 の場合:** Access エンジン 32 ビットおよび 64 ビット (Microsoft Excel が 64 ビットの場合)
    - **SQL Server 2012 以降の場合:** Access エンジン 64 ビット

- AX 2009 データベース (SQL Server で構成)

### <a name="aos-machine-prerequisites-machine-b"></a>AOS コンピューターの前提条件 (コンピューター B)
コンピューター B の AOS のインストールには、次の前提条件があります。

- AX 2009 AOS サーバー
- アプリケーション ファイル

### <a name="client-machine-prerequisites-machine-c"></a>クライアント コンピューターの前提条件 (コンピューター C)
コンピューター C のクライアントのインストールには、次の前提条件があります。

- AX 2009 クライアント

### <a name="shared-folder-permissions"></a>共有フォルダーのアクセス許可

既定のコンフィギュレーション ファイルとエクスポート パッケージ ファイルのパスは共有する必要があり、クライアント ユーザーおよび DIXF サービスにはこれらのファイルへの読み取り/書き込みアクセスが必要です。 アクセス権を付与するには、**データ移行** \> **設定** \> **マップの構成と生成** を選択し、**パスの検証** を選択して必要なアクセス権があることを確認します。

### <a name="set-up-parameters"></a>パラメータの設定

1. **データ移行** \> **設定** \> **接続の構成** を選択します。
2. **DIXF サービス ホスト** フィールドに、DIXF サービスがインストールされているリモート コンピューターの名前を入力します。 既定では、名前は **localhost** です。
3. **検証** を選択し、クライアントが DIXF サービスにアクセスできることを検証します。

### <a name="workarounds"></a>回避策
"DIXF サービスを利用できません" というエラー メッセージが表示される場合、次の回避方法を実行してポート 7000 のサービスの接続を有効にします。

1. ポート 7000 を開いた後、DMT サービス コンピューターの受信ルールで **ファイアウォール設定** を選択して **実行** \> **wf.msc** を選択します。
2. **受信ルール** \> **新しいルール** を選択した後、**ルール タイプ** タブで、**ポート** を選択し、**次へ** を選択します。
3. **特定のローカル ポート** フィールドに、**7000** と入力し、**次へ** を選択します。
4. **接続を許可する** を選択し、**次へ** を選択します。
5. 3 つのチェック ボックスをすべてオンにしてすべてのルールを適用し、**次へ** を選択します。
6. ルールの名前を入力し、**完了** を選択します。
7. 送信ルールでこれらの手順を繰り返します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]