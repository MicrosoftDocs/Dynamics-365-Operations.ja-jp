---
title: Store Commerce アプリ
description: この記事では、Windows 用の Microsoft Dynamics 365 Commerce Store Commerce アプリの設定および構成方法について説明します。 Dynamics 365 Commerce バージョン 10.0.25 以降に適用されます。
author: josaw1
ms.date: 10/25/2022
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: f998e293ac567be565ca413f42f019bdbe3eb1d8
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725564"
---
# <a name="store-commerce-app"></a>Store Commerce アプリ

[!include [banner](../includes/banner.md)]

この記事では、Windows 用の Microsoft Dynamics 365 Commerce Store Commerce アプリの設定および構成方法について説明します。 Dynamics 365 Commerce バージョン 10.0.25 以降に適用されます。

Dynamics 365 Commerce Store Commerce アプリは、物理店舗向けの次世代のオファリングです。 Modern 販売時点管理 (MPOS) および Cloud 販売時点管理 (CPOS) を 1 つのアプリケーションに統合し、拡張機能を含めて MPOS および CPOS の機能を保持しながら、小売業者に配置の選択肢を提供し、パフォーマンスの向上や、優れたアプリケーション ライフサイクル管理 (ALM) を行う、現物店舗向けの次世代オファリングです。

Store Commerce アプリは、レジ担当者、販売担当者、販売在庫担当者、在庫担当者、および店舗管理者などの第一線の作業者に豊富なコマース機能を提供します。 これらの作業者は、現金売りトランザクション、現金/シフト管理、顧客契約、支援販売、クライアンテリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、レポートなどのコマース操作を実行することができます。

Store Commerce アプリは、[Microsoft Edge WebView2](/microsoft-edge/webview2/) コントロールを使用して CPOS アプリケーションを表示する Windows 用の [Windows Presentation Foundation (WPF)](/dotnet/desktop/wpf/?view=netdesktop-6.0&preserve-view=true) シェル アプリケーションです。 CPOS は Web ブラウザでのみ実行できますが、Store Commerce は [MPOS](retail-modern-pos-architecture.md) のようにネイティブの Windows アプリケーションとして実行でき、MPOS と CPOS の両方のメリットがあります。

Store Commerce はローカル ハードウェア ステーションおよびオフライン使用をサポートし、支払ターミナル、プリンター、キャッシュ ドロワーに直接統合できます。 共有ハードウェア ステーションを設定する必要なしに、ハードウェア デバイスを使用することができます。

ユーザー インターフェイス (UI) を表示するために、Store Commerce は、ユニバーサル Windows プラットフォーム (UTC) アプリ表示フレームワークの代わりに Chromium エンジンを使用します。 Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。 MPOS と Store Commerce の主な違いは、Store Commerce がアプリを表示するのに Chromium エンジンを使用する点です。

Store Commerce アプリは、Android および iOS プラットフォームでも利用できます。 詳細については、[モバイル用 Store Commerce](store-commerce-mobile.md) を参照してください。 

## <a name="benefits-of-store-commerce"></a>Store Commerce の利点

- アプリケーション ライフサイクル管理は簡略化されました。
- コマース ソフトウェア開発キット (SDK) を使用して MPOS または CPOS 用に開発された拡張機能または独立系ソフトウェア ベンダー (ISV) のコードは、最小限の変更で Store Commerce で再利用することができます。
- 業界標準の開発者エクスペリエンスでは、Microsoft Visual Studio Code および GitHub が使用されます。
- Store Commerce は、MPOSとCPOSの両方の利点を提供します。
- パフォーマンスが大幅に向上します。
- POS および拡張機能のアップグレードは、Commerce のシールド インストーラー フレームワークを通じて簡略化できます。
- 専用のハードウェア ステーションをサポートしています。
- オフラインでの配置をサポートしています。

Store Commerce アプリの機能を確認するには、[Store Commerce アプリ機能](../store-commerce-capabilities.md)を参照してください。

## <a name="application-lifecycle-management"></a>アプリケーション ライフサイクル管理

Store Commerce アプリは Windows デバイスで実行され、[Microsoft Lifecycle Services (LCS) の共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードできます。 **共有アセット ライブラリ** ページで、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、「Store Commerce」で終わるファイルを検索します。 使用している Commerce リリースのバージョン (10.0.25 または 10.0.26 など) を選択してください。

### <a name="store-commerce-deployment-options"></a>Store Commerce の配置オプション

Store Commerce は、2 つのタイプの配置トポロジをサポートしています。

- **アプリ内**- Modern 販売時点管理 (MPOS) などのすべてのコンポーネントがローカルに配置されます。 オフライン モードおよびローカルのハードウェア ステーション (HWS) がサポートされます。
- **ハイブリッド**- Store Commerce は、Commerce Scale Unit (CSU) に配置された Cloud POS を表示し、ローカルのハードウェア ステーションをサポートします。 ただし、オフラインではサポートされていません。

ハイブリッド トポロジおよびアプリ内トポロジ用に独立したインストーラーはありません。 配置オプションは、インストール中に渡されるパラメーターによって決まります。

![Store Commerce の配置オプション。](../media/SC-Deployment.png)

### <a name="in-app-deployment"></a>アプリ内配置

アプリ内配置のオプションの場合、アプリケーション コンテンツは MPOS の場合と同様に Store Commerce にローカルで配置されます。 Store Commerce はローカル配置からアプリケーション コンテンツを表示します。 アプリケーション コンテンツを取得するのに CSU でホストされている CPOS には接続しません。

アプリケーション コンテンツを更新するには、最新バージョンの Store Commerce インストーラを実行します。 CSU を更新するとき、アプリケーション コンテンツは更新されません。 したがって、更新は個々のレジスターで管理することができます。

アプリ内配置はオフライン モードをサポートします。 インストール中に **--installoffline** パラメーターを渡して、オフラインのデータベースを配置します。 オフライン モードでは、アプリケーションは CSU または Commerce headquarters に接続できず、ローカルに配置された CRT を使用します。

> [!NOTE]
> Store Commerce のインストール中に、ユーザーはパラメーターを渡して、ハイブリッド オプションまたはアプリ内オプションのいずれかを選択できます。 既定のオプションは、アプリ内配置です。

### <a name="hybrid-deployment"></a>ハイブリッド配置

Store Commerce は、CPOS を表示し、CSU をオンライン モードで使用して Headless Commerce および Commerce 本部に接続するシェルです。 ハイブリッド モードでは、Store Commerce アプリのコンテンツは、CSU でホストされている CPOS から表示されます。 Store Commerce アプリを開くと、CPOS URL の入力を求めるメッセージが表示されます。

![Cloud POS の URL の入力を求めるメッセージが表示される Store Commerce ダイアログ ボックスを有効化します。](../media/SC-Hybrid.png)

Store Commerce を更新するには、CSU を更新します。 その後、Store Commerce は更新を自動的に受信します。 更新は CSU で集中管理されるので、個々のレジスターで管理する必要はありません。 Store Commerce アプリケーションのシェルは、別途インストーラーを使用して個別に更新する必要があります。 CSU の更新方法の詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) を参照してください。 

## <a name="store-commerce-and-mpos-parity"></a>Store Commerce と MPOS の機能

Store Commerce には MPOS と完全に同等の機能があります。 さまざまな POS アプリケーションおよびトポロジの詳細については [Modern POS (MPOS) かクラウド POS かの選択](../mpos-or-cpos.md)を参照してください。

## <a name="hardware-parity-between-mpos-and-store-commerce"></a>MPOS と Store Commerce の間のハードウェア パリティ

Store Commerce アプリは、[ポイント オブ サービス デバイス](/windows/uwp/devices-sensors/pos-get-started.md) であるユニバーサル Windows プラットフォーム (UWP) 周辺機器をサポートしません。 現在、ユニバーサル シリアル バス (USB) スキャナーや磁気ストライプ リーダーをプラグアンドプレイ モードで使用している場合は、OLE for Retail POS (OPOS) ドライバーをインストールし、ハードウェア プロファイルでこれらのデバイスを構成して、Store Commerce アプリで動作するようにする必要があります。 Store Commerce の周辺機器サポートの詳細については、[Commerce の周辺機器](../retail-peripherals-overview.md) を参照してください。

MPOS から Store Commerce に移行するには、[Modern POS を Store Commerce に移行する](pos-extension/migrate-mpos-store-commerce.md) を参照してください。

## <a name="store-commerce-and-cpos-parity"></a>Store Commerce と CPOS の機能

Store Commerce には CPOS と完全に同等の機能があります。 さらに、Store Commerce は専用のハードウェアをサポートし、オフラインで配置します。

## <a name="store-commerce-and-mposcpos"></a>Store Commerce および MPOS/CPOS

Windows およびモバイル プラットフォーム用の Store Commerce アプリは、Dynamics 365 Commerce 用の次世代の POS アプリケーションです。 Microsoft では、2023 年 10 月に MPOS および [Retail ハイブリッド アプリ](hybridapp.md) のハイブリッド アプリケーションを廃止する予定であり、新しいすべての配置には Store Commerce または CPOS の使用をお勧めします。 既存の顧客は、MPOS から Store Commerce への移行を計画する必要があります。 

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
<td>はい、ただしポイント オブ サービス デバイスの UWP 周辺機器はサポートされません。 Store Commerce の周辺機器サポートの詳細については、[Commerce の周辺機器](../retail-peripherals-overview.md) を参照してください。</td>
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

- Windows 10 のバ―ジョン 17763.0 以降、Windows 11 (Pro、Enterprise、LTSC、IOT Enterprise Edition)、または Windows Server 2019 (Standard、Essentials)
- [Microsoft Edge WebView2](https://developer.microsoft.com/microsoft-edge/webview2/) (Evergreen スタンドアロン インストーラーを使用します)。
- SQL Server Express、SQL Server Standard、または SQL Server Enterprise (オフライン モードの場合のみ必須)。 使用する SQL Server エディションの詳細については、[Commerce のオフライン実装およびトラブルシューティング](implementation-considerations-offline.md) を参照してください。
- Dynamics 365 Commerce (Commerce 本部と Cloud Scale Unit)
- .NET Framework バージョン 4.7.2 またはそれ以降。 [.NET Framework のインストール](https://dotnet.microsoft.com/download/dotnet-framework) を参照する

### <a name="device-setup-in-commerce-headquarters"></a>Commerce 本社でのデバイスの設定

Store Commerce のために、**Store Commerce** という名前の新しいアプリケーション タイプが **デバイス** ページに追加されました (**Retail と Commerce \> チャネル設定 \> POS 設定 \> デバイス**)。 Store Commerce でデバイスを作成する場合、このアプリケーション タイプを選択します。

**Store Commerce** アプリケーション タイプがドロップダウン メニューに表示されない場合は、**コマース パラメーター** ページの **一般** タブから **初期化** を実行します (**Retail と Commerce \> 本社設定 \> パラメーター \> コマース パラメーター**)。 その後、ページを更新します。

Store Commerce のために[登録](../tasks/create-associate-registers.md) と[デバイス](../tasks/create-associate-device.md) を作成する必要があります。 その後、アプリを有効にする前に、Commerce 本社の配送スケジュールからレジスター ジョブを実行します。 デバイスの作成中に、**アプリケーション タイプ** フィールドを **Store Commerce** に設定します。

### <a name="device-installation"></a>デバイスのインストール

Store Commerce は、[LCS 共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary)からダウンロードできます。 **共有アセット ライブラリ** ページで、**Retail セルフサービス パッケージ** をアセット タイプとして選択し、**Store Commerce** で終わるファイルを検索します。 ファイルをダウンロードした後、以下の手順を実行してアプリをインストールします。

1. Store Commerce をダウンロードしたフォルダーに移動し、管理者モードで PowerShell を開きます。
1. PowerShell で Store Commerce のインストーラーを検索し、**install** パラメーターを渡してアプリをインストールします。 オフライン コンポーネントをインストールするには、**--installoffline** パラメーターを渡します。 (たとえば、`Store_Commerce Installer_exe_name install --installoffline` と入力します。) インストール中にデバッグ モードを有効にする場合は、**--enablewebviewdevtools** パラメーターを渡します。 

### <a name="store-commerce-installation-parameters"></a>Store Commerce のインストール パラメーター

PowerShell で **help** コマンドを使用して、すべてのパラメーターに関する情報を検索することもできます。 PowerShell で、Store Commerce インストーラを検索し、`Store_Commerce Installer_exe_name help install` と入力します。

| パラメーター | Description |
|---|---|
| installoffline | オフラインのデータベースを配置します。 |
| sqlservername | Store Commerce がオフライン モードで使用する SQL Server のインスタンスの名前を指定します。 このパラメーターを指定しない場合、インストーラは既定のインスタンスを使用します。 |
| skipsqlfulltextcheck | オフライン配置に必要な SQL 全文検索の検証をスキップします。 |
| trustsqlservercertificate | SQL Server に対する接続が確立された場合は、SQL Server の証明書を信頼します。 セキュリティ リスクを回避するために、運用配置にこの引数を使用しないでください。 既定では、SQL Server の証明書は信頼されません。 |
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

### <a name="troubleshoot-setup-issues"></a>設定の問題に関するトラブルシューティング

トラブルシューティングの情報については、[Store Commerce のセットアップおよびインストールに関するトラブルシューティング](../troubleshoot/store-commerce-setup-installation.md) を参照してください。

## <a name="customize-the-app"></a>アプリのカスタマイズ

Store Commerce は、Commerce SDK を使用してカスタマイズできます。 POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更、検証の追加、カスタム機能の追加を行うことができます。 詳細については、[販売時点管理 (POS) 拡張機能の概要](pos-extension/pos-extension-overview.md)を参照するか、または [GitHub](https://github.com/microsoft/Dynamics365Commerce.InStore) のサンプルを確認してください。

### <a name="hardware-station-extension"></a>ハードウェア ステーション拡張機能

Store Commerceは、ハードウェア デバイスと統合できるよう拡張することができます。 GitHub で追加された[サンプル拡張機能コード](https://github.com/microsoft/Dynamics365Commerce.InStore)を使用して、Store Commerce ハードウェア ステーションの拡張機能のパッケージを生成できます。 詳細については [POS と新しいハードウェア デバイスの統合](hardware-device-extension.md) を参照してください。

## <a name="known-issues-with-the-microsoft-edge-webview2-control"></a>Microsoft Edge WebView2 コントロールに関する既知の問題

+ 有効化の際に、複数のオプションを使用して AAD パスワードを入力するように求めるメッセージが表示されたら、パスワードを選択します。 他のオプションが機能しない場合があります。

## <a name="additional-resources"></a>追加リソース
[Store Commerce アプリの機能](../store-commerce-capabilities.md)

[Dynamics 365 Commerce の店舗内テクノロジー スタックの近代化](https://www.microsoft.com/download/details.aspx?id=103896)

[Commerce SDK の技術解説シリーズ](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions)

[Store Commerce の拡張機能の概要](pos-extension/pos-extension-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
