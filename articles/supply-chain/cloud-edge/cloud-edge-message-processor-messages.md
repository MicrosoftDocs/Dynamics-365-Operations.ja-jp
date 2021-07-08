---
title: メッセージ プロセッサのメッセージ
description: このトピックでは、スケール ユニット ワークロードのッセージ プロセッサ メッセージ機能に関する情報を提供します。
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 86f15831f11dc9fdcada9639858fd3b18cdc7503
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271104"
---
# <a name="message-processor-messages"></a>メッセージ プロセッサのメッセージ

[!include [banner](../includes/banner.md)]

ッセージ プロセッサ メッセージは、[製造ワークロード](cloud-edge-workload-manufacturing.md)および[倉庫管理ワークロード](cloud-edge-workload-warehousing.md)に対してクラウドおよびエッジのスケール ユニットを実行している場合に使用します。

ハブとスケール ユニットの展開環境間での同期を維持するために大量のデータが交換されますが、*メッセージ プロセッサ* によって処理されるデータ交換はその一部分だけです。 **システム管理 > メッセージ プロセッサ > メッセージ プロセッサ メッセージ** から、メッセージ プロセッサによって処理されたメッセージを表示することができます。

## <a name="message-grid-columns-and-filters"></a>メッセージ グリッドの列およびフィルター

**メッセージ プロセッサ メッセージ** ページの上部にあるフィールドを使用して、検索する特定のメッセージ を見つけることができます。 これらのフィルターのほとんどは、メッセージ グリッド列のヘッダーと一致します。 次のフィルターと列のヘッダーが使用可能です。

- **メッセージ タイプ**: メッセージのタイプを指定します。
- **メッセージ キュー**: メッセージを処理するキューの名前を指定します。 次のキューが用意されています。
  - *ハブに対するスケール ユニット*
  - *ハブから倉庫実行スケール ユニット*
  - *ハブから製造実行スケール ユニット*
- **メッセージの状態** – メッセージの状態を指定します。 次の状態があります。
  - *キューに設定* – メッセージ プロセッサでメッセージを処理する準備ができます。
  - *処理済み* – メッセージがメッセージ プロセッサで正常に処理されました。
  - *取消済* – メッセージを処理しましたが、処理に失敗しました。
- **メッセージ コンテンツ** – このフィルターはメッセージの内容を全文検索します。 (グリッドにメッセージ コンテンツは表示されません。) このフィルターでは、ほとんどの特殊な記号 (「-」など) をスペースとして処理し、すべての空白文字をブール OR 演算子として処理します。 T= たとえば、「USMF-123456」と等しい特定の `journalid` 値を検索すると、長いリストの場合ように、システムは「USMF」または「123456」を含むすべてのメッセージを検索します。 したがって、「123456」と入力した方がより正確な結果が得られるでしょう。

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>メッセージ タイプの例: 在庫調整財務更新の要求

たとえば、**メッセージ タイプ** *在庫調整財務更新の要求* は、作業者が倉庫アプリを使用してスケール ユニットの倉庫管理ワークロードの[在庫調整の登録](cloud-edge-warehouse-inventory-adjustment.md)を行う場合に、ハブ上の棚卸仕訳帳の作成および転記を行うために使用されます。 この特定のプロセスの生成元はスケール ユニットなので、**ッセージ キュー** フィールドに *スケール ユニットからハブへ* の値が表示されます。

このメッセージ タイプの場合、スケール ユニットのワークロードは、メッセージを倉庫アプリの在庫調整操作の一部として記録します。 メッセージ データは、[Commerce Data Exchange アーキテクチャ](../../commerce/commerce-architecture.md)で使用されるのと同じプロセスの一部としてハブに転送されます。 メッセージが更新され、**メッセージの状態** が *キューに設定* として表示されます。 メッセージ プロセッサはメッセージの処理を試行し、成功時は *処理済* に、失敗時は *取消済* に **メッセージの状態** を更新します。

## <a name="view-the-message-log-message-content-and-details"></a>メッセージ ログ、メッセージ コンテンツ、および詳細の表示

グリッドで選択し、各処理イベントが表示されているメッセージ グリッドの下にある **ログ** または **メッセージ コンテンツ** タブを開くことによって、メッセージに関する詳細情報を検索することができます。

**メッセージ コンテンツ** は **メッセージ タイプ** に依存するため、テキストの長さが異なります。 一般的なメッセージ コンテンツのテキストは、**{** で始まって **}** で終わり、その間に **:** と *USMF-123456* のような値に続いて `journalId` などのフィールド名があります。

**ログ** タブのツールバーには次のボタンが含まれます。

- **ログ** – 処理結果を表示します。 これは、**処理結果** が *失敗* であるメッセージについて、処理が失敗した理由を理解するのに特に役立ちます。
- **バンドル** – 複数のメッセージ処理操作を同じバッチ プロセスの一部として実行することができます。 このボタンを選択して、この詳細データを表示します。 たとえば、システムが指定された順序で特定のメッセージを処理することが必要もなる依存関係が存在するかどうかを確認できます。

## <a name="message-processor-batch-job"></a>メッセージ プロセッサのバッチ ジョブ

クラウドおよびエッジの配置を実行する場合、処理に対して新しいメッセージが作成されるとき、*メッセージ プロセッサのバッチ ジョブ* が自動的に呼び出されるので、このジョブを手動でスケジュール必要はありません。

必要に応じて、**システム管理 > メッセージ プロセッサ > メッセージ プロセッサ** に移動して、バッチ ジョブにアクセスできます。

## <a name="manually-process-or-cancel-a-message"></a>メッセージの手動処理またはキャンセル

必要な場合、現在の状態に応じて、メッセージを手動で処理またはキャンセルすることができます。 そのためには、グリッドでメッセージを選択し、アクション ウィンドウで **処理** または **キャンセル** を選択します

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>失敗した処理結果に対する警告を配信するビジネス イベントの設定

**メッセージの状態** の値を *取消済* でフィルター処理して失敗したメッセージを照会することに加え、失敗した処理結果について警告するためにハブで[ビジネス イベント](../../fin-ops-core/dev-itpro/business-events/home-page.md)を設定することができます。 そのためには、**ビジネス イベント カタログ** ページ (**システム管理 > 設定 > ビジネス イベント > ビジネス イベント カタログ**) で *メッセージ プロセッサ メッセージ処理済* と名前の付けられたビジネス イベントを有効化します。

有効化プロセスの一部として、イベントが 1 つまたはすべての法人に指定されているかどうかを指定するよう案内が表示され、最初に定義する必要がある **エンドポイント** の名前を提供します。

>[!NOTE]
> **ビジネス イベントの発生時** が (*HTTPS* ではなく) *Microsoft Power Automate* に設定されている場合、**エンドポイント名** は、*Microsoft Power Automate* の設定に基づいて Supply Chain Management で自動的に作成されます。

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate の例

この例では、*Microsoft Power Automate* で **ビジネス イベントの発生時** を使用して、InfoLog メッセージとハブの展開で失敗した特定のメッセージの **メッセージ プロセッサ メッセージ** を開くハイパーリンクを含む電子メールを送信します。 異なるチャネルを使用して並列で通知を送信し、イベント データに基づく受信者を制御する追加ロジックを追加することができます。

1. [Power Automate](https://preview.flow.microsoft.com) では、次の図に示されているように、**JSON 解析** および **電子メール送信** のステップに続くフロー トリガー **ビジネス イベントの発生時 - Finance and Operations アプリ (Dynamics 365)** に対する新しい自動化クラウド フローを作成します。

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate 自動化クラウド フロー":::

1. **ビジネス イベントの発生時** のステップでは、次の図に示すように、**カテゴリ**、そして **ビジネス イベント** の *メッセージ プロセッサ メッセージ処理済* に続くハブ **インスタンス** の検索または入力を行うことができます。

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate ビジネス イベントの発生時のステップ":::

1. **JSON の解析** のステップで、拡張フィールドを定義する **スキーマ** を入力します。 Supply Chain Management の **ビジネス イベント カタログ** ページにある *スキーマのダウンロード* オプションを使用するか、または例にあるスキーマ テキストを貼り付けて開始することができます。 この例のテキストは、次の図の後で提供されます。

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate JSON 解析のステップ":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. **電子メールの送信** ステップにおいて、個別のフィールドを選択するか、または電子メール本文の例を **本文** フィールドに貼り付けて開始することができます。 この例は、次の図の後で提供されます。

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate 電子メール送信ステップ":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. ビジネス イベントを保存すると自動的に有効化され、Supply Chain Management の一部として使用可能になります。
