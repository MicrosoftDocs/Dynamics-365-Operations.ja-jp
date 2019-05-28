---
title: Lifecycle Services (LCS) の監視および診断ツール
description: このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations 環境の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。
author: manalidongre
manager: AnnBe
ms.date: 03/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 267184
ms.assetid: eb056816-ccf4-43a5-aed3-cf72543353de
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c13f324a921de2d7975d9efc5d0c9aa920fbc2e2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537509"
---
# <a name="monitoring-and-diagnostics-tools-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) の監視および診断ツール

[!include [banner](../includes/banner.md)]

このトピックでは、管理する Microsoft Dynamics 365 for Finance and Operations 環境の状態を監視、診断、分析するために、Microsoft Dynamics Lifecycle Services (LCS) が提供するさまざまなツールについて説明します。

Microsoft Dynamics 365 for Finance and Operations のクラウド サービスへのオンボード エクスペリエンスを成功させるには、環境の状態を常に把握しておく必要があります。 発生するすべての正常性の問題をトラブルシューティングできることも必要です。 Dynamics 365 for Finance and Operations の管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。

## <a name="telemetry-data"></a>テレメトリ データ

LCS の監視および診断ポータルの基礎となるテレメトリ データには、監視、診断、分析の 3 つの主要なユース ケースがあります。 

[![モニタリング、診断、分析](./media/monitoringanddiagnostics01.png)](./media/monitoringanddiagnostics01.png)

### <a name="monitoring"></a>監視

業務運営ソフトウェアでは、環境が立ち上がっており実行中であるかどうか常に把握して、業務運営を実行できるようにする必要があります。 LCS を通じて環境の稼働状態を簡単に表示できる必要があります。 Microsoft は、2 種類の監視機能をサポートします。

- **可用性の監視** - このタイプの監視は、いつでも利用可能であることを確認するため、環境に対してチェックを実行します。 チェックが失敗した場合、Microsoft サービス エンジニアリング チームにすぐに通知されます。
- **稼働状態の監視** – 可用性チェックに加えて、基本的な正常性チェックを実行する必要があります。 これらのヘルス チェックは、Application Object Server、バッチ フレームワーク、データのインポート/エクスポート フレームワーク、Microsoft Azure SQL、Management Reporter などのさまざまなコンポーネントを対象とします。 これらのチェックは、環境から収集されたテレメトリ、環境を継続的に監視するウォッチドッグ サービスにより実行されるチェック、環境が出力する CPU カウンターや他のシステム レベル カウンターなど、複数のデータ ソースに基づいて行われます。 いくつかのヘルス チェックは自動修復され、即座に軽減されます。 ただし、他のヘルス チェックは調査のための Microsoft サービス エンジニアリング チームに報告されます。

### <a name="diagnostics"></a>診断

ユーザーが問題を報告したとき、トラブルシューティングのために LCS にあるさまざまなツールを使用できます。 豊富なテレメトリ データは、問題が報告されたときにユーザーや他のユーザーが実行していた操作を示すストーリー ボード ビューを構築するのに役立ちます。 ユーザーのアクティビティ追跡に加えて、豊富な SQL データがパフォーマンスのトラブルシューティングに使用できます。

### <a name="analytics"></a>分析

分析は収集されるテレメトリ データの別の重要なユース ケースです。 現在のところ、Microsoft だけが分析を実行できるため、Microsoft Power BI を使用して機能の使用状況とパフォーマンスを測定し理解することができます。

## <a name="responsibilities"></a>職責

Dynamics 365 for Finance and Operations などの管理されたクラウド サービスについては、Microsoft は常に実稼動環境の正常性をアクティブに監視する責任があります。 顧客の環境が問題によって影響を受ける場合、Microsoft サービス エンジニア リング チームにすぐに警告が通知されます。 チームは問題の調査を開始し、解決策を見つけるために協力します。 ただし、非実稼働環境の状態を事前または反応的に監視およびトラブルシューティングする責任はお客様にあります。

## <a name="access-the-monitoring-and-diagnostics-portal"></a>監視および診断ポータルへのアクセス

1. LCS を開き、適切なプロジェクトに移動します。
2. **環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。
3. 環境の詳細ページで、**環境の監視**を選択して、監視および診断ポータルを開きます。 

[![環境の詳細](./media/howtogettoenvmonitoring-1024x486.jpg)](./media/howtogettoenvmonitoring.jpg)

## <a name="tools"></a>ツール

複数のツールとリソースが、監視および診断ポータルで利用できます。 

> [!NOTE]
> すべての環境に、すべてのツールが含まれるわけではありません。 次のテーブルに、各タイプの環境で使用できるツールを示します。

<table>
<thead>
<tr>
<th>環境タイプ</th>
<th>ツール</th>
</tr>
</thead>
<tbody>
<tr>
<td>生産システム</td>
<td><ul>
<li>活動の監視</li>
<li>環境の監視</li>
<li>SQL インサイト</li>
<li>システム診断</li>
</ul></td>
</tr>
<tr>
<td>ユーザー受け入れテスト (UAT)/サンドボックス</td>
<td><ul>
<li>活動の監視</li>
<li>SQL インサイト</li>
<li>システム診断</li>
</ul></td>
</tr>
<tr>
<td>デモ/ビルド</td>
<td><ul>
<li>活動の監視</li>
<li>システム診断</li>
</ul></td>
</tr>
<tr>
<td>顧客/パートナー サブスクリプションに配置される環境</td>
<td><ul>
<li>システム診断</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="monitoring-dashboard"></a>ダッシュボードの監視

**環境の監視**ページで、**正常性指標** タブを選択して、**監視**ダッシュボードを開きます。 すべてのマシンおよびコンポーネントの正常性指標が収集されます。 これらの正常性メトリックには、CPU 使用率、使用可能なメモリ、1 秒あたりに記録されるエラー、バッチ ハートビートが含まれます。 指標の異常に関する警告が表示されます。 いくつかの警告は自動修復されますが、Microsoft サービス エンジニアリング チームは他の警告の原因を調査し、それらを軽減するアクションを実行します。 特定の領域で何が発生しているかを確認するために正常性モニターを表示することができます。

### <a name="activity-monitoring"></a>活動の監視

**環境の監視**ページで、**活動**タブを選択して、活動監視ツールを使用します。 このツールは、お客様または別のユーザーが特定の期間に実行する内容を表示するストーリー ボード ビューを提供します。 

[![活動タブ](./media/activitymonitoringview-1024x507.jpg)](./media/activitymonitoringview.jpg)

- **ユーザー操作**の図は、環境および SQL 使用率の傾向でさまざまなコンピューターにおけるユーザーの活動を示しています。
- **ユーザー負荷** セクションは、すべてのシステム ユーザーを示しています。 各グラフには、ユーザーが特定のマシンに費やした時間が示されます。
- **活動負荷** セクションには、各コンピューターで実行された活動が表示されます。 活動の上にマウス ポインターを移動すると、タプルとして Form:Control:Action が表示されます。 たとえば、このセクションで LedgerJournal:New:Click を見ている場合、そのユーザー A が、新しい仕訳帳入力を作成するため **LedgerJournals** ページを開き**新規**ボタンを選択したのを表示できます。
- **ユーザー アクティビティ** グリッドには、そのセッション タイムスタンプに基づいて、ユーザーが実行したさまざまな活動が表示されます。

情報ログを絞り込むには、このページで、フィルターを使用できます。 利用可能なフィルタを次に示します。

- **期間** – 選択した日時から 60 分前に戻ります。
- **ユーザー** – 特定のユーザーの活動を表示します。
- **検索用語** – 調査中の問題に基づいて検索を作成します。

> [!NOTE]
> ページには、既定ではデータが読み込まれません。 ページを表示するために必要なデータをロードするには、期間を選択し、**送信時刻**を選択する必要があります。

> [!IMPORTANT]
> 活動の監視ツールは 30 日間だけデータを保持します。

### <a name="raw-information-logs"></a>生の情報ログ

高度なトラブルシューティングでは、原情報ログを表示できます。 一連の定義済クエリを使用して、問題の未加工ログを取得することができます。 さらに高度な分析を行うためにログをエクスポートすることができます。 以下のタイプのクエリを使用できます。

- 速度の遅いクエリ
- デッドロック
- クラッシュ
- 財務諸表の問題

### <a name="sql-insights"></a>SQL インサイト

監視および診断ポータルには、パフォーマンスの分析を有効にする高度な SQL トラブルシューティングのツールも含まれます。 これらのツールの一部は、Microsoft Dynamics AX 2012 での SQL トラブルシューティングに使用されていた DynPerf ツールと似ています。 詳細については、[Lifecycle Services (LCS) でツールを使用したパフォーマンスのトラブルシューティング](performancetroubleshooting.md)を参照してください。

## <a name="other-resources"></a>その他のリソース

- [環境監視未加工ログの使用方法](https://blogs.msdn.microsoft.com/axsa/2018/06/05/how-to-use-environment-monitoring-view-raw-logs/)
