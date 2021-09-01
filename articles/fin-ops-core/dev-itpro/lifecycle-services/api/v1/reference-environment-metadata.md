---
title: 環境メタデータをフェッチする
description: このトピックでは、LCS 環境 API 経由で Microsoft Dynamics Lifecycle Services (LCS) によって環境メタデータをフェッチする方法について説明します。
author: jorichar
ms.date: 08/19/2021
ms.topic: reference
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jorichar
ms.search.validFrom: 2021-08-32
ms.openlocfilehash: ab9f7a193c6f5e49c2394ef615b788c1cdb422f1
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7404446"
---
# <a name="fetch-environment-metadata"></a>環境メタデータをフェッチする

[!include [banner](../../../includes/banner.md)]

LCS 環境 API 経由で Microsoft Dynamics Lifecycle Services (LCS) によって環境メタデータをフェッチできます。 この API は、既定ではプロジェクトのすべての環境を含むページ設定されたリストを返します。 オプションのクエリ文字列パラメーターを使用して応答をフィルタ処理できます。

## <a name="permissions"></a>アクセス許可

### <a name="api-application"></a>API アプリケーション

この API を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[データベース移動 API - 認証](../../../database/api/dbmovement-api-authentication.md)を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

### <a name="lcs"></a>LCS

LCS では、API OAuth 認証で使用するユーザーをプロジェクト所有者または環境管理者としてプロジェクトに追加する必要があります。 ユーザーは、プロジェクトへの招待を受け入れる必要があります。

## <a name="http-request"></a>HTTP 要求

環境メタデータをフェッチするには、次の GET エンドポイントを使用します。

**プロジェクトのすべての環境のメタデータをフェッチする**

<!-- { "blockType": "ignored" } -->
```http
GET /environmentinfo/v1/detail/project/{projectId}/?page=1
```

**単一の環境のメタデータを ID でフェッチする**

<!-- { "blockType": "ignored" } -->
```http
GET /environmentinfo/v1/detail/project/{projectId}/?environmentId={environmentId}
```

**単一の環境のメタデータを名前でフェッチする**

<!-- { "blockType": "ignored" } -->
```http
GET /environmentinfo/v1/detail/project/{projectId}/?environmentName={environmentName}
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

各環境に対して、次のプロパティを使用できます。 プロパティに使用できる値がない場合 **null** が返されます。

| プロパティ | 説明 |
|----------|-------------|
| 環境 ID | LCS 環境 ID。 |
| EnvironmentName | 環境名。 |
| プロジェクト ID | 環境を含む LCS プロジェクトの ID。 |
| EnvironmentInfrastructure | 環境のインフラストラクチャ タイプ (**SelfService** または **MicrosoftManaged** など)。 |
| EnvironmentType | 環境タイプ (**実稼働** または **サンドボックス** など)。 |
| EnvironmentGroup | 環境グループ (**基本** または **DiasterRecovery** など)。 |
| EnvironmentProduct | この環境で実行されている製品。 |
| EnvironmentEndpointBaseUrl | 環境のベース URL。 |
| DeploymentState | 最新の環境運用の状態。 |
| TopologyDisplayName | 環境に配置される製品トポロジ。 |
| CurrentApplicationBuildVersion | アプリケーション バージョンの文字列。 |
| CurrentApplicationReleaseName | リリース名の文字列。 |
| CurrentPlatformReleaseName | プラットフォーム バージョンの文字列。 |
| CurrentPlatformVersion | プラットフォーム リリース名の文字列。 |
| DeployedOnUTC | 環境が配置された日時を示す協定世界時 (UTC) の日付/時刻の値。 |
| CloudStorageLocation | 環境の主要な Azure の場所。 |
| DisasterRecoveryLocation | 環境の副次的な Azure の場所。 |
| DeploymentStatusDisplay | 環境の現在の状態。 |
| CanStart | 環境を開始できるかどうかを示すブール値。 |
| CanStop | 環境を停止できるかどうかを示すブール値。 |

### <a name="example-response"></a>応答の例

**プロジェクト レベルの要求に対する正常な応答**

```json
{
    "ResultPageCurrent": 1,
    "ResultHasMorePages": true,
    "Data": [
        {
            "EnvironmentId": "d15ed3a8c2c14054840b946c93915da9",
            "EnvironmentName": "ProdEnvironment1",
            "ProjectId": 112233,
            "EnvironmentInfrastructure": "MicrosoftManaged",
            "EnvironmentType": "Production",
            "EnvironmentGroup": "Primary",
            "EnvironmentProduct": "Finance and Operations",
            "EnvironmentEndpointBaseUrl": "<example>",
            "DeploymentState": "Finished",
            "TopologyDisplayName": "Finance and Operations - High Availability (10.0.20 with Platform update 44)",
            "CurrentApplicationBuildVersion": "10.0.886.48",
            "CurrentApplicationReleaseName": "10.0.20",
            "CurrentPlatformReleaseName": "Update44",
            "CurrentPlatformVersion": "7.0.6060.45",
            "DeployedOnUTC": "8/5/2021 11:00 PM",
            "CloudStorageLocation": "East US",
            "DisasterRecoveryLocation": "West US",
            "DeploymentStatusDisplay": "Deployed",
            "CanStart": false,
            "CanStop": false
        },
        {
            "EnvironmentId": "60b557b2-fefb-4690-859e-f83caf98c17e",
            "EnvironmentName": "SandboxEnvironment1",
            "ProjectId": 112233,
            "EnvironmentInfrastructure": "MicrosoftManaged",
            "EnvironmentType": "Sandbox",
            "EnvironmentGroup": "Primary",
            "EnvironmentProduct": "Finance and Operations",
            "EnvironmentEndpointBaseUrl": "<example>",
            "DeploymentState": "Finished",
            "TopologyDisplayName": "Finance and Operations - Sandbox (10.0.20 with Platform update 44)",
            "CurrentApplicationBuildVersion": "10.0.960.24",
            "CurrentApplicationReleaseName": "10.0.21",
            "CurrentPlatformReleaseName": "Update45",
            "CurrentPlatformVersion": "7.0.6129.19",
            "DeployedOnUTC": "8/5/2021 12:42 PM",
            "CloudStorageLocation": "East US",
            "DisasterRecoveryLocation": "West US",
            "DeploymentStatusDisplay": "Failed",
            "CanStart": false,
            "CanStop": true
        }
    ],
    "IsSuccess": true,
    "OperationActivityId": "216ea45d-113d-445a-a393-f67041f7aafe",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

## <a name="rate-limits"></a>レート制限

要求の負荷分散を向上させるために、この API にはレート制限があります。

* 各プロジェクトに対して 1 分間で 6 回の呼び出し

> [!NOTE]
> 制限を超えた要求は拒否され、「HTTP 429 要求過多」の応答が返されます。 **再試行** ヘッダーは、後で要求を再試行する場合の秒数を示します。

[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
