---
title: Azure 上での AX 2012 R3 配置のトラブルシューティング
description: このトピックでは、一般的な問題を解決するための方法、および Azure で Microsoft Dynamics AX 2012 R3 環境の支援を受ける方法について説明します。
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 18691
ms.assetid: cc7c6dd5-b715-4734-9918-c25df4187c6e
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 2af454f1efc2b4f13e62ca872ec0eec0e521efe1
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811700"
---
# <a name="troubleshoot-ax-2012-r3-deployments-on-azure"></a>Azure 上での AX 2012 R3 配置のトラブルシューティング

[!include [banner](../../includes/banner.md)]

このトピックでは、一般的な問題を解決するための方法、および Azure で Microsoft Dynamics AX 2012 R3 環境の支援を受ける方法について説明します。

<a name="how-do-i-renew-the-windows-license-on-a-demo-virtual-machine"></a>デモ仮想マシンで Windows ライセンスを更新するにはどうすればよいですか。
-------------------------------------------------------------

Windows のデモ環境で仮想マシンに試用版のライセンスを更新する必要がある場合は、次の手順を実行します。

1.  **クラウド ホスト環境**ページで、デモ環境を選択します。
2.  環境に関する詳細を表示するためにページの右側にスクロールします。
3.  **DEMO-&lt;GUID&gt;** リンクをクリックします。
4.  ページの下部にある**開く**をクリックして、.rdp ファイルを開きます。
5.  資格情報を求めるメッセージが表示されたら、 この環境の **クラウドによってホストされた環境** ページにある、適切なユーザー名とパスワードを入力します。
6.  仮想マシンのデスクトップが表示されたとき、c:\\DemoFiles\\StartupScripts の場所に移動します。
7.  **rearm.cmd** を右クリックして**管理者として実行** をクリックします。

コマンド プロンプト ウィンドウが短く表示され、仮想マシンが再起動します。 ライセンスは現在 180 日間有効です。 この手順は 3 回完了することができます。

## <a name="how-do-i-renew-the-microsoft-dynamics-ax-license-on-a-demo-virtual-machine"></a>デモ仮想マシンで Microsoft Dynamics AX ライセンスを更新するにはどうすればよいですか。
Microsoft Dynamics AX のデモ環境で仮想マシンのライセンスを更新する必要がある場合、[CustomerSource](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/service-packs/AX2012DemoToolsMaterials#DemoVirtualMachineLicenses) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898) から試用版のライセンス ファイルをダウンロードします。 「[ライセンス情報の指定](https://technet.microsoft.com/library/aa496447.aspx)」に記載の手順に従います。

## <a name="how-do-i-activate-windows-on-the-virtual-machines-in-my-non-demo-environment"></a>非デモ環境で仮想マシンの Windows をアクティブにするにはどうしたらいいですか。
Windows は非デモ環境に含まれている仮想マシン上で自動的に有効化されます。 ただし、有効化には完了までに 4 日間かかる場合があります。 4 日間後に Windows を有効化するように求めるメッセージが続けて表示される場合は、Azure サポート チームに問い合わせます。 Azure サポート チームに連絡する方法の詳細については、次のセクションを参照してください。

## <a name="how-do-i-resolve-the-following-error-scriptid-installdatabase-failed-execution-on-vm-instance"></a>次のエラーを解決するには: VMインスタンスで ScriptId 「InstallDatabase」 実行の失敗
SQL Server AlwaysOn クラスターをインストールすると、プライマリ SQL Server インスタンスがセカンダリ インスタンスにフェール オーバーする場合、そのインストールは上記のエラーで失敗します。 仮想マシンがオンラインになると、すぐに失敗することは異常です。 配置されているトポロジを削除し、再配置することをお勧めします。

## <a name="how-do-i-resolve-the-following-error-script-createazurefailoverclusterhasql1-failed-execution"></a>次のエラーを解決するには: スクリプト 「CreateAzureFailoverCluster:HASQL1」 実行の失敗
既存のネットワークと Active Directory に展開した場合 (トポロジー内の VM の名前もカスタマイズしている場合)、Azure の DNS サーバーを変更せずに同じ名前のカスタマイズを再展開することはできません。 このシナリオでは、DNS サーバーに同じ名前を持つ前の VM の IP アドレスがあり、その結果、配置に失敗します。 この問題を解決するには、再配置する前にそれらの VM の DNS サーバー エントリを削除する必要があります。

## <a name="the-dynamics-ax-client-crashes-on-first-use--how-do-i-resolve-this"></a>Dynamics AX クライアントは、初回の使用時にクラッシュします。  これをどのように解決しますか。
Dynamics AX クライアントは、再起動後または最初のログイン後にクラッシュする可能性があります。 これは、カーネル 6.3.3000.287 で修正された RemoteApp の問題が原因です。  高可用性環境またはテスト環境を配置した場合、RemoteApp を使用している場合があります。 この問題を解決するには、次のいずれかの手順を実行します。

### <a name="disable-the-status-bar"></a>ステータス バーを無効にする

1.  Dynamics AX クライアントで、**オプション** フォーム (**ファイル** &gt; **ツール** &gt; **オプション**) を開きます。
2.  **ステータス バー** オプションをクリックします。
3.  **ステータス バーの表示** フィールドで**なし**を選択します。

### <a name="install-kernel-633000287-or-later"></a>カーネル 6.3.3000.287 以降のインストール

カーネルは累積型であるため、最新のカーネルはこちらを参照してください。<https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/>

## <a name="how-do-i-monitor-for-storage-account-throttling"></a>ストレージ アカウントのスロットルを監視するにはどうすればよいですか。
ストレージ アカウントのスロットルを監視するには、[[ストレージ アカウントのスロットルを監視する方法](https://blogs.msdn.microsoft.com/mast/2014/08/02/how-to-monitor-for-storage-account-throttling/)] を参照してください。 ストレージが制限されているときに通知するには、警告および通知を利用できます。 これが発生している場合、複数の Azure コネクタや LCS プロジェクトの活用に関する情報については、[Azure で AX 2012 R3 の配置を計画する](plan-2012-r3-deployment-azure.md)というトピックを参照します。

## <a name="how-do-i-contact-support"></a>サポートに連絡するにはどうすればよいですか。
ライセンスまたは技術的な質問で Microsoft に連絡する必要がある場合は、最初にどのサポート チームに連絡するかを決める必要があります。 以下の情報を参考にして、最良の担当サポート チームを見つけてください。

### <a name="azure-support"></a>Azure サポート

Azure のサポートを得るには、次の表に示すリソースを使用します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>タスク</strong></td>
<td><strong>詳細情報</strong></td>
</tr>
<tr class="even">
<td>請求書に関連する質問について援助を受けます</td>
<td>サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要を確認するには、<a href="http://azure.microsoft.com/support/understand-your-bill/">請求書を理解する</a>ページに移動してください。</td>
</tr>
<tr class="odd">
<td>コミュニティに質問する</td>
<td><a href="http://www.windowsazure.com/support/forums/">Azure フォーラム</a>ページに移動し、Azure コミュニティからの質問のヘルプを入手します。</td>
</tr>
<tr class="even">
<td>Azure サービス ダッシュ ボードの使用</td>
<td><a href="http://www.windowsazure.com/support/service-dashboard/">Azure サービス ダッシュ ボード</a>ページに移動して、Azure プラットフォームおよびサービスの現在のステータスを取得します。</td>
</tr>
<tr class="odd">
<td>Azure サポート チームとのサポート チケットを入力します。</td>
<td><a href="http://www.windowsazure.com/support/options/">Azure サポート オプション</a>ページに移動し、サポートを受けるをクリックしてサポート チケットを開きます。 Azure サポート チームは、以下に関連する問題の解決をサポートします。
<ul>
<li>Azure サブスクリプションのサイズを大きくする要求</li>
<li>Azure 管理ポータルの使用時のエラー</li>
<li>仮想ネットワークを構成する際の問題</li>
<li>仮想ネットワーク ゲートウェイを構成する際の問題</li>
</ul></td>
</tr>
</tbody>
</table>

### 

### <a name="microsoft-dynamics-ax-support"></a>Microsoft Dynamics AX のサポート

Microsoft Dynamics AX のサポートを得るには、次の表に示すリソースを使用します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>タスク</strong></td>
<td><strong>詳細</strong></td>
</tr>
<tr class="even">
<td>Microsoft Dynamics AX のライセンスに関する質問について援助を受けます。</td>
<td>次の PartnerSource のリンクをクリックして、Microsoft Dynamics Regional Operations Center にお問い合わせください。
<ul>
<li><a href="https://mbs.microsoft.com/partnersource/northamerica/pricing-ordering">価格決定と注文</a></li>
<li><a href="https://mbs.microsoft.com/partnersource/northamerica/help/help/GlobalOperationsSupportPage">工程のサポート</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>コミュニティに質問する</td>
<td><a href="http://go.microsoft.com/fwlink/?LinkId=221068">Microsoft Dynamics AX フォーラム</a>ページに移動し、Microsoft Dynamics AX コミュニティからの質問のヘルプを入手します。</td>
</tr>
<tr class="even">
<td>クラウドを利用したサポート ツールの使用</td>
<td><a href="https://lifecycleservices.dynamics.com/en/">Microsoft Dynamics Lifecycle Services</a> で、クラウドを利用したサポートはサポート インシデントを管理するためのツールです。 クラウドを利用したサポートにより、ローカル環境と同じ修正プログラムがインストールされた Azure に仮想マシンを作成できます。 仮想マシン上でインシデントを再生成して記録し、仮想マシンをサポート チームに送信することができます。 サポート チームは、インシデントを調査し、仮想マシンの修正をテストすることによってフォローアップします。 修正プログラムが見つかった場合、仮想マシンと修正プログラムを確認のために送信します。</td>
</tr>
<tr class="odd">
<td>問題検索ツールの使用</td>
<td><a href="https://lifecycleservices.dynamics.com/en/">Microsoft Dynamics Lifecycle Services</a> で、問題検索は、サポート技術情報記事、修正プログラム、および Microsoft Dynamics AX で報告された問題の回避策をすぐに検索できる検索エンジンです。 どのレポート済みの問題が修正処理中であるか表示され、Microsoft Dynamics AX で特定の機能領域の修正プログラムがリリースされるときに通知が表示されます。 リリース済の修正プログラムをダウンロードして、どのコード オブジェクトが影響を受けるか確認し、修正プログラムで導入されたコード変更を確認することができます。</td>
</tr>
<tr class="even">
<td>Microsoft Dynamics AX サポート チームとのサポート チケットを入力します。</td>
<td><a href="https://community.dynamics.com/ax/p/support.aspx">Microsoft Dynamics AX のサポート</a>ページに移動して、サポート チケットを開きます。 Microsoft Dynamics AX サポート チームは、以下に関連する技術的な問題の解決をサポートします。
<ul>
<li>Lifecycle Services の使用時のエラー</li>
<li>Microsoft Dynamics AX の使用時のエラー</li>
</ul></td>
</tr>
</tbody>
</table>





