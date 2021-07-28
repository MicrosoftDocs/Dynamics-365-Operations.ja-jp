---
title: Regression Suite Automation Tool の設定およびインストール チュートリアル
description: このトピックは、Regression Suite Automation Tool (RSAT) の設定およびインストール方法を説明するチュートリアルです。
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: fc9b330926dfc12890d0bc32e68b4b531616fc2b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357555"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool の設定およびインストール チュートリアル

このトピックは、RSAT および RSAT の使用に関連したツールをセットアップして開始するのに役立つチュートリアルです。

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> インターネット ブラウザー ツールを使用して、このページを PDF 形式でダウンロードして保存します。

## <a name="key-concepts"></a>重要な概念

- Regression Suite Automation Tool (RSAT) をサポートするさまざまなアプリケーションに必要なインストールと前提条件の設定について理解してください。
- タスク レコーダー機能と、 Microsoft Dynamics Lifecycle Services (LCS) および Microsoft Azure DevOps を組み合わせて使用することで、テスト ケースの作成、構成、実行、調査、および報告が可能になります。
- 機能ユーザーがタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくてもタスク記録を一連の自動テストに変換できるようにします。

## <a name="before-you-begin"></a>準備

### <a name="prerequisites"></a>必要条件

- このチュートリアルでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 (2019 年 4 月) またはそれ以降を実行する環境が必要です。 Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 7.3、プラットフォーム更新プログラム 20 (PU20) またはそれ以降を使用している場合もサポートされます。
- ユーザーは、環境に対して管理者権限を持っている必要があります。
- 顧客テナント LCS および Azure DevOps (以前は Microsoft Visual Studio Team Services \[VSTS\]と呼ばれていた) にアクセスできる必要があります。
- テスト スイートを作成および管理しているユーザーは、Azure DevOps テスト計画またはテスト管理者ライセンスを持っている必要があります。 次のライセンスを使用してテスト計画にアクセスすることもできます。
    - Visual Studio エンタープライズ ライセンス
    - Visual Studio Test Professional ライセンス
    - MSDN プラットフォームのサブスクライバー ライセンス
- RSAT は、テスト環境に Web ブラウザーを介してアクセスできる必要があります。
- テスト パラメーターを作成および編集するには、Microsoft Excel をインストールしておく必要があります。

## <a name="configure-azure-devops"></a>Azure DevOps のコンフィギュレーション

### <a name="user-eligibility"></a>ユーザーの適格性

ユーザーが Azure DevOps に作成されていること、および Azure テスト計画へのアクセスを提供するサブスクリプション レベルを持っていることを確認します。 Azure DevOps テスト計画ライセンスは、ユーザーがテスト ケースを作成および管理する場合にのみ必要です (つまり、すべての RSAT ユーザーがこのライセンスを必要とするわけではありません)。 ライセンスの要件については、[ライセンス要件](/azure/devops/test/manual-test-permissions#license-requirements) を参照してください。

### <a name="create-a-new-azure-devops-project"></a>新しい Azure DevOps プロジェクトの作成

RSATは、テスト ケースとテスト スイートの管理、レポート作成、およびテスト実行結果の調査に Azure Devops を使用します。

> [!NOTE]
> 既存の Azure DevOps のプロジェクトを使用できます。 ただし、既存の Azure DevOps のプロジェクトがカスタム テンプレートを持つように設定されている場合は、ビジネス プロセス モデラー (BPM) から Azure DevOps にテスト ケースを同期するときに「VSTSの同期エラー」というエラーが表示されます ([BPM から Azure DevOps への同期をテストする](#test-the-synchronization-from-bpm-to-azure-devops) セクションを参照してください)。 カスタム テンプレートに対して次のようなベスト プラクティスに従っている場合は、テストケースを Azure DevOps に同期することができます。 (これらのベスト プラクティスは、エラー メッセージに一覧表示されています)。

- 作業項目タイプや標準フィールドは削除しないでください。
- 作業項目タイプの状態は削除しないでください。
- 必須フィールドを作業項目タイプに追加しないでください。

![ベスト プラクティスの一覧に表示されるエラー メッセージです。](./media/setup_rsa_tool_02.png)

それ以外の場合は、このチュートリアルでは新しい Azure DevOps プロジェクトを作成することをお勧めします。 詳細については、[カスタム Azure DevOps (VSTS) プロセス テンプレートを使用して BPM に同期するときの問題](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/) を参照してください。

1. Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`) を開きます。
2. Azure DevOps ページの右上隅にある **プロジェクトを作成する** を選択します。

    ![プロジェクト ボタンを作成します。](./media/setup_rsa_tool_03.png)

3. 次のフィールドに入力し、**作成** をクリックします。

    - **プロジェクト名**
    - **バージョン管理** ー **Team Foundation バージョン管理** を選択します。 既定のオプションでは **Git** はサポートされていないことに注意してください。
    - **作業項目プロセス**

    ![新しいプロジェクト ダイアログ ボックスを作成します。](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>個人用アクセス トークンを作成する

このチュートリアルでは、LCS ビジネス プロセス モデラー (BPM) を使用してテスト ケース ライブラリを作成し、テスト ケースと Azure DevOps の同期を行います。 BPM を Azure DevOps と同期するには、個人用アクセス トークンが必要です。

1. Azure DevOps プロジェクトのページの右上隅にある プロファイル アイコンを選択し、**セキュリティ** を選択します。

    ![セキュリティ コマンドです。](./media/setup_rsa_tool_05.png)

2. 左ウィンドウの **セキュリティ** で、**個人用アクセス トークン** を選択します。 **新しいトークン** を選択します。

    ![ユーザー設定の個人用アクセス トークン タブの新しいトークン ボタンです。](./media/setup_rsa_tool_06.png)

3. 次のフィールドに入力し、**作成** をクリックします。

    - **氏名**
    - **有効期限 (UTC)** ー **カスタム定義** を選択し、日付の選択を使用して、使用可能な最後の日付を選択します。
    - **スコープ** ー **フル アクセス** オプションを選択します。

    ![新しい個人用アクセス トークン ダイアログ ボックスを作成します。](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > 作成された個人用アクセス トークンをメモします。 これは、RSAT の構成を設定するときに必要になります。

    ![個人用アクセス トークンです。](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>LCS プロジェクトを構成する

マスター テスト ライブラリ用の Lifecycle Services (LCS) プロジェクトが必要です。 LCS ビジネス プロセス モデラー (BPM) は、テスト ケースのマスター ライブラリとして使用されます。 BPM は、LCS プロジェクト間でテスト ライブラリを管理および配布するために使用されます。 たとえば、Microsoft のパートナーまたはテスト ライブラリを構築している独立系ソフトウェア仕入先 (ISV) は、BPM ライブラリの形式でテスト ケースをリリースします。 BPM では、テスト ケースは業務プロセスごとにまとめられています。 BPM では、テスト パスの実行順序や頻度は定義されません。 このトピックで後述するように、これらの詳細は Azure DevOps で管理されます。  

LCS プロジェクトでは、既存の顧客実装またはパートナー プロジェクトを使用できます。

### <a name="update-the-lcs-language"></a>LCS 言語を更新する

> [!NOTE]
> ユーザー インターフェイス (UI) で業務プロセスを正しく表示するには、LCS 優先言語を **英語 (米国)** に設定する必要があります。

1. LCS 実装プロジェクトに移動します。
2. ページの右上隅にある **設定** ボタン (ギヤ記号) を選択して、**言語の基本設定** を選択します。

    ![言語設定を更新します。](./media/setup_rsa_tool_09.png)

3. **優先言語** フィールドで **英語 (米国)** を選択し、**保存** を選択します。

    ![ユーザー設定の言語の基本設定タブです。](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS プロジェクトを構成して Azure DevOps プロジェクトに接続する

以前に新しい Azure DevOps プロジェクトを作成した場合は、それに接続するように LCS プロジェクトを構成します。 LCS プロジェクトが既に Azure DevOps プロジェクトに接続されている場合は、次のセクションに進むことができます。

1. LCS 実装プロジェクトに移動します。
2. **メニュー** ボタンを選択し、**プロジェクトの設定** を選択します。

    ![プロジェクト設定コマンドです。](./media/setup_rsa_tool_11.png)

3. 左ウィンドウで、**Visual Studio Team Services** を選択し、**Visual Studio Team Services の設定** を選択します。

    ![プロジェクト設定の Visual Studio Team Services タブです。](./media/setup_rsa_tool_12.png)

4. **Azure DevOps サイト URL** フィールドに、Azure DevOps サイトの URL を入力します。 **個人用アクセス トークン** フィールドに、先ほど作成した個人用アクセス トークンを入力します。

    > [!NOTE]
    > VSTS は現在、Azure DevOps と呼ばれていますが、LCS を Azure DevOps プロジェクトに接続するためには、古い URL を使用します。 たとえば、このチュートリアルで使用する Azure DevOps URL は `https://dev.azure.com/D365FOFastTrack/` です。 ただし、次の図では、`https://D365FOFastTrack.visualstudio.com/` と入力されています。

    ![Visual Studio Team Services のステップ 1 です。](./media/setup_rsa_tool_13.png)

5. **続行** を選択します。
6. **Visual Studio Team Services プロジェクト** フィールドで、選択したサイトの VSTS プロジェクトを選択して、LCS プロジェクトにリンクさせます。 **プロセス テンプレート** フィールドは、既定で **アジャイル** に設定されています。 カスタム テンプレートの場合は、[新しい Azure DevOps プロジェクトを作成する](#create-a-new-azure-devops-project) セクションのベスト プラクティスのガイダンスを参照してください。 その後 **続行** を選択します。

    ![Visual Studio Team Services のステップ 2 です。](./media/setup_rsa_tool_14.png)

7. 設定を確認し、**保存** をクリックします。

    ![Visual Studio Team Services のステップ 3 です。](./media/setup_rsa_tool_15.png)

8. **承認** を選択すると、構成された Azure DevOps サイトに代理でアクセスし、VSTS と統合する機能を有効にすることを LCS に承認します。

    ![承認ボタンです。](./media/setup_rsa_tool_16.png)

9. 「Lifecycle Services がユーザーに代わって Visual Studio Team Services に接続することを承認するために、外部サイトにリダイレクトされます。 続行しますか?」というメッセージが表示されます。 **はい** を選択します。

    ![メッセージ ボックスです。](./media/setup_rsa_tool_17.png)

10. **受け入れる** を選択します。

    ![アクセスを承認します。](./media/setup_rsa_tool_18.png)

11. ユーザーとして承認されている場合、UI は LCS プロジェクト設定ページに戻る必要があります。

    ![許可されているユーザーです。](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>新しい BPM ライブラリの作成

1. LCS 実装プロジェクトに移動します。
2. **メニュー** ボタンを選択し、**ビジネス プロセス モデラー** を選択します。

    ![ビジネス プロセス モデラー コマンドです。](./media/setup_rsa_tool_20.png)

3. **新しいライブラリ** を選択します。

    ![新しいライブラリ ボタンです。](./media/setup_rsa_tool_21.png)

4. **ライブラリの名前** フィールドで、名前を入力し、**作成** を選択します。 このチュートリアルでは、BPM ライブラリに **RSAT** という名前を付けます。

    ![新しいライブラリ ダイアログ ボックスを作成します。](./media/setup_rsa_tool_22.png)

5. 新しい **RSAT** BPM ライブラリを開きます。
6. **サンプル コア業務プロセス** プロセスを選択し、右側で **編集モード** を選択します。

    ![編集モード ボタンです。](./media/setup_rsa_tool_23.png)

7. **名前** フィールドと **説明** フィールドの両方の値を、**製品の作成** に変更します。 その後、**保存** を選択します。

    ![名前と説明フィールドです。](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>環境

### <a name="version-requirement"></a>バージョン要求

バージョン 10 を実行するテスト環境またはサンドボックス環境が必要です。 バージョン 7.3、プラットフォーム更新プログラム 20 またはそれ以降を使用している場合もサポートされます。

> [!NOTE]
> RSAT は、Web ブラウザーを介してテスト環境にアクセスできる必要があります。

### <a name="user-criteria"></a>ユーザーの条件

ユーザーは、この環境に対して管理者権限を持っている必要があります。

### <a name="set-up-help-settings-to-connect-with-lcs"></a>ヘルプ設定をセットアップして LCS に接続する

このステップは、クライアントを介して LCS の適切な BPM ライブラリにタスクの記録を保存できるように LCS と接続するために必要です。

1. クライアントを開きます。
2. **システム管理 \> 設定 \> システム パラメーター** の順に移動します。
3. **ヘルプ** タブの **Lifecycle Services ヘルプの構成** フィールドで、該当する LCS プロジェクト (このチュートリアルでは **RSAT**) を選択します。

    ![ヘルプ タブの Lifecycle Services ヘルプの構成フィールドです。](./media/setup_rsa_tool_25.png)

    適切な LCS プロジェクトの下に、BPM ライブラリが入力されます。

4. **保存** を選択します。
5. 更新されたヘルプの内容を表示するには、ブラウザーを更新する必要がある場合があります。

    ![ブラウザーの更新に関する通知です。](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>タスクの記録

> [!NOTE]
> すべてのタスクの記録が、メイン ダッシュボードから開始していることを確認してください。 個々の記録を短くし、販売注文の作成など、1 つのビジネス タスクに注目します。

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>タスク記録を作成して BPM ライブラリに保存する

対応するタスク記録を作成します。これにより、新しい BPM ライブラリで作成された単純な業務プロセスに関連付けることができます。

1. クライアントを開きます。
2. メイン ダッシュボードで、**設定** ボタン (ギヤ記号) を選択し、**タスク レコーダー** を選択します。

    ![設定メニューのタスク レコーダーを選択します。](./media/setup_rsa_tool_27.png)

3. **記録の作成** を選択します。

    ![記録ボタンを作成します。](./media/setup_rsa_tool_28.png)

4. **記録の名前** フィールドと **記録の説明** フィールドに入力し、**開始** を選択します。

    ![記録の名前と記録の説明フィールドです。](./media/setup_rsa_tool_29.png)

5. 製品を作成するステップを記録します。 完了したら、**停止** を選択して記録を停止します。

    ![製品を作成するステップです。](./media/setup_rsa_tool_30.png)

6. **Lifecycle Services に保存** を選択します。

    ![タスク記録を Lifecycle Services に保存します。](./media/setup_rsa_tool_31.png)

    ライブラリ情報が LCS から読み込まれます。

    ![ライブラリ情報を読み込みます。](./media/setup_rsa_tool_32.png)

7. タスク記録に関連付ける BPM ライブラリを選択します。 このチュートリアルでは、先ほど作成した **RSAT** BPM ライブラリとその下にある **製品の作成** 業務プロセスを選択します。 その後、**OK** を選択します。

    ![タスク記録を BPM ライブラリと業務プロセスに関連付けます。](./media/setup_rsa_tool_33.png)

    「Lifecycle Services への保存が成功しました。」というメッセージが表示されます。

    ![LCS に正常に保存されたことを示すメッセージです。](./media/setup_rsa_tool_34.png)

8. タスク記録をローカルに保存してから LCS を介して BPM にアップロードする場合は、次のステップを実行します。

    1. 記録が完了したら、**この PC に保存** を選択します。

        ![この PC に保存します。](./media/setup_rsa_tool_35.png)

    2. ブラウザーの通知バーで、**保存** または **名前を付けて保存** を選択して、ローカル コンピューターにファイルを保存します。

        ![通知バーです。](./media/setup_rsa_tool_36.png)

    3. **RSAT** BPM ライブラリに移動し、タスク記録を保存する業務プロセスを選択します。
    4. **概要** タブで、**アップロード** を選択します。

        ![アップロード ボタンです。](./media/setup_rsa_tool_37.png)

    5. **参照** をクリックし、先ほど保存した .axtr ファイルを選択します。 **アップロード** を選択します。

        ![アップロードする .axtr ファイルを選択します。](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>BPMから Azure DevOps への同期をテストする

タスク記録が業務プロセスに関連付けられたので、LCS の VSTS 同期機能を使用して、業務プロセスとそれに関連するタスク記録を機能とテスト ケースとしてそれぞれ Azure DevOps に同期できることを検証する必要があります。

> [!NOTE]
> Azure DevOps で作成された対応する作業項目タイプは、[新しい Azure DevOps プロジェクトの作成](#create-a-new-azure-devops-project) セクションで説明されているように、Azure DevOps で LCS プロジェクトを構成したときに選択したプロセス テンプレートによって異なります。

1. BPM ライブラリに移動し、先ほど作成した **RSAT** ライブラリを開きます。
2. 省略記号ボタン (**...**) を選択し、**VSTS 同期** を選択します。

    ![省略記号メニューの VSTS 同期コマンドです。](./media/setup_rsa_tool_39.png)

    VSTS の同期が完了すると、左側に **要件** タブが表示され、対応する Azure DevOps 作業項目が含まれます。

    > [!NOTE]
    > Azure DevOps で作成された作業項目には、タイトルの接頭語として BPM ライブラリ名が割り当てられます。

    ![要件タブです。](./media/setup_rsa_tool_40.png)

3. ページを更新します。
4. 省略記号ボタン (**...**) を選択すると、追加のオプションである **テスト ケースの同期** が表示されます。 このオプションを選択します。

    ![省略記号メニューのテスト ケースの同期コマンドです。](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > ページを更新した後で **テスト ケースの同期** オプションを使用できない場合は、BPMのメイン ページに移動し、ライブラリ自体の **テスト ケースの同期** を選択します。 このようにして、ライブラリ全体を効果的に同期することができます。
    >
    > ![ライブラリ全体のテスト ケースの同期を選択します。](./media/setup_rsa_tool_42.png)

    テスト ケースの同期が完了すると、**要件** タブに新しいテスト ケースが作成されます。

    ![要求タブの新しいテスト ケースです。](./media/setup_rsa_tool_43.png)

5. Azure DevOps プロジェクトに移動し、**ボード\>作業項目** を選択します。

    ![ボードの作業項目コマンドです。](./media/setup_rsa_tool_44.png)

6. BPM 同期によって作成した作業項目とテスト ケースが存在することを検証します。

    ![作業項目とテスト ケースです。](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT のインストールと構成

RSAT は、Windows 10 を実行していて、Web ブラウザー (Internet Explorer または Google Chrome) を介して環境に接続できるすべてのコンピューターにインストールできます。

> [!NOTE]
> ツールの新しいバージョンをインストールする前に、以前のバージョンをアンインストールすることをお勧めします。

### <a name="install-an-authentication-certificate"></a>認証証明書をインストールする

認証を有効にするには、RSAT が実行されているのと同じコンピューターで証明書を生成してインストールする必要があります。

#### <a name="generate-a-certificate"></a>証明書を生成する

1. 証明書ファイルを生成するには、管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行します。

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. **実行** ダイアログ ボックスに **certlm.msc** と入力して証明書マネージャーを開いて、**D365 自動テスト証明書** の証明書が **個人\>証明書** の下に作成されていることを確認します。

    > [!NOTE]
    > 証明書はローカル コンピューターに格納されているので、**certmgr.msc** ではなく、**certlm.msc** と入力してください。

    ![D365 自動テスト証明書の証明書です。](./media/setup_rsa_tool_46.png)

3. 証明書を右クリックし、**コピー** を選択します。
4. **信頼済ルート証明機関 \> 証明書** に移動します。

    ![信頼済ルート証明機関フォルダーの下の証明書フォルダです。](./media/setup_rsa_tool_47.png)

5. **アクション** メニューの **貼り付け** を選択して、証明書を **信頼済ルート証明機関** にコピーします。

    ![アクション メニューの貼り付けコマンドです。](./media/setup_rsa_tool_48.png)

6. インストールされている証明書の拇印を取得するには、スペースや特殊文字を使用しないで、管理者として Windows PowerShell ウィンドウを開き、次のコマンドを実行します。

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > 後で Application Object Server (AOS) の .wif ファイルを更新し、RSAT 構成を設定するときに必要になるため、拇印を保存します。

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>接続を信頼するように AOS コンピューターを構成する

> [!NOTE]
> 環境がレベル 2 以上である場合は、証明書の拇印は環境内の **すべての** AOS コンピューターの wif.config ファイルで更新する必要があります。

1. AOS コンピューターへのリモート デスクトップ プロトコル (RDP) 接続を確立します。 サインインの詳細については、LCS の環境の詳細ページを参照してください。
2. Microsoft インターネット インフォメーション サービス (IIS) を開いて、サイトの一覧にある **AOSService** を検索します。

    ![サイトの一覧にある AOSService です。](./media/setup_rsa_tool_49.png)

3. **エクスプローラー** を右クリックして **\<Drive\>: \\AosService\\WebRoot** フォルダーを開きます。 **wif.config** ファイルを検索します。

    ![WebRoot フォルダーの Wif.config ファイルです。](./media/setup_rsa_tool_50.png)

4. 次の例に示すように、証明書と機関名に対応する新しい機関のエントリを追加して、**wif.config** ファイルを更新します。

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > 複数のユーザーが同一のアプリケーションを使用している場合は、各ユーザーが個別のサムプリントを生成する必要があり、それぞれのサムプリントは **\<keys\>** セクションで追加する必要があります。

5. 複数の AOS コンピュータがある場合は、追加の各コンピュータに対してステップ 3 ~ 4 を繰り返します。

    > [!NOTE]
    > 従来のレベル 2 の環境とは異なり、新しいレベル 2 の環境は 2 つの AOS インスタンスを使用して配置されます。

6. すべての AOS コンピューターで **iisreset** を実行します。

    > [!NOTE]
    > レベル 1 のコンピューターで **iisreset** を実行するための管理者権限を持っていない場合は、LCS の環境の詳細ページで、メンテナス > サービスの再起動を選択します。

#### <a name="tier-2-environment"></a>レベル 2 以上の環境

レベル 2 以上 (スタンダード承認テスト サンドボックスまたはそれ以上) の環境を使用している場合は、RSAT がインストールされているコンピューターで次のレジストリ設定を確認または設定します。 認証または RSAT 接続エラーを回避するのに役立つため、このステップを実行する必要があります。

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT をインストールする

1. <https://www.microsoft.com/download/details.aspx?id=57357> に移動して、**ダウンロード** を選択します。
2. すべてのファイルを選択し、**次へ** を選択します。

    ![すべてのファイルを選択します。](./media/setup_rsa_tool_51.png)

3. .msi パッケージをダブルクリックして、インストーラーを実行します。 インストールが完了したら、**完了** をクリックします。

    ![RSAT インストーラー ファイルです。](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Selenium およびブラウザー ドライバーをインストールする

以前のバージョンの RSAT では、Selenium とブラウザー ドライバーをインストールする必要がありました。 これらのドライバーは自動的にインストールされるため、インストールする必要はありません。

1. RSAT を初めて開くときに、Selenium を自動的にダウンロードしてインストールするかどうかを確認するメッセージが表示されます。 詳細については、[RSAT を構成する](#configure-rsat) セクションを参照してください。
2. テスト ケースを実行する前に、RSAT の構成で選択されている既定のブラウザーに対応するブラウザー ドライバーを自動的にダウンロードしてインストールするかどうかを確認するメッセージが表示されます。 詳細については、[テスト ケースの読み込みと実行](#load-and-run-test-cases) セクションを参照してください。

## <a name="get-started-with-rsat"></a>RSAT の使用を開始する

### <a name="create-a-test-plan-and-test-suites"></a>テスト計画およびテスト スイートを作成する

1. Azure DevOps プロジェクトに移動して、**テスト計画** を選択します。

    ![テスト計画コマンドです。](./media/setup_rsa_tool_53.png)

2. **新しいテスト計画** を選択します。

    ![新しいテスト計画ボタンです。](./media/setup_rsa_tool_54.png)

3. **名前** フィールドに入力し、**作成** をクリックします。 このチュートリアルでは、テスト計画に **RSAT テスト計画** という名前を付けます。

    ![新しいテスト計画ダイアログ ボックスです。](./media/setup_rsa_tool_55.png)

4. プラス記号 (**+**) を選択し、**静的スイート** を選択して、新しいテスト計画の下に静的スイートを作成します。 新しいテスト スイートに **T01 ー 製造から在庫** という名前を付けます。

    > [!NOTE]
    > BPM の新しいテスト ケースを自動的に RSAT テスト スイートに取り込む必要がある場合は、クエリ ベースのスイートを作成することもできます。

    ![静的スイートを作成します。](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>テスト ケースをテスト スイートに関連付ける

1. テスト スイートに既存のテスト ケースを追加するには、右側の **既存の追加** を選択します。

    ![既存の追加ボタンです。](./media/setup_rsa_tool_57.png)

2. **スイートにテスト ケースを追加** ページで **クエリの実行** を選択し、テスト スイートに追加するテスト ケースを選択します。 このチュートリアルでは、**新しい製品の作成** テスト ケースを選択します。 次に、ページの右下隅にある **テスト ケースの追加** を選択します (このボタンは次の図には示されていません)。

    ![クエリの実行ボタンです。](./media/setup_rsa_tool_58.png)

    **T01-製造から在庫** テスト スイートにテスト ケースが追加されます。

    ![テスト スイートに追加されたテスト ケースです。](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>RSAT のコンフィギュレーション

1. RSAT を開きます。

    ![RSAT アイコンです。](./media/setup_rsa_tool_60.png)

2. 「Regression Suite Automation Tool には Seleniumが必要です。今すぐ自動的にダウンロードしてインストールしますか?」という警告メッセージが表示されます。 **はい** を選択します。

    ![Regression Suite Automation Tool が Selenium を必要とするという警告メッセージです。](./media/setup_rsa_tool_61.png)

3. 右上隅にある **設定** ボタン (ギヤ記号) を選択し、表示されるダイアログ ボックスで、次のフィールドに情報を入力します。

    - **Azure DevOpsURL** ー Azure DevOps プロジェクトの URL (`https://yourAzureDevOpsUrlHere.visualStudio.com` など) を入力します。
    - **アクセス トークン** ー ツールが Azure DevOps に接続できるアクセス トークンを入力します。 このチュートリアルで先ほど作成した個人用アクセス トークンを使用します。 詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。
    - **プロジェクトの名前** ー Azure DevOps プロジェクトの名前を選択します。
    - **テスト計画** ー テスト ケースが含まれている Azure DevOps テスト計画を選択します。 詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。 テスト計画を選択した後に **接続のテスト** を選択して Azure DevOps への接続をテストします。
    - **ホスト名** – **\<myaos\>.cloudax.dynamics.com** などのテスト環境のホスト名を入力します。 **https://** または **http://** の接頭語を含めないでください。
    - **SOAP ホスト名** ー テスト環境の SOAP ホスト名を入力します。 通常、SOAP ホスト名はホスト名と同じですが、**soap** の接尾語が付いています。 次に例を示します: **\<myaos\>soap.cloudax.dynamics.com**。 **https://** または **http://** の接頭語を含めないでください。

        > [!NOTE]
        > ホスト名と SOAP ホスト名を検索するには、IIS マネージャーを開き、**サイト \> AOSService** を右クリックして、**バインディングの編集** を選択します。 **ホスト名** 列の値によって、ホスト名と SOAP ホスト名が指定されます (SOAP ホスト名の URL には接尾語 **soap** が使用されています)。

        ![ホスト名列のホスト名と SOAP ホスト名です。](./media/setup_rsa_tool_63.png)

    - **管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレスを入力します。
    - **拇印** ー このチュートリアルの前の説明に従って、認証証明書の拇印を入力します。
    - **作業ディレクトリ** ー Excel テスト データ ファイルなどのテスト自動化ファイルを格納するフォルダの場所を指定します。 たとえば、**C:\\Temp\\RegressionTool** と入力または選択します。

        > [!NOTE]
        > フォルダの名前にスペースが含まれている場合は、フォルダが見つからないために実行が失敗します。 この問題は既知の問題であり、ツールの最新バージョンで修正する必要があります。

    - **既定のブラウザー** – **Internet Explorer** または **Google Chrome** のいずれかを選択します。 適切なブラウザー ドライバーがインストールされていることを確認してください。
    - **テストの実行タイムアウト** – テストの実行のタイムアウト期間を分単位で指定します。 タイムアウト期間が経過すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは終了します。
    - **テスト アクション タイムアウト** ー このフィールドは Finance and Operation 環境のサーバー要求のタイムアウト期間を分単位で制御します。 通常は、既定値 (2 分) で十分です。 ただし、低速な環境では、タイムアウトに関連するエラーが発生する場合、値を増やすことをお勧めします。
    - **会社名** ー Excel パラメーター ファイルを作成するときに、既定の会社として使用する会社名を入力します。 後で Excel パラメーター ファイルを編集して会社を変更できます。

    ![設定ダイアログ ボックスです。](./media/setup_rsa_tool_62.png)

4. **適用** を選択して、設定を適用または保存します。

    使用しているコンピューターの構成ファイルに現在の設定を保存するには、**名前を付けて保存** を選択します。 使用しているコンピューターの構成ファイルから設定を復元するには、**開く** を選択します。

5. **閉じる** を選択して、ダイアログ ボックスを閉じます。

### <a name="load-and-run-test-cases"></a>テスト ケースの読み込みと実行

1. Azure DevOps プロジェクトから **RSAT テスト計画** のテスト計画を読み込むには、**読み込み** を選択します。

    ![読み込みボタンです。](./media/setup_rsa_tool_64.png)

2. テスト スイートから **新しい製品の作成** テスト ケースを選択し、**新規 \> テスト実行とパラメーター ファイルの生成** を選択します。

    ![新しいメニューにテスト実行とパラメーター ファイルを生成します。](./media/setup_rsa_tool_65.png)

    Excel パラメーター ファイルは RSAT 構成 (たとえば、**C:\\Temp\\RegressionTool**) で指定したローカル フォルダーに作成されます。

    ![作成された Excel パラメーター ファイルです。](./media/setup_rsa_tool_66.png)

3. パラメーター ファイルを保存する場合は、**アップロード** を選択します。 選択したすべてのテスト ケースのテスト自動化ファイルは、将来使用するために Azure DevOps にアップロードされます。 (これらのファイルには、Excel テスト パラメーター ファイルが含まれています。)

    このようにして、**読み込み** を選択して、パラメーター ファイル (および自動化ファイル) をテストケースから直接 Azure DevOps から読み込むことができます。 パラメーター ファイルを再生成する必要はありません。 この方法は、後でパラメーター ファイルに変更を保持し、それらを上書きしたくない場合に重要になります。

4. 自動化ファイルおよびパラメーター ファイルが Azure DevOps に保存されていることを確認するには、Azure DevOps プロジェクトに移動して、**ボード  \> 作業項目** を選択し、**新しい製品の作成** テスト ケースを選択します。 **添付ファイル** タブには、次の 4 つのファイルが表示されます。

    - **.cs** – C\# 自動化ファイル
    - **.dll** ー アセンブリとしてコンパイルされた自動化ファイル
    - **.xlsx** – Excel パラメーター ファイル
    - **.xml** – 記録ファイル

    ![添付ファイル タブのファイルです。](./media/setup_rsa_tool_67.png)

5. 実行するテスト ケースを選択し、**実行** を選択します。

    > [!NOTE]
    > テスト ケースを実行する前に、ブラウザーとして Internet Explorer を使用している場合は、**Windows のディスプレイ設定 \> 拡大縮小とレイアウト** でデスクトップの解像度が **100%** に設定されていることを確認してください。 仮想マシン (VM) でこの設定を変更できない場合は、VM にアクセスしようとしているクライアント (ラップトップ) で変更します。 解像度の設定は、VM の表示設定に継承されます。

    ![デスクトップの解像度は 100% に設定されました。](./media/setup_rsa_tool_68.png)

6. ブラウザー ドライバーがシステムにインストールされていない場合は、次のような警告メッセージが表示されます: "この操作には \<browser name\> ドライバーが必要です。 今すぐ自動的にダウンロードしてインストールしますか?」という警告メッセージが表示されます。 **はい** を選択します。

    ![Internet Explorer の警告メッセージです。](./media/setup_rsa_tool_69.png)

    ![Chrome の警告メッセージです。](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > ブラウザーとして Chrome を使用していて、Chrome バージョンが正しくないためにセッションが作成されなかったことを示すエラー メッセージが表示された場合は、最新の Chrome を<http://chromedriver.chromium.org/downloads> から **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** フォルダーにダウンロードします。

    ![Chrome のエラー メッセージです。](./media/setup_rsa_tool_71.png)

    テスト ケースが実行され、**結果** フィールドが更新されます。

    ![更新された結果フィールドです。](./media/setup_rsa_tool_72.png)

    このチュートリアルに従っている場合は、製品を作成するためのタスク記録で製品名をハードコーディングされた値として保存しているので、**新しい製品の作成** テスト ケースは失敗します。 同じテスト ケースを再実行すると、製品が既に存在するため、エラー メッセージが表示されます。

    ![失敗に設定された結果フィールドです。](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>テスト結果の表示

1. 失敗したテスト ケースをダブルクリックします。

    エラー メッセージを受信します。

    ![エラー メッセージです。](./media/setup_rsa_tool_73.png)

2. **詳細** を選択すると、エラー メッセージの全体が表示されます。

    ![エラー メッセージの全体です。](./media/setup_rsa_tool_74.png)

3. Azure DevOps で詳細なバージョンのエラー メッセージを表示するには、**Azure DevOps で開く** を選択します。 Azure DevOps では、テスト ケースと詳細なエラー メッセージの状態を表示できます。

    ![Azure DevOps の詳細なエラー メッセージです。](./media/setup_rsa_tool_75.png)

4. Azure DevOps プロジェクトでテスト結果を直接表示するには、**テスト計画\>テスト計画\>実行** の順に移動します。 詳細を表示するテストの実行をダブルクリックします。

    ![Azure DevOps でのテストの実行の一覧です。](./media/setup_rsa_tool_76.png)

5. **実行の概要** タブには、テスト ケースが失敗したことが示されますが、実際のエラー メッセージは表示されません。 詳細なエラー メッセージを表示するには、**テスト結果** タブを選択します。

    ![実行の概要タブです。](./media/setup_rsa_tool_77.png)

    **テスト結果** タブには、テスト ケースの情報と共に、結果とエラー メッセージが表示されます。

    ![テスト結果タブです。](./media/setup_rsa_tool_78.png)

6. 関連するレコードをダブルクリックして、詳細なエラー メッセージを表示します。

    ![詳細なエラー メッセージです。](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > すべてのエラー メッセージは、**C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt** でローカルでも利用可能です。

7. **エクスポート** を選択して、テスト計画レベルでテストの実行の結果をエクスポートすることもできます。

    ![テスト計画をエクスポートします。](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Excel パラメーター ファイルの変更

1. RSAT を開きます。
2. テスト ケースを選択し、**編集** を選択して Excel パラメーター ファイルを開きます。

    **EcoResProductCreate** シートで、**製品番号** フィールドの値がハードコーディングされていることを確認します。 テスト ケースを再度実行する前に、このフィールドを新しい製品番号に更新する必要があります。

3. Excel パラメーター ファイルを再度開いて製品番号を毎回手動で更新することなく、実行ごとに一意の製品番号を生成するには、次の Excel の式を使用します。

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > **一般** タブに加えて、Excel パラメーター ファイルには、テスト ケースがアクセスするすべてのフォーム ページのデータ タブが含まれています。

    ![製品番号フィールドです。](./media/setup_rsa_tool_81.png)

4. **保存** を選択して、Excel ブックを閉じます。
5. **アップロード** を選択して Excel パラメーター ファイルを Azure DevOps に保存します。

    ![ファイルのアップロードに成功したことを示すメッセージです。](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > 特定のユーザー コンテキストでテスト ケースを実行するには、Excel パラメーター ファイルの **一般** タブの **テスト ユーザー** フィールドにユーザーの電子メール ID を入力します。 最新バージョンの RSAT では、Excel パラメーター ファイルのフィールドのレイアウトは更新されていますが、概念は同じです。
    >
    > ![テスト ユーザー フィールドです。](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>結果の検証

- **実行** を選択してテスト ケースを再実行し、テスト ケースが成功したことを確認します。 テスト結果は、[テスト結果の表示](#view-the-test-results) セクションの説明に従って表示できます。

    ![成功に設定された結果フィールドです。](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>テスト ケースの連鎖

RSAT の主要な機能の 1 つとして、テスト ケースの連鎖 (つまり、テストが他のテストに値を渡す機能) があります。 テスト ケースは、Azure DevOps テスト計画で定義された順序に従って実行されます。 (この順序は、テスト ツール自体で更新することもできます)。したがって、あるテスト ケースから別のテスト ケースに変数を渡す場合は、テストが正しい順序であることが非常に重要です。

このセクションでは、最初のテスト ケースで保存された変数を作成し、2 番目のテスト ケースを作成して、保存された変数を最初のテスト ケースから 2 番目のテスト ケースに渡します。 その後、テスト ケースを連鎖したテスト ケースとして RSAT で実行します。

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>既存のタスク記録を変更して保存された変数を作成する

1. クライアントを開きます。
2. **設定** ボタン (ギヤ記号) を選択し、**タスク レコーダー** を選択します。
3. **記録の編集** を選択します。

    ![記録の編集ボタンです。](./media/setup_rsa_tool_85.png)

4. **Lifecycle Services から開く** を選択します。

    ![Lifecycle Services から開くボタンです。](./media/setup_rsa_tool_86.png)

5. **Lifecycle Services ライブラリを選択する** を選択します。

    ![Lifecycle Services ライブラリの選択ボタンです。](./media/setup_rsa_tool_87.png)

    BPM ライブラリが LCS から読み込まれます。

    ![BPM ライブラリを読み込みます。](./media/setup_rsa_tool_88.png)

6. BPM ライブラリが LCS から読み込まれたら、**RSAT** BPM ライブラリと、タスク記録が関連付けられていた **新しい製品の作成** 業務プロセスを選択します。 その後、**OK** を選択します。

    ![BPM ライブラリと業務プロセスを選択します。](./media/setup_rsa_tool_89.png)

7. 適切なタスク記録の名前が **記録の名前** フィールドに入力されます。 **スタート** を選択します。

    ![記録の名前フィールド内のタスク記録の名前です。](./media/setup_rsa_tool_90.png)

8. **製品情報管理\>製品** に移動し、**新規** を選択すると、元のタスク記録や **製品の作成** などが記録されたページが開きます。
9. **ステップの挿入** を選択します。

    > [!NOTE]
    > 新しいステップは、ウィンドウで選択したステップの **後に** 挿入されます。

    ![ステップの挿入ボタンです。](./media/setup_rsa_tool_91.png)

10. **製品番号** フィールドを右クリックし、**タスク レコーダー \> コピー** を選択します。

    ![コピー コマンドです。](./media/setup_rsa_tool_92.png)

11. 新しいステップがウィンドウに追加されます。 後で必要になるため、**製品番号** フィールドの値をメモしておきます。

    ![新しいステップが追加されました。](./media/setup_rsa_tool_93.png)

12. **編集の完了** を選択します。
13. **Lifecycle Services に保存** を選択し、新しいタスク記録を、元のタスク記録が関連付けられていたのと同じ BPM ライブラリおよび業務プロセスに関連付けます。 詳細については、[タスクの記録の作成と BPM ライブラリへの保存](#create-a-task-recording-and-save-it-to-the-bpm-library) セクションを参照してください。
14. BPM ライブラリに移動し、[BPM から Azure DevOps への同期のテスト](#test-the-synchronization-from-bpm-to-azure-devops) セクションで説明しているように、**テスト ケースの同期** を選択して、Azure DevOps のテス トケースに関連付けられているタスク記録を上書きします。
15. RSAT を開き、**読み込み** を選択して、テスト スイート内のすべてのテスト ケースを再読み込みします。 [テスト ケースの読み込みと実行](#load-and-run-test-cases) セクションの説明に従って、テスト ケースを選択し、**新規 \> テストの実行とパラメーター ファイルの生成** を選択することによって、適切なテスト ケースの自動化ファイルとパラメーター ファイルを再生成する必要があります。

    > [!NOTE]
    > Excel パラメーター ファイルを開いたままにしておくと、再生成に失敗します。 したがって、新しい Excel パラメーター ファイルを生成する前に、テスト ケースの Excel パラメーター ファイルが閉じられていることを確認してください。

16. **編集** を選択して新しい Excel パラメーター ファイルを開きます。 新しい **保存された変数** のエントリが、行 9 に表示されます。 この変数 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** はタスク記録の XML ファイルに保存され、後続のテストで使用できます。

    ![保存された変数エントリです。](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>新しいテスト ケースの作成

1. **RSAT** BPM ライブラリに移動します。
2. **サンプル サポート業務プロセス** プロセスを選択し、右側で **編集モード** を選択します。
3. **名前** フィールドと **説明** フィールドの両方の値を、**製品のリリース** に変更します。 その後、**保存** を選択します。

    ![製品のリリースに変更された名前と説明です。](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>検証機能を持つ新しいタスク記録を作成します。

- 先ほど作成した製品を USRT 法人にリリースするためのタスクの記録を作成します。 詳細については、[タスクの記録の作成と BPM ライブラリへの保存](#create-a-task-recording-and-save-it-to-the-bpm-library) セクションを参照してください。

    > [!NOTE]
    > 連鎖したテスト ケースでは、*フィールドの値を手動で入力する* ことによって、必要なレコードを検出またはフィルター処理することをお勧めします。 このようにして、ツールは、後続のテスト ケースでアクションを実行する必要があるレコードを決定できます。

    ![検証機能を持つ新しいタスク記録です。](./media/setup_rsa_tool_96.png)

    上の図に示されているように、クイック フィルターを使用して製品を検出した後、**製品のリリース** を選択する前に、**製品番号** フィールドの値を検証して、製品 ID が以前に作成された製品 ID であることを確認します。 値を検証するには、**製品番号** フィールドを右クリックして、**タスク レコーダー \> 検証 \> 現在の値** を選択します。

    ![現在の値を検証します。](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>タスク記録を BPM に保存する

1. タスク記録が完了したら、**Lifecycle Services に保存** を選択します。

    ![Lifecycle Services への完了したタスク記録を保存します。](./media/setup_rsa_tool_98.png)

2. ライブラリ情報が LCS から読み込まれます。

    ![LCS からのライブラリ情報を読み込みます。](./media/setup_rsa_tool_99.png)

3. タスク記録に関連付ける BPM ライブラリを選択します。 このチュートリアルでは、先ほど作成した **RSAT** BPM ライブラリとその下にある **製品のリリース** 業務プロセスを選択します。 その後、**OK** を選択します。

#### <a name="sync-bpm-to-azure-devops"></a>BPM を Azure DevOps に同期する

1. BPM ライブラリに移動して、**RSAT** ライブラリを開きます。
2. **VSTS 同期** を選択し、**テスト ケースを同期** します。 詳細については、[BPM から Azure DevOps への同期をテストする](#test-the-synchronization-from-bpm-to-azure-devops) を参照してください。

    同期が完了したら、新しい作業項目と、**製品のリリース** 業務プロセスの対応するテスト ケースが、**ボード \> 作業項目** の Azure DevOps に表示されます。

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>既存のテスト スイートに新しいテスト ケースを追加する

1. **テスト計画 \> テスト計画** に移動し、**RSAT テスト計画** 計画を選択します。
2. **既存の追加** を選択します。
3. **スイートにテスト ケースを追加** ページで、**クエリの実行** を選択します。
4. **製品のリリース** に対して作成された新しいテスト ケースを選択し、ページの右下隅にある **テスト ケースの追加** を選択します (このボタンは次の図には示されていません)。

    ![スイートにテスト ケースを追加ページです。](./media/setup_rsa_tool_100.png)

    テスト スイートには、2 つのテスト ケースが含まれるようになりました。

    ![テスト スイートの 2 つのテスト ケースです。](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>テストケースの RSAT への読み込み

1. RSAT を開き、**読み込み** を選択します。
2. テスト ケースが読み込まれ、「このアクションは Excel のテスト データ ファイルを上書きします」という警告が表示され、ローカルの変更が失われます。 続行しますか? **はい** を選択すると、Azure DevOps にアップロードされた Excel パラメーター ファイルではなく、ローカル システムの Excel パラメーター ファイルが更新されます。

    ![このアクションにより、Excel テスト データ ファイルが上書きされます。](./media/setup_rsa_tool_102.png)

    両方のテスト ケースが、最初のテスト ケースの Excel パラメーター ファイルと共に読み込まれます。 前回の実行で **アップロード** を選択したため、パラメーター ファイルが Azure DevOps から引き出されます。

    ![テスト ケースが読み込まれました。](./media/setup_rsa_tool_103.png)

3. 2 番目のテスト ケースのみを選択して、**新規 \> テスト実行とパラメーター ファイルの生成** を選択します。

#### <a name="edit-the-excel-parameter-file"></a>Excel パラメーター ファイルの編集

1. 2 番目のテスト ケースのみを選択し、**編集** を選択して対応する Excel パラメーター ファイルを開きます。
2. 保存された変数 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** を最初のテスト ケースから製品番号が使用されているすべてのフィールドへコピーします ([既存のタスク記録を変更して保存された変数を作成する](#modify-an-existing-task-recording-to-create-a-saved-variable) セクションを参照してください)。 この場合、変数を **EcoResProductListPage** シートの **製品番号** フィールドと **製品番号の検証** フィールドにコピーします。

    ![製品番号と製品番号の検証フィールドです。](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > 変数は、同じテストの実行中にのみテスト間で受け渡すことができます。 変数の名前は完全に一致している必要があります。

3. **保存** を選択して、Excel ブックを閉じます。
4. **アップロード** を選択して、Excel パラメーター ファイルに加えた変更を保存します。

#### <a name="run-the-chained-test-cases"></a>連鎖したテスト ケースの実行

1. 両方のテスト ケースを選択し、**実行** を選択します。
2. 両方のテスト ケースが成功していることを確認します。

    ![両方のテスト ケースに対して成功に設定された結果フィールドです。](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]