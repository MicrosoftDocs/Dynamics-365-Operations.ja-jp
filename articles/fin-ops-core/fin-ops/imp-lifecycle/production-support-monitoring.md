---
title: 運用サポートと監視
description: このトピックでは、プロジェクトのライフサイクルに関連するサポートのタイプと、環境を監視するためのベスト プラクティスについて説明します。
author: PedroTubal
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: v-petbal
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c4bd0b43ddded65a4e115e3930e90e09eb11c064
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346466"
---
# <a name="production-support-and-monitoring"></a>運用サポートと監視

[!include[banner](../includes/banner.md)]

プロジェクトの実装中および Go-Live 後に適切な経験をするために、利用できるさまざまなタイプのサービスと、すべてのシナリオに対して正しいサポートを受ける方法を理解することが重要です。 このトピックでは、各タイプのサポートを手配する方法について説明し、および使用可能ないくつかのツールについて説明します。

Microsoft のツールおよびサポートは、インフラストラクチャとアプリケーションのサポートを提供することにより、環境の安定性および有効性に役立ちます。 ただし、このサポートは、実装されているシステムとその環境をパートナーおよびクライアントが正しく開発、テスト、構成、管理、および監視している場合にのみ有効です。

![Microsoft が提供するサポート。](./media/support-provided-microsoft.png)

## <a name="supporting-actions"></a>サポート アクション

サポート アクションは、次の 3 つのカテゴリにグループ化できます。

- セルフ サービス
- サービス要求
- サポート 要求

カテゴリに応じて、アクションはさまざまな方法でトリガーされ、異なるリード タイムを含む場合があります。

### <a name="self-service"></a>セルフ サービス

セルフサービス アクションは、ユーザーがいつでもトリガーすることができ、リード タイムは含まれません。 次にユーザーがセルフサービス アクションを開始するいくつかの理由を挙げます。

- プロモーション コード (非運用環境で) 。
- [非運用環境間でのデータベースの移動](../../dev-itpro/database/dbmovement-operations.md).
- [運用環境でのアップグレード](../../dev-itpro/migration-upgrade/upgrade-latest-update.md)。
- [メンテナンス モードをオンまたはオフに切り替える](../../dev-itpro/sysadmin/maintenance-mode.md)
- 今後のサービス更新の自動展開を一時停止します。
- 非運用環境でサービスを再起動します。
- パフォーマンス アクションを完了します。

### <a name="service-request"></a>サービス要求

通常、サービス要求は、サポート チケットの作成によってトリガーされます。 これらには、Dynamics Service Engineering (DSE) チームの協力が含まれます。 各要求には、指定されたリード タイムが含まれます。 たとえば、サービス要求は環境の配置を要求するために作成される場合があります。

#### <a name="recommended-practices-for-working-with-the-dse-team"></a>DSE チームを使用するための推奨事項

- 各タイプのサービス要求に対して、応答時間または Service Level Agreements (SLA) があることを考慮します。
- サポート要求の方がケースにより適している場合は、サービス要求を使用しないでください。
- 適切なタイプの要求を作成していることを確認するには、[サービス要求タイプおよび SLA](../../dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md#service-request-types-and-slas) を参照してください。

### <a name="support-request"></a>サポート要求

通常、その他のシナリオは、サポート要求を開始することで解決できます。 これらの要求にはリード タイムが含まれます。 サポート要求を作成するいくつかの理由は以下の通りです。

- Go-live 後の運用環境のポイントインタイム復元を行います。
- サービスの更新で回帰にフラグを立て、例外のオプトアウトを求めます。
- パフォーマンス関連の要求を行います (セルフサービスでは完了できないタスクのため)。
- フライティング機能 (たとえば、顧客と仕入先マスターのデータ共有) を有効にします。
- 運用環境のサイズを変更します。 (最初に、Microsoft Dynamics Lifecycle Services \[LCS \] のサブスクリプション見積りツールで新しい使用状況プロファイルを更新およびアップロードする必要があります。)
- 同じテナントに追加の LCS プロジェクトを作成します。
- 運用環境のテナントを移動します。

## <a name="requesting-support"></a>サポートの依頼

効果的なサポート プロセスを実行するには、明確なエスカレーション パスを定義する必要があります。 プロジェクト チーム (クライアントまたはパートナー) は環境テレメトリーの監視と読み取りを行なうことができ、また、必要な最初のトラブルシューティングに対応する必要があります。

問題を明確に識別し、解決プロセスを明確に定義することにより、結果の有効性が異なる場合があります。

有効なサポート要求には、次の詳細が含まれる必要があります。

- 問題が発生した環境
- 問題が識別されたプロセス
- 問題が発生した場所を表示する再現可能な手順
- 予想される結果と実際の結果
- 問題の事前調査
- 追加の要素 (エラー メッセージ、スクリーン ショット、セッション ID、追跡など)

### <a name="high-severity-support-requests"></a>重要度の高いサポート要求

重要度の高いサポート要求には、次の情報を含める必要があります。

- **ビジネスへの影響:** この問題はビジネス活動にどのような影響を及ぼすか?
- **財務的影響:** この問題は財務レベルでビジネスにどのような影響を及ぼすか?

レポートする前にそれぞれの問題を詳細に分析する必要があります。 サポート要求に詳細情報が含まれる場合や、使用可能なすべてのツールとテレメトリが使用されている場合は、インシデントの解決はより迅速になります。 サポート要求を送信する際に正しい情報をすべて含めることにより、問題を特定してレプリケートするために必要な前後の通信の量を減らします。 したがって、時間を大幅に節約できます。

選択できる複数の[サポート計画](https://go.microsoft.com/fwlink/?LinkId=871952) があります。 したがって、すべてのビジネスでは、そのニーズを満たす計画を見つける必要があります。

サポートを要求する前に、重要度の適切なレベルを選択することが重要です。 適切な重要度レベルを識別し、要求の最初の応答時間を見積もる方法の詳細については、[サポート概要](https://docs.microsoft.com/power-platform/admin/support-overview?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&amp;bc=/dynamics365/breadcrumb/toc.json#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request) および[業務停止のレポート](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) を参照してください。

## <a name="monitoring-elements"></a>監視の要素

LCS には、LCS プロジェクトの監視に使用できる統合されたツール セットがあります。

### <a name="service-health-dashboard"></a>サービス ヘルス ダッシュボード

[サービス ヘルス ダッシュボード](https://portal.office.com/servicestatus) によって Office 365 サービスの正常性が示されます。

[Microsoft 365 管理センター](https://admin.microsoft.com) でサービスの正常性を表示することもできます。 **正常性** \> **サービスの正常性** に移動するか、または **ホーム** ダッシュボードの **サービスの正常性** カードを選択します。

既定では、**サービスの正常性** ページで **すべてのサービス** タブが選択されます。  すべてのサービスおよび現在の正常性の状態が示されます。 **ステータス** 列の記号と値は各サービスの状態を示します。

Microsoft 365 サービスの問題が発生しているのに、**サービスの正常性** ページに一覧表示されない場合、**問題の報告** を選択し、短いフォームに入力して Microsoft に通知します。

問題の報告は、問題および問題の広がり具合を特定するのに役立ちます。 インシデントが識別された後、**サービスの正常性** の下のダッシュボードに表示されます。

サイン アップして電子メール通信を受信することができます。 このようにして、テナント内で識別された問題とそのステータスの変更についての警告をすぐに受け取るようにすることができます。

### <a name="environment-monitoring"></a>環境の監視

環境の監視とは、[LCS を経由した環境の正常性のトラブルシューティング](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/monitoring-diagnostics) と監視に役立つ一連のツールです。

プロジェクトの特定の環境ページの **監視** セクションには、**環境監視ダッシュボード** に移動できる **環境の監視** リンクが含まれています 。

次のサブセクションでは、使用可能なツールの一部について説明します。

#### <a name="overview"></a>概要

**概要** セクションは、ほとんどの環境タイプで共通しています。 これにより、ユーザーの活動を追跡し、定義された期間中の活動による負荷を追跡するフィルター処理可能な方法を提供します。

#### <a name="activity"></a>活動

**活動** タブでは、未加工のログをクエリできます。 環境の監視に役立つ、最も一般的なイベントおよび指標に対する定義済みのクエリが提供されます。 使用可能な定義済みクエリの一部の例を次に示します。

- 速度の遅いクエリ
- デッドロック
- クラッシュ
- 財務諸表の問題
- バッチ調整
- 別個のユーザー セッション

さらに、独自のカスタム フィルターを追加し、分析のためにログをコンマ区切り値 (CSV) ファイルにエクスポートすることもできます。

![活動タブ。](./media/activity.png)

#### <a name="health-metrics"></a>正常性指標

**正常性指標** ダッシュボードでは、インスタンス (AOS または バッチ AOS) および時間枠でフィルターされた一連のライン チャートが提供されます。 **AOS** タブでは、SQL の実行を監視できます。 **システム** タブでは、システム メモリと CPU 使用率を時間の経過とともに監視できます。 このツールを使用すると、動作の変更を簡単に識別できます。 したがって、時間の経過に伴う問題やソリューション内の変更の影響を追跡することができます。

#### <a name="sql-insights"></a>SQL インサイト

SQL インサイトは、パフォーマンス分析を有効にする高度な SQL トラブルシューティング ツールを提供します。 これらのツールの一部は、Microsoft Dynamics AX 2012 での SQL トラブルシューティングに使用されていた DynPerf ツールと類似しています。 詳細については、 [Lifecycle Services (LCS) 内のツールを使用したパフォーマンスのトラブルシューティング](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/performancetroubleshooting) および[パフォーマンスのトラブルシューティング ツール TechTalk](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-performance-troubleshooting-tools-for-dynamics-365-12-14-18) を参照してください。

SQL インサイトは、要求されるパフォーマンス測定方法を収集する信頼性の高い方法です。 これにより、顧客やパートナーは、サンドボックスまたは生産環境での問題を軽減するために使用できる事前定義された一連のアクションを実行できます。 これは直接 SQL Server をクエリするため、ほぼリアルタイムでクエリ ストア指標が取得されます。

環境を監視することは重要ですが、常に監視している必要はありません。 また Microsoft は、LCS 通知リストによって提供される電子メールを使用して、重要な問題や実行する必要のあるアクションについて警告し、実装自体に対する予防的ガイダンスを提供します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
