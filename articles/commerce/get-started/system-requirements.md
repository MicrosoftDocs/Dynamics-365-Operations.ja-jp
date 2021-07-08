---
title: Dynamics 365 Commerce のクラウド配置のシステム要件
description: このトピックでは、現在のバージョンの Dynamics 365 Commerce におけるクラウド配置のシステム要件を一覧表示します。
author: jashanno
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.search.region: Global
ms.search.industry: retail
ms.author: jashanno
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 131169b22be6a667706e8dad93dc0646dec0e402
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193456"
---
# <a name="system-requirements-for-cloud-deployments-of-dynamics-365-commerce"></a>Dynamics 365 Commerce のクラウド配置のシステム要件

[!include [banner](../includes/banner.md)]

このトピックでは、現在のバージョンの Dynamics 365 Commerce のクラウド配置のシステム要件を一覧表示します。 このステップが適切な場合は、コマースをインストールする前に、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
- Google Chrome (公開されている最新バージョン) 
- Apple Safari (公開されている最新バージョン)

> [!NOTE]
> Azure Active Directory トークンが取得できないため、クラウド POS デバイスのデバイスのアクティブ化中に Safari ブラウザーでエラーが表示されることがあります。 この問題は、[Apple デバイスの Microsoft Enterprise SSO プラグイン](/azure/active-directory/develop/apple-sso-plugin) を利用することで解決できます。

各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。

> [!NOTE]
> - タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - 財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。 Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。 匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
> - PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。

### <a name="supported-web-browsers-for-cloud-pos"></a>クラウド POS でサポートされている Web ブラウザー

クラウド販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
  > [!NOTE]
  > リリース 10.0.17 から、Internet Explorer はサポートされなくなりました。
- Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)

## <a name="network-requirements"></a>ネットワーク要件

- コマースは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントからコマースをホストする Microsoft Azure データ センターまでの待機時間のことです。 [AzureSpeed.com](http://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。
- コマースに対する帯域幅の要件は、シナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。

一般に、コマースはインターネットに最適化されます。 ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客は、コマースのプレビュー バージョンを使用する必要があります。

## <a name="net-framework-requirements"></a>.NET Framework 要件

コマースでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.7.1 以降が必要です。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。 

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

次の Microsoft Office アプリケーションがサポートされています。

- Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
- Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="system-requirements-for-commerce-client-components"></a>コマース クライアント コンポーネントのシステム要件

実稼働に移行する前に適切なパフォーマンステストを実行することが重要です。 次に示すのは、アプリケーションが機能するための最小システム要件であると考えられます。 目的のパフォーマンスを達成するには、データ量、時間あたりのトランザクション負荷、カスタマイズの影響などの概念を考慮します。 実装の初期段階と最終テストの前に再度、適切なパフォーマンステストを実施することで、必要なパフォーマンスを向上させることができます。また、基本ソリューションが必要な運用時間を満たしているかどうかを検証できます。

[!WARNING] Microsoft Windows 7 オペレーティング システムは、セキュリティ関連の修正以外ではサポートされなくなりました。 そのため、Windows 7 で Dynamics 365 Commerce コンポーネントが機能する場合がありますが、このオペレーティング システムのサポートに関連するバグ修正はありません。 Windows 7 上でコンポーネントが正常に機能するには回避策が必要な場合があるため、サポートされているオペレーティング システムにアップグレードすることを強くお勧めします。

## <a name="modern-pos-for-windows-requirements"></a>Windows 用 Modern POS 要件

> [!NOTE]
> - Modern POS でオフライン データベースを使用する場合は、Microsoft SQL Server のすべてのシステム要件を満たしていて、システムに 10 GB 以上の空きディスク領域が必要です。 20 GB 以上の空きディスク領域を用意することをお勧めします。 Modern POS のオフライン データベースは、Service Pack 3 以降の SQL Server 2014、Service Pack 2 の SQL Server 2016、または SQL Server 2017 以降が必要です。 使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。 常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。 これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。
> - 2019 年 8 月 1 日以降、 Modern POS や他のクライアント側コンポーネントを使用するには、Microsoft .NET Framework バージョン 4.7.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。

### <a name="supported-windows-operating-systems"></a>サポートされる Windows オペレーティング システム

- Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- Modern POS は Windows Server 2016、Windows 10 Pro、Windows 10 Enterprise、Windows 10 Enterprise Long Term Service Branch (LTSB)、および Windows 10 IOT Enterprise Edition でサポートされています。 少なくとも、Windows 10 Anniversary Update (バージョン 1607)、ビルド 14393 をインストールする必要があります。
- Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Modern POS およびその他の Commerce のコンポーネントの使用をお勧めしません。
- 同じコンピューターで Modern POS と他のコマース コンポーネントを組み合わせて使用することはお勧めできません。

### <a name="minimum-system-requirements"></a>最少システム要件

- POS フル レイアウト (PC およびタブレット) のサポートされている最小有効解像度は 1,024 × 768 (1366 x 768以上を推奨) です
- POS コンパクトレイアウト (電話および小型のタブレット) のサポートされている最小解像度は 320 x 568 (360x640 以上を推奨) です
- Modern POS を実行するコンピューターは以下の要件を満たす必要があります。

    - 最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。
    - 最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。 オフラインの SQL Server と組み合わせるときは、4 GB 以上の RAM が必要です。
    - インターネットにアクセスできる必要があります。

端末がオフライン データベースを使用する場合は、[SQL Server のバージョンとライセンス](../dev-itpro/implementation-considerations-cdx.md#sql-server-versions-and-licenses) セクションを確認することを強くお勧めします。 SQL Server のバージョンについては、現在メインストリーム サポートの期間内にあるバージョンの使用をお勧めします。  サポート日は、[製品とサービス ライフサイクル情報の検索](/lifecycle/products/) という記事で製品ごとに検索できます。

## <a name="modern-pos-for-apple-iphone-or-ipad-requirements"></a>Apple iPhone または iPad 用 Modern POS の要件

- iOS 11 以降

## <a name="modern-pos-for-android-phone-or-tablet-requirements"></a>Android 電話またはタブレット用 Modern POS の要件

- Android OS 6.0 以降

## <a name="retail-hardware-station-requirements"></a>Retail hardware station 要件

> [!NOTE]
> 2019 年 8 月 1 日以降、Retail ハードウェア ステーションや 他のクライアント側コンポーネントを使用するには、.NET Framework version 4.7.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。
> このコンポーネントはサーバー証明書を利用することに注意してください。 有効期限に対してサーバー証明書を管理する必要があります。 既定では、証明書は 1 つの暦年 (365 日) で期限切れになります。

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

- Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- Retail hardware station は、以下のオペレーティング システムでサポートされます。

    - Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。
    - Windows 10 Pro、Enterprise、Enterprise LTSB、および IOT Enterprise Edition。
    - Windows Server 2016 および Windows Server 2019。
    - Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail ハードウェア ステーションおよびその他のコマースのコンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。

- Microsoft Internet Information Services (IIS)
- サード パーティのハードウェア

## <a name="commerce-scale-unit-self-hosted-requirements"></a>Commerce Scale Unit (自己ホスト) 要件

> [!NOTE]
> 2019 年 8 月 1 日以降、Commerce Scale Unit や 他のクライアント側コンポーネントを使用するには、.NET Framework バージョン 4.7.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。
>
> このコンポーネントは、Azure Service to Service 認証に加えてサーバー証明書を利用することに注意してください。  生成された Azure Web アプリケーション キー (旧 *シークレット*) とサーバー証明書の両方が、有効期限に対して管理されている必要があります。  既定では、証明書と生成された Azure web アプリケーション キーは 1 つの暦年 (365日) で期限切れになります。

以下に示す最小システム要件は、テスト シナリオでの機能へ Commerce Scale Unit を取得するのに必要最低限であることに注意してください。 以下は実際的な実稼働環境を表すものではありません。 適切なパフォーマンス テストを実行し、使用するハードウェアがユーザーのニーズを満たしているのを検証することが重要です。 SQL Server のバージョンについては、現在メインストリーム サポートの期間内にあるバージョンの使用をお勧めします。 サポート日は、[製品とサービス ライフサイクル情報の検索](/lifecycle/products/) で製品ごとに検索できます。

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

- Commerce Scale Unit は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- Commerce Scale Unit は、以下のオペレーティング システムでサポートされます。

    - Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。
    - Windows 10 Pro、Enterprise、Enterprise LTSB、および IOT Enterprise Edition。
    - Windows Server 2016 および Windows Server 2019。
    - Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Commerce Scale Unit およびその他のコマース コンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

> [!NOTE]
> Commerce Scale Unit の最小システム要件を次に示します。  これらと推奨要件はどちらも、テストおよび基本的な機能のための最小要件です。  パフォーマンス テストを実行し、Commerce Scale Unit で使用するハードウェアが期待を満たしていることを検証することが重要です。

- 4 GB の RAM
- コアごとの CPU 最小処理スピードが 1.6 GHz の i5 (または同等) (最少 2 コア)。
- 少なくとも 15 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります)。
- サポートされているバージョンの SQL Server。  Express Edition では既知の制限が原因で同期の問題が発生する可能性があるので、Commerce Scale Unit (自己ホスト) の標準ライセンス以上を使用することをお勧めします。 詳細については、[SQL Server のバージョンとライセンス](../dev-itpro/implementation-considerations-cdx.md#sql-server-versions-and-licenses) を参照してください。

### <a name="recommended-system-requirements"></a>推奨システム要件

- 6 GB の RAM
- コアごとの CPU 最小処理スピードが 2.4 GHz の i7 (または同等) (4 つのコアを推奨)。
- 少なくとも 20 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります)。
- - サポートされているバージョンの SQL Server。 Express Edition では既知の制限が原因で同期の問題が発生する可能性があるので、Commerce Scale Unit (自己ホスト) の標準ライセンス以上を使用することをお勧めします。 詳細については、[SQL Server のバージョンとライセンス](../dev-itpro/implementation-considerations-cdx.md#sql-server-versions-and-licenses) を参照してください。

個人のハードウェア ニーズを決定する際に次の品目も考慮することは、組織の最高の利益となります。

- 物理的ネットワーク ポートの数 (ポートが増えると 1 秒あたりのスループットが強化されます)。
- SQL Server のログ フラッシュ サイズ (これは SQL Server パフォーマンスに直接影響します)。
- データの読み取りと書き込み能力 (これは SQL サーバー パフォーマンスに直接影響を与えます)。
- CPU コアの数、コアごとの並行スレッドの数、およびコアあたりの速度 (これはシステムの全体的なスループットに影響します)。
- 負荷分散が必要かどうか。

## <a name="connector-requirements"></a>コネクタの要件

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

- Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。
- どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- 次のオペレーティング システムでは、両方のコンポーネントがサポートされています。

    - Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。
    - Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。
    - Windows Server 2016 および Windows Server 2019。
    - Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro でコマース コンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

- 2 GB の RAM (4 GB の RAM を推奨)。
- コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)。
- 少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります)。

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件

ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../fin-ops-core/dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally) を参照してください。

## <a name="database-collation"></a>データベース照合順序

クラウドで唯一サポートされているコマース データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。 開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。 また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。

## <a name="additional-resources"></a>その他のリソース

[ベータ評価版の入手](../../fin-ops-core/dev-itpro/dev-tools/get-evaluation-copy.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
