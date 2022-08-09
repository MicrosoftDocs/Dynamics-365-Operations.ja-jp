---
title: バッチ OData API
description: この記事では、バッチ OData アプリケーション プログラミング インターフェイス (API) に関する情報を提供し、Open Data Protocol (OData) を使用してジョブを再スケジューリングする方法について説明します。
author: matapg007
ms.date: 01/10/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2021-10-21
ms.openlocfilehash: fad2a6daf0c650b4c8e2f450ffbfa6c75681a2b7
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108481"
---
# <a name="batch-odata-api"></a>バッチ OData API

[!include[banner](../includes/banner.md)]

この記事では、バッチ Open Data Protocol (OData) を開く アプリケーション プログラミング インターフェイス (API) に関する情報を提供し、OData を使用してジョブを再スケジューリングする方法について説明します。

既存の[バッチ処理](batch-processing-overview.md)機能では、エラーの解釈に基づいて、変更の有無に関わらず、一部のタイプのジョブ エラーを再試行する必要がある場合は、手動で再試行する必要があります。 顧客のアクティブな営業時間を回避するためにオフピーク時から実行される予定のジョブの場合、失敗を監視し、ジョブを再トリガーするには、24 時間のサポートまたは通常の営業時間中にユーザーが作業を再開するまでの待ち時間が必要です。

## <a name="integration-of-business-events-with-batch-functionality"></a>ビジネス イベントとバッチ機能の統合

ビジネス イベント機能を使用すると、顧客はバッチ ジョブの状態の変更 (開始、失敗、完了、またはキャンセル) に関する通知を構成できます。 [Microsoft Power Automate](../business-events/business-events-flow.md) との統合により、顧客はシステムにログインすることなく、影響を受けるジョブに関する情報を取得できます。 ただし、ビジネス イベントに基づいてアクションを実行する必要がある場合は、手動操作で確認する必要があります。

バッチ イベントを構築する方法の詳細については [バッチ ビジネス イベント](../business-events/system-business-events.md) を参照してください。

## <a name="end-to-end-automation"></a>エンドツーエンドの自動化

バージョン 10.0.22 では、バッチ機能により、バッチ ジョブを再キューするために使用できる OData API が提供されます。 顧客は、OData エンドポイントを使用して、ターミナル状態にあるバッチ ジョブを再キューできます。 この機能は、Power Automate、カスタム API その他を使用することで任意の自動化と統合できます。

![エンドツーエンドの自動化。](./media/end-to-end-automation.png)


## <a name="automate-requeuing-of-failed-batch-jobs-by-using-the-odata-api"></a>OData API を使用した、失敗したバッチ ジョブの再キューの自動化

バッチ OData エンドポイントを使用すると、ユーザーはエンドツーエンド プロセスを消費および自動化し、Power Automate またはカスタム API を使用してバッチ ジョブを再スケジュールできます。 これは、業務要件に基づいて、開始、失敗、完了、またはキャンセルされた状態から待機中の状態へのバッチ ジョブ ステータスの更新をサポートします。

Power Automate を使用して、失敗したバッチ ジョブの再キューの自動化するには、次の手順に従います。

1. [Power Automate ポータル](https://flow.microsoft.com)にサインインし、[Power Automate でクラウド フローを作成する](/power-automate/get-started-logic-flow)の手順に従ってフローを作成します。
2. 財務と運用アプリでイベントを指定して、フローを開始します。 環境の詳細、ビジネス イベント カテゴリ、ビジネス イベント (**バッチジョブの失敗** など)、および適切な法人を入力します。

    ![イベントを指定します。](./media/business-event-occurs.png)

3. **アクション** タブで新しいステップを追加して、**スキーマで JSON を解析する** という名前の操作を選択し、JavaScript Object Notation (JSON) 要求を解析します。 JSON スキーマをダウンロードする詳細については、[ビジネス イベント カタログ](../business-events/home-page.md#business-event-catalog)を参照してください。
4. イベントがターゲット バッチ ジョブからのものかどうかを判断するためにジョブ ID を使用する論理条件を含めることにより、カスタム ロジックを追加します。

    ![カスタム ロジックを追加します。](./media/condition.png)

5. 条件が true と評価された場合は、財務と運用アプリで操作を選択します。**アクションの実行** を選択してバッチ OData アクションをトリガーしてジョブを実行に戻し、アクションを追加します。

    1. 財務と運用アプリ インスタンスを入力します。
    2. **BatchJobs-SetBatchJobToWaiting** アクションを選択します。
    3. 失敗したジョブを再実行するジョブ ID を選択します。

    ![アクションを追加します。](./media/execute-odata-api.png)


6. フローを保存します。

設定したフローは、バッチ イベントをリッスンします。 構成されたバッチ ジョブが失敗すると、フローはジョブを実行に戻します。 ベスト プラクティスとして、バッチ ジョブを再試行する前に検証を実行するために、カスタム ロジック (前の例を参照) を追加することをお勧めします。 これにより、システムに対する不要な負荷を回避できます。 また、バッチを再試行できる最大回数を指定することをお勧めします。 (再試行の推奨回数は 5 回です。)

ビジネス イベントをサブスクライブする他の方法があります。 バッチ イベントを構築する方法の詳細については [バッチ ビジネス イベント](../business-events/system-business-events.md)を参照してください。

## <a name="batch-api-endpoint-and-sample-response"></a>バッチ API エンドポイントと応答サンプル

- **サービス エンドポイント:** `https://<org url>/data/BatchJobs/Microsoft.Dynamics.DataEntities.SetBatchJobToWaiting`
- **メソッドのタイプ:** POST
- **ヘッダー:**

    - **承認:** ベアラー \<Bearer token for authentication\>
    - **コンテンツ タイプ:** アプリケーション/json

- **本文:**

    ```json
    {
        "batchJobId":<BatchJobId>
    }
    ```

- **応答の例:**

    ```json
    {
        "ResponseStatusCode":200,
        "IsSuccess":true,
        "Batch JobId":<BatchJobId>,
        "ExceptionDetails":"",
        "reponseMessage":"Status of supplied BatchJobId: *********** is Successfully updated to waiting state"
    }
    ```

    応答出力の要素の説明を次に示します。

    - **ResponseStatusCode**- アクションの実行に基づく標準的な HTTP 応答コード。
    - **IsSuccess**- 全体的な成功または失敗を示すブール値。
    - **BatchJobId**- 入力バッチ ジョブの ID。
    - **ExceptionDetails**- 実行中に発生した例外に関する詳細。
    - **ReponseMessage**- 成功メッセージ。

