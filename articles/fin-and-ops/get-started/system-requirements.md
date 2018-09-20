---
title: "クラウド配置のシステム要件"
description: "このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド展開のシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: ab1c2f8b15e593d25e07de83979ff0ad26564c77
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2018

---

# <a name="system-requirements-for-cloud-deployments"></a>クラウド配置のシステム要件

[!include [banner](../includes/banner.md)]

このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド展開のシステム要件を一覧表示します。 Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
- Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)
- Mac OS X 10.10 (Yosemite)、10.11 (El Capitan)、または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)

各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。

> [!NOTE]
> - タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - ワークフロー エディターは ClickOnce アプリケーションとして起動されます。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。 ワークフロー エディター ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。
> - 財務報告のレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Chrome を使用している場合、レポート デザイナーのクライアントをダウンロードするために ClickOnce 拡張機能をインストールする必要があります。 匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
> - PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS でサポートされている Web ブラウザー

Retail Cloud 販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
- Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)

## <a name="network-requirements"></a>ネットワーク要件
- Finance and Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 これは、ブラウザー クライアントから Finance and Operations をホストする Microsoft Azure データセンターまでの待機時間です。 ネットワー待ち時間を <http://www.azurespeed.com> でテストすることをお勧めします。
- Finance and Operations の帯域幅の要件はシナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。

一般に、Finance and Operations は、インターネットに最適化されます。 ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客は、Finance and Operations のプレビュー バージョンを使用するべきです。

## <a name="net-framework-requirements"></a>.NET Framework 要件

Finance and Operations では、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として、Microsoft NET Framework バージョン 4.6.2 が必要です。 インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。

## <a name="supported-microsoft-office-applications"></a>サポートされている Microsoft Office アプリケーション

次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。


-   Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
-   [Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="retail-modern-pos-for-windows-requirements"></a>Windows 用 Retail Modern POS の要件

> [!NOTE]
> Retai Modern POS でオフライン データベースを使う場合、コンピューターは Microsoft SQL Server のすべてのシステム要件を満たす必要があります。 Retail Modern POS のオフライン データベースは、Service Pack 3 以降の SQL Server 2012、Service Pack 2 以降の SQL Server 2014 、または SQL Server 2016 が必要です。  使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。 常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。 これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。
> 2018 年 10 月 1 日以降、Retail Modern POS や 他のクライアント側コンポーネントを使用するには、Microsoft .NET Framework version 4.6.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。

### <a name="supported-windows-operating-systems"></a>サポートされる Windows オペレーティング システム

- Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- Retail Modern POS は Windows Server 2016、Windows 10 Pro、Windows 10 Enterprise、Windows 10 Enterprise Long Term Servicing Branch (LTSB) エディションでサポートされています。 少なくとも、Windows 10 Anniversary Update (バージョン 1607)、ビルド 14393 をインストールする必要があります。
- Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Modern POS およびその他の Retail のコンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

- POS フル レイアウト (PC およびタブレット) のサポートされている最小有効解像度は 1,024 × 768 (1366 x 768以上を推奨) です
- POS コンパクトレイアウト (電話および小型のタブレット) のサポートされている最小解像度は 320 x 568 (360x640 以上を推奨) です
- Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。

    - 最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。
    - 最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。  オフラインの SQL Server と組み合わせるときは、4 GB 以上の RAM が必要です。
    - インターネットにアクセスできる必要があります。

## <a name="retail-modern-pos-for-apple-iphone-or-ipad-requirements"></a>Apple iPhone または iPad 用 Retail Modern POS の要件

- iOS 11 またはそれ以降

## <a name="retail-modern-pos-for-android-phone-or-tablet-requirements"></a>Android 電話またはタブレット用 Retail Modern POS の要件

- Android OS 6.0 以降

## <a name="retail-hardware-station-requirements"></a>Retail hardware station 要件

> [!NOTE]
> 2018 年 10 月 1 日以降、Retail ハードウェア ステーションや 他のクライアント側コンポーネントを使用するには、.NET Framework version 4.6.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

- Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- Retail hardware station は、以下のオペレーティング システムでサポートされます。

    - Windows 7 Professional、Enterprise、または Ultimate エディション。
    
        > [!NOTE]
        > Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。

    - Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。
    - Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。
    - Windows Server 2012 R2 および Windows Server 2016。
    - Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail ハードウェア ステーションおよびその他の Retail のコンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。

- Microsoft Internet Information Services (IIS)
- サード パーティのハードウェア

## <a name="retail-store-scale-unit-requirements"></a>Retail Store スケール ユニット要件

> [!NOTE]
> 2018 年 10 月 1 日以降、Retail Store Scale Unit や他のクライアント側コンポーネントを使用するには、.NET Framework version 4.6.1 以降をインストールする必要があります。 インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。

以下に示す最小システム要件は、テスト シナリオでの機能へ Retail Store スケール ユニットを取得するのに必要最低限であることをご確認下さい。  以下は実際的な実稼働環境を表すものではありません。  適切なパフォーマンス テストを実行し、使用するハードウェアがユーザーのニーズを満たしているのを検証することが重要です。

### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

- Retail Store スケール ユニットは 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- Retail Store スケール ユニットは、以下のオペレーティング システムでサポートされます。

    - Windows 7 Professional、Enterprise、または Ultimate エディション。
    
        > [!NOTE]
        > Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。
    
    - Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。
    - Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。
    - Windows Server 2012 R2 および Windows Server 2016。
    - Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Store Scale Unit およびその他の Retail のコンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

- 4 GB の RAM
- コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)
- 少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

### <a name="recommended-system-requirements"></a>推奨システム要件

- 6 GB の RAM
- コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)
- 少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

個人のハードウェア ニーズを決定する際に次の品目も考慮することは、組織の最高の利益となります。
- 物理的ネットワーク ポートの数 (ポートが増えると 1 秒あたりのスループットが強化されます。)
- SQL Server のログ フラッシュ サイズ (これは SQL Server パフォーマンスに直接影響します。)
- データの読み取りと書き込み能力 (これは SQL サーバー パフォーマンスに直接影響を与えます。)
- CPU コアの数、コアごとの並行スレッドの数、およびコアあたりの速度 (これはシステムの全体的なスループットに影響します。)
- 負荷分散が必要かどうか 

## <a name="connector-requirements"></a>コネクタの要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

- Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。
- どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
- 次のオペレーティング システムでは、両方のコンポーネントがサポートされています。

    - Windows 7 Professional、Enterprise、または Ultimate エディション。
    - Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。
    - Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。
    - Windows Server 2012 R2 および Windows Server 2016。
    - Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail のコンポーネントの使用をお勧めしません。

### <a name="minimum-system-requirements"></a>最少システム要件

- 2 GB の RAM (4 GB の RAM を推奨)。
- コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)
- 少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件

ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。

## <a name="additional-resources"></a>その他のリソース

[ベータ評価版の入手](../../dev-itpro/dev-tools/get-evaluation-copy.md)

