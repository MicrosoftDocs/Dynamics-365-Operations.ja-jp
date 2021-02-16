---
title: データ管理パッケージ REST API
description: このトピックでは、データ管理フレームワークのパッケージ REST API について説明します。
author: Sunil-Garg
ms.date: 06/18/2020
manager: AnnBe
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2017-03-31
ms.dyn365.ops.version: Platform update 5
ms.openlocfilehash: 1a9da9e2af9bc71ddf16066ad6dadf2f2214a755
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685689"
---
# <a name="data-management-package-rest-api"></a>データ管理パッケージ REST API

[!include [banner](../includes/banner.md)]

このトピックでは、データ管理フレームワークのパッケージの Representational State Transfer (REST) のアプリケーション プログラミング インターフェイス (API) について説明します。 パッケージ API により、データ パッケージを使用して統合できます。 REST API はクラウド展開とオンプレミスの展開で使用できます。 オンプレミス配置では、現在この機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) (バージョン 7.2)、ビルド 7.0.4709.41184 以降で利用可能です。

オンプレミス サポートが追加されましたが、API 名は変更されていません。 したがって、Microsoft は、クラウド配置とオンプレミス配置の両方に対して単一の API セットを維持することができます。

## <a name="choosing-an-integration-api"></a>統合 API の選択

ファイル ベースの統合シナリオは、データ管理フレームワークのパッケージ API と定期的な統合 API の 2 つの API によりサポートされます。 どちらの API もデータ インポート シナリオとデータ エクスポート シナリオの両方をサポートしています。 次のテーブルでは、使用する API を決定する際に考慮する必要がある主な決定事項について説明します。

| 決定ポイント      | 定期統合 API | データ管理フレームワークのパッケージ API |
|---------------------|--------------------------------------|-----------------------------|
| スケジューリング          | Finance and Operations アプリのスケジューリング | Finance and Operations アプリ以外のスケジューリング |
| Format              | ファイルおよびデータ パッケージ | データ パッケージのみ |
| 変換      | データ ファイルが XML 形式の場合の Extensible Stylesheet Language Transformations (XSLT) のサポート | システム外部での変換 |
| サポートされているプロトコル | SOAP および REST | REST |
| サービス タイプ        | カスタム サービス | データ プロトコル (OData) アクションを開きます |
| 在庫状態        | Microsoft Dynamics Finance and Operations (2016 年 2 月) およびそれ以降。 注意: この機能は、オンプレミス バージョンの Dynamics 365 Finance and Operations には対応していません。 | Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 5 (2017 年 3 月) およびそれ以降 |

定期的な統合 API がデータ管理フレームワークのパッケージ API よりも要件を満たしていることを決定した場合、[定期統合](recurring-integrations.md) を参照します。 このトピックの残りの部分では、データ管理フレームワークのパッケージ API について説明します。

## <a name="authorization"></a>承認

データ管理フレームワークのパッケージ API は、アクセスを認可するために OAuth 2.0 を使用します。 API は、有効な OAuth アクセス トークンを使用して呼び出す必要があります。 OAuth 2.0 および Microsoft Azure Active Directory(Azure AD) の詳細については、[OAuth 2.0 と Azure Active Directory を使用して Web アプリケーションへのアクセスを承認](/azure/active-directory/develop/active-directory-protocols-oauth-code) を参照してください。 オンプレミス配置では、Active Directory フェデレーション サービス (AD FS) が承認に使用されます。

> [!NOTE]
> クライアント資格情報の付与フローを使用すると、アプリケーションはアクセス制御リストを保持します。 アクセス制御リストは、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** を順にクリックして見つけることができます。 **Azure Active Directory アプリケーション** ページには、承認済クライアント ID と、クライアント資格情報付与フローを使用して API が呼び出されたときに適用する必要があるユーザー セキュリティ マッピングが表示されます。
>
> オンプレミス配置については、このリストには AD FS からの有効なクライアント ID が必要です。 また、オンプレミスで使用する場合は、接続の確立時に、次の例にて示されている **\<baseurl\>** に **/namespaces/AXSF** を付加する必要があります。

## <a name="import-apis"></a>API のインポート

ファイル (データ パッケージ) のインポートには、次の API が使用されます。

### <a name="getimportstagingerrorfileurl"></a>GetImportStagingErrorFileUrl

GetImportStagingErrorFileUrl API は、エラーファイルのURLを取得します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージング段階で失敗したデータが格納されています。 エラーファイルが生成されなかった場合は、空の文字列が返されます。

POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportStagingErrorFileUrl

```json
Body
{
    "executionId":"<string>",
    "entityName":"<string>"
}

Successful Response:

HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorfileurl>"
}
```

**入力パラメーター**

| パラメーター     | 説明 |
|---------------------|--------------------------------------|
| string executionId          | インポート処理の実行ID。 これは、UI ではジョブ ID と呼ばれます。 |
| string entityName        | エラー ファイルの取得対象となるエンティティの名前。 |


**出力パラメーター**

| パラメーター         | 説明 |
|-------------------|-------------|
| string errorkeysfileurl | エラーファイルのURL。 エラーファイルが生成されなかった場合は、空の戻り値が返されます。 |


### <a name="generateimporttargeterrorkeysfile"></a>GenerateImportTargetErrorKeysFile

GenerateImportTargetErrorKeysFile API は、エラーファイルを生成します。エラーファイルには単一のエンティティに対するインポートの過程で、ステージングからターゲットの段階で失敗したインポート レコードのキーが格納されています。  

このAPIがtrueを返す場合は、GetImportTargetErrorKeysFileUrl API を使用して、生成されたエラーキーファイルのURLを取得します。


POST /Data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GenerateImportTargetErrorKeysFile

```json
Body

{
    "executionId":"<string>",
    "entityName":"<string>"
}

Successful Response:

HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.Boolean",
    "value": <errorsExist>
}
```

**入力パラメーター**

| パラメーター     | 説明 |
|---------------------|--------------------------------------|
| string executionId          | インポート処理の実行ID。 |
| string entityName        | エラー ファイルの取得対象となるエンティティの名前。 |

**出力パラメーター**

| パラメーター     | 説明 |
|---------------------|--------------------------------------|
| ブール値エラーが発生しています     | インポートエラーが発生した場合はtrue、 インポートエラーが発生しなかった場合はfalseとします |

### <a name="getimporttargeterrorkeysfileurl"></a>GetImportTargetErrorKeysFileUrl

**GetImportTargetErrorKeysFileUrl** API を使用して、単一のエンティティに対するインポートのステージングからターゲットへのステップで失敗したインポート レコードのキーが格納されているエラー ファイルの URL を取得します。

エラー ファイルが使用可能な場合、この API はその URL を返します。 エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、API は空の文字列を返します。

> [!IMPORTANT] 
> この API を呼び出す前に、**GenerateImportTargetErrorKeysFile** API を呼出して、エラー ファイルを生成します。 **GenerateImportTargetErrorKeysFile** API が **true** を返した場合、空でない文字列が返されるまで、ループでこの API を呼び出します。 **GenerateImportTargetErrorKeysFile** API が **false** を返した場合、エラーがないため、この API は空の文字列をかならず返します。

**疑似コードの例**

```csharp
errorsExist = GenerateImportTargetErrorKeysFile(executionId, entityName)

if (errorsExist)
{
    errorFileUrl = null

    while (errorFileUrl is not a non-empty string)
    {
        errorFileUrl = GetImportTargetErrorKeysFileUrl(executionId, entityName)
        if (errorFileUrl is not a non-empty string)
        {
            wait for some time before retrying
        }
    }
}
```

```csharp
POST
/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetImportTargetErrorKeysFileUrl

Body
{
    "executionId":"<string>",
    "entityName":"<string>"
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<errorkeysfileurl>"
}
```

**入力パラメーター**

| パラメーター         | 説明 |
|-------------------|-------------|
| string executionId | インポートの実行 ID。 これは、UI ではジョブ ID と呼ばれます。|
| string entityName | エラー ファイルを取得する対象のエンティティの名前。 |

**出力パラメータ**

| パラメーター         | 説明 |
|-------------------|-------------|
| string errorkeysfileurl | エラー キー ファイルが使用可能な場合、そのファイルの URL。 エラー ファイルがまだ生成中の場合、またはエラー ファイルが存在しない場合は、このメソッドは空の文字列を返します。 |


### <a name="getazurewritableurl"></a>GetAzureWritableUrl

**GetAzureWritableUrl** API は、書き込み可能な Blob URL を取得するために使用されます。 このメソッドには、URL に埋め込まれた共有アクセス署名 (SAS) トークンが含まれています。 この方法を使用すると、Azure Blob Storage コンテナーにデータ パッケージをアップロードすることができます。 オンプレミス配置の場合、この API はローカル ストレージに取り込まれた URL を引き続き返します。

> [!NOTE]
> SAS は有効期限の時間枠中にのみ有効です。 ウィンドウが経過した後に発行されるすべての要求はエラーを返します。 詳細については、[共有アクセス署名 (SA) の使用](/azure/storage/common/storage-dotnet-shared-access-signature-part-1) を参照してください。

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetAzureWriteUrl
BODY
{
    "uniqueFileName":"<string>"
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value": "{\"BlobId\":\"{<GUID>}\",\"BlobUrl\":\"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>\"}"
    }
}
```

**入力パラメーター**

| パラメーター         | 説明 |
|-------------------|-------------|
| 文字列 uniqueFileName | BLOB ID を追跡するために使用される一意のファイル名。 一意のファイル名であることを保証するため、グローバル一意識別子 (GUID) を含めることができます。 |

**出力パラメータ**

| パラメーター      | 説明 |
|----------------|-------------|
| string BlobId  | 割り当てられた BLOB コンテナーの BLOB ID。 |
| string BlobUrl | 埋め込みの SAS トークンを持つ URL。 URL を使用 して Blob ストレージに書き込むことができます。 |

### <a name="importfrompackage"></a>ImportFromPackage

**ImportFromPackage** API は、実装に関連付けられている Blob ストレージにアップロードされるデータ パッケージからインポートを開始するために使用します。 オンプレミス配置の場合、ファイルが以前アップロードされたローカル ストレージから、インポートが開始されます。

> [!NOTE]
> プラットフォーム更新プログラム 12 を起動すると、**ImportFromPackage** API は複合エンティティをサポートします。 ただし、1 つのパッケージで 1 つの複合エンティティのみという制限があります。

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ImportFromPackage
BODY
{
    "packageUrl":"<string>",
    "definitionGroupId":"<string>",
    "executionId":"<string>",
    "execute":<bool>,
    "overwrite":<bool>,
    "legalEntityId":"<string>"
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionId>"
}
```

**入力パラメーター**

| パラメーター                | 説明 |
|--------------------------|-------------|
| string packageUrl        | Finance and Operations アプリに関連付けられている Blob Storage 内のデータ パッケージの URL。 |
| string definitionGroupId | インポート用のデータ プロジェクトの名前。 |
| string executionId       | ジョブに使用する ID。 これは、UI ではジョブ ID と呼ばれます。 空の ID が割り当てられている場合は、新しい実行 ID が作成されます。 |
| bool execute             | このパラメーターを **True** に設定して対象の手順を実行します。 それ以外の場合、**False** に設定します。 |
| bool overwrite           | パッケージ内で複合エンティティを使用する場合は、このパラメーターを常に **False** に設定する必要があります。 それ以外の場合、**True** に設定します。 |
| string legalEntityId     | データ インポートの法人。 |

**出力パラメータ**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ インポートの実行 ID。 これは、UI ではジョブ ID と呼ばれます。 |

> [!NOTE]
> **ImportFromPackage()** はバッチを使用してインポートを実行します。 したがって、並行インポートを実行するために、データ管理で並列処理ルールを使用する必要があります。 **ImportFromPackage()** を並列スレッドで呼び出すことはできません。 それ以外の場合、これは失敗します。

## <a name="export-apis"></a>API をエキスポート

ファイル (データ パッケージ) のエクスポートには、次の API が使用されます。

### <a name="exporttopackage"></a>ExportToPackage

**ExportToPackage** API は、データ パッケージのエクスポートを開始するために使用されます。 この API は、クラウド配置とオンプレミス配置の両方に適用されます。

- この API を呼び出す前に、エクスポート データ プロジェクトを作成する必要があります。 プロジェクトが存在しない場合、API の呼び出しには、エラーが返されます。
- 変更履歴がオンの場合は、最後の実行後に更新または作成されたレコードのみがエクスポートされます。 (つまり、デルタのみが返されます。)

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
BODY
{
    "definitionGroupId":"<Data project name>",
    "packageName":"<Name to use for downloaded file.>",
    "executionId":"<Execution Id if it is a rerun>",
    "reExecute":<bool>,
    "legalEntityId":"<Legal entity Id>"
}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"<executionId>"
    }
}
```

**入力パラメーター**

| パラメーター                | 説明 |
|--------------------------|-------------|
| string definitionGroupId | エクスポート用のデータ プロジェクトの名前。 |
| string packageName       | エクスポートされたデータ パッケージの名前。 |
| string executionId       | ジョブに使用する ID。 これは、UI ではジョブ ID と呼ばれます。 空の ID が割り当てられている場合は、新しい実行 ID が作成されます。 |
| bool reExecute           | このパラメーターを **True** に設定して対象の手順を実行します。 それ以外の場合、**False** に設定します。 |
| string legalEntityId     | データ インポートの法人。 |
    
**出力パラメータ**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ エクスポートの実行 ID。 これは、UI ではジョブ ID と呼ばれます。 |

### <a name="getexportedpackageurl"></a>GetExportedPackageUrl

**GetExportedPackageUrl** API は、**ExportToPackage** を呼び出すことでエクスポートされたデータ パッケージの URL を取得するために使用されます。 この API は、クラウド配置とオンプレミス配置の両方に適用されます。

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
BODY
{"executionId":"<Execution Id>"}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":{
        "value":"https://<baseurl_id>.blob.core.windows.net/dmf/<uniqueFileName>?<SAS Token>"
    }
}
```

**入力パラメーター**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ プロジェクト実行の実行 ID。 これは、UI ではジョブ ID と呼ばれます。 |

**出力パラメーター**

| パラメーター      | 説明 |
|----------------|-------------|
| string BlobUrl | 埋め込みの SAS トークンを持つ blob URL。 URL を使用して、エクスポートしたデータ パッケージをダウンロードできます。 |

## <a name="status-check-api"></a>ステータス チェック API 

状態を確認するには、次の API を使用します。 これらは、インポート フローとエクスポート フローの両方で使用されます。

### <a name="getexecutionsummarystatus"></a>GetExecutionSummaryStatus

**GetExecutionSummaryStatus** API は、インポート ジョブとエクスポート ジョブの両方に使用されます。 これは、データ プロジェクト実行ジョブのステータスの確認に使用されます。 この API は、クラウド配置とオンプレミス配置の両方に適用されます。

```csharp
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
BODY
{"executionId":"<executionId>"}
```

成功した応答の例を次に示します。

```json
HTTP/1.1 200 OK
{
    "@odata.context":"https://<baseurl>/data/$metadata#Edm.String",
    "value":"<executionStatus>"
}
```

**入力パラメーター**

| パラメーター          | 説明 |
|--------------------|-------------|
| string executionId | データ プロジェクト実行の実行 ID。 これは、UI ではジョブ ID と呼ばれます。 |

**出力パラメーター**

<table>
<thead>
<tr>
<th>パラメーター</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr>
<td>DMFExecutionSummaryStatus executionStatus</td>
<td>実行のステータス。 以下に使用可能な値を示します。
<ul>
<li>不明</li>
<li>NotRun</li>
<li>実行中</li>
<li>成功</li>
<li>PartiallySucceeded</li>
<li>失敗</li>
<li>取消済</li>
</ul>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Blob ストレージ内のファイルはストレージに 7 日間残ります。 次に、そのファイルは自動的に削除されます。

## <a name="getting-the-list-of-errors"></a>エラーの一覧を取得する
GetExecutionErrors は、ジョブ実行のエラーのリストを取得するために使用できます。 API は、Execution ID をパラメーターとして取り、JSON リストでエラー メッセージのセットを返します。

```json
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionErrors
BODY
{"executionId":"<executionId>"}
```

## <a name="import-and-export-processes"></a>プロセスのインポートとエクスポート

次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをインポートする方法を示しています。

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのインポート](./media/data-package-import.png)

次の図は、データ管理パッケージ メソッドを使用してデータ パッケージをエクスポートする方法を示しています。

![データ管理パッケージ メソッドを使用するデータ パッケージ ファイルのエクスポート](./media/data-package-export.png)

データのインポートとデータのエクスポートのメソッドを紹介するサンプルのコンソール アプリケーションは、 GitHub から入手できます。 詳細については、「<https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/FileBasedIntegrationSamples/ConsoleAppSamples>」に移動してください。
