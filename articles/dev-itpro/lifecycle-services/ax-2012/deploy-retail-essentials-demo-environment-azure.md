---
title: Azure での Retail Essentials デモ環境の配置
description: このトピックでは、Microsoft Azure にRetail essentials デモを配置する方法について説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 01/05/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 13352
ms.assetid: be08d43a-f05e-4580-ac75-52710d06a1d7
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 7ec1e8b15e574e2d96880ed9bf6680d60f6cbd85
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555286"
---
# <a name="deploy-retail-essentials-demo-environments-on-azure"></a>Azure での Retail Essentials デモ環境の配置

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Azure にRetail essentials デモを配置する方法について説明します。 環境を展開するには、Microsoft Dynamics Lifecycle Services でクラウド ホスト環境ツールを使用します。

## <a name="prerequisites"></a>必要条件
この記事の手順を実行する前に、次の条件が満たされていることを確認します。

| カテゴリ       | 前提条件                                                                                                                                            |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| 必要なタスク | [Azure での Microsoft Dynamics AX 配置計画](plan-2012-r3-deployment-azure.md) |

## <a name="1-log-on-to-lifecycle-services"></a>1. ライフサイクル サービスにログオンする
Microsoft Dynamics Lifecycle Services は、顧客およびパートナーが Microsoft Dynamics AX の管理に使用できるクラウドベースの共同ワークスペースです。 Azure に Dynamics AX を配置するには、この Web サイトを使用します。 Lifecycle Services は顧客やパートナーがサポート計画の一部として使用できます。 CustomerSource または PartnerSource の資格情報でアクセスすることができます。 [Lifecycle Services にログオン](https://lcs.dynamics.com/)

## <a name="2-create-a-project"></a>2. プロジェクトの作成
Lifecycle Services にログインした後、既存のプロジェクトを開くか、または新しいプロジェクトを作成します。 プロジェクトは、Lifecycle Services でのエクスペリエンスの主な開催者です。 プロジェクトに関連する手法は、既定でプロジェクトに含まれるフェーズとタスクを決定します。

## <a name="3-connect-the-project-to-your-azure-subscription"></a>3. Azure サブスクリプションにプロジェクトを接続する
Azure サブスクリプションに Lifecycle Services プロジェクトを接続します。 これにより、Lifecycle Services は Dynamics AX 環境をサブスクリプションに配置できます。 Azure サブスクリプションにプロジェクトを接続するには、次の手順を実行します。

1. LCS プロジェクトで**環境**セクションに移動して、**Microsoft Azure 設定**をクリックしてから、**Azure コネクタ領域**で**追加**をクリックします。 
   >[!Note]
   > **Microsoft Azure 設定**オプションは、**クラウド-ホスト環境タイル**をクリックしたときにも使用できます。
2. Azure への接続を識別する名前を入力します。
3. Azure サブスクリプション ID を入力します。 サブスクリプション ID を検索する必要がある場合は、次の手順を実行します。
   1.  ブラウザの別のインスタンスを開きます。
   2.  [Azure ポータル](https://ms.portal.azure.com/)にログオンします。
   3.  左のナビゲーション ウィンドウで、**サブスクリプション**をクリックします。

       > [!Note]
       > 下部の **その他のサービス** をクリックしてから **サブスクリプション** をクリックすることが必要な場合があります。

   4.  サブスクリプション ID をコピーして、Lifecycle Services の **Azure サブスクリプション ID** フィールドに貼り付けます (現在別のブラウザー インスタンスに表示されています)。

4. **次へ** をクリックします。
5. **ダウンロード**をクリックして管理証明書をダウンロードします。 この管理証明書により、Lifecycle Services はお客様の代わりに Azure と通信できます。 既定では、管理証明書はコンピューターの**ダウンロード** フォルダーに保存され、**LifecycleServicesDeployment.cer** という名前が付きます。
6. 管理証明書を Azure にアップロードします。 これを行うには、[[Azure 管理 API 管理証明書をアップロード](https://docs.microsoft.com/en-us/azure/azure-api-management-certs)] の手順を参照してください。

7. Lifecycle Services で **Microsoft Azure 設定**パネルを表示するブラウザーに戻ります。 **次へ** をクリックします。
8. 地域を選択します。 AX 2012 R3 環境は、この領域のデータ センターに配置されます。
9. **接続** をクリックします。 これで、プロジェクトが指定された Azure サブスクリプションに接続できるようになりました。 

>[!Note]
> 証明書が期限切れになった場合は、新しいものを取得できます。 そのためには次の作業を行います。
> 1. プロジェクトの設定の **Azure コネクタ** 領域で接続を選択し、**編集** をクリックします。
> 2. **Microsoft Azure 設定**パネルが画面の横に表示されます。 **ダウンロード**をクリックして新しい証明書をダウンロードします。
> 3. 上の手順の手順 6 ～ 9 を繰り返します。

## <a name="4-deploy-a-retail-essentials-demo-environment-on-azure"></a>4. Azure での Retail Essentials デモ環境の配置
Azure に Retail Essentials デモ環境を配置するには、以下の手順に従ってください。

1.  **クラウド ホスト環境**ページで、**追加** (+) アイコンをクリックします。
2.  **環境のトポロジの選択**パネルで、**デモ**を選択します。
3.  **Retail Essentials デモ**をクリックします。
4.  **環境名**フィールドに、配置される環境の名前を入力します。
5.  **詳細設定**をクリックします。
6.  仮想マシン名をカスタマイズするには、**仮想マシン名をカスタマイズ** をクリックします。 一般的な IT 名前付けガイドラインをサポートするために、仮想マシンに名前を付ける機能がほとんどの配置トポロジの**詳細設定**に用意されています。 名前を定義することに加えて、各仮想マシン タイプに開始インデックスを選択できます。 インデックスは、配置される仮想マシン タイプのインスタンスごとに増加します。 仮想マシン名は 13 文字またはそれ以下にする必要があります。 インデックスはマシン名とハイフン (-) で区切られ、その後に最大 2 桁のインデックスが続きます。 例: ACustomVMName-99。 最初の展開後に、仮想マシンのインスタンスが環境に追加されるとき、配置サービスは、中断した場所で、仮想マシンの名前の増分を開始します。 たとえば、2 で始まるインデックスを持つ 4 つの AOS 仮想マシンを展開する場合、最後の AOS インスタンス名は AOS-6 になります。 もう 2 つ AOS インスタンスを追加する場合は、AOS-7 と AOS 8 になります。 展開内の仮想マシン タイプの 1 つがカスタマイズされている場合は、すべての仮想マシン名をカスタマイズする必要があります。 これは、仮想マシン名が誤って紛失してしまったため、長期的な展開が発生しないようにするためです。
7.  仮想ネットワークの設定をカスタマイズするには、**仮想ネットワークをカスタマイズする** 設定をクリックします。 情報を入力するには、次の表を使用してください。

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>以下を行う場合:</th>
    <th>手順</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Azure で環境用に新しい仮想ネットワークを作成する</td>
    <td><ol>
    <li><strong><span class="label">新しい仮想ネットワーク</span></strong>をクリックします。</li>
    <li>仮想ネットワーク名を入力します。</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Azure の既存の仮想ネットワークへの環境の追加</td>
    <td><ol>
    <li><strong><span class="label">既存の仮想ネットワーク</span></strong>をクリックします。</li>
    <li>使用する既存の仮想ネットワークの名前を選択してください。 <span class="label"><strong>アプリケーション サブネット</strong><strong>名</strong></span> および <strong><span class="label">アドレス スペース</span></strong> フィールドには、選択した仮想ネットワークに基づいて適切な情報が自動的に表示されます。 これらのフィールドの情報を確認する場合は、次の操作を行います。 <ol>
    <li><a href="https://ms.portal.azure.com/">Azure ポータル</a>にログオンします。</li>
    <li>左のナビゲーション ウィンドウで、<strong><span class="label">仮想ネットワーク</span></strong>をクリックします。</li>
    <li>使用する仮想ネットワークの名前をクリックします。</li>
    <li><strong><span class="label">構成</span></strong>をクリックします。 仮想ネットワークに関する詳細は、ページに記載されています。</li>
    <li><strong><span class="label">完了</span></strong>をクリックします。 <strong><span class="label">環境の展開</span></strong> パネルが再表示されます。</li>
    <li>配置される仮想マシンの数とサイズが一覧表示されます。 必要に応じて、仮想マシンの数とサイズを変更します。</li>
    </ol></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

    -   この環境で各仮想マシンにインストールされているソフトウェアの詳細については、[Azure での Microsoft Dynamics AX 配置の計画](plan-2012-r3-deployment-azure.md)を参照してください。
    -   仮想マシンに関するサイズおよび価格決定の詳細については、[仮想マシンの価格決定の詳細](http://azure.microsoft.com/en-us/pricing/details/virtual-machines/) を参照してください。

8.  ライセンスの条項を確認するには、**ソフトウェア ライセンス条項**をクリックします。 次に、チェック ボックスを選択して、条件に同意することを示します。
9.  **次へ** をクリックします。
10. **展開**をクリックして、環境を展開する準備が整ったことを確認します。 配置には数時間かかる場合があります。 配置が完了すると、**クラウド ホスト環境** ページの配置ステータス列に **配置済み** が表示されます。 (これを表示するにはブラウザーを更新する必要があります。) 配置が失敗すると、すぐエラー メッセージが表示される場合があります。 配置プロセスでエラーが後に発生する場合に、エラーの詳細がページの右側の詳細ペインに表示されます。

## <a name="5-open-the-dynamics-ax-client"></a>5. Dynamics AX クライアントを開く
Dynamics AX クライアントがインストールされている仮想マシンに接続するには、以下の手順を完了してください。

1.  **クラウド ホスト環境ページ**で、配置した Retail Essentials 環境を選択します。
2.  環境のプロパティを表示するためにページの右側にスクロールします。
3.  **DEMO-&lt;GUID&gt;** リンクをクリックします。
4.  ページの下部にある**開く**をクリックして、.rdp ファイルを開きます。
5.  資格情報を求めるメッセージが表示されたら、&lt;DomainName&gt; 管理者アカウントのユーザー名とパスワードを入力します。 このアカウントのパスワードはこの環境の **クラウド ホスト環境** ページで見つけることができます。
6.  仮想マシンのデスクトップが表示されたとき、**Microsoft Dynamics AX** アイコンをクリックして、Microsoft Dynamics AX クライアントを開きます。





