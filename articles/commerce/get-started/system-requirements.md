---
title: Dynamics 365 Commerce のクラウド配置のシステム要件
description: このトピックでは、現在のバージョンの Dynamics 365 Commerce におけるクラウド配置のシステム要件を一覧表示します。
author: jashanno
ms.date: 03/01/2022
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
ms.openlocfilehash: a8a20841a39568684f8f13f397a0d5dc5e626a28
ms.sourcegitcommit: 116898def829c0f78bda8a117242aa308793465d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370938"
---
# <a name="system-requirements-for-cloud-deployments-of-dynamics-365-commerce"></a>Dynamics 365 Commerce のクラウド配置のシステム要件

[!include [banner](../includes/banner.md)]

このトピックでは、現在のバージョンの Dynamics 365 Commerce のクラウド配置のシステム要件を一覧表示します。 このステップが適切な場合は、コマースをインストールする前に、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Google Chrome (公開されている最新バージョン) 
- Apple Safari (公開されている最新バージョン)

> [!NOTE]
> Azure Active Directory トークンが取得できないため、クラウド POS デバイスのデバイスのアクティブ化中に Safari ブラウザーでエラーが表示されることがあります。 この問題は、[Apple デバイスの Microsoft Enterprise SSO プラグイン](/azure/active-directory/develop/apple-sso-plugin) を利用することで解決できます。
>
> リリース 10.0.17 では、Internet Explorer はサポートされている Web ブラウザーではありません。

各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。

> [!NOTE]
> - タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - 財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。 Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。 匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
> - PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。

### <a name="supported-web-browsers-for-cloud-pos"></a>クラウド POS でサポートされている Web ブラウザー

クラウド販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)

## <a name="network-requirements"></a>ネットワーク要件

- コマースは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントからコマースをホストする Microsoft Azure データ センターまでの待機時間のことです。 [AzureSpeed.com](http://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。
- コマースに対する帯域幅の要件は、シナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。

一般に、コマースはインターネットに最適化されます。 ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客は、コマースのプレビュー バージョンを使用する必要があります。

## <a name="net-framework-requirements"></a>.NET Framework 要件

コマースでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.7.1 以降が必要です。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。 コマース クライアント コンポーネント (シールド インストーラーまたはレガシ インストーラー) については、使用可能な .NET Framework の最新バージョンを常に使用することをお勧めします。

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

次の Microsoft Office アプリケーションがサポートされています。

- Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
- Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="system-requirements-for-commerce-client-components"></a>コマース クライアント コンポーネントのシステム要件

実稼働に移行する前に適切なパフォーマンステストを実行することが重要です。 次に示すのは、アプリケーションが機能するための最小システム要件であると考えられます。 目的のパフォーマンスを達成するには、データ量、時間あたりのトランザクション負荷、カスタマイズの影響などの概念を考慮します。 実装の初期段階と最終テストの前に再度、適切なパフォーマンステストを実施することで、必要なパフォーマンスを向上させることができます。また、基本ソリューションが必要な運用時間を満たしているかどうかを検証できます。

セルフサービス コンポーネントが SQL データベースを使用する場合は、[SQL サーバーのバージョンとライセンス](../dev-itpro/implementation-considerations-cdx.md#sql-server-versions-and-licenses) を確認することを強くお勧めします。 現在メインストリーム サポートの期間内にある SQL Server のバージョンの使用をお勧めします。 [製品とサービス ライフサイクル情報](/lifecycle/products/) という記事でサポート日を製品ごとに検索できます。 セルフサービス コンポーネント用の SQL データベースには、SQL Server 2017 以降が必要です。 使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。 常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。 これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。 レガシ セルフサービス インストーラーは、Service Pack 2 以降の SQL Server 2016 もサポートしています。

セルフサービス コンポーネントがサーバー証明書を使用する場合、証明書の有効期限を管理することが重要です。 既定では、証明書は 1 つの暦年 (365 日) 後に期限切れになります。 サーバー証明書を使用するセルフサービス コンポーネントには、ハードウェア ステーション、または Commerce Scale Unit (自己ホスト) が含まれます。

> [!NOTE]
> レガシ Commerce Scale Unit (自己ホスト) のセルフサービス コンポーネントでは、Azure Service to Service 認証が使用されます。 生成された Azure Web アプリケーション キー (旧 *シークレット*) とサーバー証明書の両方の有効期限を管理することが重要です。 既定では、証明書と生成された Azure web アプリケーション キーは 1 つの暦年 (365日) 後に期限切れになります。
>
> サポートされている .NET Framework のバージョンが更新されました。 レガシ セルフサービス クライアント側コンポーネントを使用するには、.NET Framework version 4.7.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。 シールド インストーラーの場合は、常に .NET Framework の最新バージョンをターゲット コンピューターにインストールすることをお勧めします。

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

このセクションでは、各 Commerce セルフサービス インストーラーでサポートされているオペレーティング システムの一覧を示します。

> [!WARNING]
> Windows 7 オペレーティング システムは、セキュリティ関連の修正以外ではサポートされません。 そのため、Windows 7 で Commerce コンポーネントが機能する場合がありますが、このオペレーティング システムのサポートに特に関連するバグ修正はありません。

#### <a name="modern-pos"></a>Modern POS

- 使用可能な最新の更新プログラムを含む Windows 10 (Pro、Enterprise、LTSC、および IOT エンタープライズ エディション) がサポートされます。

    > [!NOTE]
    > Windows 更新プログラムを適切にスケジュール設定できるよう、Windows 10 Pro はドメインの一部を除いてお勧めしません。

- Windows Server 2019 はサポートされます。
- 別のセルフサービス コンポーネント (たとえば、ハードウェア ステーションまたは Commerce Scale Unit \[自己ホスト\]) と同じコンピューターの Modern POS を使用することはお勧めしません。
- レガシ セルフサービス インストーラーは、利用可能な最新の更新プログラムを使用して Windows Server 2016 および Windows 10 LTSB もサポートします。
- Modern POS for iOSは、iOS バージョン 11 以降をサポートしています。
- Modern POS for Android は、Android バージョン 6.0 以降をサポートしています。

> [!NOTE]
> Modern POS がオフライン データベースを使う場合、コンピューターは SQL Server のすべてのシステム要件を満たす必要があります。 また、システムに少なくとも 15 ギガバイト (GB) の使用可能なディスク領域が必要です。 ただし、最低 25 GB の使用可能なディスク領域をお勧めします。

#### <a name="hardware-station-and-commerce-scale-unit-self-hosted"></a>ハードウェア ステーションと Commerce Scale Unit (自己ホスト)

- 使用可能な最新の更新プログラムを含む Windows 10 (Pro、Enterprise、LTSC、および IOT エンタープライズ エディション) がサポートされます。

    > [!NOTE]
    > Windows 更新プログラムを適切にスケジュール設定できるよう、Windows 10 Pro はドメインの一部を除いてお勧めしません。

- Windows Server 2019 はサポートされます。
- 別のセルフサービス コンポーネント (たとえば、Modern POS) と同じコンピューターの セルフサービス コンポーネントを使用することはお勧めしません。
- レガシ セルフサービス インストーラーは Windows Server 2016 および Windows 10 LTSB もサポートします。

### <a name="system-requirements"></a>システム要件

Commerce セルフサービス コンポーネントを正しく使用するには、パフォーマンス テストが重要であることに注意してください。 すべてのコンポーネントで、テスト機能を目的として、次のような最低限のシステムがサポートされています。

- コアあたり 2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサ。
- 3 GB の RAM。
- 要求と応答の流れを処理するためのインターネット アクセスおよび十分なネットワーク スループット。 (この要件は、コンピュータ レベルとネットワーク レベルの両方にあることに注意してください)。
- SQL Server および Internet Information Services (IIS) の要件など、コンポーネント固有のシステム要件。
- ディスク領域の少なくとも 10% 以上が使用可能です。 (SQL Server を使用する場合は、使用可能なディスク領域を 10 GB 未満にすることをお勧めします)。

また、カスタマイズやパフォーマンス要件が生成される場合、通常は、ユーザーのニーズを満たすために、各コンポーネントにより強力なシステムが必要になります。

#### <a name="modern-pos"></a>Modern POS

- POS フル レイアウト モード (PC およびタブレット) のサポートされている最小有効解像度は、1,024 × 768 です。 (ただし、1366 × 768 以上をお勧めします)。
- POS コンパクト レイアウト モード (電話および小型のタブレット) のサポートされている最小有効解像度は 320 x 568 です。 (ただし、360 × 640 以上をお勧めします)。
- よりパフォーマンスの高い Modern POS ターミナルに対する最小推奨事項を次に示します。

    - 最低限 128 MB の専用グラフィカル メモリまたは 256 MB の共有グラフィカル メモリが推奨されています。
    - 4 GB 以上の RAM が推奨されています。 この推奨事項では、オフライン データベース サポートに関する SQL Server の要件をさらに確認する必要があります。
    - SQL Express は、多くの場合、オフライン データベースで使用されます。 これらのシナリオでは、オフライン データベース サイズを追跡する必要があります。 (最大サイズは 10 GB です)。

#### <a name="hardware-station"></a>Hardware station

- IIS でサポートされる最小システム要件
- 関連付けおよび使用しているすべてのサードパーティ ハードウェアでサポートされる最小システム要件

#### <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (自己ホスト)

Commerce Scale Unit (自己ホスト) の最小システム要件は、通常テスト シナリオにある機能に必要な必要最低限を記載しています。 ここで説明されている要件は、現実的な実稼働環境を表すのではありません。 適切なパフォーマンス テストを行い、使用されるハードウェア ステーション、Modern POS、クラウド POS、および Commerce Scale Unit (自己ホスト) コンポーネントまたはコンピューターにアクセスして使用するサードパーティ コンポーネントの需要を満たすコンピューター ハードウェアを検証する必要があります。 さらに、SQL Server の標準ライセンス バージョン以上 (例えば、Enterprise 版) を使用して、プロセッサと RAM の全機能を活用することを強くお勧めします。

追加要件を次に示します。

- 最低 6 GM の RAM が必要だが、64 GB 以上の RAM が必要な場合がある
- 2.4 GHz マルチコア CPU ですが、サーバー グレードのハードウェアには複数のマルチコア CPU が必要になる場合があります (4コア プロセッサを推奨しています)。
- 関連付けられているすべての店舗 (チャネル) のすべての Commerce データの合計を格納するのに十分なディスク領域

    必要なディスク量は、最小で 10 GB から 20 GB、最大で数テラバイトになる場合があります。

また、Commerce Scale Unit (自己ホスト) のシステム要件を決定する場合は、次のパフォーマンス面も考慮することを強くお勧めします。

- 物理的ネットワーク ポートの数 (ポートが増えると 1 秒あたりのスループットが強化されます)。
- SQL Server のログ フラッシュ サイズ (これは SQL Server パフォーマンスに直接影響します)。
- データの読み取りと書き込み能力 (これは SQL サーバー パフォーマンスに直接影響を与えます)。
- 独立した Commerce Scale Unit サブコンポーネントを処理する複数のシステム (複数の Retail サーバーや障害復旧が有効なデータベースのフェールオーバーなど) に負荷分散が必要になる

## <a name="dynamics-ax-2012-r3-connector-requirements"></a>Dynamics AX 2012 R3 Connector の要件

以前の Dynamic AX 2012 R3 では Enterprise POS のようなコンポーネントが分離した性質を持ち、特別な用途が与えられたので、2 つのコネクタ コンポーネントは別のセクションに保管されていました。

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

Connector for Microsoft Dynamics AX 2012 R3 には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。

- どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- 次のオペレーティング システムでは、両方のコンポーネントがサポートされています。

    - Windows 10 Pro、Enterprise、および Enterprise LTSB エディション

        > [!NOTE]
        > Windows 更新プログラムを適切にスケジュール設定できるよう、Windows 10 Pro はドメインの一部を除いてお勧めしません。

    - Windows Server 2016 および Windows Server 2019

### <a name="minimum-system-requirements"></a>最少システム要件

Commerce Scale Unit (自己ホスト) に関して、レガシ POS システムのエンタープライズ アーキテクチャ全体のスループットを処理するために、サーバーグレードの非常に大きいハードウェアが必要になる場合があります。 ただし、ここでは機能をテストするために必要な絶対最小要件を次に示します。

- 2 GB の RAM (ただし 4 GB の RAM を推奨)。
- コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)
- 少なくとも 15 GB の空き領域 (チャネル データベースが大量の領域を必要とする場合があります)。 サイズは数テラバイトでも指定できます)。

## <a name="recommended-network-exceptions"></a>推奨されるネットワーク例外

多くの場合 (特に企業環境) 、ネットワーク関連のセキュリティに関して、特定の例外に注意する必要があります。 これらのセキュリティ重視のネットワークでは、ネットワーク関連の許可リストに少なくとも次の例外を追加することをお勧めします:

- \*.static.akamaitechnologies.com
- \*.azure.com
- \*.dynamics.com
- \*.microsoft.com
- \*.visualstudio.com
- \*.windows.net

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件

ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../fin-ops-core/dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally) を参照してください。

## <a name="database-collation"></a>データベース照合順序

クラウドで唯一サポートされているコマース データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。 開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。 また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。

## <a name="additional-resources"></a>追加リソース

- [ベータ評価版の入手](../../fin-ops-core/dev-itpro/dev-tools/get-evaluation-copy.md)
- [Dynamics 365 Commerce アーキテクチャの概要](../commerce-architecture.md)
- [店舗内トポロジの選択](../dev-itpro/retail-in-store-topology.md)
- [デバイス管理実装ガイダンス](../implementation-considerations-devices.md)
- [Modern POS (MPOS) のコンフィギュレーション、インストール、および有効化](../retail-modern-pos-device-activation.md)
- [Commerce Scale Unit のコンフィギュレーションとインストール (自己ホスト)](../dev-itpro/retail-store-scale-unit-configuration-installation.md)
- [Commerce Data Exchange 実装ガイダンス](../dev-itpro/implementation-considerations-cdx.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
