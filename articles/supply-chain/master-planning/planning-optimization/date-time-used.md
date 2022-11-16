---
title: 計画の最適化で使用される日付と時刻のパラメーター
description: この記事では、計画の最適化が動作中に使用する日付と時刻のパラメータに関する情報について解説しています。
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2ef78c73a1c7033735f9586229ff7ba21daaa5ef
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740907"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>計画の最適化で使用される日付と時刻のパラメーター

[!include [banner](../../includes/banner.md)]

この記事では、計画の最適化が動作中に使用する日付と時刻のパラメータに関する情報について解説しています。

非推奨のマスタ プラン エンジンではすべての計算でトランザクション日付が使用されるのに対し、計画の最適化では日付に変換される日付と時刻の値が使用されます。 この動作の違いにより、たとえば、マスタープランを実行した日の午前 0 時に作成された予測トランザクションは、計画の最適化では現在日付より前に作成されたものとみなされるため、含まれないという状況が発生します。

## <a name="parameters-for-issue-and-demand-transactions"></a>発行トランザクションと需要トランザクションのパラメーター

次の表は、計画最適化が発行と需要のトランザクションを処理する際に使用するパラメータの一覧です。

| パラメーター | 計画最適化のパラメーター名 | 説明 | Microsoft Dynamics 365 Supply Chain Management の同等のフィールド (ReqTrans テーブル内) |
|---|---|---|---|
| 計画済発行時間 | `PlannedIssueTime` | 発行が現在予定されている日付です。 | **終了日** (`FuturesDate`) および **遅延期間**(`FuturesTime`) |
| 要求された発行時間 | `RequestedIssueTime` | ユーザーから要求され、Supply Chain Management で設定された発行日です。 このパラメータは、リリース済または承認済の計画オーダーにのみ適用されます。 計画オーダーの場合、既定では空白になります。 | **要求日** (`ReqDateDlvOrig`) |
| 要求される発行時間 | `RequiredIssueTime` | 計画の最適化によって調整された要求される発行日です。 計画最適化の実行時に要求された発行時刻が過去のものであった場合、要求された発行時刻は、今日の日付よりも早くない最初のオープン日に調整されます。 要求された発行時刻がカレンダー上でブロック化されている場合、要求された発行時刻は、その日より前の最初のオープン日にに調整されます。 | **要求日** (`ReqDate`) および **要求時間** (`ReqTime`) |
| 発行時間の遅延 | `IssueTimeDelay` | 計画された発行時間と、承認およびリリースされた注文の要求された発行時間、または要求された発行時間との時間差。 | **遅延 (日数)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>入庫トランザクションと供給トランザクションのパラメーター

次の表は、計画最適化が受領、供給トランザクションを処理する際に使用するパラメーターの一覧です。

| パラメーター | 計画最適化のパラメーター名 | 説明 | Supply Chain Management の同等のフィールド (ReqTrans または ReqPO テーブル内) |
|---|---|---|---|
| 利用可能予定時刻 | `PlannedAvailabilityTime` | 領収書の発行予定日です。 | **要求日** (`ReqDate`) および **要求時間** (`ReqTime`) |
| 予定受領時間 | `PlannedReceiptTime` | ロケーションに入庫ができる日付です。 | **終了日** (`FuturesDate`)、**遅延時刻** (`FuturesTime`)、**出荷日** (`ReqDateDlv`)、**要求日** (`ReqDateDlvOrig`) は、まだ注文がリリースされていない場合に使用します。 |
| 必要な稼働時間 | `RequiredAvailabilityTime` | 計画の最適化で調整される必要な稼働日です。 | **要求日** (`ReqDate`) および **要求時間** (`ReqTime`) |
| 入庫予定時間 | `ExpectedReceiptTime` | リリースされた入庫の受領予定日です。 この値は、Supply Chain Management でユーザーが設定されるものであり、計画の最適化では調整されません。 このパラメーターはリリース済の受領にのみ適用されます。 | **要求日** (`ReqDateDlvOrig`) |
| 要求された受領時間 | `RequiredReceiptTime` | 計画の最適化で調整される必要な受領日です。 | **要求日** (`ReqDate`) および **要求時間** (`ReqTime`) |
| 発注予定時間 | `PlannedOrderingTime` | 計画の最適化で算出される発注日です。 | **注文日** (`ReqDateOrder`) および **注文時刻** (`ReqTimeOrder`) |
| 計画済活動の開始時刻 | `PlannedActivityStartTime` | この受領のアクティビティを開始する日付です。 | **開始日** (`SchedFromDate`) |
| 受領時間の遅延 | `ReceiptTimeDelay` | 計画された受信時刻と要求された受信時刻との時間差です。 | **遅延 (日数)** ( `FuturesDays`) および **遅延時間** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>計画の最適化による日付パラメーターの使用例

以下の図の計画は日レベルのものですが、計画の最適化はより詳細なレベルで実行されます。 たとえば、利益幅は時間単位で指定できるので、計画の発注時間は 2021 年 1 月 22 日の 11 時 35 分などと設定できます。

### <a name="example-1-simple-scenario"></a>例1: 単純なシナリオ

1 月 22 日を発行希望日とする 1 つの販売注文は、1 つの発注書でカバーされます。 以下の設定が使用されます:

- リード タイムなし
- カレンダーなし (すべての日付はオープンです)。
- 利益幅なし

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![シンプルなシナリオ。](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>例2: リード タイムのシナリオ

1 月 22 日を発行希望日とする 1 つの販売注文は、1 つの発注書でカバーされます。 以下の設定が使用されます:

- 3 日間のリード タイム
- カレンダーなし (すべての日付はオープンです)。
- 利益幅なし

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![リード タイムのシナリオ。](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>例3: 利益幅のシナリオ

1 月 22 日を発行希望日とする 1 つの販売注文は、1 つの発注書でカバーされます。 以下の設定が使用されます:

- 3 日間のリード タイム
- 4 日間の注文利益幅
- 5 日間の可用性利益幅
- カレンダーなし (すべての日付はオープンです)。

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![利益幅のシナリオ。](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>例4: 遅延シナリオ

1 月 22 日に発行時刻を要求している 1 つの販売注文は、1つの発注書でカバーされています。 この例では、例 3 と同じ設定を使用していますが、計画日が 1 月 15 日に変更されています。 過去日付へのスケジュール設定 (赤い印) は、計画された注文時刻が今日の日付より前でなければならないため、失敗します。 そのため、マスター プランは未来日付で進めなければならず、そうでない場合は遅延が生じてしまいます。

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![遅延のシナリオ。](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>例5: 転送のシナリオ

1 月 22 日に発行要求された倉庫 1 からの 1 つの販売オーダーは、計画された購買オーダーでカバーされている倉庫 2 からの 1 つの転送オーダーでカバーされています。 以下の設定が使用されます:

- 3日間の転送リードタイム (倉庫 1)
- 2 日間の購入リードタイム (倉庫 2)
- カレンダーなし (すべての日付はオープンです)。

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![転送のシナリオ。](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>例 6: カレンダーのシナリオを含むリード タイム

1 月 22 日を発行希望日とする 1 つの販売注文は、1 つの発注書でカバーされます。 以下の設定が使用されます:

- 3 日間のリード タイム
- 発行カレンダー (金曜日に終了)
- カレンダー (木曜日と金曜日に終了)
- 受領カレンダー (火曜日、水曜日、日曜日に終了)
- リード タイム カレンダー (木曜日と金曜日に終了)
- 注文カレンダー (月曜日と土曜日にオープン)

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![カレンダーのシナリオを含むリード タイム。](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>例 7: カレンダーのシナリオを含む遅延

1 月 22 日を発行希望日とする 1 つの販売注文は、1 つの発注書でカバーされます。 この例では、例 6 と同じ設定を使用していますが、計画日が 1 月 13 日に変更されています。 過去日付へのスケジュール設定 (赤い印) は、計画された注文時刻が今日の日付より前でなければならないため、失敗します。 そのため、マスター プランは未来日付で進めなければならず、そうでない場合は遅延が生じてしまいます。

次の図は、このシナリオを示しています。 (図を選択すると、大きなバージョンを開きます)。

[![カレンダーのシナリオを含む遅延。](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
