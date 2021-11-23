---
title: バッチ OData API
description: このトピックでは、バッチ OData アプリケーション プログラミング インターフェイス (API) に関する情報を提供し、Open Data Protocol (OData) を使用してジョブを再スケジューリングする方法について説明します。
author: matapg007
ms.date: 10/18/2021
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2021-10-21
ms.openlocfilehash: ec58a24c83cf9720bfc5baa5d421504ded98efd5
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679069"
---
# <a name="batch-odata-api"></a>バッチ OData API

[!include[banner](../includes/banner.md)]

このトピックでは、バッチ OData アプリケーション プログラミング インターフェイス (API) に関する情報を提供し、Open Data Protocol (OData) を使用してジョブを再スケジューリングする方法について説明します。

既存の Finance and Operations [バッチ処理](batch-processing-overview.md) では、一部のタイプのジョブ エラーを (エラーの解釈に基づき、変更または変更せずに) 再試行できる場合は、手動でバッチから再実行する必要があります。 顧客のアクティブな営業時間を回避するためにオフピーク時から実行される予定のジョブの場合、失敗を監視し、ジョブを再トリガーするには、24 時間のサポートまたは通常の営業時間中にユーザーが作業を再開するまでの待ち時間が必要です。

## <a name="current-available-automation-business-events-integration"></a>現在使用可能な自動化 (ビジネス イベント統合)

ビジネス イベント機能を使用すると、顧客はバッチ ジョブの状態の変更 (開始、失敗、完了、またはキャンセル) に関する通知を構成できます。 [Microsoft Power Automate](../business-events/business-events-flow.md) との統合により、顧客はシステムにログインすることなく、影響を受けるジョブに関する情報を取得できます。 ただし、ビジネス イベントに基づいてアクションを実行する必要がある場合は、手動操作で確認する必要があります。

バッチ イベントを構築する方法の詳細については [バッチ ビジネス イベント](../business-events/system-business-events.md) を参照してください。

## <a name="end-to-end-automation"></a>エンドツーエンドの自動化

バージョン 10.0.22 では、バッチ機能により、バッチ ジョブを再キューするために使用できる OData API が公開されます。 顧客は、OData エンドポイントを使用して、ターミナル状態にあるバッチ ジョブを再キューできます。 この機能は、Power Automate、カスタム API その他を使用することで任意の自動化と統合できます。

![エンドツーエンドの自動化。](media/BatchAPI.png)

## <a name="automate-requeuing-of-failed-batch-jobs-by-using-odata-api"></a>OData API を使用した、失敗したバッチ ジョブの再キューの自動化

バッチ OData エンドポイントを使用すると、ユーザーはエンドツーエンド プロセスを消費および自動化し、Power Automate またはカスタム API を使用してバッチ ジョブを再スケジュールできます。 これは、業務要件に基づいて、開始、失敗、完了、またはキャンセルされた状態から待機中の状態へのバッチ ジョブ ステータスの更新をサポートします。

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
