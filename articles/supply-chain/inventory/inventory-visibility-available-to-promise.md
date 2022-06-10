---
title: Inventory Visibility の手持変更スケジュールと納期回答可能在庫
description: このトピックでは、将来の手持変更をスケジュールし、納期回答可能在庫 (ATP) 数量を計算する方法について説明します。
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7456f87bede7bd0073223fa4762f96f919799e06
ms.sourcegitcommit: 38d97efafb66de298c3f504b83a5c9b822f5a62a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/17/2022
ms.locfileid: "8763256"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Inventory Visibility の手持変更スケジュールと納期回答可能在庫

[!include [banner](../includes/banner.md)]

このトピックでは、*手持在庫変更スケジュール* 機能を設定して、将来の手持在庫変更をスケジュールし、納期回答可能在庫 (ATP) 数量を計算する方法について説明します。 ATP は、使用可能な品目の数量で、次の期間に顧客に約束できます。 この計算を使用すると、注文のフルフィルメント機能を大幅に強化できます。

製造元、小売企業、販売者の多くは、現在の手持在庫状況を把握するだけでなく、他の情報も必要です。 将来の使用可能性に、簡単にすべてアクセスできる必要があります。 この将来の使用可能性には、将来の供給、需要、および ATP が含まれます。

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>機能の有効化と設定

ATP を使用するには、1 つ以上の計算メジャーを設定して ATP 数量を計算する必要があります。 また、この機能を有効にして、Microsoft Power Apps で ATP 設定を構成する必要があります。

### <a name="set-up-calculated-measures-for-atp-quantities"></a>ATP 数量に対する計算メジャーの設定

*ATP 計算メジャー* は、現在使用可能な手持在庫数量を把握するのに通常使用される、事前に定義された計算メジャーです。 *供給数量* は、モディファイア タイプが *加算* の現物メジャーの数量の合計であり、*需要数量* は、モディファイア タイプが *減算* の現物メジャーの数量の合計です。

複数の計算メジャーを追加して複数の ATP 数量を計算することができます。 ただし、すべての ATP 計算メジャーの異なる現物メジャーの合計数は、9 未満である必要があります。

> [!IMPORTANT]
> 計算メジャーは、現物メジャーの構成です。 その式には、計算メジャーではなく、重複しない現物メジャーのみを含めることができます。

たとえば、次の計算メジャーを設定します。

**手持使用可能在庫** = (*現物在庫* + *手持在庫* + *制限なし* + *品質検査* + *入庫*) – (*引当済現物* + *仮引当現物* + *出庫*)

SUM (*現物在庫* + *手持在庫* + *制限なし* + *品質検査* + *入庫*) は供給を表し、SUM (*引当済現物* + *仮引当現物* + *出庫*) は需要を表します。 したがって、計算メジャーは次のようになります。

**手持可能在庫** = *供給* – *需要*

別の計算メジャーを追加して、**On-hand-physical** ATP 数量を計算できます。

**On-hand-physical** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

この 2 つの ATP 計算メジャーには、次の 8 つの異なる現物メジャーがあります: *PhysicalInvent*、*OnHand*、*Unrestricted*、*QualityInspection*、*Inbound*、*ReservPhysical*、*SoftReservePhysical*、*Outbound*。

計算メジャーの詳細については、[計算メジャー](inventory-visibility-configuration.md#calculated-measures)を参照してください。

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>手持在庫変更スケジュール機能を有効にして ATP 設定を構成する

次の手順に従って、Power Apps で *手持在庫変更スケジュール* 機能を有効にして ATP 設定を構成します。

1. Power Apps にサインインして、[在庫視覚化] を開きます。
1. **構成** ページを開きます。
1. **機能管理** タブで、*OnhandChangeSchedule* 機能を有効にします。
1. **ATP 設定** タブを選択します。
1. 在庫視覚化を照会すると、ここに追加した各 ATP 計算メジャーを含む結果が得られます。 **追加** を選択して、ATP の新しい計算メジャーを追加します。
1. 次のフィールドを設定します。

    - **データ ソース** – 計算メジャーに関連付けられているデータ ソースを選択します。
    - **計算メジャー** : 選択したデータ ソースに関連付けられた計算メジャーを選択し、現在使用可能な在庫数量を探す場合に使用します。
    - **期間のスケジュール設定** – 選択した計算メジャーが使用されている場合に、ユーザーがスケジュール済みの手持在庫変更を表示または提出できる日数を入力します。 在庫情報のクエリを実行するユーザーは、現在の日付を開始日として、この期間のそれぞれ日の手持在庫数量、スケジュール済み手持在庫変更、および ATP を取得します。 1 から 7 までの整数を選択します。

    > [!IMPORTANT]
    > スケジュール期間には現在の日付が含まれます。 したがって、ユーザーは、現在の日付 (変更が送信された日) から (スケジュール期間 – 1) 将来の任意の日付に実行される手持在庫変更をスケジュールできます。

1. **保存** を選択します。
1. 手順 5 から 7 を繰り返して、ATP に必要なすべての計算メジャーを追加します。
1. 必要なすべての設定の構成が完了したら、**構成の更新** を選択します。

詳細については、[構成の完了と更新](inventory-visibility-configuration.md) を参照してください。

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>手持在庫変更ケジュールと ATP 計算の機能について

*手持在庫変更スケジュール* は、スケジュール済み手持在庫変更の予定日と数量を設定します。 **スケジュール期間** 設定 ([機能の有効化と設定](#setup) セクションを参照) で定義されている期間内の日付である場合のみ、手持在庫変更スケジュールを在庫視覚化に送信できます。。 在庫情報のクエリを実行するユーザーは、この期間のそれぞれ日の手持在庫数量、スケジュール済み手持在庫変更、および ATP を取得します。

スケジュール済みの変更は、最初はコミットされていないので、システムの実際の手持在庫数量には影響しません。 変更をコミットするには、実際に使用可能な手持在庫の数量を更新する *手持在庫変更イベント* を送信する必要があります。 その後、負の数量に一致する手持在庫変更スケジュールを送信し、スケジュール済みの変更を元に戻す必要があります。

たとえば、自転車を 10 台注文して、明日到着する予定だとします。 この場合は、入庫数量が 10 台で、日付が明日である手持在庫変更スケジュールを送信します。 注文した自転車が翌日に到着したら、その自転車を現物手持在庫に追加します。 その後、変更をシステムにコミットして実際の手持在庫数量を更新する必要があります。 変更をコミットするには、入庫数量が 10 の手持在庫変更イベントを送信します。 その後、入庫数量が -10 の手持在庫変更スケジュールを送信し、スケジュール済みの変更を元に戻します。

手持在庫数量と ATP 数量の在庫可視性のクエリを実行すると、スケジュール期間のそれぞれの日に関する次の情報が返されます。

- **日付** – 結果を適用する日付。 タイム ゾーンは協定世界時 (UTC) です。
- **手持在庫数量** – 指定した日付の実際の手持在庫数量。 この計算は、在庫可視性に対して構成されている ATP 計算メジャーに従って実行されます。
- **スケジュール済み供給** – 指定された日付の時点で、すぐに消費したり出荷したりするために物理的にはまだ入手できない、スケジュール済み入庫数量の合計。
- **スケジュール済み需要** – 指定された日付の時点で、消費または出荷されていない、スケジュール済みのすべての出荷数量の合計。
- **ATP 数量** – 指定された日付からスケジュール期間の終了日まで、入手可能な予想手持在庫の最低数量。 この数量には、調節されたすべてのスケジュール済み数量が含まれます。 これは、現在の日付での配送または消費を約束できる最大数量です。

たとえば、現在の日付が 2022 年 2 月 1 日で、スケジュール期間が 7 の場合、ユーザーは 2022 年 2 月 1 日から 2 月 7 日までに行われる予定のスケジュール済み手持在庫変更を送信できます。 この場合、たとえば、2 月 3 日の ATP 数量は、その日の手持在庫数量と 2 月 3 日から 2 月 7 日のスケジュール済みの数量に基づいて計算されます。

## <a name="example"></a>例

次の例では、一連のスケジュール済み数量の変更が、在庫可視性レポートの手持在庫数量および ATP 数量にどのように影響するかを説明します。 また、スケジュール済みの変更をコミットする方法、コミットされたスケジュールの変更が結果に与える影響、スケジュール済みの変更をコミットしない場合に起こりうる問題などについても説明します。

この例の結果は、*予想手持在庫* 値を表示します。 この値には、説明目的でスケジュール済み更新もすべて含まれていますが、在庫可視性のクエリを実行する際には報告されません。

1. 次の設定は、Power Apps の **ATP 設定** ページでシステムに構成されます。

    - **ATP 計算メジャー** – *手持在庫* という名前の計算メジャーがあります。 *手持在庫 = 供給 – 需要* と計算されます。 ここでそのメジャーを選択します。
    - **スケジュール期間** – *7* を選択します。

1. 次の条件も適用されます。

    - 現在の日付は 2022 年 2 月 1 日です。
    - 現在の手持在庫数量が 20 であるとします。

1. 現在の日付 (2022 年 2 月 1 日) に対して、在庫可視性にスケジュール済み需要数量 3 を送信します。 したがって、予想手持在庫数量は 17 品目になります。 次の表に、この結果を示します。

    | 日付 | 手持在庫 | スケジュール済み供給 | スケジュール済み需要 | 予想手持在庫 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. 現在の日付 (2022 年 2 月 1 日) に、2022 年 2 月 3 日に対する予想供給数量を 10 として送信します。 次の表に、この結果を示します。

    | 日付 | 手持在庫 | スケジュール済み供給 | スケジュール済み需要 | 予想手持在庫 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. 現在の日付 (2022 年 2 月 1 日) に、次のスケジュール済み数量変更を送信します。

    - 2022 年 2 月 4 日の需要数量が 15
    - 2022 年 2 月 5 日の供給数量が 1
    - 2022 年 2 月 6 日の供給数量が 3

    次の表に、この結果を示します。

    | 日付 | 手持在庫 | スケジュール済み供給 | スケジュール済み需要 | 予想手持在庫 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | 15 | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. 現在の日付 (2022 年 2 月 1 日) に、スケジュール済み需要数量 3 を出荷します。 したがって、実際の手持在庫数量に反映させるためには、この変更をコミットする必要があります。 変更をコミットするには、出庫数量が 3 の手持在庫変更イベントを送信します。 その後、出庫数量が -3 の手持在庫変更スケジュールを送信し、スケジュール済みの変更を元に戻します。 次の表に、この結果を示します。

    | 日付 | 手持在庫 | スケジュール済み供給 | スケジュール済み需要 | 予想手持在庫 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. 翌日 (2022 年 2 月 2 日) に、スケジュール期間は 1 日後にずれます。 次の表に、この結果を示します。

    | 日付 | 手持在庫 | スケジュール済み供給 | スケジュール済み需要 | 予想手持在庫 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. しかし、2 日後 (2022 年 2 月 4 日)、2 月 3 日に予定されていた供給数量 10 がまだ到着していません。 次の表に、この結果を示します。

    | 日付 | 手持在庫 | スケジュール済み供給 | スケジュール済み需要 | 予想手持在庫 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | 15 | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    ご覧のように、スケジュール済み (確定されていない) 手持在庫変更は、実際の在庫数量には影響されません。

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>API を使用した変更スケジュール、変更イベント、および ATP クエリの送信

次のアプリケーション プログラミング インターフェイス (API) URL を使用して、手持在庫変更スケジュール、変更イベント、およびクエリを送信できます。

| パス | メソッド | Description |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | スケジュール済み手持在庫変更を 1 つ作成します。 |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | 複数のスケジュール済み手持在庫変更を作成します。 |
| `/api/environment/{environmentId}/onhand` | `POST` | 手持在庫変更のイベントを 1 つ作成します。 |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | 複数の変更イベントを作成します。 |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | `POST` メソッドを使用してクエリを実行します。 |
| `/api/environment/{environmentId}/onhand` | `GET` | `GET` メソッドを使用してクエリを実行します。 |

詳細については、[Inventory Visibility のパブリック API](inventory-visibility-api.md) を参照してください。

### <a name="create-one-on-hand-change-schedule"></a>手持変更スケジュールを 1 つ作成する

手持変更スケジュールは、関連する Inventory Visibility サービス URL に `POST` 要求を送信することで作成されます ([変更スケジュールの送信、変更イベント、および API を使用した ATP クエリ](#api-urls) セクションを参照)。 一括要求を送信することもできます。

手持変更スケジュールは、予定日が現在の日付と現在の予定期間の終了日の間にある場合にのみ作成できます。 datetime 形式は、*年-月-日* (例: **2022-02-01**)。 time 形式は、その日についてのみ正確である必要があります。

この API により、1 つの手持変更スケジュールが作成されます。

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

次の例は、`dimensionDataSource` なしのサンプル本文コンテンツを示しています。

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>複数の手持変更スケジュールを作成する

この API で、同時に複数の記録を作成できます。 この API とシングル イベント API の違いは、`Path` 値と `Body` 値のみです。 この API では、`Body` は記録の配列を提供します。 レコードの最大数は 512 です。 したがって、手持変更スケジュールの一括 API では、一度に最大 512 件のスケジュール済の変更をサポートできます。

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

次の例は、サンプル本文コンテンツを示しています。

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a> 手持在庫変更のイベントの作成

手持在庫変更イベントは、該当する在庫可視性サービスの URL に `POST` 要求を送信することで作成します ([変更スケジュールの送信、変更イベント、および API を使用した ATP クエリ](#api-urls) セクションを参照)。 一括要求を送信することもできます。

> [!NOTE]
> 手持在庫変更のイベントは、ATP 機能に固有ではありませんが、標準の在庫可視性 API の一部です。 この例が含まれているのは、ATP を使用して作業する場合にイベントが関連するからです。 手持在庫変更イベントは、手持在庫変更予約と似ていますが、イベント メッセージは別の API URL に送信される必要があり、イベントは、メッセージ本文で `quantityByDate` の代わりに `quantities` を使用します。 手持在庫イベントおよび在庫可視性 API のその他の機能に関する詳細については、[在庫可視性パブリック API](inventory-visibility-api.md#create-one-onhand-change-event) を参照してください。

次の例は、1 回の手持在庫イベントを含む要求本文を示します。

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>スケジュール済みの手持在庫変更および ATP 結果のクエリを実行する

スケジュール済み手持在庫変更および ATP の結果のクエリを実行するには、`POST` 要求または `GET` 要求を該当する API URL に送信します ([変更スケジュールの送信、イベントの変更、APIを使用した ATP クエリ](#api-urls) セクションを参照)。

要求で、スケジュール済みの手持在庫変更および ATP 結果のクエリを実行する場合は、`QueryATP` を *true* に設定します。

- `GET` メソッドを使用して要求を送信する場合は、URL でこのパラメータを設定します。
- `POST` メソッドを使用して要求を送信する場合は、要求本文でこのパラメータを設定します。

> [!NOTE]
> 要求本文で、`returnNegative` パラメーターの設定が *true* か *false* かに関係なく、スケジュール済みの手持在庫変更や ATP 結果のクエリを実行するときに、結果に負の値が含まれます。 これらの負の値が含まれるのは、需要注文のみがスケジュールされている場合、または供給数量が需要数量よりも少ない場合に、スケジュール済み手持在庫変更の数量が負になるからです。 負の値が含まれていない場合は、結果は複雑になります。 このオプション、および他のタイプのクエリに関する情報は、[在庫可視性パブリック API](inventory-visibility-api.md#query-with-post-method) を参照してください。

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

次の例では、`POST` メソッドを使用して在庫可視性に送信できる要求本文を作成する方法を示します。

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>GET メソッドの例

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

次の例では、要求 URL を `GET` 要求として作成する方法を説明します。

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

この `GET` 要求の結果は、前の例で使用した `POST` 要求の結果とまったく同じです。

### <a name="query-result-example"></a>結果の例のクエリを実行する

以前のクエリの両方の例で、次の返信が作成される場合があります。 たとえば、システムは次の設定で構成されています。

- **ATP 計算メジャー:** *iv.onhand = pos.inbound – pos.outbound*
- **スケジュールの期間:** *7*

次は、返信本文の例です。

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
