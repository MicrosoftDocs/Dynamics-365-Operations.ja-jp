---
title: 倉庫アプリ イベント
description: このトピックでは、倉庫アプリ イベントのメッセージをバッチ ジョブの一部として処理するために使用される、倉庫アプリのイベント処理について説明します。
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 286786445f72db20e993d37a63df0b886f8f5e99
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988386"
---
# <a name="warehouse-app-event-processing"></a>倉庫アプリのイベント処理

[!include [banner](../includes/banner.md)]

Supply Chain Management で実行されるバッチ ジョブでは、キューのデータを使用して、倉庫アプリによって発行されたイベントを処理し、必要に応じて通知されたイベントに対応することができます。 この機能は、アプリを使用しているユーザーが実行する特定のタイプのアクションに応じて、関連するイベントをキューに追加します。 たとえば、**倉庫アプリから作成および処理される移動オーダー**機能を使用する場合は、システムで**倉庫アプリのイベント処理**バッチ ジョブを実行しているときに、移動オーダー ヘッダーと明細行がバック エンドで作成および更新されます。

## <a name="enable-the-process-warehouse-app-events-feature"></a>倉庫アプリのイベント処理機能を有効にする

この機能を使用する前に、システム上で有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページを使用して、機能状態を確認し、必要に応じてそれを有効にすることができます。 倉庫アプリのイベント処理機能は次のように一覧表示されます。

- **モジュール** - 倉庫管理
- **機能名** - 倉庫アプリのイベント処理

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>倉庫アプリのイベントを処理するためのバッチ ジョブを設定する

### <a name="process-warehouse-app-events"></a>倉庫アプリ イベントの処理

移動オーダーの作成と行の更新のための倉庫アプリ イベントを処理するために、スケジュールされたバッチ ジョブを設定します。

1. **倉庫管理 \> 定期タスク \> 倉庫アプリのイベント処理**の順に移動します。
1. 倉庫アプリのイベント処理ダイアログ ボックスが開きます。 **バックグラウンドで実行**クイックタブを展開し、**バッチ処理**を**はい**に設定します。
1. **バックグラウンドで実行**クイックタブで、**繰り返し**を選択します。
1. **繰り返しの定義**ダイアログ ボックスが開きます。 業務の要件に応じて実行スケジュールを設定します。
1. **OK** をクリックし、**倉庫アプリのイベント処理**ダイアログ ボックスに戻ります。
1. **倉庫アプリのイベント処理**ダイアログ ボックスで **OK** を選択し、バッチ ジョブをバッチ キューに追加します。

## <a name="query-warehouse-app-events"></a>倉庫アプリ イベントのクエリ

倉庫アプリによって生成されたイベント キューとイベント メッセージを表示するには、**倉庫管理 \> 照会およびレポート \> モバイル デバイスのログ \> 倉庫アプリのイベント**の順に移動します。

## <a name="the-standard-event-queue-process"></a>標準のイベント キュー プロセス

倉庫アプリのイベント キューは、通常、次の説明のフローで使用されます。

1. イベント メッセージを使用して、イベントがキューに追加されます。 新しいメッセージには最初、**待機中**のイベントの状態が含まれます。このメッセージは、**倉庫アプリのイベント処理**バッチ ジョブによって取得および処理されることはありません。
1. メッセージの状態が**キューに設定**に更新されるとすぐに、**倉庫アプリの処理**イベント バッチ ジョブによってイベントが取得および処理されます。
1. バッチ ジョブは、要求された処理が可能かどうかに応じて、イベントの状態を**完了**または**失敗**に更新します。
1. すべての関連するイベント メッセージが**完了**になると、そのイベントがキューから削除されます。

 詳細な例については、「[倉庫アプリから移動オーダーを作成のプロセス](create-transfer-order-from-warehouse-app.md)」を参照してください。

## <a name="handle-event-errors"></a>イベント エラーの処理

倉庫イベント処理の一部として、要求されたメッセージ活動がバッチ ジョブからプロセスを受け取らないことがあります。 この場合、イベント メッセージは**失敗**に変更されます。 **バッチ ログ**情報を使用して理由を確認し、問題を修正するために必要なアクションを実行できます。

詳細な例については、「[倉庫アプリから移動オーダーを作成](create-transfer-order-from-warehouse-app.md)」を参照してください。

失敗した倉庫アプリのイベント メッセージをリセットするには、次の操作を行います。

1. **倉庫管理 \> 照会およびレポート \> モバイル デバイスのログ \> 倉庫アプリのイベント**の順に移動します。
1. **倉庫アプリ イベントのメッセージ** クイックタブで、**イベントの状態**列で**失敗**を表示している関連イベントを見つけて選択します。
1. **倉庫アプリ イベントのメッセージ** ツールバーで**リセット**を選択します。
1. 該当するすべてのメッセージがリセットされるまで作業を続行します。

また、**倉庫アプリ イベントのメッセージ** ツールバーの**削除**オプションを使用して、**失敗**したイベント メッセージを削除することもできます。