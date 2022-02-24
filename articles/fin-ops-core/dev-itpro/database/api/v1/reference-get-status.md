---
title: データベース移動の API - 参照 - v1 - ステータスの取得
description: このトピックでは、データベース移動に関するアプリケーション プログラミング インターフェイス (API) バージョン 1 (v1) の参照資料を提供します。
author: laneswenka
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a5659e221150d75827d9f333610f4c62b15b292e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681108"
---
# <a name="get-status"></a>ステータスの取得

[!include [banner](../../../includes/banner.md)]

進行中の操作のステータスを取得することができます。

## <a name="permissions"></a>アクセス許可

このアプリケーション プログラミング インターフェイス (API) を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[認証](../dbmovement-api-authentication.md) を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->
```http
GET /databasemovement/v1/fetchstatus/project/{projectId}/environment/{environmentId}/operationactivity/{operationactivityId}
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
GET /databasemovement/v1/fetchstatus/project/12345/environment/5362377c-bc37-4f92-b30e-fe0c1e664cc0/operationactivity/55eb4327-9346-4c7b-82bd-fe8ef15112c6
```

```json
{
    "IsSuccess": true,
    "OperationActivityId": "6a90b45f-1764-4077-b924-3f4671540237",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999",
    "ProjectId": 12345,
    "EnvironmentId": "5362377c-bc37-4f92-b30e-fe0c1e664cc0",
    "ActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "CompletionDate": null,
    "OperationStatus": "InProgress"
}
```

### <a name="operationstatus-property"></a>OperationStatus プロパティ

| ステータス             | 説明                                           |
|--------------------|-------------------------------------------------------|
| NotStarted         | アクションはまだ開始されていません。                   |
| InProgress         | アクションは進行中です。                            |
| 完成          | アクションが正常に完了しました。                |
| 失敗             | アクションが停止されました。                                |
| SignedOff          | アクションが正常に完了し、サインオフしました。 |
| 中止            | アクションは自動クリーンアップなしでキャンセルされました。    |
| RollbackInProgress | アクションは取消中です。                |
| RollbackFailed     | アクションの取消が停止されました。                    |
| RollbackCompleted  | アクションの取り消しが正常に完了しました。    |
