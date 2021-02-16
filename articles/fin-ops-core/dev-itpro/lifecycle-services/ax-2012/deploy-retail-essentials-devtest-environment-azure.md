---
title: Azure での Retail Essentials 開発/テスト環境の配置
description: このトピックでは、Microsoft Azure に Retail essentials 開発環境またはテスト環境を配置する方法について説明します。 環境を配置するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。
author: aamirallaqaband
manager: AnnBe
ms.date: 01/05/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13261
ms.assetid: 00e58780-7373-4c53-b3af-1e9d3d4eebff
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: ab90351791709fd9ee2d3c3e814516f5a056b269
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688541"
---
# <a name="deploy-retail-essentials-devtest-environments-on-azure"></a>Azure での Retail Essentials 開発/テスト環境の配置

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Azure に Retail essentials 開発環境またはテスト環境を配置する方法について説明します。 環境を配置するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。

<a name="prerequisites"></a>必要条件
-------------

このトピックの手順を実行する前に、次の条件が満たされていることを確認します。

| カテゴリ       | 前提条件                                                                                                                                                    |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 必要なタスク | [Azure で AX 2012 R3 の配置を計画する](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a>1. ライフサイクル サービスにログオンする
Microsoft Dynamics Lifecycle Services (LCS) は、顧客およびパートナーが Dynamics AX のプロジェクトの管理に使用できるクラウドベースの共同ワークスペースです。 Azure に Dynamics AX を配置するには、この Web サイトを使用します。 Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。 CustomerSource または PartnerSource の資格情報でアクセスすることができます。詳細については、[Lifecycle Services にログオン](https://lcs.dynamics.com/en/) を参照してください。

## <a name="2-create-a-project"></a>2. プロジェクトの作成
LCS にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。 プロジェクトは、LCS でのエクスペリエンスの主な開催者です。 プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。

## <a name="3-connect-the-project-to-your-azure-subscription"></a>3. Azure サブスクリプションにプロジェクトを接続する
Azure サブスクリプションに LCS プロジェクトを接続します。 これにより、LCS は Dynamics AX 環境をサブスクリプションに展開できます。 Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。

1. LCS プロジェクトで **環境** セクションに移動して、**Microsoft Azure 設定** をクリックしてから、**Azure コネクタ領域** で **追加** をクリックします。 
   >[!Note]
   > **Microsoft Azure 設定** オプションは、**クラウド-ホスト環境タイル** をクリックしたときにも使用できます。
2. Azure への接続を識別する名前を入力します。
3. Azure サブスクリプション ID を入力します。 サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。
   1.  ブラウザの別のインスタンスを開きます。
   2.  [Azure ポータル](https://ms.portal.azure.com/)にログオンします。
   3.  左のナビゲーション ウィンドウで、**サブスクリプション** をクリックします。 

       > [!Note]
       > 下部の **その他のサービス** をクリックしてから **サブスクリプション** をクリックすることが必要な場合があります。

   4.  サブスクリプション ID をコピーして、LCS の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。

4. **次へ** をクリックします。
5. **ダウンロード** をクリックして管理証明書をダウンロードします。 この管理証明書により、LCS はお客様の代わりに Azure と通信できます。 既定では、管理証明書はコンピューターの **ダウンロード** フォルダーに保存され、**LifecycleServicesDeployment.cer** という名前が付きます。
6. 管理証明書を Azure にアップロードします。 これを行うには、[[Azure 管理 API 管理証明書をアップロード](https://docs.microsoft.com/azure/azure-api-management-certs)] の手順を参照してください。

7. LCS で **Microsoft Azure 設定** パネルを表示するブラウザーに戻ります。 **次へ** をクリックします。
8. 地域を選択します。 AX 2012 R3 環境は、この領域のデータ センターに配置されます。
9. **接続** をクリックします。 これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。 

>[!Note]
> 証明書が期限切れになった場合は、新しいものを取得できます。 そのためには次の作業を行います。
> 1. プロジェクトの設定の **Azure コネクタ** 領域で接続を選択し、**編集** をクリックします。
> 2. **Microsoft Azure 設定** パネルが画面の横に表示されます。 **ダウンロード** をクリックして新しい証明書をダウンロードします。
> 3. 上の手順の手順 6 ～ 9 を繰り返します。

## <a name="4-deploy-a-retail-essentials-devtest-environment-on-azure"></a>4. Azure での Retail Essentials 開発/テスト環境の配置
Azure に Retail Essentials 開発/テスト環境を配置するには、以下の手順に従ってください。

1. **クラウド ホスト環境** ページで、**追加** (**+**) アイコンをクリックします。
2. **環境のトポロジの選択** パネルで、**開発/テスト** を選択します。
3. **Retail Essentials 開発/テスト** をクリックします。
4. **環境名** フィールドに、配置される環境の名前を入力します。
5. **詳細設定** をクリックします。
6. ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。 情報を入力するには、次の表を使用してください。
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th>以下を行う場合</th>
   <th>操作</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td>Azure で環境用に新しいドメインを作成する</td>
   <td><ol>
   <li><strong>新規ドメイン</strong>をクリックします。</li>
   <li>ドメイン名を入力します。 既定では、ドメインは <em>contoso.com</em> と呼ばれます。</li>
   </ol></td>
   </tr>
   <tr class="even">
   <td>Azure の既存のドメインへの環境の追加</td>
   <td><ol>
   <li><strong>既存のドメイン</strong>をクリックします。</li>
   <li>ドメイン名を入力します。 たとえば、<em>contoso.com</em>。</li>
   </ol></td>
   </tr>
   </tbody>
   </table>

7. ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。 展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。 どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。 次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。 アカウントとパスワードのルール:
   - 有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。
   - 有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \['@', '!', '=', '\*'\] 次のような一般的なパスワードは使用できません: pass@word1

8. 使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン** をクリックします。 既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。 CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。
9. 仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。 一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの **詳細設定** に用意されています。 名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。 インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。 仮想マシン名は 13 文字またはそれ以下にする必要があります。 インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。 例: ACustomVMName-99。 最初の展開後に、仮想マシンのインスタンスが環境に追加されるとき、配置サービスは、中断した場所で、仮想マシンの名前の増分を開始します。 たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。 もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。 展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。 これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。
10. 仮想ネットワークの設定をカスタマイズするには、<strong>仮想ネットワークをカスタマイズする</strong> をクリックします。 情報を入力するには、次の表を使用してください。
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>以下を行う場合</th>
    <th>操作</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Azure で環境用に新しい仮想ネットワークを作成する</td>
    <td><ol>
    <li><strong>新しい仮想ネットワーク</strong>をクリックします。</li>
    <li>仮想ネットワーク名を入力します。</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Azure の既存の仮想ネットワークへの環境の追加</td>
    <td><ol>
    <li><strong>既存の仮想ネットワーク</strong>をクリックします。</li>
    <li>使用する既存の仮想ネットワークの名前を選択してください。</li>
    <li><strong>アドレス空間</strong> フィールドには、適切な値が自動的に表示されます。 提供された値を選択します。</li>
    <li><strong>アプリケーション サブネット名</strong> フィールドには、使用可能なオプションが表示されます。 Lifecycle Servicesによって以前に展開した広告に配置する場合は、選択した <strong>APPNET</strong> 値を選択します。</li>
    <li>Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。
    <ol>
    <li><a href="https://ms.portal.azure.com/">Azure ポータル</a>にログオンします。</li>
    <li>左のナビゲーション ウィンドウで、 <strong>仮想ネットワーク</strong> をクリックします。</li>
    <li>使用する仮想ネットワークの名前をクリックします。</li>
    <li><strong>構成</strong>をクリックします。 仮想ネットワークに関する詳細は、ページに記載されています。</li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

11. **完了** をクリックします。 **環境** **の展開** パネルが再表示されます。
12. 配置される仮想マシンの数とサイズが一覧表示されます。 必要に応じて、仮想マシンの数とサイズを変更します。
    -   この環境で各仮想マシンにインストールされているソフトウェアの詳細については、 [Azure 上での AX 2012 R3の 配置計画](plan-2012-r3-deployment-azure.md) を参照してください。
    -   仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](https://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。

13. ライセンスの条項を確認するには、**ソフトウェア ライセンス条項** をクリックします。 次に、チェック ボックスを選択して、条件に同意することを示します。
14. **次へ** をクリックします。
15. **展開** をクリックして、環境を展開する準備が整ったことを確認します。 配置には数時間かかる場合があります。 配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。 (これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。 配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。

## <a name="5-prepare-the-environment-for-use"></a>5. 使用する環境を準備
Retail Essentials 環境が Azure に配置されたので、これを設定して使用するためにコンフィギュレーションする必要があります。 詳細については、以降のセクションを参照してください。

### <a name="log-on-to-the-retails-essentials-virtual-machine"></a>Retail Essentials 仮想マシンにログオンします。

ESSEN-&lt;GUID&gt; 仮想マシンに &lt;DomainName&gt;DynamicsInstallUser アカウントを使用してログオンします。 手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。 トピック [Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。

### <a name="compile-dynamics-ax-2012-r3"></a>Dynamics AX 2012 R3 のコンパイル

Ax Build.exe. を使用した Dynamics AX 2012 R3 のコンパイル 手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/library/dn528954.aspx) を参照してください。

### <a name="initialize-dynamics-ax-2012-r3"></a>Dynamics AX 2012 R3 の初期化

Dynamics AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。 手順については、[初期化チェックリスト](https://technet.microsoft.com/library/aa497061.aspx) を参照してください。

### <a name="install-sample-data"></a>サンプル データのインストール

サンプル データを環境にインストールする場合は、次の手順を実行します。

1.  次の場所に移動します: F:TestTransferTool
2.  テスト データ ツールをインストールします。 手順については、 [テスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md) を参照してください。
3.  コマンド プロンプトを開いて、次の場所に移動します: C:\Program Files (x86) \Microsoft Dynamics AX 2012 R3 Test Data Transfer Tool (Beta)
4.  次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx

> [!NOTE]
> サンプル データには、Dynamics AX の試用版のライセンス キーが含まれています。 サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます

### <a name="set-up-retail-essentials"></a>Retail Essentials の設定

Dynamics AX クライアントを開いて、次の手順を実行します。

1.  **Retail essentials** エリア ページに移動します。
2.  **チャネル &gt; 設定** **&gt; 小売パラメーター** の順にクリックします。
3.  **小売パラメーター** フォームで、次の手順を完了します。
    1.  フォーム上部の **初期化** ボタンをクリックします。
    2.  **はい** をクリックして、基本構成データを初期化することを確認します。 初期化プロセスが完了すると、情報ログが表示されます。
    3.  フォームを閉じます。

4.  **データ同期 &gt; 設定 &gt; 小売用スケジューラのパラメーター** の順にクリックします。
5.  **小売用スケジューラ パラメーター** フォームで、次の手順を完了します。
    1.  **サーバー名** フィールドに、仮想マシンの名前を入力します。
    2.  フォーム上部の **メタデータの同期** ボタンをクリックします。
    3.  **はい** をクリックしてメタデータを同期することを確認します。 このプロセスが完了すると、情報ログが表示されます。
    4.  フォームを閉じます。

6.  **データ同期 &gt; 設定 &gt; チャネル統合 &gt; Real-time Service プロファイル** の順にクリックします。
7.  **Commerce Data Exchange: Real-time Service** プロファイル フォームで、次の手順を完了します。
    1.  **サーバー名** フィールドに、仮想マシンの名前を入力します。
    2.  **共通名** フィールドに、証明書の共通名を入力します。
    3.  フォームを閉じます。

8.  **データ同期 &gt; 設定 &gt; チャネル統合 &gt; 作業フォルダー** とクリックします。
9.  **作業フォルダー** フォームで、次の手順を完了します。
    1.  **ダウンロード パス** フィールドの場所に注意してください。 通常は C:\DemoFiles\Retail\CDXDownload です。 C ドライブにこれらのフォルダーを作成します。
    2.  **アップロード パス** フィールドの場所に注意してください。 通常は C:\DemoFiles\Retail\CDXUpload です。 C ドライブにこれらのフォルダーを作成します。
    3.  フォームを閉じます。

10. **データ同期 &gt; 設定 &gt; チャネル統合 &gt; チャネル データベース** とクリックします。
11. **チャネル データベース** フォームで、次の手順を完了します。
    1.  **HoustonStore** レコードを選択します。
    2.  フォームの右側にあるウィンドウで、**Retail サーバー** セクションに移動します。 (表示するためにウィンドウの一番下までスクロールしなければならない場合があります。)
    3.  **サーバー名** フィールドに、仮想マシンの名前を入力します。
    4.  フォーム上部の **完全データ同期** ボタンをクリックします。 次に、リストから 9999 配布スケジュールを選択します。 **OK** をクリックします。
    5.  フォームを閉じます。

## <a name="6-enable-users-to-access-dynamics-ax-2012-r3-on-azure"></a>6. Azure で Dynamics AX 2012 R3 へのユーザーのアクセスを可能にする
次のセクションでは、企業ユーザーが Dynamics AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。

### <a name="create-a-site-to-site-vpn-connection"></a>サイト間 VPN 接続を作成する

企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。 これを行う方法の詳細については、以下を参照してください。

-   [仮想ネットワークの概要](https://msdn.microsoft.com/library/windowsazure/jj156007.aspx)
-   [仮想ネットワークのコンフィギュレーション タスク](https://msdn.microsoft.com/library/jj156206.aspx)
-   [Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN](https://msdn.microsoft.com/library/dn636917.aspx)
-   [管理ポータルに仮想ネットワーク ゲートウェイを構成する](https://msdn.microsoft.com/library/azure/jj156210.aspx)

### <a name="create-a-domain-trust"></a>ドメイン信頼の作成

企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。 信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/library/cc754626.aspx)」を参照してください。 このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。

### <a name="give-users-access"></a>ユーザーのアクセス許可を付与します

ユーザが Dynamics AX にアクセスできるようにするには、以下のタスクを実行します。

-   CLI- &lt;GUID&gt; 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。
-   ユーザーに Dynamics AX へのアクセス許可を付与します。 手順については、[Microsoft Dynamics AX で新しいユーザーを作成する](https://technet.microsoft.com/library/aa548139.aspx)を参照してください。

> [!NOTE]
> VPN 接続とドメイン信頼を作成しない場合でも、ユーザーに Dynamics AX へのアクセス権を付与することができます。 これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。 その後、上記の 2 つのタスクを完了する必要があります。

## <a name="7-learn-more-about-the-service-accounts-for-this-environment"></a>7. この環境のサービス アカウントに関する詳細
次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。

### <a name="domain-accounts"></a>ドメイン アカウント

次のテーブルに、環境を配置したときに作成されたドメイン アカウントの既定の名前を示します。

| ドメイン アカウント                  | 説明                                                                                                           |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <DomainName>AOSServiceUser      | 次のサービスを実行するために使用されたアカウント: Microsoft Dynamics AX Object Server                                   |
| <DomainName>SQLServiceUser      | 次のサービスを実行するために使用されるアカウント: SQL Server Analysis Services (MSSQLSERVER)。                            |
| <DomainName>DynamicsInstallUser | Dynamics AX をインストールするために使用したアカウント。                                                                              |
| <DomainName>RetailServiceUser   | 次のサービスの実行に使用したアカウント: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。 |
| <DomainName>BCProxyUser         | ビジネス コネクタ プロキシとして使用されるアカウント。                                                                     |

> [!NOTE]
> パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の **クラウド ホスト 環境** ページに表示されます。

### <a name="local-administrator-accounts"></a>ローカル管理者アカウント

配置した各仮想マシンには、ローカル Administrator アカウントがあります。 このアカウントは builtinaxlocaladmin です。 ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の **クラウド ホスト 環境** ページに表示されます。



