---
title: Inventory Visibility の公開 API
description: この記事では、Inventory Visibility によって提供されるパブリック API について説明します。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762837"
---
# <a name="inventory-visibility-public-apis"></a>Inventory Visibility の公開 API

[!include [banner](../includes/banner.md)]

この記事では、Inventory Visibility によって提供されるパブリック API について説明します。

Inventory Visibility アドインのパブリック REST API は、特定の統合エンドポイントを複数提供します。 次の 4 つの主要な相互作用タイプをサポートします。

- 外部システムから、手持在庫の変更をアドインに転記する
- 外部システムから、アドインの手持在庫数量を設定または上書きする
- 外部システムから、予約イベントをアドインに転記する
- 外部システムから現在の手持在庫数量を問い合わせる

次のテーブルに、現在使用可能な API を示します。

| パス | メソッド | 説明 |
|---|---|---|
| /api/environment/{environmentId}/onhand | 転記 | [1 つの手持在庫変更のイベントの作成](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | 転記 | [複数の変更イベントの作成](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | 転記 | [手持在庫数量の設定/上書き](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | 投稿 | [1 つの仮引当イベントの作成](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | 投稿 | [複数の仮引当イベントの作成](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | 投稿 | [1 つの仮引当イベントの取り消し](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | 投稿 | [複数の仮引当イベントの取り消し](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | 転記 | [1 つのスケジュール済み手持在庫変更の作成](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | 投稿 | [日付を指定した複数の手持在庫変更の作成](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | 投稿 | [POST メソッドを使用したクエリ](#query-with-post-method) (推奨) |
| /api/environment/{environmentId}/onhand | 取得 | [取得メソッドを使用したクエリ](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | 投稿 | [POST メソッドを使用した正確なクエリ](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | 投稿 | [1 つの配賦イベントの作成](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | 転記 | [1 つの未配賦イベントの作成](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | 転記 | [1 つの再配賦イベントの作成](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | 転記 | [1 つの消費イベントの作成](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | 転記 | [クエリの配賦結果](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> パスの {environmentId} 部分は Microsoft Dynamics Lifecycle Services の環境 ID です。
> 
> バルク API では、要求ごとに最大 512 件のレコードを返します。

Microsoft では、すぐに利用できる *Postman* 要求コレクションを提供しています。 次の共有リンクを使用して、*Postman* ソフトウェアにこのコレクションをインポートできます: <https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>。

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>Lifecycle Services 環境に従ってエンドポイントを検索する

Inventory Visibility マイクロサービスは、複数の地域および複数のリージョンの Microsoft Azure Service Fabric に配置されます。 対応する地域およびリージョンに自動的に要求をリダイレクトできる中央のエンドポイントは現在存在しません。 したがって、次のパターンを使用して情報を URL に作成する必要があります。

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

このリージョンの短縮名は Lifecycle Services 環境で確認できます。 次のテーブルに、現在使用可能なリージョンを示します。

| Azure リージョン        | リージョンの短縮名 |
| ------------------- | ----------------- |
| オーストラリア東部      | eau               |
| オーストラリア南東部 | seau              |
| カナダ中部      | cca               |
| カナダ東部         | eca               |
| 北ヨーロッパ        | neu               |
| 西ヨーロッパ         | weu               |
| 米国東部             | eus               |
| 米国西部             | wus               |
| イギリス南部            | suk               |
| イギリス西部             | wuk               |
| 東日本          | ejp               |
| 西日本          | wjp               |
| インド中部       | cin               |
| インド南部         | sin               |
| スイス北部   | nch               |
| スイス西部    | wch               |
| フランス南部        | sfr               |
| 東アジア           | eas               |
| 東南アジア     | seas              |
| アラブ首長国連邦北部           | nae               |
| ノルウェー東部         | eno               |
| ノルウェー西部         | wno               |
| 南アフリカ西部   | wza               |
| 南アフリカ北部  | nza               |

島番号は、Lifecycle Services 環境が Service Fabric に配置されている場所です。 現在、この情報をユーザー側から取得する方法はありません。

Microsoftでは、Power Apps にユーザー インターフェイス (UI) を構築し、マイクロサービスの完全なエンドポイントを取得できます。 詳細については、[サービス エンドポイントの検索](inventory-visibility-configuration.md#get-service-endpoint) を参照してください。

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>認証

プラットフォーム セキュリティ トークンは、Inventory Visibility パブリック API を呼び出すために使用されます。 したがって、Azure AD アプリケーションを使用して *Azure Active Directory (Azure AD) トークン* を生成する必要があります。 その後、この Azure AD トークンを使用して、セキュリティ サービスから *アクセス トークン* を取得する必要があります。

Microsoft では、すぐに利用できる *Postman* get トークン コレクションを提供しています。 次の共有リンクを使用して、*Postman* ソフトウェアにこのコレクションをインポートできます: <https://www.getpostman.com/collections/496645018f96b3f0455e>。

セキュリティ サービス トークンを取得するには、次の手順を行います。

1. Azure ポータルにサインインし、このサインインを使用して Dynamics 365 Supply Chain Management アプリの `clientId` と `clientSecret` の値を検索します。
1. 次のプロパティを持つ HTTP 要求を送信することにより、Azure AD トークン (`aadToken`) をフェッチします。

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **メソッド:** `GET`
    - **本文の内容 (フォーム データ):**

        | キー           | 先頭値                                            |
        | ------------- | -------------------------------------------------|
        | クライアント ID     | ${aadAppId}                                      |
        | クライアント シークレット | ${aadAppSecret}                                  |
        | 付与タイプ    | client_credentials                               |
        | scope         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    応答で Azure AD トークン (`aadToken`) を取得する必要があります。 これは次の例に類似しているはずです。

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. 次の例に似た JavaScript Object Notation (JSON) 要求を作成します。

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type": "aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope": "https://inventoryservice.operations365.dynamics.com/.default",
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    次のポイントに注意します。

    - `client_assertion` 値は、前の手順で受け取った Azure AD トークン (`aadToken`) である必要があります。
    - この `context` 値は、アドインを配置する Lifecycle Services 環境 ID である必要があります。
    - 例に示すように、他のすべての値を設定します。

1. 次のプロパティを持つ HTTP 要求を送信することにより、アクセス トークン (`access_token`) を取得します。

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **メソッド:** `POST`
    - **HTT Pヘッダー:** API バージョンを含めます。 (キーは `Api-Version` で、値は `1.0` です。)
    - **本文の内容:** 前の手順で作成した JSON 要求を含めます。

    応答でアクセス トークン (`access_token`) を取得する必要があります。 Inventory Visibility API を呼び出すためのベアラー トークンとしてこのトークンを使用する必要があります。 次に例を示します。

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

> [!IMPORTANT]
> *Postman* 要求コレクションを使用してInventory Visibility パブリック API を呼び出す場合は、各要求に対してベアラー トークンを追加する必要があります。 ベアラー トークンを見つけるには、要求 URL の下の **認証** タブを選択し、**ベアラー トークン** のタイプを選択して、最後の手順で取得したアクセス トークンをコピーします。 この記事の後半セクションでは、最後の手順で取得したトークンを表すために `$access_token` を使用します。

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a> 手持在庫変更のイベントの作成

2 つの API を使用して、手持在庫変更のイベントを作成できます。

- 1 つの記録の作成: `/api/environment/{environmentId}/onhand`
- 複数の記録の作成: `/api/environment/{environmentId}/onhand/bulk`

次のテーブルでは、JSON 本文の各フィールドの意味が要約されています。

| フィールド ID | Description |
|---|---|
| `id` | 特定の変更イベントの固有 ID。 サービス障害で再転記が発生した場合、この ID を使用してシステム上で同じイベントが 2 回カウントされることを予防します。 |
| `organizationId` | イベントにリンクされている組織の ID。 この値は、Supply Chain Management での組織またはデータ領域 ID にマップされます。 |
| `productId` | 製品の識別子。 |
| `quantities` | 手持在庫の数量の変更が必要な数量。 たとえば、新たに帳簿を 10 つ追加すると、この値は `quantities:{ shelf:{ received: 10 }}` になります。 棚から 3 つの帳簿が削除される場合、または販売される場合、この値は `quantities:{ shelf:{ sold: 3 }}` になります。 |
| `dimensionDataSource` | イベントやクエリ変更の転記で使用する分析コードのデータ ソース。 データ ソースを指定する場合は、指定されたデータ ソースのカスタム分析コードを使用できます。 Inventory Visibility は、分析コードの構成を使用して、カスタム分析コードを既定の標準分析コードにマップできます。 `dimensionDataSource` の値が指定されていない場合は、クエリで標準の[基準分析コード](inventory-visibility-configuration.md#data-source-configuration-dimension) のみを使用できます。 |
| `dimensions` | 動的なキーと値のペア。 値は Supply Chain Management の分析コードの一部にマップされます。 ただし、カスタム分析コード (*ソース* など)を追加して、イベントが Supply Chain Management から取得されたか、または外部システムから取得されたかどうかを示したりすることもできます。 |

> [!NOTE]
> `siteId` および `locationId` パラメーターは、[パーティションの構成](inventory-visibility-configuration.md#partition-configuration)を構築します。 そのため、手持変更イベントの作成、手持数量の設定または上書き、または引当イベントの作成を行う際は、これらの情報を分析コードで指定する必要があります。

次のサブセクションでは、これらの API の使用方法を示す例を示します。

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a> 1 つの手持在庫変更のイベントの作成

この API により、1 つの手持在庫変更のイベントが作成されます。

```txt
Path:
    /api/environment/{environmentId}/onhand
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
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

次の例は、サンプル本文コンテンツを示しています。 この例では、会社には店舗トランザクションを処理する販売時点管理 (POS) システムがあるため、在庫が変更されます。 顧客が赤い T シャツを店舗に返品してきました。 変更を反映するには、*T シャツ* の商品に対して 1 つの変更イベントを転記します。 このイベントにより、*T シャツ* 製品の数量が 1 つ増加します。

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

次の例は、`dimensionDataSource` なしのサンプル本文コンテンツを示しています。 この場合、`dimensions` は [基準分析コード](inventory-visibility-configuration.md#data-source-configuration-dimension)になります。 `dimensionDataSource` が設定されている場合、`dimensions` はデータ ソース分析コードまたは基本分析コードのいずれかになります。

```json
{
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a> 複数の変更イベントの作成

この API は、[1 つのイベント API](#create-one-onhand-change-event) と同じ方法で変更イベントを作成できます。 唯一の違いは、この API で同時に複数のレコードを作成できる点です。 したがって、`Path` と `Body` の値は異なります。 この API では、`Body` は記録の配列を提供します。 レコードの最大数は 512 です。 したがって、手持在庫変更の一括 API では、一度に最大 512 件の変更イベントをサポートできます。 

たとえば、小売店舗 POS コンピューターで次の 2 つのトランザクションが処理されたとします:

- 赤い T シャツ 1 枚の返品依頼 1 件
- 黒の T シャツ 3 枚の販売トランザクション 1 件

この場合、1 つの API 呼び出しに両方の在庫更新を含めることができます。

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a> 手持在庫数量の設定/上書き

*手持在庫数量の設定* API は、指定された製品の現在のデータを上書きします。 通常、この機能は在庫棚卸の更新を実行するために使用されます。 たとえば、ある店舗では、日々の在庫棚卸で、赤い T シャツの実際の手持在庫が 100 枚であることが分かったとします。 したがって、POS の入荷数量は、以前の数量にかかわらず、100 に更新する必要があります。 この API を使用すると、既存の値を上書きできます。

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
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
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

次の例は、サンプル本文コンテンツを示しています。 この API の動作は、この記事の前半の [手持在庫変更のイベントの作成](#create-onhand-change-event) セクションで説明されている API の動作とは異なります。 このサンプルでは、*T シャツ* 製品の数量が 1 つに設定されます。

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>予約イベントの作成

*予約* API を使用するには、予約機能をオンにして、予約の構成を完了する必要があります。 詳細 (データフローおよびサンプル シナリオを含む) については、[引当の構成 (オプション)](inventory-visibility-configuration.md#reservation-configuration) を参照してください。

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a> 1 つの予約イベントの作成

引当は別のデータ ソース設定に対して作成できます。 このタイプの引当を構成するには、最初に `dimensionDataSource` パラメーターでデータ ソースを指定します。 次に、`dimensions` パラメーターで、ターゲット データ ソースの分析コード設定に従って分析コードを指定します。

引当 API を呼び出す際に、要求本文のブール値 `ifCheckAvailForReserv` パラメーターを指定することで、引当の検証を制御できます。 `True` という値は検証が必要であることを意味するのに対し、`False` という値は検証が必要ないことを意味します。 既定値は [`True`] です。

予約の取り消しや、指定した引当在庫数量を解除する場合は、数量を負の値に設定し、`ifCheckAvailForReserv` パラメーターを `False` に設定して検証をスキップします。 また、同様のことを行う専用の取り消し API も用意されています。 この 2 つの API の違いは、呼び方の違いだけです。 *予約取り消し* API で `reservationId` を使用すると、特定の予約イベントを取り消すことが簡単にできます。 詳細については、[1 件の引当イベントを取り消す](#reverse-reservation-events) セクションを参照してください。

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
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
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

次の例は、サンプル本文コンテンツを示しています。

```json
{
    "id": "reserve-0",
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

次の例では、正常な応答例を示しています。

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a> 複数の予約イベントの作成

この API は、[1 つのイベント API](#create-reservation-events) の一括バージョンです。

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
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
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="reverse-reservation-events"></a>予約イベントの取り消し

*取り消し* API は、[*取り消し*](#create-reservation-events) イベントの逆の操作として機能します。 `reservationId` で指定された予約イベントを取り消したり、予約数量を減らしたりする方法を提供します。

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>予約イベントの取り消し

予約が作成されると、応答の本文に `reservationId` が含まれます。 予約をキャンセルする場合は、同じ `reservationId` を指定し、予約 API 呼び出しに使用したのと同じ `organizationId` と `dimensions` を含める必要があります。 最後に、前回の予約から解放する個数を表す `OffsetQty` 値を指定します。 予約は、指定された `OffsetQty` によって、完全または部分的に取り消すことができます。 たとえば、*100* 個の商品を予約した場合、`OffsetQty: 10` を指定すると、最初の予約量の *10* 個を予約解除できます。

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

次のコードは、本文コンテンツの例を示しています。

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

次のコードは、成功した応答分の例を示しています。

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> 応答本文では、`OffsetQty` が予約数量以下の場合、`processingStatus` には "*成功*"、`totalInvalidOffsetQtyByReservId` には *0* が格納されます。
>
> `OffsetQty` が予約の数量より大きい場合、`processingStatus` は "*partialSuccess*"、`totalInvalidOffsetQtyByReservId` は `OffsetQty` と予約金額との差となります。
>
>たとえば、予約の数量が *10* で、`OffsetQty` の値が *12* であれば、`totalInvalidOffsetQtyByReservId` は *2* になります。

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>複数の予約イベントの取り消し

この API は、[1 つのイベント API](#reverse-one-reservation-event) の一括バージョンです。

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>手持在庫をクエリする

*手持在庫をクエリする* API を使用して、製品の手持在庫データを取り込むことができます。 この API は、eコマースの Web サイトで製品の在庫レベルを確認する場合や、地域全体および近くの店舗や倉庫で製品の在庫状況を確認する場合など、在庫を知る必要があるときにいつでも使用できます。 現在、この API は、最大 5000 個の個別アイテムを `productID` 値で照会することをサポートしています。 各クエリには、複数の `siteID` と `locationID` の値を指定することもできます。 上限は以下の式で定義されます:

*NumOf(SiteID) \* NumOf(LocationID) <= 100*。

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a> 転記メソッドを使用したクエリ

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

この要求の本文では、`dimensionDataSource` は引き続きオプションのパラメーターとなります。 設定をしていない場合、`filters` が *基本分析コード* として扱われます。 `filters` には `organizationId`、`productId`、`siteId`、`locationId`の 4 つの必須フィールドがあります。

- `organizationId` には 1 つの値だけが含まれる必要がありますが、それはまだ配列になっています。
- `productId` には 1 つ以上の値が含まれます。 空の配列であれば、すべての製品が返されます。
- `siteId` と `locationId` は、Inventory Visibility でのパーティション分割に使用されます。 *手持在庫をクエリする* 要求では、複数の `siteId` と `locationId` の値を指定できます。 現在のリリースでは、`siteId` と `locationId` の両方の値を指定する必要があります。

`groupByValues` パラメーターを使用して、インデックス作成の設定に従うことをお勧めします。 詳細については、[製品インデックス階層の構成](./inventory-visibility-configuration.md#index-configuration)を参照してください。

`returnNegative` パラメーターは、結果に負のエントリが含まれるかどうかを制御します。

> [!NOTE]
> 手持在庫変更スケジュールおよび納期回答可能在庫 (ATP) 機能を有効にした場合は、クエリ結果に ATP 情報を含めるかどうかを制御する `QueryATP` ブール値パラメーターをクエリに含めることもできます。 詳細と例については、[Inventory Visibility の手持変更スケジュールと納期回答可能在庫](inventory-visibility-available-to-promise.md) を参照してください。

次の例は、サンプル本文コンテンツを示しています。 複数の場所 (倉庫) から手持在庫を照会できることが示されています。

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

次の例では、特定のサイトおよび場所にあるすべての製品をクエリする方法を示します。

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a> 取得メソッドを使用したクエリ

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

URL 所得のサンプルは次のとおりです。 この取得要求は、以前に提供された転記サンプルとまったく同じです。

```txt
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>手持在庫の正確なクエリ

手持在庫の正確なクエリは通常の手持在庫クエリに似てますが、サイトと場所の間でマッピング階層を指定できます。 たとえば、次の 2 つのサイトがあるとします:

- サイト 1、場所 A にマッピング
- サイト 2、場所 B にマッピング

通常の手持在庫クエリの場合、`"siteId": ["1","2"]` および `"locationId": ["A","B"]` を指定すると、Inventory Visibility は次のサイトと場所の結果を自動的にクエリします。

- サイト 1、場所 A
- サイト 1、場所 B
- サイト 2、場所 A
- サイト 2、場所 B

このように、通常の手持在庫クエリでは、場所 A がサイト 1 にのみ存在し、場所 B がサイト 2 にのみ存在することを認識しません。 そのため、冗長なクエリになります。 この階層マッピングに対応するするために、手持在庫の正確なクエリを使用し、クエリ本文で場所のマッピングを指定できます。 この場合、サイト 1、場所 A と、サイト 2、場所 B に対してのみクエリして、結果を受け取ります。

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>POST メソッドを使用した正確なクエリ

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

この要求の本文では、`dimensionDataSource` はオプションのパラメーターとなります。 設定をしていない場合、`filters` の `dimensions` が *基本分析コード* として扱われます。 `filters` には `organizationId`、`productId`、`dimensions`、`values`の 4 つの必須フィールドがあります。

- `organizationId` には 1 つの値だけが含まれる必要がありますが、それはまだ配列になっています。
- `productId` には 1 つ以上の値が含まれます。 空の配列であれば、すべての製品が返されます。
- `dimensions` 配列で、`siteId` と `locationId` が必要ですが、任意の順序で他の要素と一緒に表示できます。
- `values` には、`dimensions` に対応する値の 1 つ以上の異なる組み合を含めることができます。

`filters` の `dimensions` は自動的に `groupByValues` に追加されます。

`returnNegative` パラメーターは、結果に負のエントリが含まれるかどうかを制御します。

次の例は、サンプル本文コンテンツを示しています。

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

次の例では、複数のサイトと場所にあるすべての製品をクエリする方法を示します。

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>納期回答可能在庫

Inventory Visibility を設定すると、今後の手持在庫変更をスケジュールし、ATP 数量を計算できます。 ATP は、使用可能な品目の数量で、次の期間に顧客に約束できます。 ATP 計算を使用すると、注文のフルフィルメント機能を大幅に強化できます。 この機能を有効にする方法、および機能が有効化された後に API で Inventory Visibility と対話する方法については、[Inventory Visibility の手持変更スケジュールと納期回答可能在庫](inventory-visibility-available-to-promise.md#api-urls) を参照してください。

## <a name="allocation"></a>割り当て

配賦関連 API は、[Inventory Visibility の配賦](inventory-visibility-allocation.md#using-allocation-api) に配置されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
