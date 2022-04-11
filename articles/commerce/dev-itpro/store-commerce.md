---
title: Store Commerce アプリ
description: このトピックでは、Microsoft Dynamics 365 Commerce Store Commerce アプリの設定および構成方法について説明します。
author: mugunthanm
ms.date: 03/10/2022
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 03-01-2022
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 22f101530be9770bcf1453055a69209a1ea99579
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489011"
---
# <a name="store-commerce-app"></a>Store Commerce アプリ

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce Store Commerce アプリの設定および構成方法について説明し、Microsoft Dynamics 365 Commerce バージョン 10.0.25 およびそれ以降に適用します。

Dynamics 365 Commerce Store Commerce アプリは、物理店舗に対する次世代の提供です。 Modern 販売時点管理 (MPOS) とクラウド販売時点管理 (CPOS) を 1 つのアプリケーションに統合して小売業者の配置の選択肢を提供し、パフォーマンスを向上させ、より優れたアプリケーション ライフサイクル管理 (ALM) を提供します。 同時に、拡張機能を含め、MPOS および CPOS のすべての機能が保持されます。

Store Commerce アプリは、レジ担当者、販売担当者、販売在庫担当者、在庫担当者、および店舗管理者などの第一線の作業者に豊富なコマース機能を提供します。 これらの作業者は、現金売りトランザクション、現金/シフト管理、顧客契約、支援販売、クライアンテリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、レポートなどのコマース操作を実行することができます。

Store Commerce は、[Microsoft Edge WebView2](/microsoft-edge/webview2/) コントロールを使用して CPOS アプリケーションを表示する Windows 用の [Windows Presentation Foundation (WPF)](/dotnet/desktop/wpf/?view=netdesktop-6.0&preserve-view=true) シェル アプリケーションです。 CPOS は Web ブラウザーでのみ実行できますが、Store Commerce は [MPOS](retail-modern-pos-architecture.md) などのネイティブ WIndows アプリケーションとして実行できます。 したがって、MPOSとCPOSの両方の利点を提供することができます。

Store Commerce はローカル ハードウェア ステーションおよびオフライン使用をサポートし、支払ターミナル、プリンター、キャッシュ ドロワーに直接統合できます。 共有ハードウェア ステーションを設定する必要なしに、ハードウェア デバイスを使用することができます。

ユーザー インターフェイス (UI) を表示するために、Store Commerce は、ユニバーサル Windows プラットフォーム (UTC) アプリ表示フレームワークの代わりに Chromium エンジンを使用します。 Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。 MPOS と Store Commerce の主な違いは、Store Commerce がアプリを表示するのに Chromium エンジンを使用する点です。

## <a name="benefits-of-store-commerce"></a>Store Commerce の利点

- ALM が簡略化されました。
- コマース ソフトウェア開発キット (SDK) を使用して MPOS または CPOS 用に開発された拡張機能または独立系ソフトウェア ベンダー (ISV) のコードは、最小限の変更で Store Commerce で再利用することができます。
- Store Commerce は、MPOSとCPOSの両方の利点を提供します。
- パフォーマンスが向上しました。
- POS および拡張機能のアップグレードがより簡単になりました。
- 専用のハードウェア ステーションをサポートしています。
- オフラインでの配置をサポートしています。

## <a name="application-lifecycle-management"></a>アプリケーション ライフサイクル管理

Store Commerce アプリは Windows デバイスで実行され、[Microsoft Lifecycle Services (LCS) の共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードできます。 **共有アセット ライブラリ** ページで、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、「Store Commerce」で終わるファイルを検索します。 使用している Commerce リリースのバージョン (10.0.25 または 10.0.26 など) を選択してください。

### <a name="store-commerce-deployment-topology"></a>Store Commerce の配置トポロジ

Store Commerce は、2 つのタイプの配置トポロジをサポートしています。

- **オンライン** – Cloud Scale Unit (CSU) に接続されています。
- **オフライン** – コマースの本部への接続なしに、ローカルに配置された Commerce Runtime (CRT) に接続されています。

### <a name="online-deployment"></a>オンラインでの配置

Store Commerce は、CPOS を表示し、CSU をオンライン モードで使用して Headless Commerce および Commerce 本部に接続するシェルです。 オンライン モードで Store Commerce にアプリケーションを表示するには、2 つのオプションがあります。

- **リモート アプリ コンテンツ** – Store Commerce アプリのコンテンツは、CSU でホストされている CPOS から表示されます。
- **ローカル配置** – Store Commerce アプリのコンテンツは、MPOS のように、Store Commerce アプリ内でローカルに配置されます。 このオプションは、既定で使用されています。

#### <a name="store-commerce-app-content-rendered-from-cpos-hosted-in-csu-remote-app-content"></a>CSU でホストされている CPOS から表示された Store Commerce アプリのコンテンツ (リモート アプリ コンテンツ)

リモート アプリ コンテンツのオプションの場合、Store Commerce は CSU でホストされている CPOS からアプリケーション コンテンツをダウンロードして表示します。 Store Commerce を更新するには、CSU を更新します。 Store Commerce は更新を自動的に受信します。 更新は CSU で集中管理されるので、個々のレジスターで管理する必要はありません。 Store Commerce アプリケーションのシェルは、インストーラを使用して個別に更新する必要があります。 CSU の更新方法の詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) を参照してください。 

#### <a name="store-commerce-app-content-rendered-from-local-deployment"></a>ローカル配置から表示された Store Commerce アプリのコンテンツ

ローカル配置のオプションの場合、アプリケーション コンテンツは Store Commerce にローカルで配置されます。 Store Commerce はローカル配置からアプリケーション コンテンツを表示します。 アプリケーション コンテンツを取得するのに CSU でホストされている CPOS には接続しません。

アプリケーション コンテンツを更新するには、最新バージョンの Store Commerce インストーラを実行します。 CSU を更新するとき、アプリケーション コンテンツは更新されません。 したがって、更新は個々のレジスターで管理することができます。

Store Commerce のインストール中に、ユーザーはパラメーターを渡して、リモート アプリ コンテンツのオプションまたはローカル配置のオプションのいずれかを選択できます。 既定では、Store Commerce はローカル配置を使用します。

### <a name="offline-deployment"></a>オフラインでの配置

オフラインで配置する場合は、Store Commerceのインストール中に **--installoffline** パラメーターを渡して、オフラインのデータベースを配置します。 オフラインでの配置中は、アプリケーションを CSU または Commerce 本部に接続することはできません。 代わりに、ローカルに配置された CRT を使用します。

## <a name="store-commerce-and-mpos-parity"></a>Store Commerce と MPOS の機能

Store Commerce には MPOS と完全に同等の機能があります。 現在、Store Commerce はデュアル ディスプレイをサポートしていません。 さまざまな POS アプリケーションおよびトポロジの詳細については [Modern POS (MPOS) かクラウド POS かの選択](../mpos-or-cpos.md)を参照してください。

## <a name="store-commerce-and-cpos-parity"></a>Store Commerce と CPOS の機能

Store Commerce には CPOS と完全に同等の機能があります。 さらに、Store Commerce は専用のハードウェアをサポートし、オフラインで配置します。

## <a name="store-commerce-and-mposcpos"></a>Store Commerce および MPOS/CPOS

新しい配置にはすべて、Store Commerce または CPOS を使用することをお勧めします。 既存の顧客は、MPOS から Store Commerce への移行を計画する必要があります。 

### <a name="comparison-between-store-commerce-and-mpos"></a>Store Commerce と MPOS の比較

<table>
<thead>
<tr>
<th></th>
<th>Store Commerce</th>
<th>MPOS</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row">操作環境</th>
<td>Windows</td>
<td>Windows</td>
</tr>
<tr>
<th scope="row">ALM</th>
<td>Store Commerce は、LCS および Commerce 本社を使用してセルフサービスを行います。 Store Commerce インストーラを使用してパッケージ化され、インストールされます。CPOS は CSU を通じて配置されます。</td>
<td>MPOS は、LCS および Commerce 本社を使用してセルフサービスを行います。 MPOS インストーラーを使用してパッケージ化され、インストールされます。</td>
</tr>
<tr>
<th scope="row">拡張子</th>
<td>拡張機能は、CPOS に配置するか、拡張機能インストーラを使用してインストールします。</td>
<td>拡張機能が MPOS と共にパッケージ化されるか、あるいは独立した拡張パッケージが使用されます。</td>
</tr>
<tr>
<th scope="row">オフライン モードでのサポート</th>
<td>有効</td>
<td>有効</td>
</tr>
<tr>
<th scope="row">ローカル ハードウェア ステーションのサポート</th>
<td>有効</td>
<td>有効</td>
</tr>
<tr>
<th scope="row">UI レンダリング エンジン</th>
<td>UI の表示には、Curomium エンジンが使用されます。</td>
<td>UI の表示には UWP アプリの表示フレームワークが使用されます。</td>
</tr>
</tbody>
</table>

## <a name="setup-and-installation"></a>設定およびインストール

### <a name="prerequisites"></a>必要条件

- Windows 10 のバージョン 17763.0 以降、Windows 11、または Windows Server 2019
- Microsoft Edge、アプリケーションが Microsoft Edge WebView2 コントロールを使用するため
- Dynamics 365 Commerce (コマース本部および CPOS)

### <a name="device-setup-in-commerce-headquarters"></a>Commerce 本社でのデバイスの設定

Store Commerce のために、**Store Commerce** という名前の新しいアプリケーション タイプが **デバイス** ページに追加されました (**Retail と Commerce \> チャネル設定 \> POS 設定 \> デバイス**)。 Store Commerce でデバイスを作成する場合、このアプリケーション タイプを選択します。

**Store Commerce** アプリケーション タイプがドロップダウン メニューに表示されない場合は、**コマース パラメーター** ページの **一般** タブから **初期化** を実行します (**Retail と Commerce \> 本社設定 \> パラメーター \> コマース パラメーター**)。 その後、ページを更新します。

Store Commerce のために[登録](../tasks/create-associate-registers.md) と[デバイス](../tasks/create-associate-device.md) を作成する必要があります。 その後、アプリを有効にする前に、Commerce 本社の配送スケジュールからレジスター ジョブを実行します。 デバイスの作成中に、**アプリケーション タイプ** フィールドを **Store Commerce** に設定します。

### <a name="device-installation"></a>デバイスのインストール

Store Commerce は、[LCS 共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードできます。 **共有アセット ライブラリ** ページで、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、**Store Commerce** で終わるファイルを検索します。 ファイルをダウンロードした後、以下の手順を実行してアプリをインストールします。

1. Store Commerce をダウンロードしたフォルダーに移動し、管理者モードで PowerShell を開きます。
1. PowerShell で Store Commerce のインストーラを検索し、**install** パラメーターを渡してアプリをインストールします。 オフライン コンポーネントをインストールするには、**--installoffline** パラメーターを渡します。 (たとえば、`Store_Commerce Installer_exe_name install --installoffline` と入力します。) インストール中にデバッグ モードを有効にする場合は、**--enablewebviewdevtools** パラメーターを渡します。 

### <a name="store-commerce-installation-parameters"></a>Store Commerce のインストール パラメーター

PowerShell で **help** コマンドを使用して、すべてのパラメーターに関する情報を検索することもできます。 PowerShell で、Store Commerce インストーラを検索し、`Store_Commerce Installer_exe_name help install` と入力します。

| パラメーター | Description |
|---|---|
| installoffline | オフラインのデータベースを配置します。 |
| sqlservername | Store Commerce がオフライン モードで使用する SQL Server のインスタンスの名前を指定します。 このパラメーターを指定しない場合、インストーラは既定のインスタンスを使用します。 |
| skipsqlfulltextcheck | オフライン配置に必要な SQL 全文検索の検証をスキップします。 |
| trustsqlservercertificate | SQL Server に対する接続が確立された場合は、SQL Server の証明書を信頼します。 セキュリティ リスクを回避するために、実稼働の配置にこの引数を使用しないでください。 既定では、SQL Server の証明書は信頼されません。 |
| enablewebviewdevtools | Store Commerce の開発者ツールを有効にします。 このパラメーターを指定しない場合、Windows 開発者モードが有効になっている場合にのみ開発者ツールが有効になります。 |
| retailserverurl | Store Commerce に使用する既定の Retail Server URL を指定します。 このパラメーターを指定しない場合、ユーザーがデバイスの有効化を行うときに Retail Server URL を入力するように求められます。 |
| useremoteappcontent | リモート アプリケーション コンテンツを使用して CSU でホストされている CPOS から Store Commerce アプリ コンテンツをダウンロードします。 既定では、Store Commerce と共に配置されたローカル アプリケーション コンテンツが使用されます。 |
| skipversioncheck | ダウングレード時に検証をスキップします。 |
| skipurlcheck | インストーラに渡される URL の検証をスキップします。 |
| logdirectorypath | ログのディレクトリのパスを指定します。 |
| config | インストールの一部として使用される構成ファイルのパスを指定します。 |
| verbosity | オフラインのデータベースを配置します。 |
| ヘルプ | パラメーターの情報を表示します。|
| のバージョン | アプリのバージョンに関する情報を表示します。 |

### <a name="activate-store-commerce"></a>Store Commerce のアクティブ化

インストールの後、以下の手順を実行して Store Commerce のアクティブ化を行ってください。

1. Windows の **スタート** メニューで **Store Commerce** を検索し、アプリケーションを開きます。
1. アプリケーションの開始ページで配置オプションとして **リモート アプリ コンテンツ** を選択した場合は、CPOS URL を入力し、**保存** を選択します。 CPOS URL は LCS の環境詳細ページ、または Commerce の **チャネル プロファイル** ページで確認できます (**Dynamics 365 Commerce\> チャネル設定 \> チャネル プロファイル**)。
1. [POS のアクティブ化ガイド](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation)の手順に従って、Store Commerce のアクティブ化を行います。
1. アクティブ化が完了したら、従業員アカウントを使用してアプリケーションにサインインします。

### <a name="troubleshooting-setup-issues"></a> 設定の問題に関するトラブルシューティング

#### <a name="reset-the-app"></a>アプリのリセット

入力した CPOS URL が無効で、変更したい場合、または、有効化の際にアプリがエラー状態にある場合は、アプリをリセットしてプロセスを再開できます。

1. Windowsvの **スタート** メニューで、アプリを選択したまま (あるいは右クリックして) 、それから **詳細 \>アプリの設定** を選択します。
2. アプリ設定ページを **リセット** ボタンが見つかるまで下にスクロールします。
3. **リセット** を選択し、表示されたらアプリのリセットを確認します。

## <a name="customizing-the-app"></a>アプリのカスタマイズ

Store Commerce は、Commerce SDK を使用してカスタマイズできます。 POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更、検証の追加、カスタム機能の追加を行うことができます。 詳細については、[販売時点管理 (POS) 拡張機能の概要](pos-extension/pos-extension-overview.md)を参照するか、または [GitHub](https://github.com/microsoft/Dynamics365Commerce.InStore) のサンプルを確認してください。

### <a name="hardware-station-extension"></a>ハードウェア ステーション拡張機能

Store Commerceは、ハードウェア デバイスと統合できるよう拡張することができます。 GitHub で追加された[サンプル拡張機能コード](https://github.com/microsoft/Dynamics365Commerce.InStore)を使用して、Store Commerce ハードウェア ステーションの拡張機能のパッケージを生成できます。 詳細については [POS と新しいハードウェア デバイスの統合](hardware-device-extension.md) を参照してください。

## <a name="known-issues-with-the-microsoft-edge-webview2-control"></a>Microsoft Edge WebView2 コントロールに関する既知の問題

+ 有効化の際に、複数のオプションを使用して AAD パスワードを入力するように求めるメッセージが表示されたら、パスワードを選択します。 他のオプションが機能しない場合があります。

## <a name="additional-resources"></a>追加リソース
[Dynamics 365 Commerce の店舗内テクノロジー スタックの近代化](https://www.microsoft.com/download/details.aspx?id=103896)

[Commerce SDK の技術解説シリーズ](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions)

[Store Commerce の拡張機能の概要](pos-extension/pos-extension-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
