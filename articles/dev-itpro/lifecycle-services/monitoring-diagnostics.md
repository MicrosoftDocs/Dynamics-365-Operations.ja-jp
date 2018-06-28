---
title: "監視および診断 (Lifecycle Services、LCS)"
description: "このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。"
author: manalidongre
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 267184
ms.assetid: eb056816-ccf4-43a5-aed3-cf72543353de
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 2711898f83510648cee570742634f1ff686c134a
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="monitoring-and-diagnostics-lifecycle-services-lcs"></a>監視および診断 (Lifecycle Services、LCS)

[!include [banner](../includes/banner.md)]

このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。

Microsoft Dynamics 365 for Finance and Operations のクラウド サービスへのオンボード エクスペリエンスを成功させるには、環境の状態を常に把握しておく必要があります。 発生するすべての正常性の問題をトラブルシューティングできることも必要です。 Dynamics 365 for Finance and Operations の管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。

## <a name="telemetry-data"></a>テレメトリ データ
LCS の監視および診断ポータルの基礎となるテレメトリ データには、監視、診断、分析の 3 つの主要なユース ケースがあります。 [![monitoringanddiagnostics01](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)

### <a name="monitoring"></a>監視

業務運営ソフトウェアでは、環境が立ち上がっており実行中であるかどうか常に把握して、業務運営を実行できるようにする必要があります。 LCS を通じて環境の稼働状態を簡単に表示できる必要があります。 Microsoft は、2 種類の監視機能をサポートします。

-   **可用性の監視** - このタイプの監視は、いつでも利用可能であることを確認するため、環境に対してチェックを実行します。 チェックが失敗した場合、Microsoft サービス エンジニアリング チームにすぐに通知されます。
-   **稼働状態の監視** – 可用性チェックに加えて、基本的な正常性チェックを実行する必要があります。 これらの基本的な正常性チェックには、CPU レベル、仮想マシン (VM) のメモリ消費量、および 5 分間の合計デッドロック数が含まれます。 Microsoft テレメトリ インフラストラクチャは、環境から多くの正常性指標を収集します。 メトリックがしきい値を超えている場合は、Microsoft サービス エンジニアリング チームに警告が表示され、問題を調査できます。

### <a name="diagnostics"></a>診断

ユーザーが問題を報告したとき、トラブルシューティングのために LCS にあるさまざまなツールを使用できます。 豊富なテレメトリ データは、問題が報告されたときにユーザーや他のユーザーが実行していた操作を示すストーリー ボード ビューを構築するのに役立ちます。 ユーザーのアクティビティ追跡に加えて、豊富な SQL データがパフォーマンスのトラブルシューティングに使用できます。

### <a name="analytics"></a>分析

分析は収集されるテレメトリ データの別の重要なユース ケースです。 現在のところ、Microsoft だけが分析を実行できるため、Microsoft Power BI を使用して機能の使用状況とパフォーマンスを測定し理解することができます。

## <a name="responsibilities"></a>職責
Dynamics 365 for Finance and Operations などの管理されたクラウド サービスについては、Microsoft は常に製造環境の正常性をアクティブに監視する責任があります。 顧客の環境が問題によって影響を受ける場合、Microsoft サービス エンジニア リング チームにすぐに警告が通知されます。 チームは問題の調査を開始し、解決策を見つけるために協力します。 ただし、非実稼働環境の状態を事前または反応的に監視およびトラブルシューティングする責任はお客様にあります。

## <a name="access-the-monitoring-and-diagnostics-portal"></a>監視および診断ポータルへのアクセス
1.  LCS を開き、適切なプロジェクトに移動します。
2.  **環境**セクションで、表示する環境を選択してから**完全な詳細**をクリックします。
3.  **環境の詳細**ページで、**環境の監視**をクリックして、監視および診断ポータルを開きます。 [![howtogettoenvmonitoring](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)

## <a name="tools"></a>ツール
複数のツールとリソースが、監視および診断ポータルで利用できます。 **注記:** すべての環境に、すべてのツールが含まれるわけではありません。 次のテーブルに、各タイプの環境で使用できるツールを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>環境タイプ</th>
<th>ツール</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>生産システム</td>
<td><ul>
<li>活動の監視</li>
<li>環境の監視</li>
<li>SQL インサイト</li>
<li>システム診断</li>
</ul></td>
</tr>
<tr class="even">
<td>ユーザー受け入れテスト (UAT)/サンドボックス</td>
<td><ul>
<li>活動の監視</li>
<li>SQL インサイト</li>
<li>システム診断</li>
</ul></td>
</tr>
<tr class="odd">
<td>デモ/ビルド</td>
<td><ul>
<li>活動の監視</li>
<li>システム診断</li>
</ul></td>
</tr>
 <tr class="even">
<td>顧客/パートナー サブスクリプションに配置される環境</td>
<td><ul>
<li>システム診断</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="monitoring-dashboard"></a>ダッシュボードの監視

監視および診断ポータルで、監視ダッシュボードを表示するには**環境**タブをクリックします。 ダッシュ ボードで、緑のチェック マークは、事業運営を実行できる環境があることを示します。 すべてのマシンおよびコンポーネントの正常性指標が収集されます。 これらの正常性メトリックには、CPU 使用率、1 秒あたりに記録されるエラー、バッチ ハートビートが含まれます。 一部のメトリックでは、Microsoft にはしきい値の設定があります。 メトリックがしきい値を超えた場合に警告が発生します。 たとえば、CPU 使用率が 70% を超えた場合、警告が発生します。 特定の領域で何が発生しているかを確認するために正常性モニターを表示することができます。

### <a name="activity-monitoring"></a>活動の監視

監視および診断ポータルで、アクティビティ監視ツールを使用するには**アクティビティ** タブをクリックします。 このツールは、お客様または別のユーザーが特定の期間に実行する内容を表示するストーリー ボード ビューを提供します。 [![activitymonitoringview](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)

-   **ユーザー操作**の図は、環境および SQL 使用率の傾向でさまざまなコンピューターにおけるユーザーの活動を示しています。
-   **ユーザー負荷** セクションは、すべてのシステム ユーザーを示しています。 各グラフには、ユーザーが特定のマシンに費やした時間が示されます。
-   **活動負荷** セクションには、各コンピューターで実行された活動が表示されます。 活動の上にマウス ポインターを移動すると、タプルとして Form:Control:Action が表示されます。 たとえば、このセクションで LedgerJournal:New:Click を見ている場合、そのユーザー A が、新しい仕訳帳入力を作成するため **LedgerJournals** ページを開き**新規**ボタンをクリックしたのを表示できます。
-   **ユーザー アクティビティ** グリッドには、そのセッション タイムスタンプに基づいて、ユーザーが実行したさまざまな活動が表示されます。

情報ログを絞り込むには、このページで、フィルターを使用できます。 利用可能なフィルタを次に示します。

-   **期間** – 選択した日時から 60 分前に戻ります。
-   **ユーザー** – 特定のユーザーの活動を表示します。
-   **検索用語** – 調査中の問題に基づいて検索を作成します。

**重要:** 活動の監視ツールは 30 日間だけデータを保持します。

### <a name="raw-information-logs"></a>生の情報ログ

高度なトラブルシューティングでは、原情報ログを表示できます。 一連の定義済クエリを使用して、問題の未加工ログを取得することができます。 さらに高度な分析を行うためにログをエクスポートすることができます。 以下のタイプのクエリを使用できます。

-   速度の遅いクエリ
-   デッドロック
-   クラッシュ
-   財務諸表の問題

### <a name="sql-insights"></a>SQL インサイト

監視および診断ポータルには、パフォーマンスの分析を有効にする高度な SQL トラブルシューティングのツールも含まれます。 これらのツールの一部は、SQL Microsoft Dynamics AX 2012 でのトラブルシューティングに使用されていた DynPerf ツールと似ています。

#### <a name="performance-metrics"></a>パフォーマンス メトリックス

**パフォーマンス メトリックス** ページには、論理入出力、実行カウント、期間、CPU 時間、および待機数に基づいて、選択した期間にシステムで実行された最もコストのかかったクエリが表示されます。 このデータは SQL クエリ ストアからクエリされます。 データは 30 日間保持され、ツールは毎日、協定世界時 (UTC) の午後 10 時にデータ収集を実行します。 [![sqlinsights](./media/sqlinsights-1024x512.jpg)](./media/sqlinsights.jpg) このツールを使用するには、次の手順に従います。

1.  過去 30 日間の期間を選択します。
2.  クエリ結果が表示されたら、期間グラフ内の 1 つ目のバーを選択して、クエリが他の基準に該当する場所を強調表示します。
3.  **ステートメント**タブで、クエリを表示、またはクエリの実行計画をダウンロードします。

#### <a name="sql-now-tool"></a>SQL now ツール

just-in-time 診断では、SQL now ツールを使用することができます。 たとえば、レポートの実行が遅いと、任意のロック/ブロック問題があるか、およびバック グラウンドでどの SQL ステートメントが実行しているかを表示します。 この場合、レポートの実行中にこのページを開いて更新できます。

#### <a name="index-analysis"></a>インデックス分析

インデックス分析ツールには、ユーザーのスキャン、ユーザーのシーク、ユーザーの更新プログラム、および行の数に基づいて、集計インデックスとテーブル情報が表示されます。 パフォーマンス測定基準と同様に、このツールは追加のテーブル メトリックスと共に選択したインデックスのトレンドを表示します。

### <a name="system-diagnostics"></a>システム診断

システム診断ツールは、環境に対して事前に定義されたルール セットを実行するルール ベースのフレームワークであり、ルールのステータスに関するレポートを提供します。 エラーが発生した場合、このツールは、問題に対処するための推奨事項を提供します。 システムの診断ツールを開始するには、LCSプロジェクト ダッシュ ボードで [ハンバーガー] アイコンをクリックし、**システム診断** をクリックします。




