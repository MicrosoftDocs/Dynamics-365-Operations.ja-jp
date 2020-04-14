---
title: データベース移動の API - 参照 - v1 - データベース更新の作成
description: このトピックでは、データベース移動に関するアプリケーション プログラミング インターフェイス (API) バージョン 1 (v1) の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: ac5ce59fc98abc4d3f10eb5d9c441c5d6e147c2c
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150781"
---
# <a name="create-a-database-refresh"></a>データベース更新の作成

[!include [banner](../../../includes/banner.md)]

2 つの環境間でのデータベース更新を作成することができます。 Microsoft Dynamics Lifecycle Services (LCS) の詳細ページと同じ検証ルールは、 アプリケーション プログラミング インターフェイス (API) に適用されます。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->
```http
POST /databasemovement/v1/refresh/project/{projectId}/source/{sourceEnvironmentId}/target/{targetEnvironmentId}
```

## <a name="request-headers"></a>要求ヘッダー

| 表題         | 金額                     |
|----------------|---------------------------|
| 承認  | ベアラー {token} (必須) |
| 「x-ms-version」 | 「2017-09-15」 (必須)   |
| Content-Type   | アプリケーション /json          |

## <a name="request-body"></a>要求の本文

このメソッドの要求の本文を供給しないでください。

## <a name="response"></a>応答

正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。 アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。

## <a name="example"></a>例

```http
POST /databasemovement/v1/refresh/project/12345/source/5362377c-bc37-4f92-b30e-fe0c1e664cc0/target/6a90b45f-1764-4077-b924-3f4671540237
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```
