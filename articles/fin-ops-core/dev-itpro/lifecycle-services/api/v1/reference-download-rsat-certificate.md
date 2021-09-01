---
title: ZIP ファイルで RSAT 証明書をフェッチする
description: このトピックでは、LCS 環境 API 経由で Microsoft Dynamics Lifecycle Services (LCS) を使用して、環境の Regression Suite Automation Tool (RSAT) 証明書バンドルをフェッチする方法について説明します。
author: jorichar
ms.date: 08/19/2021
ms.topic: reference
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jorichar
ms.search.validFrom: 2021-08-12
ms.openlocfilehash: 6bd068cc8826ae2acb824241be42565e2af6e7a2
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7404447"
---
# <a name="fetch-an-environments-rsat-certificate-in-a-zip-file"></a>ZIP ファイルで RSAT 証明書をフェッチする

[!include [banner](../../../includes/banner.md)]

LCS 環境 API 経由で Microsoft Dynamics Lifecycle Services (LCS) を使用して、環境の Regression Suite Automation Tool (RSAT) 証明書バンドルをフェッチできます。 この API は、プライベート証明書パスワード用の Base 64 エンコードされた zip ファイルと Base 64 エンコードされたパスワードを返します。

この zip の使用についての完全なプロセスは、[Regression Suite Automation Tool のインストールとコンフィギュレーション](../../../perf-test/rsat/rsat-install-configure.md) ページで確認できます。

## <a name="permissions"></a>アクセス許可

### <a name="api-application"></a>API アプリケーション

この API を呼び出すには、次のアクセス許可の 1 つが必要です。 アクセス許可およびその選択方法の詳細については、[データベース移動 API - 認証](../../../database/api/dbmovement-api-authentication.md)を参照してください。

| アクセス許可のタイプ                    | アクセス許可 (最小の特権から最大の特権) |
|------------------------------------|--------------------------------------------------------|
| 委任 (勤務先または学校アカウント) | ユーザー \_ 偽装                                    |

### <a name="lcs"></a>LCS

LCS では、API OAuth 認証で使用するユーザーをプロジェクト所有者または環境管理者としてプロジェクトに追加する必要があります。 ユーザーは、プロジェクトへの招待を受け入れる必要があります。

## <a name="http-request"></a>HTTP 要求

次の GET エンドポイントを使用して、環境の RSAT 証明書用の zip ファイルをフェッチします。

**環境別の RSAT 証明書をフェッチする**

<!-- { "blockType": "ignored" } -->
```http
GET /environmentinfo/v1/rsatdownload/project/{projectId}/
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

### <a name="data"></a>データ

| プロパティ | 説明 |
|----------|-------------|
| CertificateZipEncoded | Base 64 エンコードされたバイト配列の .PFX ファイルと .CER ファイルを含む zip。 |
| CertificateSecretEncoded | Base 64 エンコードされた文字列としての、プライベート証明書のプライベート シークレット。 これにより、すべての要求が変更されます。 |
| ExpirationDateTimeUTC | 以降に証明書が無効になる日付と時刻 (UTC)。 |
| ファイル名 | 返される zip のファイル名。 |

### <a name="example-response"></a>応答の例

**プロジェクト レベルの要求に対する正常な応答**

```json
{
    "Data": {
        "CertificateZipEncoded": "<base 64-encoded zip>",
        "CertificateSecretEncoded": "<base 64-encoded password>",
        "ExpirationDateTimeUTC": "Thursday, June 30, 2022 8:52:13 PM",
        "Filename": "RSATCertificate_TestEnv1_20210805-100102.zip"
    },
    "IsSuccess": true,
    "OperationActivityId": "2234bff0-432d-478b-a5ac-1ccb529ee698",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```

## <a name="parsing-data-via-powershell"></a>PowerShell を使用したデータ解析

次のスクリプトの例では、LCS API と通信して、ローカル コンピューターに、RSAT 証明書の zip ファイルをダウンロードします。 プライベート証明書のパスワードがコンソール ウィンドウに表示されます。 アクセス トークンを指定する必要があります。

```powershell
# Basic LCS API RSAT certificate zip download script
#
# This will download the RSAT certificate bundle for an environment
# to the current directory and display the private certificate's password
# in the console.
#
# The user used in the API authentication must be added to the
# project as an Environment Admin or Project Owner

# Configuration
$accessToken = "{access token string}";
$projId = {project id integer};
$envId = "{environment id GUID}"
$baseLCSAPI = "lcsapi.lcs.dynamics.com";

$url = "https://$baseLCSAPI/environmentinfo/v1/rsatdownload/project/$projId/environment/$envId"
 
$headers = @{
    "Authorization" = "Bearer $accessToken"
    "x-ms-version" = "2017-09-15"
    "Content-Type" = "application/json"
}

# Reset variable between executions
$certificateResponse = $null 
$shouldRetry = $false

do {
    $shouldRetry = $false

    try {
        # GET request to LCS API
        $certificateResponse = Invoke-RestMethod $url -Method 'GET' -Headers $headers
    } catch {
        # Check if this is a HTTP 429 error
        if ($_.Exception.Response.StatusCode.value__ -eq 429) {

            # Too many requests for this environment, wait and retry
            $shouldRetry = $true
            $retrySeconds = [int]$_.Exception.Response.Headers['Retry-After']
            Write-Host "Too many requests - Retrying in $retrySeconds seconds"
            Start-Sleep -Seconds $retrySeconds
        } else {
            throw
        }
    }
} while($shouldRetry)

if ((-not $certificateResponse.IsSuccess) -or ($certificateResponse.Data -eq $null)) {
    Write-Host $certificateResponse.ErrorMessage
    throw
}

$fileName = $certificateResponse.Data.Filename
$certificateZip = [System.Convert]::FromBase64String($certificateResponse.Data.CertificateZipEncoded)
$certificateSecret = [System.Text.Encoding]::ASCII.GetString(
                            [System.Convert]::FromBase64String(
                                $certificateResponse.Data.CertificateSecretEncoded))

# Save the zip to the local disk.
# Could add unzipping in memory and install certificates to correct local certificate stores.
Set-Content $fileName -Value $certificateZip -Encoding Byte

Write-Host "Certificate bundle downloaded to $fileName with private certificate password $certificateSecret"
```

## <a name="rate-limits"></a>レート制限

要求の負荷分散を向上させるために、この API にはレート制限があります。 これらの制限は、LCS Web インターフェイスでも共有されます。

* 各環境に対して 1 分間で 1 回の呼び出し

> [!NOTE]
> レート制限を超えた要求は拒否され、「HTTP 429 要求過多」の応答が返されます。 **再試行** ヘッダーは、後で要求を再試行する場合の秒数を示します。

[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
