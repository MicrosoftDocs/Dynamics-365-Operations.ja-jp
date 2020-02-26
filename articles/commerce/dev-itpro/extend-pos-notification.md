---
title: POS のカスタム通知の表示
description: このトピックでは、販売時点管理 (POS) でカスタム通知を追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c775c8e39e180ee50fb60faf2ac590eaaa4fb3a4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004582"
---
# <a name="show-custom-notifications-in-pos"></a>POS のカスタム通知の表示

[!include [banner](../includes/banner.md)]

このトピックでは、POS でカスタム通知を追加する方法について説明します。 このトピックは、最新のバイナリ修正プログラムが適用された Dynamics 365 for Finance and Operations および Dynamics 365 for Retail 7.3 以降のバージョンに適用されます。

次のようなシナリオで、POS 通知フレームワークを拡張できます。 

- カスタム通知を表示して、店舗の関連付けが通知に基づいて必要なアクションを実行したり、カスタム ロジックを実行したりできるようにします。 
- バックグラウンドで定期的に操作を実行します。 ただし、パフォーマンスの問題が発生する可能性があるため、この方法はお勧めしません。

## <a name="how-it-works"></a>この機能の動作

POS の通知フレームワークは、バックオフィスでコンフィギュレーションされた操作 (頻度はコンフィギュレーション可能) に対して定期的に実行され、Commerce Runtime (CRT) の通知サービス、およびバックオフィスのリアルタイム サービスを呼び出すことができます。 POS が CRT で通知サービスに対する呼び出しを行うと、CRT はビジネス ロジックを実行し、特定の操作に対して POS に送信される通知があるかどうかを確認します。 操作 ID はパラメーターとして要求に渡され、CRT 通知サービスが操作 ID を確認して通知の詳細を返します。 

通知が存在する場合、CRT は POS に利用可能な通知があることを報告する応答を返します。 この通知は、POS によって解析され、UI に表示されます。 POS ユーザーが通知をクリックすると、POS の関連する操作が実行されます。 通知は操作に関連付けられ、操作ハンドラー内で実行するビジネス ロジックを記述します。

CRT が通知に対する応答を返すと、通知、メッセージ、およびアクション パラメーターの数が返されます。 POS フレームワークには、応答を解析して POS 操作 ID を取得し、ユーザーが通知をクリックしたときにそれを呼び出す組み込みロジックがあります。 

POS ユーザーが通知をクリックしたときに行われる動作について、操作内のカスタム ロジックに記述できます。 CRT からの POS への追加パラメーターをアクション プロパティを使用して送信し、POS の操作要求内で使用できるようになります。

### <a name="example"></a>例
集配の注文を準備するように POS ユーザーに通知するために、CRT に集配の注文があるかどうかを確認します。 その場合、関連するパラメーターを使用して通知応答を更新します。 POS が応答を解析し、通知を表示します。 POS ユーザーが通知をクリックすると、POS は通知からのパラメーターを持つ操作を呼び出し (パラメーターを送信するかどうかは拡張機能ロジックによって異なります)、操作内で保留中のすべての集配の注文が読み取られ、POS ユーザーが追加のアクションを実行できるように、UI に表示されます。

## <a name="steps-required-to-enable-notification-for-custom-operation"></a>カスタム操作の通知を有効にするために必要な手順

1. **Retail とコマース > チャネル設定 > POS 設定 > POS > POS 操作**のバックオフィスで新しい操作を作成します。

    > [!NOTE]
    > カスタム操作に 5000 より大きい操作 ID を使用します。
    
2. 通知サービスを拡張します。  通知サービスのスケジューラが実行されると、通知メッセージを取得するために、CRT とリアルタイム トランザクション サービス拡張コードの両方が呼び出されます。

3.  POS の拡張。 POS では、ユーザーが通知をクリックしたときに行われる動作について、POS 操作内のロジックに記述します。 新しい POS 操作の作成方法については、[ボタン グリッド デザイナーを使用して POS 操作を POS レイアウトに追加](add-pos-operations.md) を参照してください。

4. カスタム操作を使用して、バックオフィスの通知サービスをコンフィギュレーションします。 スケジューラを実行する場合、カスタム操作が含まれます。 POS で通知をコンフィギュレーションする方法については、[ボタン グリッド デザイナーを使用して POS 操作を POS レイアウトに追加](../notifications-pos.md) を参照してください。

    POS ユーザーが通知をクリックすると、CRT から返された応答に基づいて、フレームワークは適切な操作を呼び出します。 バックオフィスでコンフィギュレーションされているすべての通知に対して通知サービスが実行され、操作 ID と通知の詳細と共に応答が返されます。 そのため、POS は操作 ID のコンテキストを持つことになり、フレームワークはこれを使用してオペレーションの実装を呼び出します。

> [!NOTE] 
> 通知スケジューラは、CRT とバックオフィスの両方で、新しい通知があるかどうかを確認します。 シナリオに応じて、バックオフィスまたは CRT のみのリアルタイム トランザクション サービスを拡張します。 通知にリアルタイム処理が必要なシナリオでは、バックオフィスのリアルタイム トランザクション サービス メソッドを拡張し、リアルタイム処理が不要な場合には、CRT のみを拡張します。

## <a name="extend-the-notification-service-in-crt"></a>CRT の通知サービスの拡張

CRT の通知サービスを拡張するには、**GetNotificationsExtensionServiceRequest** を上書きし、**GetNotificationsExtensionServiceResponse** を返します。

通知サービスを拡張する方法については、Retail SDK にサンプルが用意されています (**RetailSDK\SampleExtensions\CommerceRuntime\Extensions.NotificationSample**)。
+ **GetNotificationsExtensionServiceRequest** には、操作 ID、スタッフ、およびチャネルが含まれます。 この Retail Headquarters コンフィギュレーションに基づいて、POS はコンフィギュレーションされた各操作に対して通知スケジューラを実行します。
+ **GetNotificationsExtensionServiceResponse** は、応答で通知の詳細エンティティ (**NotificationDetailCollection**) を返し、**GetNotificationsExtensionServiceResponse** を更新して、すべての通知を返します。 これはコレクションなので、複数の通知を返すことができます。

## <a name="notification-details-entity-contains-the-below-property"></a>通知の詳細エンティティには次のプロパティが含まれます。

| プロパティ名          | データ型      | 説明                                                                 |
|------------------------|----------------|---------------------------------------------------------------------------------|
| ActionProperty         | 文字列         | POS 操作に送信するカスタム プロパティ。                                       |
| DisplayText            | 文字列         | 通知ディスプレイ テキスト。                                                       |
| IsLiveContentOnly      | ブール           | 通知がライブ コンテンツのみを対象としているかどうかを示すインジケーター。                    |
| IsNew                  | ブール           | 通知が新しいかどうかを示すインジケーター。                                |
| IsSuccess              | ブール           | 通知が成功したかどうかを示すインジケーター。                           |
| ItemCount              | long           | 通知の数                                                          |
| LastUpdatedDateTime    | DateTimeOffset | アクション プロパティの項目が最後に更新された日時。                   |
| LastUpdatedDateTimeStr | 文字列         | 文字列形式のアクション プロパティの項目が最後に更新された日時。 |

## <a name="detailed-steps"></a>詳細な手順

1. Retail SDK から **Runtime.Extensions.NotificationSample.proj** を開きます (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**)。
2. 標準の名前付け規則に従ってプロジェクトの名前を変更します。
3. プロジェクト内には、**NotificationExtensionService.cs** と呼ばれるクラス ファイルがあります。 ファイルを開きます。
4. **GetNotificationsExtensionServiceRequest** クラスは、カスタム通知を追加するために上書きされます。 **GetNotificationsExtensionServiceRequest** を上書きし、**GetNotificationsExtensionServiceResponse** を返します。
5. 新しいクラスを作成して **GetNotificationsExtensionServiceRequest** を上書きするか、サンプル テンプレートを使用します。 次の手順では、テンプレートが使用されていることを前提としています。
6. **NotificationExtensionService** クラスには、メソッド名 **Process** があります。 このコードは、メソッド内で操作 ID を確認し、操作 ID に基づいて通知の詳細オブジェクトを作成し、通知を追加します。 カスタム操作 ID かどうかを確認し、通知があるかどうかを確認するロジックを作成します。 通知がある場合は、詳細を含む通知オブジェクトを作成し、応答と共に返します。 その後、POS が応答を解析し、通知を表示します。
    > [!NOTE]
    > プロセス メソッド内のサンプルの実装を削除し、カスタム ロジックだけを保持します。

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
                        // when the notification tile is clicked, define the action property as well.
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
7. 変更を完了すると、プロジェクトをビルドし、**\RetailServer\webroot\bin\Ext** に出力ライブラリをドロップします。
8. **CommerceRuntime.Ext.config** に出力ライブラリを登録します。
9. CRT 拡張機能で使用されているのと同じ操作 ID を使用して、POS で新しい操作を作成します。 この例の場合、**5000** です。 5000 より大きい操作 ID を使用します。
    ユーザーが通知タイルをクリックすると、POS フレームワークは使用される操作 ID の操作ハンドラーを呼び出します。 ハンドラー内で、POS ユーザーが通知をクリックしたときに行われる動作について、必要なロジックを追加します。 POS 操作要求、応答、およびハンドラーの作成方法については、 [販売時点管理 (POS) での注文通知の表示](add-POS-operations.md) を参照してください。
    > [!NOTE]
    > 通知の詳細エンティティのアクション プロパティが POS 操作要求に送信され、そのアクション プロパティを使用して通知サービスから POS にカスタム情報が渡されます。
10. [販売時点管理 (POS) での注文通知の表示](../notifications-pos.md) の指示に従って、通知スケジューラをコンフィギュレーションします。

## <a name="validate-the-customization"></a>カスタマイズの検証

1. 拡張 Cloud POS または Modern POS を起動します。
2. POS は、通知スケジューラのコンフィギュレーションに基づいて通知サービスをトリガーします。
3. CRT プロジェクトを w3wp.exe にアタッチして、CRT コードをデバッグします。 このブレークポイントは、通知サービスが POS から呼び出されたときに必ずヒットします。
4. POS で通知を受信したら、通知をクリックします。 POS 操作ハンドラーを呼び出し、ハンドラー内に記述されたカスタムロジックを実行します。
