---
title: 完成品を仕訳帳に転記する前に現物在庫にする
description: 製造品目が完了として報告されると、追加の現物処理に使用可能として登録され、1 つ以上の仕訳帳が転記されます。 この記事では、メッセージ キュー内のバッチ ジョブで処理できるようにして、仕訳帳転記を繰延する方法について説明します。
author: johanhoffmann
ms.date: 08/02/2022
ms.topic: article
ms.search.form: ProdParameters, JmgProdParameters, InventLocation, JmgMES3PMessageProcessorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-08-02
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7a8327552d9e6c38721fdac9ee1795e61f90f329
ms.sourcegitcommit: 8d072505f66f507aafbaae65bedf3b530eb6cb7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9266486"
---
# <a name="make-finished-goods-physically-available-before-posting-to-journals"></a>完成品を仕訳帳に転記する前に現物在庫にする

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

作業員が製造品目を完了としてレポートすると、システムはその品目を追加の現物処理 (出荷やプットアウェイなど) で利用可能として登録します。 このプロセスでは、1 つ以上の仕訳帳も転記されます (完了レポート仕訳帳が、ピッキング リスト仕訳帳、工順カード仕訳帳など)。 すべての転記が処理される前に品目を現物で使用可能にする場合は、仕訳帳転記を繰延するようにシステムを設定できます。 繰延転記は、システム リソースが許可するときに、転記を処理するバッチ ジョブによって管理されます。

次の図は、仕訳帳を転記するためのプロセスが、繰延した転記の有無にかかわらずどのように呼び出されるかを示しています。

![繰延した仕訳帳転記がある場合とない場合の完了レポートのプロセス。](media/deferred-posting-flowchart.png "繰延した仕訳帳転記がある場合とない場合の完了レポートのプロセス")

## <a name="turn-on-deferred-journal-posting-for-your-system"></a>システムで繰延した仕訳帳転記を有効にする

繰延した仕訳帳転記を使用するには、システム上で有効化する必要があります。 管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています。

- **モジュール:** *生産制御*
- **機能名:** *(プレビュー) 完成品を仕訳帳に転記する前に現物在庫にする*

## <a name="set-up-journal-posting-options-for-reporting-as-finished"></a>完了としてレポートするために仕訳帳転記オプションを設定する

作業員は、以下のいずれかのクライアントを使用して、品目を完了としてレポートできます。

- Web クライアント
- Warehouse Management モバイル アプリ
- 生産現場の実行インターフェース

Web クライアントでは、Warehouse Management モバイル アプリと同じ転記方法の構成を使用します。 ただし、生産現場の実行インターフェースが使用する転記方法は、個別に構成する必要があります。

### <a name="set-journal-posting-options-for-the-web-client-and-the-warehouse-management-mobile-app"></a>Web クライアントおよび Warehouse Management モバイル アプリ用の仕訳帳転記オプションを設定する

モバイル アプリでは、作業員は、**作業作成プロセス** の値が *完了レポート* または *完了レポートとプット アウェイ* であるモバイル デバイス メニュー項目を開いて、品目の完了を報告します。 Web クライアントでは、作業者は **すべての製造オーダー** リスト ページまたは **製造オーダー (詳細)** ページから品目の完了をレポートします。 会社全体の既定の方法を構成し、必要に合じて倉庫固有の上書きを設定することもできます。

Web クライアントまたは Warehouse Management モバイル アプリから品目の完了を報告するために、会社全体の既定の転記方法を構成するには、次の手順に従います。

1. **生産管理 \> 設定 \> 生産管理パラメーター** の順に移動します。
1. **仕訳帳** タブの **完了レポート仕訳帳** セクションで、**転記方法** フィールドに次のいずれかの値を設定します:

    - *即時* – 品目が完了と報告されると、完成品目が現物使用可能とマークされる前に、関連のすべての仕訳帳転記がシステムによって完全に処理されます。
    - *繰延* – 品目が完了と報告されると、システムは完成品目を現物使用可能としてマークし、仕訳帳転記をメッセージ キューに追加します。 システムは、転記が完全に処理されるのを待たずに、完成品目が現物使用可能とマークします。

次の手順を使用して、**生産管理パラメーター** ページで構成されている既定の転記方法に対して倉庫固有の上書きを構成します。

1. **Warehouse Management \> 設定 \> 在庫詳細 \> 倉庫** の順に移動します。
1. 設定する倉庫を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **倉庫** FastTab の **製造オーダー** セクションで、**転記方法** フィールドに次のいずれかの値を設定します:

    - *継承* – 選択した倉庫は、**生産管理パラメーター** ページの設定を継承します。
    - *即時* – 品目が完了と報告されると、完成品目が現物使用可能とマークされる前に、関連のすべての仕訳帳転記がシステムによって完全に処理されます。
    - *繰延* – 品目が完了と報告されると、システムは完成品目を現物使用可能としてマークし、仕訳帳転記をメッセージ キューに追加します。 システムは、転記が完全に処理されるのを待たずに、完成品目が現物使用可能とマークします。

### <a name="set-journal-posting-options-for-the-production-floor-execution-interface"></a>生産現場の実行インターフェースに仕訳帳転記オプションを設定する

次の手順を使用して、生産現場の実行インターフェースから品目が完了として報告されたときに使用される転記方法を構成します。

1. **生産管理 \> 設定 \> 製造実行 \> 製造オーダーの既定値** の順に移動します。
1. **完了レポート** タブの **完了レポート仕訳帳** セクションで、**転記方法** フィールドに次のいずれかの値を設定します:

    - *即時* – 品目が完了と報告されると、完成品目が現物使用可能とマークされる前に、関連のすべての仕訳帳転記がシステムによって完全に処理されます。
    - *繰延* – 品目が完了と報告されると、システムは完成品目を現物使用可能としてマークし、仕訳帳転記をメッセージ キューに追加します。 システムは、転記が完全に処理されるのを待たずに、完成品目が現物使用可能とマークします。

## <a name="schedule-the-message-processor-batch-job-to-process-deferred-postings"></a>繰延転記を処理するメッセージ プロセッサ バッチ ジョブをスケジュールする

メッセージ プロセッサ バッチ ジョブは、キューに入れらた後に仕訳帳転記を処理します。 仕訳帳転記を確実に処理するには、定期的に実行するようにジョブを構成する必要があります。 次の手順を使用して、必要なバッチ ジョブを設定します。

1. **システム管理 \> メッセージ プロセッサ \> メッセージ プロセッサ** に移動します。
1. **パラメーター** FastTab で、**メッセージ キュー** フィールドを *生産* に設定します。
1. **バックグラウンドで実行** クイックタブで、**バッチ処理** オプションを *はい* に設定します。 その後、定期的なスケジュールを設定し、必要に応じてその他の設定を構成します。 設定は、Microsoft Dynamics 365 Supply Chain Management の他の種類の [バックグラウンド ジョブ](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) と同様に機能します。

## <a name="track-the-progress-of-your-deferred-postings"></a>繰延転記の進捗状況を追跡する

繰延仕訳帳転記は、*メッセージ プロセッサ* によって処理されるまで待機する *メッセージ プロセッサ メッセージ* としてキューに入れられます。 メッセージ プロセッサは、スケジュールされたバッチ ジョブとして実行するために設定する必要があります。 メッセージ プロセッサによって処理された、または処理される繰延転記メッセージを表示するには、**生産管理 \> 製造オーダー \> 繰延製造オーダーの転記** に移動します。

### <a name="message-grid-columns-and-filters"></a>メッセージ グリッドの列およびフィルター

**繰延製造オーダーの転記** ページの上部にあるフィールドを使用して、検索する特定のメッセージ を見つけることができます。

次のフィルターを使用できます:

- **メッセージ タイプ** – グリッドに表示されるメッセージのタイプを指定します。
- **メッセージの状態** – グリッドに表示されるメッセージの状態を指定します。 次の状態があります:

    - *キューに設定* – メッセージ プロセッサでメッセージを処理する準備ができます。
    - *処理済み* – メッセージがメッセージ プロセッサで正常に処理されました。
    - *キャンセル済み* – メッセージは最後の試行中に処理に失敗し、その後ユーザーによってキャンセルされました。
    - *失敗* – メッセージが前回の試行中に処理に失敗しました。 システムは、失敗したメッセージを 3 回再試行します。 その後、中止され、メッセージは *失敗* 状態のままになります。 この 3 回の試みが完了するまで、メッセージを手動でキャンセルまたは編集することはできません。

- **メッセージ コンテンツ** – このフィルターはメッセージの内容を全文検索します。 (グリッドにメッセージ コンテンツは表示されません。) このフィルターでは、ほとんどの特殊記号 (「-」など) を空白文字として処理し、すべての空白文字をブール OR 演算子として処理します。 たとえば、*USMF-123456* に等しい特定の `journalid` 値を検索すると、システムは、"USMF" または "123456" を含むすべてのメッセージを検索します。 この場合、結果の一覧が長くなる可能性があります。 そのため、*123456* だけ入力した方がより正確な結果が得られます。

また、列見出しを選択し、ドロップダウン ダイアログ ボックスに条件を入力することで、リストを並べ替えたりフィルターすることもできます。

### <a name="view-the-message-log-message-content-and-details"></a>メッセージ ログ、メッセージ コンテンツ、および詳細の表示

グリッドで選択し、各処理イベントが表示されているメッセージ グリッドの下にある **ログ** または **生コンテンツ** タブを選択することで、メッセージに関する詳細情報を検索することができます。

**ログ** タブのツールバーには次のボタンが含まれます。

- **ログ** – 処理結果を表示する場合は、このボタンを選択します。 このボタンは、メッセージの **処理結果** の値が *失敗* で、処理が失敗した理由を調べる場合に特に役立ちます。
- **バンドル** – 複数のメッセージ処理操作を同じバッチ プロセスの一部として実行することができます。 このボタンを選択して、この詳細データを表示します。 たとえば、一部のメッセージに対して特定の処理順序を必要とする依存関係が存在するかどうかを確認できます。

### <a name="manually-process-or-cancel-a-message"></a>メッセージの手動処理またはキャンセル

現在の状態により、必要に応じてメッセージを手動で処理またはキャンセルすることができます。 グリッドでメッセージを選択し、アクション ウィンドウで **処理** または **キャンセル** を選択します。

### <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>失敗した処理結果に対する警告を配信するビジネス イベントの設定

処理の失敗を警告する [ビジネス イベント](../../fin-ops-core/dev-itpro/business-events/home-page.md) を設定することができます。 **システム管理 \> 設定 \> ビジネス イベント \> ビジネス イベント カタログ** に移動し、*メッセージ プロセッサのメッセージが処理済み* と名前の付けられたビジネス イベントをアクティブにします。

アクティブ化プロセスの一環として、イベントが特定の法人に固有であるか、すべての法人に適用されるかを指定するように求められます。 また、**エンドポイント名** の値を指定するように求められます。 最初に、この値を定義する必要があります。

> [!NOTE]
> **ビジネス イベントの発生時** フィールドが *Microsoft Power Automate* (たとえば *HTTPS* の代わりに) に設定されている場合、**エンドポイント名** の値は、*Microsoft Power Automate* の設定に基づいて Supply Chain Management で自動的に作成されます。