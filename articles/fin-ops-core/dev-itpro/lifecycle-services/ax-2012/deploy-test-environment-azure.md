---
title: Azure でのテスト環境の配置
description: このトピックでは、Microsoft Azure でのテスト環境の配置方法について説明します。
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13281
ms.assetid: 861f276d-adeb-4591-b53f-beafd1b77999
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 38ab92da173f2e9485ba8c24536080d57a6edc4b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812064"
---
# <a name="deploy-test-environments-on-azure"></a>Azure でのテスト環境の配置

[!include [banner](../../includes/banner.md)]

<a name="prerequisites"></a>必要条件
-------------

この記事の手順を実行する前に、次の条件が満たされていることを確認します。

|                |                                                                                                                                                                 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **カテゴリ**   | **前提条件**                                                                                                                                                |
| 必要なタスク | [Azure で AX 2012 R3 の配置を計画する](plan-2012-r3-deployment-azure.md) |



## <a name="1-log-on-to-lifecycle-services"></a>1. ライフサイクル サービスにログオンする
Microsoft Dynamics Lifecycle Services は、顧客およびパートナーが Microsoft Dynamics AX の管理に使用できるクラウドベースの共同ワークスペースです。 Azure に AX 2012 R3 を配置するには、この Web サイトを使用します。 Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。 CustomerSource または PartnerSource の資格情報でアクセスすることができます。 [Lifecycle Services にログオン](https://lcs.dynamics.com/en/)

## <a name="2-create-a-project"></a>2. プロジェクトの作成
Lifecycle Services にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。 プロジェクトは、Lifecycle Services でのエクスペリエンスの主な開催者です。 プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。

## <a name="3-connect-the-project-to-your-azure-subscription"></a>3. Azure サブスクリプションにプロジェクトを接続する
Azure サブスクリプションに Lifecycle Services プロジェクトを接続します。 これにより、Lifecycle Services は AX 2012 R3 環境をサブスクリプションに展開できます。 Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。 プロジェクトは 1 つの Azure サブスクリプションにだけ接続できることに留意してください。 複数の Azure サブスクリプションがある場合、この手順を実行する前にどのサブスクリプションを使用するかを必ず識別します。

1.  **クラウド ホスト環境**をクリックします。 **クラウド ホスト環境** ページが表示されます。
2.  **Microsoft Azure 設定**パネルが画面の横に表示されます。 表示されない場合は、**Microsoft Azure 設定**をクリックします。
3.  Azure サブスクリプション ID を入力します。 サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。
    1.  ブラウザの別のインスタンスを開きます。
    2.  **Azure 管理ポータル**にログオンします。
    3.  左のナビゲーション ウィンドウで、**設定**をクリックします。 (**設定**リンクを表示するには、ナビゲーションペインの一番下までスクロールしなければならない場合があります。) **設定**ページが表示されます。
    4.  サブスクリプション ID をコピーして、Lifecycle Services の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。

4.  **次へ** をクリックします。
5.  **ダウンロード**をクリックして管理証明書をダウンロードします。 この管理証明書により、Lifecycle Services はお客様の代わりに Azure と通信できます。 既定では、管理証明書はコンピューターのダウンロード フォルダーに保存され、LifecycleServicesDeployment.cer という名前が付きます。
6.  管理証明書を Azure にアップロードします。 そのためには、次の手順を実行します。
    1.  ブラウザの別のインスタンスを開きます。 (または、手順 3 で開いた可能性のあるブラウザインスタンスに移動します。)
    2.  **Azure 管理ポータル**にログオンします。
    3.  左のナビゲーション ウィンドウで、**設定**をクリックします。 **設定** ページが表示されます。
    4.  **管理証明書**をクリックします。
    5.  ページの下部にある**アップロード**をクリックします。
    6.  **管理証明書をアップロード** ウィンドウで、手順 5 でダウンロードした管理証明書を参照します。 その後、チェック マークをクリックします。

7.  Lifecycle Services で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。 **次へ** をクリックします。
8.  最も近い地域を選択します。 AX 2012 R3 環境は、この領域のデータ センターに配置されます。
9.  **接続** をクリックします。 これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。 プロジェクトを間違った Azure サブスクリプション (複数の Azure サブスクリプションがあると仮定した場合) に接続していることが分かった場合、プロジェクトを削除し、新しいプロジェクトを作成し、新しいプロジェクトを適切な Azure サブスクリプションに接続させるためのこの手順を繰り返す必要があります。

## <a name="4-connect-your-corporate-network-to-the-azure-virtual-network"></a>4. 会社のネットワークを Azure 仮想ネットワークに接続する
次のセクションでは、企業ユーザーが AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。 企業の資格情報を使用してこれらのシステムにログインする必要がある場合、環境を配置する前に接続を設定することを推奨します。 これには、Azure のネットワーク機能を使用して企業ネットワークを 1 つ以上の Azure 仮想ネットワークに拡張する必要があります。 さらに、Azure 仮想ネットワークに Active Directory を配置する必要があり、これは会社の Active Directory に対する信頼のために設定されます。 この Active Directory は、Azure 仮想ネットワーク内の VM 関連リソースを管理するために適用されます。 この Active Directory はシングルサインオンには使用されません。社内ディレクトリを同期するように設定しないでください。 シングル サインオン機能は、ドメインの信頼関係を通じて提供されます。

### <a name="create-a-site-to-site-vpn-connection"></a>サイト間 VPN 接続を作成する

企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。 これを行う方法の詳細については、以下を参照してください。

-   [仮想ネットワークの概要](https://msdn.microsoft.com/library/windowsazure/jj156007.aspx)
-   [仮想ネットワークのコンフィギュレーション タスク](https://msdn.microsoft.com/library/jj156206.aspx)
-   [テスト用にシミュレーションしたハイブリッド クラウド環境を設定する](http://azure.microsoft.com/documentation/articles/virtual-networks-setup-simulated-hybrid-cloud-environment-testing/)
-   [Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN](https://msdn.microsoft.com/library/dn636917.aspx)
-   [管理ポータルに仮想ネットワーク ゲートウェイを構成する](https://msdn.microsoft.com/library/azure/jj156210.aspx)

### <a name="create-an-active-directory-account-in-azure"></a>Azure の Active Directory アカウントの作成

Active Directory は Azure 仮想ネットワークに必須です。 Active Directory は Azure 仮想ネットワークに配置できます。 [Azure 仮想マシンに Windows Server Active Directory を展開するためのガイドライン](https://msdn.microsoft.com/library/azure/jj156090.aspx)に従ってください。 Active Directory フェデレーション サービスは現在 AX 2012 R3 でサポートされていないことに注意してください。 Active Directory を提供する場合は、LCS 展開サービスで使用できる範囲で次のサービス アカウントを作成する必要があります。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>勘定</strong></td>
<td><strong>説明</strong></td>
</tr>
<tr class="even">
<td>&lt;DomainName&gt;AXServiceUser</td>
<td>AX 2012 R3 サービス アカウント</td>
</tr>
<tr class="odd">
<td>&lt;DomainName&gt;AOSServiceUser</td>
<td>AOS サービス アカウント</td>
</tr>
<tr class="even">
<td>&lt;DomainName&gt;BCProxyUser</td>
<td>Business Connector プロキシ アカウント</td>
</tr>
<tr class="odd">
<td>&lt;DomainName&gt;SPServiceUser</td>
<td>SharePoint サービス アカウント</td>
</tr>
<tr class="even">
<td>&lt;DomainName&gt;SqlServiceUser</td>
<td>SQL Server サービス アカウント</td>
</tr>
<tr class="odd">
<td>&lt;DomainName&gt;DynamicsInstallUser</td>
<td>AX 2012 R3 インストール アカウント </br>
    <strong>注記:</strong> このアカウントは、コンピューターをドメインに参加させるためのアクセス許可を持つ必要があります。 このアカウントにアクセス許可を与えるには、次の手順を実行します。
<ol>
<li><strong>開始</strong>をクリックし、dsa.msc 型で<strong>実行</strong>をクリックし、 <strong>OK</strong> をクリックします。</li>
<li>作業ウィンドウで、ドメイン ノードを展開します。</li>
<li>変更する組織単位を検索し、右クリックしてから<strong>デリゲート コントロール</strong>をクリックします。</li>
<li><strong>コントロールのデリゲート ウィザード</strong>で、<strong>次へ</strong>をクリックします。</li>
<li>特定のユーザーまたは特定のグループを一覧に追加するには、<strong>追加</strong>をクリックし、次に <strong>次へ</strong>をクリックします。</li>
<li><strong>委任するタスク</strong> ページで、<strong>委任するカスタム タスクを作成</strong>をクリックしてから、<strong>次へ</strong>をクリックします。</li>
<li><strong>フォルダ内の次のオブジェクトのみ</strong>をクリックし、一覧から<strong>コンピューター オブジェクト</strong> チェック ボックスをクリックして選択します。 その後、リスト下部で <strong>このフォルダーの選択したオブジェクトを作成する</strong> および <strong>このフォルダーの選択したオブジェクトを削除する</strong> の各チェック ボックスを選択します。</li>
<li><strong>次へ</strong> をクリックします。</li>
<li><strong>アクセス許可</strong>リストで、次のチェック ボックスをクリックしてオンにします。
<ul>
<li><strong>パスワードのリセット</strong></li>
<li><strong>アカウントの制限の読み取りと書き込み</strong></li>
<li><strong>DNS ホスト名への検証済みの書き込み</strong></li>
<li><strong>サービス プリンシパル名への検証済みの書き込み</strong></li>
</ul></li>
<li><strong>次へ</strong>をクリックし、<strong>完了</strong>の順にクリックします。</li>
<li><strong>Active Directory ユーザーおよびコンピューター MMC スナップイン</strong>を閉じます。</li>
</ol></td>
</tr>
</tbody>
</table>

環境を配置するとき、これらのアカウントのパスワードを入力する必要があります。

### <a name="create-a-domain-trust"></a>ドメイン信頼の作成

企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。 信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/library/cc754626.aspx)」を参照してください。 このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。

### <a name="give-the-administrators-group-the-right-to-log-on-as-a-batch-job"></a>バッチ ジョブとしてログオンする権限を管理者グループに付与します

Active Directory ドメイン コントローラーにログインし、次の手順を完了して、ビルトイン Administrator グループにバッチ ジョブとしてログオンする権利を付与します。

1.  **開始**、**すべてのプログラム**の順にクリックし、**管理ツール**をクリックします。
2.  **管理ツール** メニューで、**グループ ポリシーの管理**を選択します。
3.  **グループ ポリシー管理**コンソール ツリーで、**フォレスト: &lt;ServerName&gt;** をクリックしてから、**ドメイン**をクリックします。
4.  サーバーの名前をクリックし、**ドメイン コントローラー**を展開します。**既定のドメイン コント ローラー ポリシー**を右クリックし、**編集**をクリックします。
5.  **グループ ポリシー管理エディター**で、**既定のドメイン コントローラ ポリシー &lt; ServerName &gt; ポリシー**とクリックし、**コンピューターの構成**を展開してから**ポリシー**をクリックします。
6.  **ポリシー** ツリーで、**Windows 設定**を展開してから**セキュリティの設定**をクリックします。
7.  **セキュリティの設定**ツリーで、**ローカル ポリシー**を展開してから**ユーザーの権限の割り当て**をクリックします。
8.  結果ウィンドウで、スクロールして**バッチ ジョブとしてログオン**をクリックします。
9.  **バッチ ジョブとしてログオン プロパティ** ダイアログ ボックスで、**ユーザーまたはグループの追加**をクリックします。
10. **ユーザーまたはグループの追加**ダイアログ ボックスで、**参照**をクリックします。
11. **ユーザー、コンピュータ、またはグループの選択**ダイアログ ボックスで、**管理者**と入力します。
12. **名前の確認**をクリックして、あらかじめ登録された Administrator アカウントが表示されていることを確認し、**OK** を 3 回クリックします。

### <a name="change-the-default-organizational-unit"></a>既定の組織単位の変更

仮想マシンをカスタム組織単位 (デフォルトの組織単位と比較して) の Active Directory に追加する場合は、展開を開始する前に Active Directory 内の既定の組織単位を変更できます。 詳細については、[ここ](http://pc-addicts.com/server-2012-change-default-ou/) をクリックしてください。

## <a name="5-deploy-a-test-environment-on-azure"></a>5. Azure でのテスト環境の配置
Azure にテスト環境を配置するには、以下の手順に従ってください。

1. **クラウド ホスト環境**ページで、追加 (+) アイコンをクリックします。
2. **環境のトポロジの選択**パネルで、**開発/テスト**を選択します。
3. **テスト** をクリックします。
4. **環境名**フィールドに、配置される環境の名前を入力します。
5. **詳細設定**をクリックします。
6. ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。 情報を入力するには、次の表を使用してください。
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td><strong>以下を行う場合:</strong></td>
   <td><strong>手順</strong></td>
   </tr>
   <tr class="even">
   <td>Azure で環境用に新しいドメインを作成する</td>
   <td><ol>
   <li><strong>新規ドメイン</strong>をクリックします。</li>
   <li>ドメイン名を入力します。 既定では、ドメインは <em>contoso.com</em> と呼ばれます。</li>
   </ol></td>
   </tr>
   <tr class="odd">
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
   - 有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含ている必要があります: \['@', '!', '=', '\*'\] 次のような分かりやすいパスワードを使用することはできません: pass@word1

8. 使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン**をクリックします。 既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。 CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。
9. 仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。 一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。 名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。 インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。 仮想マシン名は 13 文字またはそれ以下にする必要があります。 インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。 例: ACustomVMName-99。仮想マシン インスタンスが最初の展開後に環境へ追加されると、展開サービスは中断した仮想マシン名のインクリメントを開始します。 たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。 もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。 展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。 これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。
10. リモート デスクトップ サービスの仮想マシンを配置することを選択した場合、**リモート デスクトップ サービスをカスタマイズ**をクリックし、ユーザーが web 経由で AX 2012 R3 にアクセスする方法を指定します。 次のオプションのいずれかを選択します。
    -   **リモート デスクトップ:** このオプションはユーザーの完全なリモート デスクトップへのログインを有効にします。
    -   **RemoteApp プログラム**: このオプションを使用すると、完全なデスクトップウィンドウを使用しなくても、ユーザは直接 AX 2012 R3 にログインできます。 RemoteApp は既定で有効になります。

    環境が配置されると、**クラウド ホスト環境**ページで次のリンクが使用できます:
    -   **RDS Web アクセス証明書**: これは、RDS Web アクセス サイトへの安全なアクセスを許可するために提供される自己署名証明書です。 リンクをクリックしてこの証明書を開き、RDS Web アクセス サイトにアクセスする前に、**ローカル コンピューター**&gt;**信頼済ルート証明機関**にインストールします。 この環境を生産能力に配置する前に、RDS クラスターに自分の証明書をインストールすることをお勧めします。
    -   **RDS Web アクセス**: これにより、ユーザはウェブ上で AX 2012 R3 環境にアクセスできます。 **リモート デスクトップ** オプションを選択すると、ユーザーは完全なリモート デスクトップにログインできます。 **RemoteApp プログラム** を選択すると、ユーザーが AX 2012 R3 に直接ログインできます。
    -   **RDS ファーム アクセス**: これにより、ユーザは VPN 接続されたネットワークで AX 2012 R3 環境にアクセスできます。 この機能は、次の場合にのみ利用できます。
        1.  この AX の配置を VPN 接続されている会社のドメインに結合しました。
        2.  VPN 接続されたネットワークからの接続を受け入れるように RDS ゲートウェイをコンフィギュレーションしました。

    > [!NOTE]
    > **RDS Web アクセス**および **RDS Farm アクセス**の両方で、既存の Active Directory ドメインに配置を結合する際には、内部ロード バランサーの IP アドレスを使用して、AD/DNS に RDS ファームを追加する必要があります。 次の手順を参照してください。
  
    1.  RDS ファームの名前を取得します。これは、LCS の RDS ファーム アクセス リンクから入手できます。 この場合、**RdsFarm0c0fa75** とする必要があります。

        [![MachineName](./media/machinename-300x165.png)](./media/machinename.png)

    2.  Azure ポータルでクラウド サービス ダッシュ ボードから内部ロード バランサの IP を取得します。 ポート **3389** の横に内部 IP がある RDS マシンを検査します。 以下の例では、内部ロード バランサーの IP は 10.1.3.4 です。

        [![IP アドレス](./media/ip-address-144x300.png)](./media/ip-address.png)

    3.  上記で取得した情報を使用して、AD のコンピューターとして RDS フォームを追加します。

        [![AddToAD](./media/addtoad-300x113.png)](./media/addtoad.png)

    これらの手順を実行しないと、RD Web アクセスを実行する際に次のエラーが発生します。*リモート デスクトップには、コンピューター「RdsFarm0c0fa75.contoso.com」が見つかりません。これは、「RdsFarm0c0fa75.contoso.com」が指定されたネットワークに属していないことを意味する可能性があります。接続しようとしているコンピュータ名およびドメインを確認してください。*
11. 仮想ネットワークの設定をカスタマイズするには、<strong>仮想ネットワークをカスタマイズする</strong> をクリックします。 情報を入力するには、次の表を使用してください。
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>以下を行う場合:</strong></td>
    <td><strong>手順</strong></td>
    </tr>
    <tr class="even">
    <td>Azure で環境用に新しい仮想ネットワークを作成する</td>
    <td><ol>
    <li><strong>新しい仮想ネットワーク</strong>をクリックします。</li>
    <li>仮想ネットワーク名を入力します。</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Azure の既存の仮想ネットワークへの環境の追加</td>
    <td><ol>
    <li><strong>既存の仮想ネットワーク</strong>をクリックします。</li>
    <li>使用する既存の仮想ネットワークの名前を選択してください。</li>
    <li><strong>アドレス空間</strong> フィールドには、適切な値が自動的に表示されます。 提供された値を選択します。</li>
    <li><strong>アプリケーション サブネット名</strong> フィールドには、使用可能なオプションが表示されます。 Lifecycle Services によって以前に展開した広告に配置する場合は、選択した <strong><em>APPNET</em></strong> 値を選択します。</li>
    <li>Active Directory サブネットを入力する必要があり、ターゲットとする AD の Azure 管理ポータルにある Active Directory サブネット IP/範囲と一致している必要があります。
    <ol>
    <li><a href="https://manage.windowsazure.com/"><span style="color: #0066cc">Azure 管理ポータル</span></a>へのログオン</li>
    <li>左のナビゲーション ウィンドウで、<strong>ネットワーク</strong>をクリックします。</li>
    <li>使用する仮想ネットワークの名前をクリックします。</li>
    <li><strong>構成</strong>をクリックします。</li>
    </ol>
仮想ネットワークに関する詳細は、ページに記載されています。</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

12. **完了** をクリックします。 **環境の展開** パネルが再表示されます。
13. 配置される仮想マシンの数とサイズが一覧表示されます。 必要に応じて、仮想マシンの数とサイズを変更します。
    -   この環境で各仮想マシンにインストールされているソフトウェアの詳細については、 [Azure 上での AX 2012 R3の 配置計画](plan-2012-r3-deployment-azure.md) を参照してください。
    -   仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](http://azure.microsoft.com/pricing/details/virtual-machines/) を参照してください。

14. ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。 次に、チェック ボックスを選択して、条件に同意することを示します。
15. **次へ** をクリックします。
16. 環境を展開する準備が整った**確認するための展開**をクリックします。 配置には数時間かかる場合があります。 配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。 (これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。 配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。

## <a name="6-prepare-ax-2012-r3-for-use"></a>6. 使用する AX 2012 R3 の準備
環境が Azure に配置されたので、使用するために AX 2012 R3 を設定し、コンフィギュレーションする必要があります。 詳細については、以降のセクションを参照してください。

### <a name="log-on-to-the-aos-virtual-machine"></a>AOS 仮想マシンへのログオン

AOS-&lt;GUID&gt; 仮想マシンに &lt;DomainName&gt;DynamicsInstallUser アカウントを使用してログオンします。 手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。 [Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。

### <a name="compile-ax-2012-r3"></a>AX 2012 R3 のコンパイル

AxBuild.exe. を使用した AX 2012 R3 のコンパイル 手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/library/dn528954.aspx) を参照してください。

### <a name="initialize-ax-2012-r3"></a>AX 2012 R3 の初期化

AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。 手順については、[初期化チェックリスト](https://technet.microsoft.com/library/aa497061.aspx) を参照してください。

### <a name="install-sample-data"></a>サンプル データのインストール

サンプル データを環境にインストールする場合は、次の手順を実行します。

1.  SQL-&lt;GUID&gt; 仮想マシンにログオンします。 DynamicsInstallUser アカウントを使用して仮想マシンにログオンします。 手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。 [Azure で AX 2012 R3 配置を管理する](manage-2012-r3-deployment-azure.md) を参照してください。
2.  仮想マシンで次の場所に移動します: F:TestTransferTool
3.  テスト データ転送ツールをインストールします。 手順については、 [テスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md) を参照してください。
4.  コマンド プロンプトを開いて、次の場所にアクセスします: C:\Program Files (x86) \Microsoft Dynamics AX 2012 テスト データ確認転送ツール (ベータ)
5.  次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx

> [!NOTE]
> サンプル データには、AX 2012 R3 の試用版のライセンス キーが含まれています。 サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます

### <a name="give-users-access"></a>ユーザーのアクセス許可を付与します

ユーザが AX 2012 R3 にアクセスできるようにするには、以下のタスクを実行します。

-   CLI- &lt;GUID&gt; 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。
-   ユーザーに AX 2012 R3 へのアクセス許可を付与します。 手順については、[Microsoft Dynamics AX で新しいユーザーを作成する](https://technet.microsoft.com/library/aa548139.aspx)を参照してください。

> [!NOTE]
> VPN接続とドメインの信頼を作成しない場合でも、ユーザーに AX 2012 R3 へのアクセス権を与えることができます。 これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。 その後、上記の 2 つのタスクを完了する必要があります。

### <a name="set-up-and-configure-ax-2012-r3"></a>AX 2012 R3 の設定およびコンフィギュレーション

Azure 上で AX 2012 R3 を設定およびコンフィギュレーションする手順は、オンプレミス展開の設定およびコンフィギュレーションに使用される手順と同じです。 詳細については、次のリソースを参照してください。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>タスク</strong></td>
<td><strong>リソース</strong></td>
</tr>
<tr class="even">
<td>TechNet の手順を参照してください。</td>
<td><ul>
<li><a href="https://technet.microsoft.com/library/gg732218.aspx">Microsoft Dynamics AX のシステム設定</a></li>
<li><a href="https://technet.microsoft.com/library/gg732158.aspx">Microsoft Dynamics AX クライアント</a></li>
<li><a href="https://technet.microsoft.com/library/gg731868.aspx">Application Object Server</a></li>
<li><a href="https://technet.microsoft.com/library/ee873263.aspx">Microsoft Dynamics AX でのレポート</a></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><strong>メモ</strong></td>
</tr>
<tr class="even">
<td><a href="https://technet.microsoft.com/library/dd309703.aspx">既定のレポートを展開</a>し、ユーザーに<a href="https://technet.microsoft.com/library/aa496432.aspx">アクセス権を付与</a>してください。</td>
</tr>
</tbody>
</table>
<ul>
<li><a href="https://www.microsoft.com/download/details.aspx?id=5916">Management Reporter 2012</a></li>
<li><a href="https://technet.microsoft.com/library/ee873272.aspx"> Microsoft Dynamics AX での分析</a></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><strong>メモ</strong></td>
</tr>
<tr class="even">
<td>AX 2012 R3 に含まれているキューブを処理するには、ExternalCommandTimeout 値を 7200 に増やすことをお勧めします。</td>
</tr>
</tbody>
</table>
<ul>
<li><a href="https://technet.microsoft.com/library/gg866975.aspx">ヘルプ サーバー</a></li>
<li><a href="https://technet.microsoft.com/library/gg751374.aspx">エンタープライズ ポータルおよびロール センター</a></li>
</ul>
<table>
<tbody>
<tr class="odd">
<td><strong>メモ</strong></td>
</tr>
<tr class="even">
<td>エンタープライズ ポータルはポート 81 で実行するように設定されているため、ファイアウォール設定でそのポートを除外してください。</td>
</tr>
</tbody>
</table>
<ul>
<li><a href="https://technet.microsoft.com/library/gg731850.aspx">エンタープライズ検索</a></li>
<li><a href="https://technet.microsoft.com/library/gg731810.aspx">サービス & アプリケーション統合フレームワーク (AIF)</a></li>
<li><a href="https://technet.microsoft.com/library/jj710398.aspx">Microsoft Dynamics AX Retail IT プロおよび開発者向け</a></li>
<li><a href="https://technet.microsoft.com/library/aa834453.aspx">.NET Business Connector</a></li>
<li><a href="https://technet.microsoft.com/library/gg731779.aspx">セキュリティ</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>印刷可能なガイドおよびホワイト ペーパーの表示</td>
<td><ul>
<li><a href="https://technet.microsoft.com/library/gg732268.aspx">印刷可能なガイド</a></li>
<li><a href="https://technet.microsoft.com/library/gg188985.aspx">システム管理者向けのホワイト ペーパー</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Microsoft Dynamics AX ウェブ検索ツールの使用</td>
<td><ul>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=212924">開発者用の Web 検索</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=212925">システム管理者用の Web 検索</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=212922">アプリケーション ユーザー用の Web 検索</a></li>
<li><a href="http://go.microsoft.com/fwlink/?LinkID=194311">結合された Web 検索</a></li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="7-learn-more-about-the-service-accounts-for-this-environment"></a>7. この環境のサービス アカウントに関する詳細
次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。

### <a name="domain-accounts"></a>ドメイン アカウント

次のテーブルに、環境を配置したときに作成されたドメイン アカウントの既定の名前を示します。

| ドメイン アカウント                  | 説明                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <DomainName>AOSServiceUser      | 次のサービスを AOS-<GUID> 仮想マシンで実行するために使用されたアカウント: Microsoft Dynamics AX Object Server。                                                                                                                                                                                                                                      |
| <DomainName>SQLServiceUser      | 次のサービスを SQL で実行するために使用されるアカウント -<GUID> 仮想マシン: SQL Server Analysis Services (MSSQLSERVER)。                                                                                                                                                                                                                                |
| <DomainName>DynamicsInstallUser | AX 2012 R3 をインストールするために使用したアカウント。                                                                                                                                                                                                                                                                                                                  |
| <DomainName>SPServiceUser       | 次のサービスを EP-<GUID> 仮想マシンで実行するために使用したアカウント - : AppFabric、SharePoint Search Host Controller、SharePoint Server Search 15、SharePoint Timer Service、および SharePoint User Code Host。                                                                                                                                         |
| <DomainName>BCProxyUser         | ビジネス コネクタ プロキシとして使用されるアカウント。                                                                                                                                                                                                                                                                                                        |
| <DomainName>AXServiceUser       | AOS<GUID> 仮想マシンで次のサービスを実行するためにアカウントが使用されます: Microsoft Dynamics AX Data Import/Export Framework Service および Microsoft Dynamics ERP RapidStart Connector。 アカウントは、次のサービスを CLI-<GUID> 仮想マシンで実行するためにも使用されます: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。 |

> [!NOTE] 
> パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) のクラウド ホスト環境ページに表示されます。



### <a name="local-administrator-accounts"></a>ローカル管理者アカウント

配置した各仮想マシンには、ローカル Administrator アカウントがあります。 このアカウントは builtinaxlocaladmin です。 ローカル管理者アカウントのパスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) の クラウド ホスト 環境ページに表示されます。



