---
title: Azure での高可用性環境の配置
description: この記事では、Microsoft Azure に高可用性環境を展開する方法について説明します。 環境を展開するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 21231
ms.assetid: c53d7b21-1638-41a8-826b-89105d2e51e8
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: af384c62339800b55546bcc830602e10ad41812f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537422"
---
# <a name="deploy-high-availability-environments-on-azure"></a>Azure での高可用性環境の配置

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Azure に高可用性環境を展開する方法について説明します。 環境を展開するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。 

<a name="prerequisites"></a>必要条件
-------------

この記事の手順を実行する前に、次の条件が満たされていることを確認します。

|                |                                                                                                                                                                 |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **カテゴリ**   | **前提条件**                                                                                                                                                |
| 必要なタスク | [Azure 上での Microsoft Dynamics AX 2012 R3 の配置計画](plan-2012-r3-deployment-azure.md) |



## <a name="1-use-azure-premium-storage"></a>1. Azure premium storage を使用する
Azure Premium Storage は、Azure 仮想マシン (VM) 上で実行される I/O 集約型ワークロードに対して高パフォーマンス、待機時間が短いディスク サポートを提供します。 Premium Storage では、アプリケーションは VM ごとに 32 TB までのストレージを持つことができ、VM ごとに 50,000 IOPS (秒単位の入力/出力オペレーション) を達成し、読み取り操作での待機時間は非常に短くなります。 一貫したパフォーマンスを確保するため、Azure で AX 2012 R3 を実行するには Premium Storage をお勧めします。 Premium Storage の使用方法の詳細については、[Azure で Microsoft Dynamics AX 2012 R3 の配置を計画](plan-2012-r3-deployment-azure.md)を参照してください。

## <a name="2-log-on-to-lifecycle-services"></a>2. ライフサイクル サービスにログオンする
Microsoft Dynamics Lifecycle Services は、顧客およびパートナーが Microsoft Dynamics AX の管理に使用できるクラウドベースの共同ワークスペースです。 Azure に AX 2012 R3 を配置するには、この Web サイトを使用します。 Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。 CustomerSource または PartnerSource の資格情報でアクセスすることができます。 [Lifecycle Services にログオン](https://lcs.dynamics.com/en/)

## <a name="3-create-a-project"></a>3. プロジェクトの作成
Lifecycle Services にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。 プロジェクトは、Lifecycle Services でのエクスペリエンスの主な開催者です。 プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。

## <a name="4-connect-the-project-to-your-azure-subscription"></a>4. Azure サブスクリプションにプロジェクトを接続する
Azure サブスクリプションに Lifecycle Services プロジェクトを接続します。 これにより、Lifecycle Services は AX 2012 R3 環境をサブスクリプションに展開できます。 Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。 プロジェクトは 1 つの Azure サブスクリプションにだけ接続できることに留意してください。 複数の Azure サブスクリプションがある場合、この手順を実行する前にどのサブスクリプションを使用するかを必ず識別します。

1.  **クラウド ホスト環境**をクリックします。 **クラウド ホスト環境** ページが表示されます。
2.  **Microsoft Azure 設定**パネルが画面の横に表示されます。 表示されない場合は、**Microsoft Azure 設定**をクリックします。
3.  Azure サブスクリプション ID を入力します。 サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。
    1.  ブラウザの別のインスタンスを開きます。
    2.  Azure 管理ポータルにログオンします。
    3.  左のナビゲーション ウィンドウで、**設定**をクリックします。 (**設定**リンクを表示するには、ナビゲーションペインの一番下までスクロールしなければならない場合があります。) **設定**ページが表示されます。
    4.  サブスクリプション ID をコピーして、Lifecycle Services の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。

4.  **次へ** をクリックします。
5.  **ダウンロード**をクリックして管理証明書をダウンロードします。 この管理証明書により、Lifecycle Services はお客様の代わりに Azure と通信できます。 既定では、管理証明書はコンピューターのダウンロード フォルダーに保存され、LifecycleServicesDeployment.cer という名前が付きます。
6.  管理証明書を Azure にアップロードします。 そのためには、次の手順を実行します。
    1.  ブラウザの別のインスタンスを開きます。 (または、手順 3 で開いた可能性のあるブラウザインスタンスに移動します。)
    2.  Azure 管理ポータルにログオンします。
    3.  左のナビゲーション ウィンドウで、**設定**をクリックします。 **設定** ページが表示されます。
    4.  **管理証明書**をクリックします。
    5.  ページの下部にある**アップロード**をクリックします。
    6.  **管理証明書をアップロード** ウィンドウで、手順 5 でダウンロードした管理証明書を参照します。 その後、チェック マークをクリックします。

7.  Lifecycle Services で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。 **次へ** をクリックします。
8.  最も近い地域を選択します。 AX 2012 R3 環境は、この領域のデータ センターに配置されます。
9.  **接続** をクリックします。 これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。 プロジェクトを間違った Azure サブスクリプション (複数の Azure サブスクリプションがあると仮定した場合) に接続していることが分かった場合、プロジェクトを削除し、新しいプロジェクトを作成し、新しいプロジェクトを適切な Azure サブスクリプションに接続させるためのこの手順を繰り返す必要があります。

## <a name="5-connect-your-corporate-network-to-the-azure-virtual-network"></a>5. 会社のネットワークを Azure 仮想ネットワークに接続する
次のセクションでは、企業ユーザーが AX 2012 R3 にアクセスできるように、Azure 仮想ネットワークとドメインを設定する方法について説明します。 企業の資格情報を使用してこれらのシステムにログインする必要がある場合、環境を配置する前に接続を設定することを推奨します。 これには、Azure のネットワーク機能を使用して企業ネットワークを 1 つ以上の Azure 仮想ネットワークに拡張する必要があります。 さらに、Azure 仮想ネットワークに Active Directory を配置する必要があり、これは会社の Active Directory に対する信頼のために設定されます。 この Active Directory は、Azure 仮想ネットワーク内の VM 関連リソースを管理するために適用されます。 この Active Directory はシングルサインオンには使用されません。社内ディレクトリを同期するように設定しないでください。 シングル サインオン機能は、ドメインの信頼関係を通じて提供されます。

### <a name="create-a-site-to-site-vpn-connection"></a>サイト間 VPN 接続を作成する

企業ユーザーが Azure 仮想ネットワーク内の仮想マシンのリソースにアクセスできるようにするには、Azure 仮想ネットワークとオンプレミス社内ネットワークの間にサイト間 VPN 接続を作成する必要があります。 これを行う方法の詳細については、以下を参照してください。

-   [仮想ネットワークの概要](https://msdn.microsoft.com/en-us/library/windowsazure/jj156007.aspx)
-   [仮想ネットワークのコンフィギュレーション タスク](https://msdn.microsoft.com/en-us/library/jj156206.aspx)
-   [テスト用にシミュレーションしたハイブリッド クラウド環境を設定する](http://azure.microsoft.com/en-us/documentation/articles/virtual-networks-setup-simulated-hybrid-cloud-environment-testing/)
-   [Windows Server 2012 ルーティングおよびリモート アクセスサービス (RRAS) を使用した Azure 仮想ネットワークのサイト間 VPN](https://msdn.microsoft.com/library/dn636917.aspx)
-   [管理ポータルに仮想ネットワーク ゲートウェイを構成する](https://msdn.microsoft.com/en-us/library/azure/jj156210.aspx)

### <a name="create-an-active-directory-in-azure"></a>Azure の Active Directory アカウントの作成

Active Directory は Azure 仮想ネットワークに必須です。 Active Directory は Azure 仮想ネットワークに配置できます。 [Azure 仮想マシンに Windows Server Active Directory を展開するためのガイドライン](https://msdn.microsoft.com/en-us/library/azure/jj156090.aspx)に従ってください。 Active Directory フェデレーション サービスは現在 AX 2012 R3 でサポートされていないことに注意してください。 Active Directory を提供する場合は、LCS 展開サービスで使用できる範囲で次のサービス アカウントを作成する必要があります。

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
<td>&lt;DomainName&gt;RetailServiceUser</td>
<td>小売サービス アカウント</td>
</tr>
<tr class="even">
<td>&lt;DomainName&gt;DynamicsInstallUser</td>
<td>AX 2012 R3 インストール アカウント <strong>注記:</strong> このアカウントは、コンピューターをドメインに参加させるためのアクセス許可を持つ必要があります。 このアカウントにアクセス許可を与えるには、次の手順を実行します。
<ol>
<li><strong>開始</strong>をクリックし、dsa.msc 型で<strong>実行</strong>をクリックし、 <strong>OK</strong> をクリックします。</li>
<li>作業ウィンドウで、ドメイン ノードを展開します。</li>
<li>変更する組織単位を検索し、右クリックしてから<strong>デリゲート コントロール</strong>をクリックします。</li>
<li><strong>コントロールのデリゲート</strong> ウィザードで、<strong>次へ</strong>をクリックします。</li>
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
<li><strong>Active Directory ユーザーおよびコンピューター MMC</strong> スナップインを閉じます。</li>
</ol></td>
</tr>
</tbody>
</table>

環境を配置するとき、これらのアカウントのパスワードを入力する必要があります。

### <a name="create-a-domain-trust"></a>ドメイン信頼の作成

企業ユーザーが Azure ドメイン内の仮想マシンのリソースにアクセスできるようにするには、ドメイン間で Active Directory のトラストを作成する必要があります。 信託の作成方法の詳細については、「[フォレスト信託の作成](https://technet.microsoft.com/en-us/library/cc754626.aspx)」を参照してください。 このプロセスは、2 つのオンプレミス ドメイン間で信頼関係を作成する場合と同じプロセスです。

### <a name="give-the-administrators-group-the-right-to-log-on-as-a-batch-group"></a>バッチ グループとしてログオンする権限を管理者グループに付与します

Active Directory ドメイン コントローラーにログインし、次の手順を完了して、ビルトイン Administrator グループにバッチ ジョブとしてログオンする権利を付与します。

1.  **開始**、**すべてのプログラム**の順にクリックし、**管理ツール**をクリックします。
2.  **管理ツール** メニューで、**グループ ポリシーの管理**を選択します。
3.  **グループ ポリシー管理コンソール** ツリーで、**フォレスト: &lt;ServerName&gt;** をクリックしてから、**ドメイン**をクリックします。
4.  サーバーの名前をクリックし、**ドメイン コントローラー**を展開します。**既定のドメイン コント ローラー ポリシー**を右クリックし、**編集**をクリックします。
5.  **グループ ポリシー管理エディター**で、**既定のドメイン コントローラ ポリシー &lt;ServerName&gt; ポリシー**とクリックし、**コンピューターの構成**を展開してから**ポリシー**をクリックします。
6.  **ポリシー** ツリーで、**Windows 設定**を展開してから**セキュリティの設定**をクリックします。
7.  **セキュリティの設定**ツリーで、**ローカル ポリシー**を展開してから**ユーザーの権限の割り当て**をクリックします。
8.  結果ウィンドウで、スクロールして**バッチ ジョブとしてログオン**をクリックします。
9.  **バッチ ジョブとしてログオン プロパティ** ダイアログ ボックスで、**ユーザーまたはグループの追加**をクリックします。
10. **ユーザーまたはグループの追加**ダイアログ ボックスで、**参照**をクリックします。
11. **ユーザー、コンピュータ、またはグループの選択**ダイアログ ボックスで、管理者と入力します。
12. **名前の確認**をクリックして、あらかじめ登録された Administrator アカウントが表示されていることを確認し、**OK** を 3 回クリックします。

### <a name="change-the-default-organizational-unit"></a>既定の組織単位の変更

仮想マシンをカスタム組織単位 (デフォルトの組織単位と比較して) の Active Directory に追加する場合は、展開を開始する前に Active Directory 内の既定の組織単位を変更できます。 詳細については、[ここ](http://pc-addicts.com/server-2012-change-default-ou/) をクリックしてください。

## <a name="6-deploy-a-high-availability-environment-on-azure"></a>6. Azure に高可用性環境を配置する
Azure に高可用性環境を配置するには、以下の手順に従ってください。

1. **クラウド ホスト環境**ページで、追加 (+) アイコンをクリックします。
2. **環境のトポロジの選択**パネルで、**高可用性**を選択します。
3. **高可用性**をクリックします。
4. **環境名**フィールドに、配置される環境の名前を入力します。
5. Lifecycle Services でインフラストラクチャ見積もりツールを使用して実稼働環境の見積もりを作成した場合、**見積**リストが表示されます。 この一覧から見積もりを選択します。 配置する仮想マシンの数とサイズは、選択した見積に基づいて変更されます。 見積を作成する方法の詳細については、[インフラストラクチャ見積もりツール (Lifecycle Services、LCS)](infrastructure-estimator-lcs.md) を参照してください。
6. **詳細設定**をクリックします。
7. ドメイン設定をカスタマイズするには、**ドメイン設定をカスタマイズ** をクリックします。 情報を入力するには、次の表を使用してください。
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

8. ドメインで作成されるサービス アカウントをカスタマイズするには、**サービス アカウントをカスタマイズ** をクリックします。 展開の **詳細設定** オプションを通じてサービス アカウントやサービス アカウントのパスワードを指定することができます。 どちらもが指定されていない場合は、既定の勘定が使用され、ランダムなパスワードが選択されています。 次の機能は、企業のアカウントの命名規則とパスワードの規則を管理する場合に使用します。 アカウントとパスワードのルール:
   - 有効なサービス名は、特殊文字を含まない 20 文字未満である必要があります。
   - 有効なパスワードは 8 文字以上で、大文字、小文字、数字、および次の文字のうち少なくとも 1 つが含まれます: \['@', '!', '=', '\*'\] 次のような一般的なパスワードは使用できません: pass@word1

9. 使用を希望する AX 2012 R3 のバージョンを選択するには、**サポートされているバージョン**をクリックします。 既定では、この環境の AX 2012 R3 CU8 バージョンが配置されます。 CU8 バージョンを使用しない場合は、**Dynamics ERP 2012 R3 RTM** をリストから選択します。
10. 仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。 一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。 名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。 インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。 仮想マシン名は 13 文字またはそれ以下にする必要があります。 インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。 例: ACustomVMName-99。仮想マシン インスタンスが最初の展開後に環境へ追加されると、展開サービスは中断した仮想マシン名のインクリメントを開始します。 たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。 もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。 展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。 これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。
11. SQL Server 構成オプションを入力するには、**SQL Server 構成のカスタマイズ** をクリックします。 使用する SQL Server イメージと、SQL Server 仮想マシンに関連付けるディスクの数とサイズを選択します。 詳細については、[Azure で Microsoft Dynamics AX 2012 R3 の配置を計画](plan-2012-r3-deployment-azure.md)を参照してください。
12. リモート デスクトップ サービスの仮想マシンを配置することを選択した場合、**リモート デスクトップ サービスをカスタマイズ**をクリックし、ユーザーが web 経由で AX 2012 R3 にアクセスする方法を指定します。 次のオプションのいずれかを選択します。
    -   **リモート デスクトップ:** このオプションはユーザーの完全なリモート デスクトップへのログインを有効にします。
    -   **RemoteApp プログラム**: このオプションを使用すると、完全なデスクトップウィンドウを使用しなくても、ユーザは直接 AX 2012 R3 にログインできます。 RemoteApp は既定で有効になります。

    環境が配置されると、**クラウド ホスト環境**ページで次のリンクが使用できます:
    -   **RDS Web アクセス証明書**: これは、RDS Web アクセス サイトへの安全なアクセスを許可するために提供される自己署名証明書です。 リンクをクリックしてこの証明書を開き、RDS Web アクセス サイトにアクセスする前に、**ローカル コンピューター**&gt;**信頼済ルート証明機関**にインストールします。 この環境を生産能力に配置する前に、RDS クラスターに自分の証明書をインストールすることをお勧めします。
    -   **RDS Web アクセス**: これにより、ユーザはウェブ上で AX 2012 R3 環境にアクセスできます。 **リモート デスクトップ** オプションを選択すると、ユーザーは完全なリモート デスクトップにログインできます。 **RemoteApp プログラム** を選択すると、ユーザーが AX 2012 R3 に直接ログインできます。
    -   **RDS ファーム アクセス**: これにより、ユーザは VPN 接続されたネットワークで AX 2012 R3 環境にアクセスできます。 この機能は、次の場合にのみ利用できます。
        1.  この AX の配置を VPN 接続されている会社のドメインに結合しました。
        2.  VPN 接続されたネットワークからの接続を受け入れるように RDS ゲートウェイをコンフィギュレーションしました。

    **注記:** **RDS Web アクセス**および **RDS ファーム アクセス**の両方で、既存の Active Directory ドメインに配置を結合する際には、内部ロード バランサーの IP アドレスを使用して、AD/DNS に RDS ファームを追加する必要があります。 次の手順を参照してください。
    1.  RDS ファームの名前を取得します。これは、LCS の RDS ファーム アクセス リンクから入手できます。 この場合、**RdsFarm0c0fa75** とする必要があります。

        [![MachineName](./media/machinename-300x165.png)](./media/machinename.png)

    2.  Azure ポータルでクラウド サービス ダッシュ ボードから内部ロード バランサの IP を取得します。 ポート **3389** の横に内部 IP がある RDS マシンを検査します。 以下の例では、内部ロード バランサーの IP は 10.1.3.4 です。

        [![IP アドレス](./media/ip-address-144x300.png)](./media/ip-address.png)

    3.  上記で取得した情報を使用して、AD のコンピューターとして RDS フォームを追加します。

        [![AddToAD](./media/addtoad-300x113.png)](./media/addtoad.png)

    これらの手順を実行しないと、RD Web アクセスを実行する際に次のエラーが発生します。*リモート デスクトップには、コンピューター「RdsFarm0c0fa75.contoso.com」が見つかりません。これは、「RdsFarm0c0fa75.contoso.com」が指定されたネットワークに属していないことを意味する可能性があります。接続しようとしているコンピュータ名およびドメインを確認してください。*
13. 仮想ネットワークの設定をカスタマイズするには、**仮想ネットワークをカスタマイズする** をクリックします。 情報を入力するには、次の表を使用してください。
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
    <li><strong>仮想ネットワーク名</strong>フィールドで、使用する既存の仮想ネットワークの名前を選択します。
    <table>
    <colgroup>
    <col width="100%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><strong>メモ</strong></td>
    </tr>
    <tr class="even">
    <td>仮想ネットワークの詳細を表示するには、次の手順を実行します。 <ol>
    <li><a href="https://manage.windowsazure.com/">Azure 管理ポータル</a>にログオンします。</li>
    <li>左のナビゲーション ウィンドウで、<strong>ネットワーク</strong>をクリックします。</li>
    <li>詳細を表示する仮想ネットワークの名前をクリックします。</li>
    <li><strong>構成</strong>をクリックします。 仮想ネットワークに関する詳細は、ページに記載されています。</li>
    </ol></td>
    </tr>
    </tbody>
    </table></li>
    <li><strong>アドレス空間</strong>フィールドで、展開するための適切なアドレス空間を選択します。</li>
    <li><strong>アプリケーション サブネット名</strong>フィールドで、アプリケーション VM の適切なアドレス空間を選択します。</li>
    <li><strong>SQL Server 高可用性サブネット名</strong>フィールドで、SQL Server VM の適切なアドレス空間を選択します。 <strong>注記</strong> 次の点に注意してください。 <ul>
    <li><strong>アプリケーション サブネット名</strong> フィールドで選択したのと同じアドレス空間を選択することができます。</li>
    <li>このサブネットには 4 つの IP アドレスが必要です。</li>
    </ul></li>
    <li><strong>Active Directory サブネット</strong> フィールドで、次の操作を行います。 <ul>
    <li>Azure の<strong>新しいドメイン</strong>をユーザーの環境に作成する場合、新しい Active Directory のサブネットの IP アドレスとサブネット マスクを入力します。 Lifecycle Services はこのサブネットを作成します。</li>
    <li>環境を Azure の<strong>既存のドメイン</strong>に追加する場合、既存の Active Directory サブネットの IP アドレスを入力します。 <strong>注記</strong>: このサブネットには 3 つの IP アドレスが必要です。</li>
    </ul></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

14. **完了** をクリックします。 **環境の展開** パネルが再表示されます。
15. 配置される仮想マシンの数とサイズが一覧表示されます。 必要に応じて、仮想マシンの数とサイズを変更します。
    -   この環境で各仮想マシンにインストールされているソフトウェアの詳細については、[Azure での Microsoft Dynamics AX 2012 R3 配置の計画](plan-2012-r3-deployment-azure.md) の記事の高可用性環境セクションを参照してください。
    -   仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](http://azure.microsoft.com/en-us/pricing/details/virtual-machines/) を参照してください。

16. ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。 次に、チェック ボックスを選択して、条件に同意することを示します。
17. **次へ** をクリックします。
18. 環境を展開する準備が整った**確認するための展開**をクリックします。 配置には数時間かかる場合があります。 配置が完了すると、**クラウド ホスト環境** ページの **配置ステータス** 列に **配置済み** が表示されます。 (これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。 配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。

## <a name="7-prepare-ax-2012-r3-for-use"></a>7. 使用する AX 2012 R3 の準備
環境が Azure に配置されたので、使用するために AX 2012 R3 を設定し、コンフィギュレーションする必要があります。 詳細については、以降のセクションを参照してください。

### <a name="log-on-to-an-aos-virtual-machine"></a>AOS 仮想マシンにログオンします。

DynamicsInstallUser アカウントを使用して AOS 仮想マシンにログオンします。 手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。 [Azure での Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md)という記事を参照してください。

### <a name="compile-ax-2012-r3"></a>AX 2012 R3 のコンパイル

AxBuild.exe. を使用した AX 2012 R3 のコンパイル 手順については、[X++ から P コードへの AOS の並列コンパイルに対する AxBuild.exe](https://technet.microsoft.com/en-us/library/dn528954.aspx) を参照してください。

### <a name="initialize-ax-2012-r3"></a>AX 2012 R3 の初期化

AX 2012 R3 クライアントを開いて、初期化チェックリストを完了します。 手順については、[初期化チェックリスト](https://technet.microsoft.com/en-us/library/aa497061.aspx) を参照してください。

### <a name="install-sample-data"></a>サンプル データのインストール

サンプル データを環境にインストールする場合は、次の手順を実行します。

1.  SQL-&lt;GUID&gt; 仮想マシンにログオンします。 DynamicsInstallUser アカウントを使用して仮想マシンにログオンします。 手順については、「仮想マシンにどのようにログオンしますか?」を参照してください。 [Azure での Microsoft Dynamics AX 2012 R3 配置の管理](manage-2012-r3-deployment-azure.md)という記事を参照してください。
2.  仮想マシンで次の場所に移動します: F:TestTransferTool
3.  テスト データ転送ツールをインストールします。 手順については、[Microsoft Dynamics AX 用のテスト データ転送ツール (ベータ版) をインストールする](install-test-data-transfer-tool-beta.md)を参照してください。
4.  コマンド プロンプトを開いて、次の場所にアクセスします: C:\Program Files (x86) \Microsoft Dynamics AX 2012 テスト データ確認転送ツール (ベータ)
5.  次のコマンドを実行します: dp.exe import F:DemoData MicrosoftDynamicsAx

**注記:** サンプル データには、AX 2012 R3 の試用版のライセンス キーが含まれています。 サンプル データをインストールしないように選択する場合は、開発またはテスト用の試用版ライセンス キーを [CustomerSource](https://mbs.microsoft.com/downloads/customer/AX/AXDemoTools/MicrosoftDynamicsAX2012R2v4DemoLicense.zip) または [MSDN](https://msdn.microsoft.com/en-us/subscriptions/securedownloads/hh442898#FileId=57028) からダウンロードすることができます

### <a name="give-users-access"></a>ユーザーのアクセス許可を付与します

ユーザが AX 2012 R3 にアクセスできるようにするには、以下のタスクを実行します。

-   CLI- 仮想マシンのリモート デスクトップ ユーザー グループに各ユーザーのドメイン アカウントを追加します。
-   ユーザーに AX 2012 R3 へのアクセス許可を付与します。 手順については、 [Microsoft Dynamics AXで新しいユーザーを作成する](https://technet.microsoft.com/en-us/library/aa548139.aspx) を参照してください。

**注記:** VPN 接続とドメイン信頼を作成しない場合でも、ユーザーに AX 2012 R3 へのアクセス権を与えることができます。 これを行うには、ドメイン コントローラとして機能する仮想マシンにログオンし、各ユーザーのドメイン アカウントを作成する必要があります。 その後、上記の 2 つのタスクを完了する必要があります。

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
<li><a href="https://technet.microsoft.com/en-us/library/gg732218.aspx">Microsoft Dynamics AX のシステム設定</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/gg732158.aspx">Microsoft Dynamics AX クライアント</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/gg731868.aspx">Application Object Server</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/ee873263.aspx">Microsoft Dynamics AX でのレポート</a> <strong>注:</strong> 既定により、レポートは 1 つの ビジネス インテリジェンス (BI) 仮想マシンに配置されます。 環境内で追加の BI 仮想マシンごとに、以下の点を行う必要があります。
<ol>
<li><a href="https://technet.microsoft.com/EN-US/library/dd309703.aspx">既定のレポートを配置します。</a></li>
<li><a href="https://technet.microsoft.com/EN-US/library/aa496432.aspx">ユーザーにレポートへのアクセス許可を付与します。</a></li>
<li>各 AOS インスタンスを各 SSRS インスタンスに接続するには、<a href="https://technet.microsoft.com/EN-US/library/aa548504.aspx">レポート サーバー フォーム</a>を開きます。 これを行う方法の段階を追った手順を確認するには、<a href="https://technet.microsoft.com/en-us/library/hh389773.aspx">Microsoft Dynamics AX を新しい Reporting Services インスタンスに接続する</a> を参照してください。</li>
</ol></li>
<li><a href="https://www.microsoft.com/en-us/download/details.aspx?id=5916">Management Reporter 2012</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/ee873272.aspx">Microsoft Dynamics AX での分析</a> <strong>注:</strong> AX 2012 R3 に含まれているキューブを処理するには、ExternalCommandTimeout 値を 7200 に増やすことをお勧めします。</li>
<li><a href="https://technet.microsoft.com/en-us/library/gg866975.aspx">ヘルプ サーバー</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/gg751374.aspx">エンタープライズ ポータルおよびロール センター</a><strong>注:</strong> エンタープライズ ポータルはポート 81 で実行するように設定されているため、ファイアウォール設定でそのポートを除外してください。</li>
<li><a href="https://technet.microsoft.com/en-us/library/gg731850.aspx">エンタープライズ検索</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/gg731810.aspx">サービス & アプリケーション統合フレームワーク (AIF)</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/jj710398.aspx">Microsoft Dynamics AX Retail IT プロおよび開発者向け</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/aa834453.aspx">.NET Business Connector</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/gg731779.aspx">セキュリティ</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>印刷可能なガイドおよびホワイト ペーパーの表示</td>
<td><ul>
<li><a href="https://technet.microsoft.com/en-us/library/gg732268.aspx">印刷可能なガイド</a></li>
<li><a href="https://technet.microsoft.com/en-us/library/gg188985.aspx">システム管理者向けのホワイト ペーパー</a></li>
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

## <a name="8-prepare-the-whole-environment-for-use"></a>8. 使用する全環境を準備
次のセクションでは、この環境を使用するための設定に役立つ情報を提供します。

### <a name="understand-the-high-availability-architecture"></a>高可用性アーキテクチャを理解する

冗長性を提供するために、仮想マシンは*可用性セット*にグループ分けされています。 可用性セットは計画的または予定外の保守イベント中に、可用性セット内の少なくとも 1 台の仮想マシンが実行されていることを保証します。 可能性セットの各仮想マシンは、基礎 Azure プラットフォームによって、**更新プログラム ドメイン**および**障害ドメイン**に割り当てられます。

-   **ドメインの更新:** 更新ドメインで同じ更新スケジュールを共有する仮想マシンのグループを定義します。
-   **障害ドメイン:** 障害ドメインは、共通の電源とネットワークスイッチを共有する仮想マシンのグループを定義します。

高可用性環境には、仮想マシンの層ごとに設定された可用性が含まれます。 たとえば、ドメイン コントローラ、データベース サーバー、AOS サーバーなどの、可用性セットがあります。

### <a name="install-the-data-importexport-framework-and-rapidstart-connector"></a>Data import/export framework および RapidStart Connector のインストールを行う

可用性を高めるためにには、 **Data import/export framework** と **RapidStart Connector** をAOSサーバーであるすべての仮想マシンにインストールする必要があります。 これらのコンポーネントをインストールすることが必要な場合があります。 手順については、次を参照してください: • [Install the Data import/export framework (DIXF, DMF)](install-dixf.md) • [Install the RapidStart Connector](https://technet.microsoft.com/en-us/library/hh771574.aspx)

### <a name="configure-microsoft-sql-server-reporting-services-for-load-balancing"></a>負荷分散のための Microsoft SQL Server Reporting Services のコンフィギュレーション

環境内のBI サーバーは、Microsoft SQL Server Reporting Services をホストします。 負荷分散のために Reporting Services を構成するには、[[Azure 展開で SSRS を負荷分散に構成する](http://blogs.msdn.com/b/axsupport/archive/2015/06/25/configure-ssrs-for-load-balancing-in-your-azure-deployment.aspx)] ブログ ポストを参照してください。

### <a name="join-enterprise-portal-servers-in-a-single-server-farm"></a>エンタープライズ ポータル サーバーの 1 つのサーバー ファームへの結合

Lifecycle Services でエンタープライズ ポータル サーバーが配置されると、各サーバーは独自のサーバー ファームに配置されます。 単一のサーバー ファーム内のすべてのエンタープライズ ポータル サーバーに参加するには、[[単一サーバー ファーム内のエンタープライズ ポータル サーバーに参加する](join-enterprise-portal-servers-single-server-farm.md)] を参照してください。

### <a name="configure-the-environment-for-optimal-performance"></a>最適なパフォーマンスを得るための環境をコンフィギュレーションする

次のタスクを実行して、最適なパフォーマンスを得るための環境をコンフィギュレーションします。• [データベース ファイルの初期化](https://msdn.microsoft.com/en-us/library/ms175935.aspx) • [ロックページを有効にする](https://technet.microsoft.com/en-us/library/ms190730.aspx) • [クライアントがローミング プロファイルを使用するようコンフィギュレーションし、クライアントの起動時間を短縮する](https://technet.microsoft.com/en-us/library/dn479031.aspx)

### <a name="learn-more-about-the-high-availability-configuration"></a>高可用性構成の詳細の確認

高可用性のためにこの環境をどのように構成したかについては、次のリソースを参照してください。

-   [Active Directory ドメイン コントローラでの FSMO の配置と最適化](http://support.microsoft.com/kb/223346)
-   [SQL Serverとストレージの設定を構成する](https://technet.microsoft.com/en-us/library/dd309734.aspx)
-   [WSFC クォーラム モードおよび採決のコンフィギュレーション](https://msdn.microsoft.com/en-us/library/hh270280.aspx)
-   [Windows PowerShell での リモート デスクトップ コマンドレット](/powershell/module/remotedesktop/?view=win10-ps)

## <a name="9-learn-more-about-the-service-accounts-for-this-environment"></a>9. この環境のサービス アカウントに関する詳細
次のセクションでは、環境を配置したときに作成されたサービス アカウントについて説明します。

### <a name="domain-accounts"></a>ドメイン アカウント

次のテーブルに、環境を配置したときに作成されたドメイン アカウントを示します。

| ドメイン アカウント                  | 説明                                                                                                                                                                                         |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <DomainName>AOSServiceUser      | 次のサービスを実行するために使用されたアカウント: Microsoft Dynamics AX Object Server                                                                                                                 |
| <DomainName>SQLServiceUser      | 次のサービスを実行するために使用されるアカウント: SQL Server Analysis Services (MSSQLSERVER)。                                                                                                          |
| <DomainName>DynamicsInstallUser | Dynamics AX 2012 R3 をインストールするために使用したアカウント。                                                                                                                                                    |
| <DomainName>SPServiceUser       | 次のサービスを実行するために使用したアカウント: AppFabric Caching Service、SharePoint Search Host Controller、SharePoint Server Search 15、SharePoint Timer Service、および SharePoint User Code Host。 |
| <DomainName>BCProxyUser         | ビジネス コネクタ プロキシとして使用されるアカウント。                                                                                                                                                   |
| <DomainName>AXServiceUser       | 次のサービスの実行に使用したアカウント: Microsoft Dynamics AX Data Import/Export Framework Service and Microsoft Dynamics ERP RapidStart Connector.                                         |
| <DomainName>RetailServiceUser   | 次のサービスの実行に使用したアカウント: Microsoft Dynamics AX for Retail Commerce Data Exchange Async Client。                                                                               |

注記: パスワードは、[Lifecycle Services](https://lifecycleservices.dynamics.com/en/) のクラウド ホスト環境ページに表示されます。

### <a name="local-administrator-accounts"></a>ローカル管理者アカウント

配置した各仮想マシンには、ローカル Administrator アカウントがあります。 このアカウントは builtinaxlocaladmin です。 ローカル管理者アカウントのパスワードは、Lifecycle Services の **クラウド ホスト 環境** ページに表示されます。



