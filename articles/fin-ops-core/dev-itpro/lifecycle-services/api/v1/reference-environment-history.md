---
title: フェッチ環境履歴
description: この記事では、LCS 環境 API 経由で Microsoft Dynamics Lifecycle Services (LCS) によって環境履歴メタデータをフェッチする方法について説明します。
author: jorichar
ms.date: 08/19/2021
ms.topic: reference
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jorichar
ms.search.validFrom: 2021-08-12
ms.openlocfilehash: 68014d80009812e7564f2aaa571ef48dde3e0535
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866502"
---
# <a name="fetch-environment-history"></a>フェッチ環境履歴

[!include [banner](../../../includes/banner.md)]

LCS 環境 API 経由で Microsoft Dynamics Lifecycle Services (LCS) によって環境履歴メタデータをフェッチできます。 この API は、進行中および過去の操作を含むページ設定されたリストを返します。

## <a name="permissions"></a>アクセス許可

### <a name="api-application"></a>API アプリケーション

この API を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[データベース移動 API - 認証](../../../database/api/dbmovement-api-authentication.md)を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

### <a name="lcs"></a>LCS

LCS では、API OAuth 認証で使用するユーザーをプロジェクト所有者または環境管理者としてプロジェクトに追加する必要があります。 ユーザーは、プロジェクトへの招待を受け入れる必要があります。

## <a name="http-request"></a>HTTP 要求

次の GET エンドポイントを使用して、特定の環境の環境履歴をフェッチします。

<!-- { "blockType": "ignored" } -->
```http
GET /environmentinfo/v1/history/project/{projectId}/environment/{environmentId}/?page=1
```

## <a name="request-headers"></a>要求ヘッダー

HTTP 要求のヘッダーで次のヘッダー値を使用します。

| 表題         | 先頭値                         |
|----------------|-------------------------------|
| 認証  | **ベアラー {token}** (必須) |
| 「x-ms-version」 | **'2017-09-15'** (必須)   |
| Content-Type   | **アプリケーション /json**          |

## <a name="request-body"></a>要求の本文

このメソッドの要求の本文を供給しないでください。

## <a name="response"></a>応答

### <a name="http"></a>HTTP

正しく認証されていない場合を除き、応答は常に「200 OK」応答になります。 アクションの成功または失敗を検証するには、**IsSuccess** プロパティを使用してください。

### <a name="pagination"></a>改ページ位置

この結果には、結果の別のページが利用できるかどうかを示すブール値の **ResultHasMorePages** プロパティが含まれます。 **?page=** クエリ文字列パラメーターを使用して、特定のページをフェッチできます。

### <a name="data"></a>データ

各履歴操作に対して、次のプロパティを使用できます。 プロパティに使用できる値がない場合 **null** が返されます。

| プロパティ | 説明 |
|----------|-------------|
| 氏名 | 指定された操作履歴の名前。 |
| 種類 | 操作タイプ。 |
| TypeDisplay | 操作タイプの表示文字列。 |
| StartDateTimeUtc | 協定世界時 (UTC) での操作の開始日時。 |
| EndDateTimeUtc | UTC での操作の終了日時。 |
| 状態 | 操作の状態。 |
| 活動 ID | 操作活動のグローバル一意識別子 (GUID)。 |
| 環境 ID | 操作が実行された環境の ID。 |
| プロジェクト ID | 操作が実行されたプロジェクトの ID。 |

### <a name="example-response"></a>応答の例

**正常な応答**

```json
{
    "ResultPageCurrent": 1,
    "ResultHasMorePages": false,
    "Data": [
        {
            "Name": "Finance insights",
            "Type": "InstallAddin",
            "TypeDisplay": "Install addin",
            "StartDateTimeUTC": "2021-06-03T15:10:00.0",
            "EndDateTimeUTC": "2021-06-03T15:11:00.0",
            "Status": "Completed",
            "ActivityId": "0924ecdd-1b80-40cc-8158-172785841c15",
            "EnvironmentId": "9ba7fcc3e3b941e09eccd40abde85429",
            "ProjectId": 112233
        },
        {
            "Name": "Contoso Package deployment",
            "Type": "ApplicationHotfix",
            "TypeDisplay": "Application deployable package",
            "StartDateTimeUTC": "2021-06-03T10:10:00.0",
            "EndDateTimeUTC": "2021-06-03T10:11:00.0",
            "Status": "Completed",
            "ActivityId": "34703e5c3d224d1685dbaa7f8677d237",
            "EnvironmentId": "9ba7fcc3e3b941e09eccd40abde85429",
            "ProjectId": 112233
        }
    ],
    "IsSuccess": true,
    "OperationActivityId": "47bb9956-6fae-49c1-8669-6ec0431e7ee9",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

## <a name="rate-limits"></a>レート制限

要求の負荷分散を向上させるために、この API にはレート制限があります。

* 各環境に対して、30 秒おきに 6 回の呼び出し
* 各プロジェクトに対して 1 分間で 6 回の呼び出し

> [!NOTE]
> 制限を超えた要求は拒否され、「HTTP 429 要求過多」の応答が返されます。 **再試行** ヘッダーは、後で要求を再試行する場合の秒数を示します。

[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
