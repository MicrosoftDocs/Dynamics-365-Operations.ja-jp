---
title: "Azure での Retail Mobility 開発/テスト環境の配置"
description: "このトピックでは、Microsoft Azure に小売モビリティ開発環境またはテスト環境を展開する方法について説明します。 環境を展開するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。"
author: aamirallaqaband
manager: AnnBe
ms.date: 01/05/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13332
ms.assetid: ffc3e49a-c2a7-48ce-9f3d-3950b3133cbc
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8cf63a63ff98b6168bdc61536334c9d7a44579b0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="deploy-retail-mobility-devtest-environments-on-azure"></a>Azure での Retail Mobility 開発/テスト環境の配置

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Azure に小売モビリティ開発環境またはテスト環境を展開する方法について説明します。 環境を展開するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。

<a name="prerequisites"></a>前提条件
-------------

このトピックの手順を実行する前に、次の条件が満たされていることを確認します。

| カテゴリ       | 前提条件                                                                                                                                                    |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 必要なタスク | [Azure での Microsoft Dynamics AX 2012 R3 配置の計画](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a>1. ライフサイクル サービスにログオンする
Microsoft Dynamics Lifecycle Services (LCS) は、顧客およびパートナーが Dynamics AX のプロジェクトの管理に使用できるクラウドベースの共同ワークスペースを提供します。 Azure に Dynamics AX を配置するには、この Web サイトを使用します。 Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。 CustomerSource または PartnerSource の資格情報でアクセスすることができます。詳細については、[Lifecycle Services にログオン](https://lcs.dynamics.com/) を参照してください

## <a name="2-create-a-project"></a>2. プロジェクトの作成
LCS にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。 プロジェクトは、LCS でのエクスペリエンスの主な開催者です。 プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。

## <a name="3-connect-the-project-to-your-azure-subscription"></a>3. Azure サブスクリプションにプロジェクトを接続する
Azure サブスクリプションに LCS プロジェクトを接続します。 これにより、LCS は Dynamics AX 環境をサブスクリプションに展開できます。 Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。

1. LCS プロジェクトで **環境**セクションに移動して、**Microsoft Azure 設定**をクリックしてから、**Azure コネクタ**領域で**追加**をクリックします。 
   >[!Note]
   > **Microsoft Azure 設定** オプションは、**クラウド ホスト環境** タイルをクリックしたときにも使用できます。
2. Azure への接続を識別する名前を入力します。
3. Azure サブスクリプション ID を入力します。 サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。
   1.  ブラウザの別のインスタンスを開きます。
   2.  [Azure ポータル](https://ms.portal.azure.com/)にログオンします。
   3.  左のナビゲーション ウィンドウで、**サブスクリプション**をクリックします。 

       > [!Note]
       > 下部の **その他のサービス** をクリックしてから **サブスクリプション** をクリックすることが必要な場合があります。

   4.  サブスクリプション ID をコピーして、LCS の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。

4. **次へ** をクリックします。
5. **ダウンロード**をクリックして管理証明書をダウンロードします。 この管理証明書により、LCS はお客様の代わりに Azure と通信できます。 既定では、管理証明書はコンピューターの**ダウンロード** フォルダーに保存され、**LifecycleServicesDeployment.cer** という名前が付きます。
6. 管理証明書を Azure にアップロードします。 これを行うには、[[Azure 管理 API 管理証明書をアップロード](https://docs.microsoft.com/en-us/azure/azure-api-management-certs)] の手順を参照してください。

7. LCS で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。 **次へ** をクリックします。
8. 地域を選択します。 AX 2012 R3 環境は、この領域のデータ センターに配置されます。
9. **接続** をクリックします。 これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。 

>[!Note]
> 証明書が期限切れになった場合は、新しいものを取得できます。 そのためには次の作業を行います。
> 1. プロジェクトの設定の **Azure コネクタ** 領域で接続を選択し、**編集** をクリックします。
> 2. **Microsoft Azure 設定** パネルが画面の横に表示されます。 **ダウンロード**をクリックして新しい証明書をダウンロードします。
> 3. 上の手順の手順 6 ～ 9 を繰り返します。

## <a name="4-deploy-a-retail-mobility-devtest-environment-on-azure"></a>4. Azure での Retail Mobility 開発/テスト環境の配置
Azure に Retail Mobility 開発/テスト環境を配置するには、以下の手順に従ってください。

1. **クラウド ホスト環境**ページで、追加 (**+**) アイコンをクリックします。
2. **環境のトポロジの選択**パネルで、**開発/テスト**を選択します。
3. **Retail Mobility 開発/テスト**をクリックします。
4. **環境名**フィールドに、配置される環境の名前を入力します。
5. **詳細設定**をクリックします。
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
   <li><strong><span class="label">新規ドメイン</span></strong>をクリックします。</li>
   <li>ドメイン名を入力します。 既定では、ドメインは <em>contoso.com</em> と呼ばれます。</li>
   </ol></td>
   </tr>
   <tr class="even">
   <td>Azure の既存のドメインへの環境の追加</td>
   <td><ol>
   <li><strong><span class="label">既存のドメイン</span></strong>をクリックします。</li>
   <li>ドメイン名を入力します。 たとえば、<em>contoso.com</em>。</li>
   </ol></td>
   </tr>
   </tbody>
   </table>

7. ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。 展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。 どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。 次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。 アカウントとパスワードのルール:
   1. 有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。
   2. 有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \[「@」、「!」、「=」、「\*」\] 次のような一般的なパスワードは使用できません: pass@word1

8. 使用する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン** をクリックします。 既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。 CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。
9. 仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。 一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。 名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。 インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。 仮想マシン名は 13 文字またはそれ以下にする必要があります。 インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。 例: ACustomVMName-99。 最初の展開後に、仮想マシンのインスタンスが環境に追加されるとき、配置サービスは、中断した場所で、仮想マシンの名前の増分を開始します。 たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。 もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。 展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。 これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。
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
    <li><span class="label"><strong>新しい仮想ネットワー</strong>ク</span>をクリックします。</li>
    <li>仮想ネットワーク名を入力します。</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Azure の既存の仮想ネットワークへの環境の追加</td>
    <td><ol>
    <li><strong><span class="label">既存の仮想ネットワーク</span></strong>をクリックします。</li>
    <li>使用する既存の仮想ネットワークの名前を選択してください。</li>
    <li><strong><span class="label">アドレス空間</span></strong> フィールドには、適切な値が自動的に表示されます。 提供された値を選択します。</li>
    <li><strong><span class="label">アプリケーション サブネット名</span></strong>フィールドには、使用可能なオプションが表示されます。 Lifecycle Services によって以前に展開した広告に配置する場合は、選択した <strong><span class="label"><em>APPNET</em></span></strong> 値を選択します。</li>
    <li>Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。
    <ol>
    <li><a href="https://ms.portal.azure.com/">Azure ポータル</a>にログオンします。</li>
    <li>左のナビゲーション ウィンドウで、<strong><span class="label">仮想ネットワーク</span></strong>をクリックします。</li>
    <li>使用する仮想ネットワークの名前をクリックします。</li>
    <li><strong><span class="label">構成</span></strong>をクリックします。 仮想ネットワークに関する詳細は、ページに記載されています。</li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

11. **完了** をクリックします。 **環境の展開** パネルが再表示されます。
12. 配置される仮想マシンの数とサイズが一覧表示されます。 必要に応じて、仮想マシンの数とサイズを変更します。
    -   この環境で各仮想マシンにインストールされているソフトウェアの詳細については、[Azure での Microsoft Dynamics AX 2012 R3 配置の計画](plan-2012-r3-deployment-azure.md) を参照してください。
    -   仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](http://azure.microsoft.com/en-us/pricing/details/virtual-machines/) を参照してください。

13. ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。 次に、チェック ボックスを選択して、条件に同意することを示します。
14. **次へ** をクリックします。
15. **展開**をクリックして、環境を展開する準備が整ったことを確認します。 配置には数時間かかる場合があります。 配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。 (これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。 配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の**詳細**ペインに表示されます。

## <a name="5-prepare-the-retail-mobility-devtest-environment-for-use"></a>5. 使用する Retail mobility 開発/テスト環境の配置
Retail Mobility 開発/テスト環境が Azure に配置されたので、オンプレミスまたは Azure に存在する Dynamics AX 環境に接続できます。 詳細については、以降のセクションを参照してください。

### <a name="prerequisites"></a>前提条件

以下の手順を実行する前に、次の条件が満たされていることを確認します。

| 前提条件                                                                                                                                                     | 詳細情報                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dynamics AX アプリケーション オブジェクト サーバー (AOS)、データベース、およびクライアントを設定して構成します。 前述のように、Dynamics AX はオンプレミスまたは Azure にインストールできます。 | [Microsoft Dynamics AX のシステム設定](http://technet.microsoft.com/library/e9256fe4-888c-413e-aa35-53e1a6de5806(AX.60).aspx)                                                                                                                                                                                        |
| Dynamics AX にデータをインポートします。                                                                                                                                    | Dynamics AX 環境にサンプル データをインストールする場合は、データ転送テスト ツールを使用してサンプル データをインストールします。 手順については、[Microsoft Dynamics AX 2012 用のテスト データ転送ツール (ベータ版)](test-data-transfer-tool-beta-2012.md) を参照してください。 |
| Async Server を設定およびコンフィギュレーションします。                                                                                                                               | [Commerce Data Exchange: Async Server](http://technet.microsoft.com/library/8f802c2f-37bc-4a5c-805e-bece3640245f(AX.60).aspx)                                                                                                                                                                                          |
| Real-time Service を設定およびコンフィギュレーションします。                                                                                                                          | [Commerce Data Exchange: Real-time Service](http://technet.microsoft.com/library/7dc09b26-47ba-403e-9b69-a61601d46bae(AX.60).aspx)                                                                                                                                                                                     |
| Commerce Data Exchange のメタデータを同期します。                                                                                                                        | [小売用スケジューラのパラメーターを入力する](http://technet.microsoft.com/library/bfe69872-8fb9-41d9-8f61-d206055dbd87(AX.60).aspx)                                                                                                                                                                                         |
| Retail サーバーの一般公開 URL を使用して、Retail サーバーのチャネル プロファイルを作成します。                                                                | [チャンネル プロファイルの設定](http://technet.microsoft.com/library/4ef00ad9-9da2-4d21-b3e1-637f77cab208(AX.60).aspx)                                                                                                                                                                                                      |

### 

### <a name="complete-configuration-tasks-on-the-aos-servervirtual-machine"></a>AOS サーバー/仮想機械でコンフィギュレーション タスクを完了する

AOS がインストールされているサーバーまたは仮想マシンにログオンし、次の手順を実行します。

1.  サーバーまたは仮想マシンのエンドポイントを設定します。 仮想マシンのエンドポイントを設定する方法については、[ブログ投稿](https://blogs.msdn.microsoft.com/axsupport/2014/06/27/connecting-retail-components-on-an-external-computer-to-the-microsoft-dynamics-ax-r3-azure-lifecycle-services-demo-virtual-machine/) の「はじめに」セクションを参照してください。
2.  リアルタイム サービスをコンフィギュレーションし、プロファイルを更新します。 手順については、この [ブログ投稿](https://blogs.msdn.microsoft.com/axsupport/2014/06/27/connecting-retail-components-on-an-external-computer-to-the-microsoft-dynamics-ax-r3-azure-lifecycle-services-demo-virtual-machine/) の「Real-time Service のコンフィギュレーション」セクションを参照してください。
3.  チャンネル データベースを設定するためのスケジューラ ジョブを実行します。 手順については、この [ブログ投稿](https://blogs.msdn.microsoft.com/axsupport/2014/06/27/connecting-retail-components-on-an-external-computer-to-the-microsoft-dynamics-ax-r3-azure-lifecycle-services-demo-virtual-machine/)「チャンネル データベースを設定するスケジューラ ジョブを実行する」セクションを参照してください。

### <a name="complete-configuration-tasks-on-the-mobil-virtual-machine"></a>MOBIL 仮想機械でコンフィギュレーション タスクを完了する

**クラウド ホスト環境**ページから、Retail Mobility 開発環境を選択します。 その後右にスクロールし、**MOBIL-&lt;GUID&gt;** リンクをクリックして仮想マシンにログオンします。 マシンにログオンした後は、次の手順を実行します。

1.  自己署名証明書を使用する場合は、MOBI-&lt;GUID&gt; 仮想マシンに証明書をインストールします。 手順については、この [ブログ投稿](https://blogs.msdn.microsoft.com/axsupport/2014/06/27/connecting-retail-components-on-an-external-computer-to-the-microsoft-dynamics-ax-r3-azure-lifecycle-services-demo-virtual-machine/) 「外部マシンで証明書をインストール」セクションを参照してください。
2.  Async サーバーの URL を使用するように Async クライアントを更新します。 手順については、この [ブログ投稿](https://blogs.msdn.microsoft.com/axsupport/2014/06/27/connecting-retail-components-on-an-external-computer-to-the-microsoft-dynamics-ax-r3-azure-lifecycle-services-demo-virtual-machine/) の「CDX Async Client のインストール」セクションを参照してください。
3.  ポート 35080 用にエンドポイントを設定します。 仮想マシンのエンドポイントを設定する方法については、[ブログ投稿](https://blogs.msdn.microsoft.com/axsupport/2014/06/27/connecting-retail-components-on-an-external-computer-to-the-microsoft-dynamics-ax-r3-azure-lifecycle-services-demo-virtual-machine/) の「はじめに」セクションを参照してください。
4.  ポート 35080 を除外する場合は、Windows ファイアウォールをコンフィギュレーションします。 Windows ファイアウォールの詳細については、Windows ドキュメントを参照してください。

### <a name="install-modern-pos-on-external-devices"></a>外部デバイスに Modern POS をインストールします。

Dynamics AX は、Modern POS、PC の販売時点管理アプリ、タブレットおよび携帯電話を含みます。 インストールする方法の詳細については、[Retail Modern POS のインストール](https://technet.microsoft.com/EN-US/library/dn741434.aspx) を参照してください。

## <a name="6-learn-more-about-the-service-accounts-for-this-environment"></a>6. この環境のサービス アカウントに関する詳細
次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。

### <a name="domain-accounts"></a>ドメイン アカウント

次のテーブルに、環境を配置したときに作成されたドメイン アカウントを示します。 環境を配置したときに、これらのアカウントのパスワードを入力している場合があります。 持っていない場合は、パスワードを変更することをお勧めします。

| ドメイン アカウント                  | 説明                                                                                                                  |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <DomainName>SQLServiceUser      | 次のサービスを SQL で実行するために使用されるアカウント -<GUID> 仮想マシン: SQL Server Analysis Services (MSSQLSERVER)。 |
| <DomainName>DynamicsInstallUser | Dynamics AX をインストールするために使用するアカウント。                                                                                     |
| <DomainName>RetailServiceUser   | 次のサービスを実行するために使用されるアカウント: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。        |

> [!NOTE]
> 既定のパスワードは、[Lifecycle Services](https://lcs.dynamics.com/) の **クラウド ホスト 環境** ページに表示されます。

### <a name="local-administrator-accounts"></a>ローカル管理者アカウント

配置した各仮想マシンには、ローカル Administrator アカウントがあります。 このアカウントは builtinaxlocaladmin です。 ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lcs.dynamics.com/) の **クラウド ホスト 環境** ページに表示されます。




