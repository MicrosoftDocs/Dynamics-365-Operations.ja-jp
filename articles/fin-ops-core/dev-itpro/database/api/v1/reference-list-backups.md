---
title: データベース移動 API - 参照 - v1 - データベースのバックアップのリスト
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
ms.openlocfilehash: de2528c6304c89387120a24aff6f89a138e5613f
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150753"
---
# <a name="list-database-backups"></a>データベースのバックアップのリスト

[!include [banner](../../../includes/banner.md)]

データベースのバックアップのリストは、プロジェクトの資産ライブラリから取得することができます。

## <a name="permissions"></a>アクセス許可

このアプリケーション プログラミング インターフェイス (API) を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->
```http
GET /databasemovement/v1/databases/project/{projectId}
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
GET /databasemovement/v1/databases/project/12345
```

```json
{

    "DatabaseAssets": [
        {
            "Id": "4a2c52d4-49ca-4606-94a9-92b3a6b42985",
            "ProjectId": 12345,
            "OrganizationId": 1,
            "Name": "LanesBackupRecord",
            "FileName": "RandomFile.bacpac",
            "FileDescription": "",
            "FileLocation": "https://scrubbed.blob.core.windows.net/product-ax7productname/e6244b15-5112-4d1d-a422-49c63496ab6d/AX7ProductName-12-17-83c6e642-676a-4048-b413-6e284f5d1f55-e6244b15-5112-4d1d-a422-49c63496ab6d?sv=2015-12-11&sr=b&sig=rO3zmAZ3zM6s%2FV%2BeihBA2LMVvqMsxbtsnbauvd8keYo%3D&se=2019-09-28T15%3A18%3A05Z&sp=r",
            "ModifiedDateTime": "2019-09-27T15:17:35.867",
            "CreatedDateTime": "2019-09-27T15:17:35.867",
            "CreatedByName": null,
            "ModifiedByName": null
        }
    ],
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```
