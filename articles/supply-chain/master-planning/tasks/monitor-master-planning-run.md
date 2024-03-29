---
title: マスター プランの実行の監視
description: この記事では、生産計画担当が、マスター プランの実行が進行中かどうかを確認する方法について説明します。
author: t-benebo
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da04ef95f2f7e411ecea3fadf7ff31b3502d3d99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860757"
---
# <a name="monitor-a-master-planning-run"></a>マスター プランの実行の監視

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>ガント チャートを使用して、マスター プランの進行状況を視覚化する

**マスター プランの進行状況の表示** ページで、マスター プランの実行履歴の詳細をガント チャートとして表示できます。 この機能は、マスター プランのさまざまなフェーズにかかる時間を理解するのに役立ちます。 現在有効な計画ジョブの場合は、**マスター プランの進行状況の表示** ページを使用して進行状況を追跡し、見積った残り時間を表示できます。

### <a name="turn-the-master-plan-progress-visualization-feature-on-or-off"></a>マスター プランの進行状況の視覚化機能をオンまたはオフにする

Supply Chain Management のバージョン 10.0.21 では、この機能は既定で有効になっています。 Supply Chain Management 10.0.25 では、この機能は必須なため、オフにすることはできません。 10.0.25 より以前のバージョンを使用している場合、管理者は [機能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースで *マスター プランの進捗状況の可視化* 機能を検索して、この機能をオンまたはオフにすることができます。

### <a name="use-the-master-plan-progress-visualization-feature"></a>マスター プランの進行状況の視覚化機能を使う

**マスター プランの進行状況の表示** ページには、計画ジョブの履歴と有効な計画ジョブの両方を表示できます。 

計画ジョブの履歴を表示するには、2 つのオプションがあります。 

1. **マスター プラン \> 設定 \> 計画 \> マスター プラン** の順に移動し、アクション ペインで **履歴** を選択します。 目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。
1. **マスター プラン \> ワークスペース \> マスター プラン** の順に移動し、マスター プラン タイルで、**履歴** をクリックします。 目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。

有効な計画ジョブを表示するには、2 つのオプションがあります。 
1. **マスター プラン \> ワークスペース \> マスター プラン** の順に移動し、アクション ペインで、**未完了の計画プロセス** を選択します。 目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。
1. **マスター プラン \> ワークスペース \> マスター プラン** の順に移動し、マスター プラン タイルで、**進捗状況の表示** をクリックします。 目的のジョブを選択して、**照会** を選択し、**進捗状況の表示** を選択します。

有効なジョブは、計画ジョブが処理中の場合にのみ表示できることに注意してください。

### <a name="analyze-a-master-planning-job"></a>マスター プラン ジョブの分析

ガント チャートでは、次の各計画プロセスを展開して、以下に対して費やされた時間に関する追加情報を表示できます。

- 初期化
- データの削除と挿入
- 補充計画
- 遅延
- アクション メッセージ
- 終了処理
- 自動確定

アクション メッセージを使用した場合の影響を表示する場合は、ガント チャートは役に立つツールです。

#### <a name="navigation-in-the-gantt-chart"></a>ガント チャートのナビゲーション

- 選択したグループを展開して詳細を表示するには、ツリー ビューでプラス符号 (**+**) を選択します。
- 選択したグループを折りたたむには、ツリービューのマイナス記号 (**-**) を選択します。
- キーボードを使用してナビゲーションを行うことができます。 **上方向** キーと **下方向** キーを使用して行間を移動します。 **右矢印** キーと **左矢印** キーを使用してグループを展開したり折りたたんだりします。
- ガント チャートのすべてのレベルを開くか閉じるかするには、**すべて展開** または **すべて折りたたむ** を選択します。
- 関連する処理時間を表示するには、タスク上にポイントします。 (タスクは、ガント チャートの最下位レベルです。)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>追加のマスター プランの実行を表示してジョブを比較する

**追加のマスター プランの実行を表示** フィールドでマスター プラン ジョブを選択することにより、ガント チャートで追加のマスター プランの実行を表示し、2 つのジョブを比較することができます。

#### <a name="bom-level-display"></a>BOM-レベルの表示

部品表 (BOM) レベルは、補充計画、遅延、アクション、および確定に対して異なる方法で表示されます。

- **補充計画** – BOM レベルが予想どおりに表示されます。 これらは、トップダウン方式で計算されます。

    **例:** BOM レベル 0、1、2

- **遅延** – BOM レベルは、補充計画 BOM レベルに –1 を掛けた値として表示されます。 (つまり、マイナス記号が付けられています。)

    **例:** BOM レベル –2、–1、0

- **アクション メッセージ** – BOM レベルが予想どおりに表示されます。 これらは、トップダウン方式で計算されます。

    **例:** BOM レベル 0、1、2

- **自動確定** – BOM レベルは、999 から、補充計画 BOM レベルを差し引いた値として表示されます。

    **例:** BOM レベル 999、998、997

次の表で、この動作が要約されています。

| 表示される BOM レベル | 最終品目 | サブコンポーネント | 原材料 |
|---|---|---|---|
| 補充計画 | 0 | 1 | 2 |
| 遅延 | 0 | –1 | –2 |
| アクション メッセージ | 0 | 1 | 2 |
| 自動確定 | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>進行状況の視覚化

現在実行中のマスター プラン ジョブを表示する場合は、ガント チャートの色によって進行状況が表示されます。 次の色は、青のテーマに適用されます。 他の色のテーマでは、色が異なります。

- **濃い青** – プラン タスクが完了しました。
- **オレンジ** – 現在処理中のタスク。
- **ライト ブルー** – 残りのタスクの見積。

色は、ガント チャートの最下位レベルにのみ表示されます。 **すべて展開** を選択して、マスター プラン ジョブのすべてのタスクを表示します。 残りのタスクの見積は、マスター プラン ジョブの履歴に基づいて行われます。

## <a name="run-master-planning-and-track-processing-time"></a>マスター プランの実行と処理時間の追跡

1. 既定のダッシュボードで、**マスター プラン** を選択します。
1. **計画** フィールドで値を入力または選択します。
1. **実行** を選択します。
1. **処理時間の追跡** オプションを **はい** に設定します。
1. **スレッド数** フィールドに数値を入力します。
1. **対象に含めるレコード** クイック タブで、**フィルター** を選択します。
1. グリッドで、**フィールド** フィールドが **品目番号** に設定されている行を選択します。
1. **基準** フィールドに値を入力します。
1. **OK** を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]