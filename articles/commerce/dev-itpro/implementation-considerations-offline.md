---
title: Commerce のオフライン実装とトラブルシューティング
description: この記事では、Microsoft Dynamics 365 Commerce オフライン実装に関する考慮事項とトラブルシューティングの概要を説明します。
author: jashanno
ms.date: 09/29/2022
ms.topic: article
audience: IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2021-08-31
ms.openlocfilehash: 2653cdd1d71327d12e78f953191d1ae0bd195a5b
ms.sourcegitcommit: ce4e56d798281258479432ad821287a1cc8e26bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2022
ms.locfileid: "9601556"
---
# <a name="commerce-offline-implementation-and-troubleshooting"></a>Commerce のオフライン実装とトラブルシューティング

[!include[banner](../includes/banner.md)]

この記事は、Microsoft Dynamics 365 Commerce Modern POS または Store Commerce アプリケーションに関連するオフライン機能を実装するユーザーを対象としています。 この記事では、オフライン機能の使用に関連する機能、機能、実装のヒント、およびトラブルシューティング方法について説明します。

## <a name="overview"></a>概要

データの適切な構成と同期は、正しい実装とって非常に重要です。 ビジネス要件、IT インフラストラクチャ、および全体的な準備にかかわらず、データが正しく同期されていないと、環境全体が実質的に役に立たなくなります。 したがって、最優先事項は、完全な実装全体でデータをコンフィギュレーション、生成、同期、検証するために何が必要かを理解することです。 これは、Commerce Headquarters から Commerce Scale Unit を経由して、Modern POS (オフライン データベースの有無にかかわらず) やその他の店舗内コンポーネントを使用する従来型の店舗にまで及びます。 Commerce Data Exchange (CDX) は、データベース間でデータを複製および同期する Commerce の機能です。 ただし、CDX はフィルタリングも可能であるため、一般的なデータ レプリケーション機能とは異なります。 CDX は、選択のために指定されたチャネルに固有のデータのみを生成したり、オフライン データベースから特定のテーブルをフィルター処理したり、使用されなくなったデータについて、期限切れの割引など、使用されなくなったデータのために期限切れレコードをフィルター処理することで、データ セットを最小限に抑えることができます。

この記事を確認する前に、チャネル (店舗)、レジスターとデバイス、および Modern POS オフライン データベースの概念を理解することが重要です。 したがって、この記事の最後に表示されている[デバイス管理実装ガイダンス](../implementation-considerations-devices.md)および [Commerce アーキテクチャの概要](../commerce-architecture.md)などのリソースを確認することをお勧めします。


## <a name="important-offline-features"></a>重要なオフライン機能

(CDX に基づく) オフライン データベースのデータ同期を強化または変更する機能の詳細については、[Commerce Data Exchange ベスト プラクティス](CDX-Best-Practices.md) を参照してください。 次の表では、いくつかの重要なオフライン機能を強調表示します。 

| 機能名 | 説明 |
|--------------|-------------|
| オフラインの詳細 | この機能は、オフライン プロファイルの一連の設定で構成されます。 これらの設定により、追加のオフライン切り替えシナリオを使用できるようになり、ユーザーが POS にサインインする前にオフライン モードに切り替える機能を提供し、強化された Commerce Headquarters の可用性テストが可能になるため、簡単にオフライン モードに切り替え、オンライン状態に戻すことができます。 |
| オフライン状態ダッシュボード | Commerce バージョン 10.0.20 リリース以降に用意された新しいダッシュボードには、各デバイスの最新のオフライン状態、エラー、およびデータベースの詳細が表示されます。  このダッシュボードは、**Retail と Commerce \> チャネル設定 \> POS 設定 \> レジスターのオフライン状態** で確認できます。 このダッシュボードが正しく機能するには、**機能管理** ワークスペースで **最新化の POS オフライン監視** 機能をオンにしてから、**1110** 配送スケジュール ジョブを実行する必要があります。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 |
| オフライン データベース圧縮 | この機能は Commerce リリース 10.0.29 以降で使用でき、オフライン データベースのサイズを縮小するために、チャネル [営業時間](store-hours.md) 外で自動インデックス圧縮を有効化します。 営業時間を構成していないか、または適切に機能しない場合は、常に圧縮します。 圧縮が発生すると、営業時間に基づくかどうかにかかわらず、Modern POS や Store Commerce は、100 MB を超える、またはデータベースの合計サイズの少なくとも 1% である、非圧縮と非クラスター化インデックスに対し、オフライン データベースにクエリを実行します。 この基準を満たすインデックスが見つかった場合、リストが含む最大のインデックスに対して圧縮を開始し、その後 10 分間アイドル状態になります。 この時間が経過すると、次のインデックスに対して圧縮を開始し、選択したすべてのインデックスを圧縮するまで、このサイクルを繰り返します。 インデックスが見つからない場合、圧縮ロジックは 30 分間一時停止してから、もう一度確認します。 このダッシュボードが正しく機能するには、**昨日管理** ワークスペースで **POS オフライン データベース圧縮** をオンにして、その後 **1070** 配信スケジュール ジョブを実行する必要があります。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 記事を参照してください。 |
| パフォーマンス ベースのオフライン切り替え (パフォーマンスを低下させる POS シームレスなオフライン) | この機能はリリース 10.0.20 以降で提供されており、アウトバウンド Web 要求のパフォーマンスが低下した場合に、最新の POS デバイスをシームレスにオフラインモードに切り替えることができます。  この機能を使用するには、本社の **オフライン プロファイル** ページから **詳細なオフライン切り替えの有効化** 機能を有効にする必要があります。 **パフォーマンスを低下させる POS シームレスなオフライン** 機能は、機能管理ワークスペースでオンにする必要があります。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。 |

### <a name="advanced-offline-feature"></a>オフラインの詳細機能

オフラインの詳細機能は、オフライン プロファイルで構成できます。 この機能に関連する設定は次のとおりです。

- **サインイン前に手動でのオフライン切り替えを許可する** – この設定により、Modern POS ユーザーは POS にサインインする前にオフライン モードに切り替えることができます。 これは、サインインが完了する前にタイムアウトが発生する可能性がある場合や、Commerce Scale Unit (クラウドまたは自己ホスト) からの非定型の応答コードが発生している場合のシナリオで役立ちます。 この設定を有効にすると、オフライン データベースを使用している Modern POS ユーザーが、POS サインイン ページから **設定** メニューにアクセスできるようになります。 このメニューには、オフライン モードに切り替えるための新しいオプションが含まれています。 このオプションを選択すると、ユーザーは、Commerce Scale Unit への呼び出しによって最初にログインする必要がなく、オフライン データベースに対して直接サインインできます。
- **詳細なオフライン切り替えの有効化** – この設定により、Modern POS をより簡単により頻繁にオフライン モードに切り替えることができます。 通常、Modern POS はオンライン状態を維持しようとし、機能を続行するためにこのようなスイッチが必要になった場合にのみオフライン モードに切り替えます。 この設定を有効にすると、Modern POS は、特にサインインや POS 操作への遅延とみなされる可能性のある追加の Commerce Scale Unit の応答を含むシナリオで、より頻繁に切り替えることができます。 この設定は、オンラインのみの機能の可用性を維持するより速度を優先するシナリオ (Headquarters への接続を必要とするギフト カードでの支払など) で最も重要です。
- **システムの正常性チェックの間隔 (分)** – この設定は、上記で説明した **詳細なオフライン切り替えの有効化** 設定のサブ機能として機能します。 通常、この設定がオフで、Modern POS がオフライン モードの場合、POS は **オフライン プロファイル** の構成に基づいて特定の時間だけ待機し、次に発生する操作呼び出し中に Commerce Scale Unit への再接続を試みます。 この詳細なオフラインの正常性チェックは、オンラインの可用性を確認し、オンライン機能が再び使用可能になると切り替える、より頻繁な操作に依存しない方法を提供します。

## <a name="implementation-considerations"></a>実装の考慮事項

このセクションでは、オフラインで機能しているときに POS 使用シナリオの計画を開始するときに考慮する必要があるオフラインのさまざまな側面と構成について説明します。 ここで説明する機能は、データ管理、オフライン使用およびデータ構成に関連しています。 ここに記載されているガイダンスを読む前に、これらの概念を理解することを強くお勧めします。 追加情報を取得するために、[Commerce Data Exchange ベスト プラクティス](CDX-Best-Practices.md) を読むことをお勧めします。

### <a name="sql-server-versions-and-licenses"></a>SQL Server のバージョンとライセンス 
SQL Server には、さまざまなバージョン (SQL Server 2017 や SQL Server 2019 など) やエディション (SQL Standard や SQL Express など) があります。 これらのバージョンの詳細な情報については、[SQL Server 2019 (15.x) のエディションとサポートされている機能](/sql/sql-server/editions-and-components-of-sql-server-version-15#Cross-BoxScaleLimits)を参照してください。 この記事の下部にある[追加のリソース](implementation-considerations-offline.md#additional-resources)も参照してください。

SQL Server のバージョンについては、現在メインストリーム サポートの期間内にあるバージョンの使用のみをお勧めします。 サポート日は、[製品とサービス ライフサイクル情報](/lifecycle/products/)という記事で製品ごとに検索できます。

#### <a name="which-sql-server-edition-to-use"></a>使用する SQL Server エディション
包括的なリストは作成できませんが、Dynamics 365 Commerce で最も使用される SQL Server エディションを次に示します。 各エディションには、さまざまな詳細と使用ケースのシナリオが一覧表示されます。

| エディション | ユース ケース |
|--------------|-------------|
| 速達 | オフライン データベースの SQL Server バージョンとして SQLServer Express を使用する場合、CPU コア数や RAM 使用など、いくつかの制限があることを理解することが重要です。 最大の制限の要因は、10 GB のデータベース サイズ制限です。 このバージョンを自由に使用できる機能を与えられた Express は、多くの場合、CSU (セルフホスト) チャネル データベースではなく、Modern POS オフライン データベースに使用されます。 Express Edition を CSU (自己ホスト) に使用する場合、データベースが 10 GB の最大サイズ制限に達するとデータ同期に問題が生じ、データの損失などの問題が発生する可能性があります。 Express Edition を使用する場合は、圧縮と Dynamics 365 Commerce 機能を使用して、オフライン データベースからデータを除外することが重要です。 SQL 圧縮の詳細については、[Commerce Data Exchange のベスト プラクティス](CDX-Best-Practices.md#enable-table-and-index-compression)を参照してください。 データベースのサイズは 8 GB 以下で管理することをお勧めします。 |
| 標準 | SQL Server Standard は多くの場合、CSU (自己ホスト) チャネル データベースで使用されます。  これにより、一般に 1 つ以上の小売店舗の場所で CSU (自己ホスト) チャネル データベースを処理するのに十分なサイズとシステム使用率が提供されます。 一般的ではありませんが、Standard バージョンは、オフライン データベースで制限を取り除き、オフライン パフォーマンスを最大化するために使用されることがあります。 さらに、設定された数の Modern POS レジスターのみが完全な Standard バージョンを利用し、他のレジスターが Express バージョンを利用する (またはオフライン データベースがない可能性があり、Modern POS の代わりに Cloud POSを使用する) 場合は、よりハイブリッドな方法を使用できます。 |
| 企業 | SQL Server Enterprise の必要はほとんどありませんが、価値のあるシナリオがあります。 たとえば、データセンター VM で CSU (自己ホスト) をホストして、多くのデバイスの広い領域で使用する場合、パフォーマンス機能を最大限にするには、制限を取り除くことが重要です。 |

### <a name="offline-testing"></a>オフライン テスト
更新を実行する場合、Modern POS (MPOS) とオフライン機能を徹底的にテストすることが重要です。 正しい機能を確認するために、オフライン中にテストする必要がある機能の包括的ではないリストを示します。

-   レジ担当者とマネージャーがサインインをテストします。
-   シフトの開始と終了をテストします。
-   カテゴリを使用して製品閲覧をテストします。
-   検索バーを使用して製品の検索をテストします。
-   現金売りトランザクションをテストします。
-   ブラインド返品をテストします。
-   割引をテストします。
-   測定単位の変更をテストします。
-   支払機能をテストします。 オフライン時には、以下のすべての支払タイプが機能し、使用可能である必要があります。
    -   現金
    - 通貨
    - 検査
    -   ロイヤルティ
    -   カード
    -   顧客 ID
    -   ギフト カード
-   **仕訳帳の表示** をテストします。
-   オンライン モード中にトランザクションを開始します。 次に、強制的にオフライン モードに切り替え (つまり、手動でオフライン モードに切り替える代わりに、システムをインターネットから切断)、精算を続行します。
-   たとえば、オフライン データベースに顧客の最新データ (欠落) またはカート内の製品 (欠落) がない場合は、前のテストを実行します。 この場合、レジ担当者は警告またはエラー メッセージを受信しますが、オフライン モードで MPOS を引き続き使用して、新しい現金売りトランザクションを実行できることが期待されます。
-   オフライン中に 1 つ以上のトランザクションを実行します。 その後、オンライン モードに切り替え、トランザクションがアップロード済みであることを確認します。


## <a name="troubleshooting"></a>トラブルシューティング

次の表に表示されているエラーがリストされていない場合は、Microsoft サポートが問題の解決を援助できるようにサポート依頼を作成してください。 このセクションは追加のエラーで時間の経過とともに更新されるため、オフライン データベースを利用する最新の POS レジスターを実装または更新する前に、このドキュメントを確認することをお勧めします。

| エラー | 説明 |
|---------------|--------------------------------------------------------------------------------|
| Microsoft_Dynamics_Commerce_Runtime_AuthenticationMethodDisabled Microsoft_Dynamics_Commerce_Runtime_ChannelConfigurationNotFound Microsoft_Dynamics_Commerce_Runtime_ChannelNotPublished Microsoft_Dynamics_Commerce_Runtime_InvalidChannelConfiguration |  オフライン モードに切り替えできません。 チャンネル情報が使用できないか、正しく構成されていないかのどちらかです。 この問題を解決するには、チャンネル コンフィギュレーション スケジューラ ジョブを実行します (既定では、1070 スケジューラ ジョブです)。 システム管理者に連絡してください。 |
| Microsoft_Dynamics_Commerce_Runtime_CredentialsNotConfigured Microsoft_Dynamics_Commerce_Runtime_CredentialsNotFound Microsoft_Dynamics_Commerce_Runtime_InvalidAuthenticationCredentials Microsoft_Dynamics_Commerce_Runtime_LocalLogonFailed Microsoft_Dynamics_Commerce_Runtime_UserBlockedDueToTooManyFailedLogonAttempts | オフライン モードに切り替えできません。 ユーザー情報が使用できないか、正しく構成されていないかのどちらかです。 この問題を解決するには、スタッフ スケジューラ ジョブを実行します (既定では、1060 スケジューラ ジョブです)。 システム管理者に連絡してください。 |
| Microsoft_Dynamics_Commerce_Runtime_CriticalStorageError  | オフライン db のアクセス許可、サイズ、ディスク容量のステータスを確認するには (オフライン ダッシュボードを使用できます) |
| Microsoft_Dynamics_Commerce_Runtime_ElevatedUserSameAsLoggedOnUser | このエラーは、同じユーザーがマネージャの上書きを実行しようとする場合に発生します。 異なるユーザーが使用されている必要があります。 |
| Microsoft_Dynamics_Commerce_Runtime_RealtimeServiceNotSupported Microsoft_Dynamics_Commerce_Runtime_TransientStorageError | オフライン モードに切り替えできません。 オフライン データベースが正しくインストールされていないか、正しく構成されていないかのどちらかです。 すべてが正常に設定されたことを確認します。 システム管理者に連絡してください。 |
| Microsoft_Dynamics_Commerce_Runtime_TerminalNotFound | この問題を解決するには、チャンネル コンフィギュレーション スケジューラ ジョブを実行します (既定では、1070 スケジューラ ジョブです)。 システム管理者に連絡してください。 |
| Microsoft_Dynamics_Internal_Server_Error | このエラーはいくつかの考えられるシナリオをカバーしているため、サポートに問い合わせて、直接援助を受けることをお勧めします。 |

## <a name="additional-resources"></a>追加リソース

- [Commerce Data Exchange 実装ガイダンス](implementation-considerations-cdx.md)
- [Commerce Data Exchange のトラブルシューティング](CDX-Troubleshooting.md)
- [Commerce Data Exchange ベスト プラクティス](CDX-Best-Practices.md)
- [Dynamics 365 Commerce アーキテクチャの概要](../commerce-architecture.md)
- [店舗内トポロジの選択](retail-in-store-topology.md)
- [デバイス管理実装ガイダンス](../implementation-considerations-devices.md)
- [Modern POS (MPOS) のコンフィギュレーション、インストール、および有効化](../retail-modern-pos-device-activation.md)
- [Commerce Scale Unit のコンフィギュレーションとインストール (自己ホスト)](retail-store-scale-unit-configuration-installation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
