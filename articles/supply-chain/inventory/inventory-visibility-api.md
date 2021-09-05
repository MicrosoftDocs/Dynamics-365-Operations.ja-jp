---
title: 在庫の可視化パブリック API
description: このトピックでは、在庫の可視化によって提供されるパブリック API について説明します。
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0aca5838ff6d7c9c4d881698be1e2da2e0e1c02e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343635"
---
# <a name="inventory-visibility-public-apis"></a>在庫の可視化パブリック API

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

このトピックでは、在庫の可視化によって提供されるパブリック API について説明します。

在庫の視覚化アドインのパブリック REST API は、特定の統合エンドポイントを複数提供します。 次の 4 つの主要な相互作用タイプをサポートします。

- 外部システムから、手持在庫の変更をアドインに転記する
- 外部システムから、アドインの手持在庫数量を設定または上書きする
- 外部システムから、予約イベントをアドインに転記する
- 外部システムから現在の手持在庫数量を問い合わせる

次のテーブルに、現在使用可能な API を示します。

| パス | メソッド | 説明 |
|---|---|---|
| /api/environment/{environmentId}/onhand | 転記 | [1 つの手持在庫変更のイベントの作成](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | 転記 | [複数の変更イベントの作成](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | 転記 | [手持在庫数量の設定/上書き](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | 転記 | [1 つの予約イベントの作成](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | 転記 | [複数の予約イベントの作成](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | 取得 | [転記メソッドを使用したクエリ](#query-with-post-method) |
| /api/environment/{environmentId}/onhand/indexquery | 転記 | [取得メソッドを使用したクエリ](#query-with-get-method) |

Microsoft では、すぐに利用できる *Postman* 要求コレクションを提供しています。 次の共有リンクを使用して、*Postman* ソフトウェアにこのコレクションをインポートできます: <https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>。

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>Lifecycle Services 環境に従ってエンドポイントを検索する

在庫の可視化のマイクロサービスは、複数の地域および複数のリージョンの Microsoft Azure Service Fabric に配置されます。 対応する地域およびリージョンに自動的に要求をリダイレクトできる中央のエンドポイントは現在存在しません。 したがって、次のパターンを使用して情報を URL に作成する必要があります。

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

このリージョンの短縮名は Microsoft Dynamics Lifecycle Services (LCS) 環境で確認できます。 次のテーブルに、現在使用可能なリージョンを示します。

| Azure リージョン | リージョンの短縮名 |
|---|---|
| オーストラリア東部 | eau |
| オーストラリア南東部 | seau |
| カナダ中部 | cca |
| カナダ東部 | eca |
| 北ヨーロッパ | neu |
| 西ヨーロッパ | weu |
| 米国東部 | eus |
| 米国西部 | wus |
| イギリス南部 | suk |
| イギリス西部 | wuk |

島番号は、LCS 環境が Service Fabric に配置されている場所です。 現在、この情報をユーザー側から取得する方法はありません。

Microsoftでは、Power Apps にユーザー インターフェイス (UI) を構築し、マイクロサービスの完全なエンドポイントを取得できます。 詳細については、[サービス エンドポイントの検索](inventory-visibility-power-platform.md#get-service-endpoint) を参照してください。

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>認証

プラットフォーム セキュリティ トークンは、在庫の視覚化パブリック API を呼び出すために使用されます。 したがって、Azure AD アプリケーションを使用して _Azure Active Directory (Azure AD) トークン_ を生成する必要があります。 その後、この Azure AD トークンを使用して、セキュリティ サービスから _アクセス トークン_ を取得する必要があります。

セキュリティ サービス トークンを取得するには、次の手順を行います。

1. Azure ポータルにサインインし、このサインインを使用して Dynamics 365 Supply Chain Management アプリの `clientId` と `clientSecret` の値を検索します。
1. 次のプロパティを持つ HTTP 要求を送信することにより、Azure AD トークン (`aadToken`) をフェッチします。

    - **URL:** `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **メソッド:** `GET`
    - **本文の内容 (フォーム データ):**

        | キー | 先頭値 |
        |---|---|
        | クライアント ID | ${aadAppId} |
        | クライアント シークレット | ${aadAppSecret} |
        | 付与タイプ | client_credentials |
        | リソース | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

    応答で Azure AD トークン (`aadToken`) を取得する必要があります。 これは次の例に類似しているはずです。

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
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
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    次のポイントに注意します。

    - `client_assertion` 値は、前の手順で受け取った Azure AD トークン (`aadToken`) である必要があります。
    - この `context` 値は、アドインを配置する環境 ID である必要があります。
    - 例に示すように、他のすべての値を設定します。

1. 次のプロパティを持つ HTTP 要求を送信します。

    - **URL:** `https://securityservice.operations365.dynamics.com/token`
    - **メソッド:** `POST`
    - **HTT Pヘッダー:** API バージョンを含めます。 (キーは `Api-Version` で、値は `1.0` です。)
    - **本文の内容:** 前の手順で作成した JSON 要求を含めます。

    応答でアクセス トークン (`access_token`) を取得する必要があります。 在庫の可視化 API を呼び出すためのベアラー トークンとしてこのトークンを使用する必要があります。 次に例を示します。

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 3600
    }
    ```

後のセクションでは、最後の手順でフェッチされたトークンを表すための `$access_token` を使用します。

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a> 手持在庫変更のイベントの作成

2 つの API を使用して、手持在庫変更のイベントを作成できます。

- 1 つの記録の作成: `/api/environment/{environmentId}/onhand`
- 複数の記録の作成: `/api/environment/{environmentId}/onhand/bulk`

次のテーブルでは、JSON 本文の各フィールドの意味が要約されています。

| フィールド ID | 説明 |
|---|---|
| `id` | 特定の変更イベントの固有 ID。 この ID を使用して、サービスとの通信が転記時に失敗した場合にイベントを再送信しても、同じイベントがシステムで 2 回カウントされることがないようにすることができます。 |
| `organizationId` | イベントにリンクされている組織の ID。 この値は、Supply Chain Management での組織またはデータ領域 ID にマップされます。 |
| `productId` | 製品の識別子。 |
| `quantities` | 手持在庫の数量の変更が必要な数量。 たとえば、新たに帳簿を 10 つ追加すると、この値は `quantities:{ shelf:{ received: 10 }}` になります。 棚から 3 つの帳簿が削除される場合、または販売される場合、この値は `quantities:{ shelf:{ sold: 3 }}` になります。 |
| `dimensionDataSource` | イベントやクエリ変更の転記で使用する分析コードのデータ ソース。 データ ソースを指定する場合は、指定されたデータ ソースのカスタム分析コードを使用できます。 在庫の可視化は、分析コードの構成を使用して、カスタム分析コードを既定の標準分析コードにマップできます。 `dimensionDataSource` の値が指定されていない場合は、クエリで標準の[基準分析コード](inventory-visibility-configuration.md#data-source-configuration-dimension) のみを使用できます。 |
| `dimensions` | 動的なキーと値のペア。 値は Supply Chain Management の分析コードの一部にマップされます。 ただし、カスタム分析コード (_ソース_ など)を追加して、イベントが Supply Chain Management から取得されたか、または外部システムから取得されたかどうかを示したりすることもできます。 |

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

次の例は、サンプル本文コンテンツを示しています。 このサンプルでは、*T シャツ* 製品の変更イベントを転記します。 このイベントは、販売時点管理 (POS) システムから取得され、赤い T シャツを顧客が店舗に返品したとします。 このイベントにより、*T シャツ* 製品の数量が 1 つ増加します。

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

次の例は、`dimensionDataSource` なしのサンプル本文コンテンツを示しています。

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a> 複数の変更イベントの作成

この API で、同時に複数の記録を作成できます。 この API と [1 つのイベント API](#create-one-onhand-change-event) の違いは、`Path` 値と `Body` 値のみです。 この API では、`Body` は記録の配列を提供します。

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
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "@PRODUCT1",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a> 手持在庫数量の設定/上書き

_手持在庫数量の設定_ API は、指定された製品の現在のデータを上書きします。

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

次の例は、サンプル本文コンテンツを示しています。 この API の動作は、このトピックの前半の[手持在庫変更のイベントの作成](#create-onhand-change-event) セクションで説明されている API の動作とは異なります。 このサンプルでは、*T シャツ* 製品の数量が 1 つに設定されます。

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>予約イベントの作成

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

*予約* API を使用するには、予約機能を開いて、予約の構成を完了する必要があります。 詳細については、[予約の構成 (オプション)](inventory-visibility-configuration.md#reservation-configuration) を参照してください。

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a> 1 つの予約イベントの作成

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
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a> 複数の予約イベントの作成

この API は、[1 つのイベント API](#create-one-reservation-event) の一括バージョンです。

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

## <a name="query-on-hand"></a>手持在庫をクエリする

_手持在庫をクエリする_ API は、製品の手持在庫データをフェッチするために使用されます。

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
        organizationId: string,
        filters: {
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

次の例は、サンプル本文コンテンツを示しています。

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a> 取得メソッドを使用したクエリ

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
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

サンプル取得 URL を次に示します。 この取得要求は、以前に提供された転記サンプルとまったく同じです。

```txt
/api/environment/{environmentId}/onhand/indexquery?organizationId=usmf&productId=T-shirt&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]