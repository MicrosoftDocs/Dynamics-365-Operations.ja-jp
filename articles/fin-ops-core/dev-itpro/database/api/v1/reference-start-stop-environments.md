---
title: データベース移動 API - 参照 - v1 - 環境の開始および停止
description: このトピックでは、データベース移動 API のバージョン 1 の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: d1ba79f6dc8eec9ebab20cded084e6404ff47176
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035828"
---
# <a name="start-and-stop-environments"></a>環境の開始および停止

[!include [banner](../../../includes/banner.md)]

データベース移動 API を介した Microsoft Dynamics Lifecycle Services (LCS) を通じて、環境の開始および停止をすることができます。 これらの API を使用することにより、確実に LCS 環境の状態を実際の環境と同期させることができます。 

LCS の詳細ページと同じ検証ルールが、API に適用されます。

> [!NOTE]
> - **顧客管理** 環境のみがサポートされます。 セルフサービス環境は、停止と開始の概念が同じではなく、この API ではサポートされていません。 これらの API は、操作をトリガーまたは呼び出し、成功した応答のみがトリガーが成功したことを示します。
> - **停止** については、環境がすでに別の操作を実行しているか、または環境がすでに停止されている場合に、成功しなかったと返されます。
> - **開始** については、環境がすでに別の操作を実行している場合には成功しなかったと返されますが、環境がすでに開始されている場合は成功が返されます。


## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

## <a name="http-request"></a>HTTP 要求

次の POST メソッドを使用して、環境を停止または開始する HTTP 要求を送信します。 

**環境の停止**
<!-- { "blockType": "ignored" } -->
```http
POST /environment/v1/stop/project/{projectId}/environment/{environmentId}
```
**環境の開始**
```http
POST /environment/v1/start/project/{projectId}/environment/{environmentId}
```

## <a name="request-headers"></a>要求ヘッダー

HTTP 要求のヘッダーで次のヘッダー値を使用します。 

| 表題         | 先頭値                     |
|----------------|---------------------------|
| 認証  | ベアラー {token} (必須) |
| 「x-ms-version」 | 「2017-09-15」 (必須)   |
| Content-Type   | アプリケーション /json          |

## <a name="request-body"></a>要求の本文

このメソッドの要求の本文を供給しないでください。

## <a name="response"></a>応答

正しく認証されていない場合を除き、応答は常に **200 OK** 応答になります。 アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。

## <a name="example"></a>例

```http
POST /environment/v1/stop/project/{projectId}/environment/{environmentId}
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

