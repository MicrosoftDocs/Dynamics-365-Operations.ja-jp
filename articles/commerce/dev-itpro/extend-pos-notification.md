---
title: POS でカスタム通知を表示する
description: このトピックでは、販売時点管理 (POS) でカスタマイズした通知を追加する方法について説明します。
author: mugunthanm
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6dce2afb2716f23d1b99109a2e31aabeae349d0d63639f175b6d2b55d29b68db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742404"
---
# <a name="show-custom-notifications-in-the-pos"></a>POS でカスタム通知を表示する

[!include [banner](../includes/banner.md)]

このトピックでは、販売時点管理 (POS) でカスタマイズした通知を追加する方法について説明します。 このトピックは、最新のバイナリ修正がある Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 および Dynamics 365 for Retail 7.3 とそれ以降のバージョンに適用されます。

次のシナリオで、POS 通知フレームワークを拡張できます。

- カスタム通知を表示して、店舗の関連付けが通知に基づいて必要なアクションを実行したり、カスタム ロジックを実行できるようにします。
- 定期的に、バックグラウンドで操作を実行します。 ただし、パフォーマンスの問題が発生する可能性があるため、このシナリオはお勧めしません。

## <a name="how-custom-notifications-work"></a>カスタム通知の仕組み

POS の通知フレームワークは、Retail Headquarters で構成されている操作に対して定期的に実行されます。 (定期処理の実行頻度をコンフィギュレーションできます。) また、Commerce runtime (CRT) および Retail Headquarters のリアルタイム サービスで通知サービスを呼び出します。 POS が CRT で通知サービスに対する呼び出しを行うと、CRT はビジネス ロジックを実行し、操作に対して POS に送信される通知があるかどうかを決定します。 操作 ID は、要求にパラメータとして渡されます。 CRT 通知サービスは操作 ID をチェックし、通知の詳細を返します。

通知が存在する場合、CRT は POS に利用可能な通知があることを報告する応答を返します。 この通知は、POS によって解析され、ユーザー インターフェース (UI) に表示されます。 POS ユーザーが通知を選択すると、POS の関連する操作が実行されます。 通知は、操作にリンクされています。 操作ハンドラー内で、実行する必要があるビジネス ロジックを書き込みます。

CRT が通知に対する応答を返すと、通知、メッセージ、およびアクション パラメーターの数が返されます。 POS フレームワークには、応答を解析して POS 操作 ID を取得し、ユーザーが通知を選択したときにそれを呼び出す組み込みロジックがあります。

操作内で、POS ユーザーが通知を選択したときに行われる特定の動作について、カスタム ロジックに書き込むことができます。 アクション プロパティを使用して、追加のパラメータを CRT から POS に送信することができます。 その後、これらのパラメータは、POS の操作要求内で使用可能です。

### <a name="example"></a>例

集荷の注文を準備するよう POS ユーザーに通知するために、CRT に集荷の注文があるかどうかを確認します。 ある場合、関連するパラメーターを使用して通知応答を更新します。 POS が応答を解析し、通知を表示します。 POS ユーザーが通知を選択すると、POS は通知からのパラメータを使用して操作を呼び出します。 (拡張ロジックは、パラメータを送信する必要があるかどうかを決定します。) 操作内で、POS が集荷の保留中の注文をすべて読み取り、POS ユーザーがさらにアクションを実行できるように、注文を UI に表示します。

## <a name="required-steps-to-make-notifications-available-for-a-custom-operation"></a>カスタム操作の通知を使用可能にするための必要な手順

1. Retail Headquarters で **Retail と Commerce \> チャネル設定 \> POS 設定 \> POS \> POS 操作** に移動し、操作を作成します。

    > [!NOTE]
    > カスタム操作に 5000 以上の操作 ID を使用します。

2. 通知サービスを拡張します。 通知サービスのスケジューラが実行されると、通知メッセージを取得するために、CRT とリアルタイム トランザクション サービス拡張コードの両方の拡張コードが呼び出されます。
3. POS を拡張します。 POS で、POS ユーザーが通知を選択したときに行われる特定の動作について、POS 操作内のロジックに書き込みます。 POS 操作の作成方法については、[ボタン グリッド デザイナーを使用して POS 操作を POS レイアウトに追加](add-pos-operations.md) を参照してください。
4. Retail Headquarters で、カスタム操作の通知サービスを構成します。 その後、スケジューラが通知サービスを実行すると、カスタム操作が含まれます。 POS で通知を構成する方法については、[ボタン グリッド デザイナーを使用して POS 操作を POS レイアウトに追加](../notifications-pos.md) を参照してください。

    POS ユーザーが通知を選択すると、CRT から返された応答に基づいて、フレームワークは適切な操作を呼び出します。 Retail Headquarters で構成されているすべての通知に対して通知サービスが実行され、操作 ID と通知の詳細を含む応答が返されます。 そのため、POS は操作 ID のコンテキストを持つことになり、フレームワークはこのコンテキストを使用してオペレーションの実装を呼び出します。

> [!NOTE]
> 通知スケジューラは、CRT と Retail Headquarters の両方で、新しい通知を確認します。 シナリオに応じて、Retail Headquarters または CRT のみのリアルタイム トランザクション サービスを拡張できます。 通知にリアルタイム処理が必要なシナリオでは、Retail Headquarters でリアルタイム トランザクション サービスを拡張します。 リアルタイム処理を必要としない場合は、CRT のみを拡張します。

## <a name="extend-the-notification-service-in-crt"></a>CRT の通知サービスの拡張

CRT の通知サービスを拡張するには、**GetNotificationsExtensionServiceRequest** を上書きし、**GetNotificationsExtensionServiceResponse** を返します。

Retail ソフトウェア開発キット (SDK) には、通知サービス (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**) を拡張する方法を示すサンプルが含まれています。

+ **GetNotificationsExtensionServiceRequest** – このクラスには、操作 ID、スタッフ、およびチャネルが含まれます。 Retail Headquarters の構成に基づいて、POS は構成された各操作に対して通知スケジューラを実行します。
+ **GetNotificationsExtensionServiceResponse** – 応答で、通知の詳細エンティティ (**NotificationDetailCollection**) を返し、**GetNotificationsExtensionServiceResponse** を更新して、すべての通知を返します。 応答はコレクションなので、複数の通知を返すことができます。

## <a name="properties-of-the-notification-detail-entity"></a>通知の詳細エンティティのプロパティ

通知の詳細エンティティには、次のプロパティがあります。

| プロパティ               | データ型      | 説明                                                                            |
|------------------------|----------------|----------------------------------------------------------------------------------------|
| ActionProperty         | 文字列         | POS 操作に送信するカスタム プロパティ。                                        |
| DisplayText            | 文字列         | 通知の表示テキスト。                                                  |
| IsLiveContentOnly      | ブール           | 通知がライブ コンテンツのみを対象とするかどうかを示す値。              |
| IsNew                  | ブール           | 通知が新しいかどうかを示す値。                                |
| IsSuccess              | ブール           | 通知が成功したかどうかを示す値。                        |
| ItemCount              | long           | 通知の数。                                                           |
| LastUpdatedDateTime    | DateTimeOffset | アクション プロパティの項目が最後に更新された日時。                   |
| LastUpdatedDateTimeStr | 文字列         | 文字列形式のアクション プロパティの項目が最後に更新された日時。 |

## <a name="detailed-steps"></a>詳細な手順

1. Retail SDK から **Runtime.Extensions.NotificationSample.proj** を開きます (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**)。
2. 標準の名前付け規則に従ってプロジェクトの名前を変更します。
3. プロジェクト内には、**NotificationExtensionService.cs** という名前のクラス ファイルがあります。 このファイルを開きます。
4. **GetNotificationsExtensionServiceRequest** クラスは、カスタム通知を追加するために上書きされます。 **GetNotificationsExtensionServiceRequest** を上書きし、**GetNotificationsExtensionServiceResponse** を返します。
5. 新しいクラスを作成して、**GetNotificationsExtensionServiceRequest** を上書きするか、サンプル テンプレートを使用します。 
6. **NotificationExtensionService** クラスには、**Process** という名前のメソッドがあります。 このコードは、メソッド内で操作 ID を確認し、操作 ID に基づいて通知の詳細オブジェクトを作成し、通知を追加します。 カスタム操作 ID かどうかを確認し、通知があるかどうかを確認するロジックを記述します。 通知がある場合は、詳細を含む通知オブジェクトを作成し、応答と共に返します。 その後、POS が応答を解析し、通知を表示します。 テンプレートに基づくコード例を次に示します。

    > [!NOTE]
    > プロセス メソッド内のサンプル実装を削除します。 カスタム ロジックのみを保持します。

    ```csharp
    namespace Contoso
    {
        namespace Commerce.Runtime.NotificationSample
        {
            using System;
            using Microsoft.Dynamics.Commerce.Runtime;
            using Microsoft.Dynamics.Commerce.Runtime.DataModel;
            using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
            /// <summary>
            /// Service class responsible executing the service requests.
            /// </summary>
            public class NotificationExtensionService : SingleRequestHandler<GetNotificationsExtensionServiceRequest, GetNotificationsExtensionServiceResponse>
            {
                /// <summary>
                /// The handler for the <c>GetNotificationsExtensionServiceRequest</c> request.
                /// </summary>
                /// <param name="request">The request with the operation.</param>
                /// <returns>The notification details for the operation.</returns>
                protected override GetNotificationsExtensionServiceResponse Process(GetNotificationsExtensionServiceRequest request)
                {
                    ThrowIf.Null(request, "request");
                    NotificationDetailCollection details = new NotificationDetailCollection();
                    DateTimeOffset lastNotificationDateTime = DateTimeOffset.Now;
                    string myOperationId = "5000";
                    // do the actual work here
                    if ((request.SubscribedOperation).ToString() == myOperationId)
                    {
                        NotificationDetail detail = new NotificationDetail()
                        {
                        // Text which will display for the notification detail in the POS notification center
                        DisplayText = "Custom notification",
                        // Number of notifications found
                        ItemCount = 1,
                        // Timestamp of creation of latest notification item (Used to determine whether notification is new)
                        LastUpdatedDateTime = lastNotificationDateTime,
                        // Boolean value representing whether the attempt to get notifications for the given operation was successful
                        IsSuccess = true,
                        // If you would like POS to navigate to a specific action property for the given operation
                        // when the notification tile is selected, define the action property as well.
                        ActionProperty = "1"
                        };
                    details.Add(detail);
                    }
                    var serviceResponse = new GetNotificationsExtensionServiceResponse(details);
                    return serviceResponse;
                }
            }
        }
    }
    ```

7. 変更が完了したら、プロジェクトをビルドし、出力ライブラリを **\\RetailServer\\webroot\\bin\\Ext** にドロップします。
8. **CommerceRuntime.Ext.config** ファイルに出力ライブラリを登録します。
9. POS で、CRT 拡張機能で使用されているのと同じ操作 ID を使用して、新しい操作を作成します。 この例では、操作 ID は **5000** です。 5000 以上の任意の操作 ID を使用できます。
10. POS ユーザーが通知タイルを選択すると、POS フレームワークは使用される操作 ID の操作ハンドラーを呼び出します。 ハンドラー内で、POS ユーザーが通知を選択したときに行われる特定の動作について、必要なロジックを追加します。 POS 操作要求、応答、およびハンドラーの作成方法については、 [販売時点管理 (POS) での注文通知の表示](add-POS-operations.md) を参照してください。

    > [!NOTE]
    > 通知の詳細エンティティのアクション プロパティが POS 操作要求に送信されます。 このアクション プロパティを使用すると、通知サービス から POS にカスタム情報を渡すことができます。

11. [販売時点管理 (POS) での注文通知の表示](../notifications-pos.md) の指示に従って、通知スケジューラをコンフィギュレーションします。

## <a name="validate-the-customization"></a>カスタマイズの検証

1. 拡張 Cloud POS または Modern POS アプリケーションを開きます。

    POS は、通知スケジューラのコンフィギュレーションに基づいて通知サービスをトリガーします。

3. CRT プロジェクトを w3wp.exe にアタッチして、CRT コードをデバッグします。 このブレークポイントは、通知サービスが POS から呼び出されたときに必ずヒットします。
4. POS で通知を受信したら、通知をクリック選択します。 POS 操作ハンドラーを呼び出し、ハンドラー内に記述されたカスタム ロジックを実行します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]